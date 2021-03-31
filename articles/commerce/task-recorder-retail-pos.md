---
title: Oppgaveopptaker og hjelp for Retail Modern POS (MPOS) og Cloud POS
description: Dette emnet beskriver hvordan du bruker Oppgaveopptaker i Retail Modern POS og Cloud POS.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: aa892f4335d9b1aeee62f5571ee36601cab031cd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220419"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="2ea91-103">Oppgaveopptaker og hjelp for Retail Modern POS (MPOS) og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="2ea91-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2ea91-104">Dette emnet beskriver hvordan du bruker Oppgaveopptaker i Retail Modern POS og Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="2ea91-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="2ea91-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="2ea91-105">Overview</span></span>

<span data-ttu-id="2ea91-106">Oppgaveopptaker i Retail Modern POS og Cloud POS er en ny løsning som ble bygd med fokus på høy hastighet.</span><span class="sxs-lookup"><span data-stu-id="2ea91-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="2ea91-107">Den gir et fleksibelt Application Program Interface (API) for fleksibilitet og sømløs integrasjon med forbrukere av forretningsprosessregistreringer.</span><span class="sxs-lookup"><span data-stu-id="2ea91-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="2ea91-108">I tillegg er Oppgaveopptaker-integrasjon med verktøyet Forretningsprosessmodelerer (BPM) på Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) implementert.</span><span class="sxs-lookup"><span data-stu-id="2ea91-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="2ea91-109">Derfor kan brukere fortsette å produsere rike forretningsprosessdiagrammer fra opptak for å analysere og utforme programmene.</span><span class="sxs-lookup"><span data-stu-id="2ea91-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="2ea91-110">Arkitektur</span><span class="sxs-lookup"><span data-stu-id="2ea91-110">Architecture</span></span>

<span data-ttu-id="2ea91-111">Oppgaveopptaker kan registrere brukerhandlinger i klienten med nøyaktig gjengivelse.</span><span class="sxs-lookup"><span data-stu-id="2ea91-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="2ea91-112">Hver kontroll er utstyrt for å varsle Oppgaveopptaker om utførelsen av en handling.</span><span class="sxs-lookup"><span data-stu-id="2ea91-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="2ea91-113">Kontrollen varsler Oppgaveopptaker om at en hendelse oppstod og sender all relevant informasjon om den aktuelle brukerhandlingen i sanntid.</span><span class="sxs-lookup"><span data-stu-id="2ea91-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="2ea91-114">Ved hjelp av denne informasjonen kan Oppgaveregistrering registrere typen brukerhandling (for eksempel en knapp klikkes, verdiregistrering eller navigasjon) og eventuelle data som er knyttet til handlingen (for eksempel inndataverdien og typen, skjemakontekst eller postkontekst).</span><span class="sxs-lookup"><span data-stu-id="2ea91-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="2ea91-115">Oppgaveopptaker behandler informasjonen detaljert nok til å sikre at en avspilling av opptaket kan utføre de registrerte handlingene nøyaktig slik brukeren har utført dem.</span><span class="sxs-lookup"><span data-stu-id="2ea91-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="2ea91-116">(Avspillingsfunksjonen er ennå ikke implementert i Moderne salgssted for detaljhandel eller Skybasert salgssted.)</span><span class="sxs-lookup"><span data-stu-id="2ea91-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="2ea91-117">Grunnleggende konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="2ea91-117">Basic configuration</span></span>

<span data-ttu-id="2ea91-118">Følg disse trinnene for å aktivere oppgaveopptak på salgssted.</span><span class="sxs-lookup"><span data-stu-id="2ea91-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="2ea91-119">Klikk **Retail og Commerce** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-119">Click **Retail and Commerce** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="2ea91-120">Klikk kassen for å aktivere oppgaveopptak.</span><span class="sxs-lookup"><span data-stu-id="2ea91-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="2ea91-121">I kategorien **Register** i hurtigfanen **Generelt** angir du alternativet **Aktiver oppgaveregistrering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="2ea91-122">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-122">Click **Save**.</span></span>
5. <span data-ttu-id="2ea91-123">Gå til **Retail og Commerce** &gt; **IT for Retail og Commerce** &gt; **Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-123">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="2ea91-124">Velg jobben **Kasser (1090)**, og klikk deretter **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="2ea91-125">Opprett et opptak</span><span class="sxs-lookup"><span data-stu-id="2ea91-125">Create a recording</span></span>

<span data-ttu-id="2ea91-126">Følg denne fremgangsmåten for å opprette en ny registrering ved hjelp av oppgaveopptaker.</span><span class="sxs-lookup"><span data-stu-id="2ea91-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="2ea91-127">Start Retail Modern POS eller Cloud POS, og logg på.</span><span class="sxs-lookup"><span data-stu-id="2ea91-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="2ea91-128">På **Innstillinger**-siden, i delen **Oppgaveopptaker**, klikker du **Åpne Oppgaveregistrering**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="2ea91-129">Ruten **Oppgaveopptaker** vises.</span><span class="sxs-lookup"><span data-stu-id="2ea91-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="2ea91-130">Du kan klikke **Lukk**-knappen (**X**) i øvre høyre hjørne for å lukke ruten **Oppgaveopptaker** før du begynner et nytt opptak.</span><span class="sxs-lookup"><span data-stu-id="2ea91-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="2ea91-131">For å åpne ruten igjen gjentar du trinn 2.</span><span class="sxs-lookup"><span data-stu-id="2ea91-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="2ea91-132">[![Rute for oppgaveopptaker](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="2ea91-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="2ea91-133">Skriv inn et navn på og en beskrivelse av opptaket, og klikk deretter **Start**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="2ea91-134">Opptaksøkten begynner når du klikker **Start**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2ea91-135">Hvis du klikker **Lukk**-knappen (**X**) i øvre høyre hjørne når et opptak pågår, lukkes ruten **Oppgaveopptak**, men opptaksøkten avsluttes ikke.</span><span class="sxs-lookup"><span data-stu-id="2ea91-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="2ea91-136">For å åpne ruten for oppgaveopptaker på nytt kan du klikke **Hjelp**-knappen (spørsmålstegn) øverst på skjermen.</span><span class="sxs-lookup"><span data-stu-id="2ea91-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="2ea91-137">[![Spørsmålstegn](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="2ea91-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="2ea91-138">Når du har klikket **Start**, går oppgaveopptak inn i opptaksmodus.</span><span class="sxs-lookup"><span data-stu-id="2ea91-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="2ea91-139">Ruten for **oppgaveopptak** viser informasjon og kontroller som er knyttet til opptaksprosessen.</span><span class="sxs-lookup"><span data-stu-id="2ea91-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="2ea91-140">Utfør handlingene du vil utføre i grensesnittet for Retail Modern POS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="2ea91-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="2ea91-141">Klikk **Stopp** for å avslutte opptaksøkten.</span><span class="sxs-lookup"><span data-stu-id="2ea91-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="2ea91-142">Nedlastingsalternativer</span><span class="sxs-lookup"><span data-stu-id="2ea91-142">Download options</span></span>

<span data-ttu-id="2ea91-143">Når du har avsluttet opptaksøkten, vises flere alternativer, slik at du kan laste ned opptaket.</span><span class="sxs-lookup"><span data-stu-id="2ea91-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="2ea91-144">[![Nedlastingsalternativer](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="2ea91-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="2ea91-145">Lagre på denne PC-en</span><span class="sxs-lookup"><span data-stu-id="2ea91-145">Save to this PC</span></span>

<span data-ttu-id="2ea91-146">Du kan bruke opptakspakken til å spille av en oppgaveveiledning, vedlikeholde opptaket eller redigere merknader i opptaket.</span><span class="sxs-lookup"><span data-stu-id="2ea91-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="2ea91-147">(Denne funksjonen er ennå ikke implementert i Retail Modern POS og Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="2ea91-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="2ea91-148">Eksporter som Word-dokument</span><span class="sxs-lookup"><span data-stu-id="2ea91-148">Export as Word document</span></span>

<span data-ttu-id="2ea91-149">Du kan lagre opptaket som et Microsoft Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="2ea91-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="2ea91-150">Dokumentet inneholder trinnene du har tatt opp samt skjermbilder som er tatt.</span><span class="sxs-lookup"><span data-stu-id="2ea91-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="2ea91-151">Lagre som utvikleropptak</span><span class="sxs-lookup"><span data-stu-id="2ea91-151">Save as developer recording</span></span>

<span data-ttu-id="2ea91-152">Rå opptaksfilen er nyttig for utviklerscenarioer, for eksempel generering av testkode.</span><span class="sxs-lookup"><span data-stu-id="2ea91-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="2ea91-153">(Denne funksjonen er ikke implementert ennå.)</span><span class="sxs-lookup"><span data-stu-id="2ea91-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="2ea91-154">Opptakskontroller</span><span class="sxs-lookup"><span data-stu-id="2ea91-154">Recording controls</span></span>

<span data-ttu-id="2ea91-155">[![Opptakskontroller](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="2ea91-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="2ea91-156">Stopp</span><span class="sxs-lookup"><span data-stu-id="2ea91-156">Stop</span></span>

<span data-ttu-id="2ea91-157">Klikk **Stopp** for å avslutte opptaksøkten.</span><span class="sxs-lookup"><span data-stu-id="2ea91-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="2ea91-158">Vær oppmerksom på at du ikke kan starte en økt på nytt når du har avsluttet den.</span><span class="sxs-lookup"><span data-stu-id="2ea91-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="2ea91-159">Derfor må du sørge for at opptaket er fullført før det avsluttes.</span><span class="sxs-lookup"><span data-stu-id="2ea91-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="2ea91-160">Stans midlertidig</span><span class="sxs-lookup"><span data-stu-id="2ea91-160">Pause</span></span>

<span data-ttu-id="2ea91-161">Klikk **Stans midlertidig** for å stanse opptaksøkten midlertidig og fortsette med operasjonen.</span><span class="sxs-lookup"><span data-stu-id="2ea91-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="2ea91-162">Trinnene du utfører når du har klikket **Stans midlertidig**, tas ikke opp.</span><span class="sxs-lookup"><span data-stu-id="2ea91-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="2ea91-163">Fortsett</span><span class="sxs-lookup"><span data-stu-id="2ea91-163">Continue</span></span>

<span data-ttu-id="2ea91-164">For å gjenoppta opptaksøkten når du har stanset midlertid, klikker du **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="2ea91-165">Ta skjermbilder</span><span class="sxs-lookup"><span data-stu-id="2ea91-165">Capture screenshots</span></span>

<span data-ttu-id="2ea91-166">Oppgaveopptaker kan ta skjermbilder av brukergrensesnittet for Retail Modern POS mens du tar opp en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="2ea91-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="2ea91-167">Hvis du vil aktivere opptaksfunksjonen for skjermbilde, kan du angi **Ta skjermbilder** til **Ja** og deretter kjøre opptaket.</span><span class="sxs-lookup"><span data-stu-id="2ea91-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="2ea91-168">Når opptaket er fullført, klikker du på **Stopp** og laster ned Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="2ea91-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="2ea91-169">Dokumentet inneholder trinnene med relevante skjermbilder.</span><span class="sxs-lookup"><span data-stu-id="2ea91-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="2ea91-170">Funksjonen for å ta skjermbilder støttes ikke i skysalgssted.</span><span class="sxs-lookup"><span data-stu-id="2ea91-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="2ea91-171">Start oppgave og avslutt oppgave</span><span class="sxs-lookup"><span data-stu-id="2ea91-171">Start task and End task</span></span>

<span data-ttu-id="2ea91-172">Du kan angi begynnelsen og slutten av et sett med grupperte trinn ved hjelp av knappene **Start oppgave** og **Avslutt** **oppgave**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="2ea91-173">Klikk **Start oppgave** for å legge til et "Start oppgave"-trinn, og utfør deretter trinnene som skal tas med i gruppen.</span><span class="sxs-lookup"><span data-stu-id="2ea91-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="2ea91-174">Når du er ferdig med å utføre trinnene for gruppen, klikker du **Avslutt oppgave**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="2ea91-175">Oppgavene hjelper deg med å organisere dine prosedyrer.</span><span class="sxs-lookup"><span data-stu-id="2ea91-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="2ea91-176">Oppgaver kan nestes i andre oppgaver.</span><span class="sxs-lookup"><span data-stu-id="2ea91-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="2ea91-177">På denne måten kan du organisere svært lange og kompliserte forretningsprosesser bedre.</span><span class="sxs-lookup"><span data-stu-id="2ea91-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="2ea91-178">Å legge til merknader</span><span class="sxs-lookup"><span data-stu-id="2ea91-178">Adding annotations</span></span>

<span data-ttu-id="2ea91-179">En merknad er tilleggstekst du legger til et trinn i en registrering.</span><span class="sxs-lookup"><span data-stu-id="2ea91-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="2ea91-180">Du kan for eksempel bruke merknader til å gi brukeren mer kontekst eller instruksjoner.</span><span class="sxs-lookup"><span data-stu-id="2ea91-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="2ea91-181">Du kan legge til merknader før eller etter et trinn.</span><span class="sxs-lookup"><span data-stu-id="2ea91-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="2ea91-182">Du kan legge til en merknad til et hvilket som helst trinn ved å klikke knappen **Rediger** (blyantsymbol) til høyre for trinnet.</span><span class="sxs-lookup"><span data-stu-id="2ea91-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="2ea91-183">[![Rediger-knappen for et trinn](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="2ea91-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="2ea91-184">Tekster og merknader</span><span class="sxs-lookup"><span data-stu-id="2ea91-184">Texts and notes</span></span>

<span data-ttu-id="2ea91-185">Du kan bruke feltene **Tekster** og **Merknader** til å legge til tekst som skal knyttes til et trinn i en oppgaveveiledning.</span><span class="sxs-lookup"><span data-stu-id="2ea91-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="2ea91-186">[![Tekst og merknader-felt](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="2ea91-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="2ea91-187">Tekst</span><span class="sxs-lookup"><span data-stu-id="2ea91-187">Text</span></span>

<span data-ttu-id="2ea91-188">Teksten du skriver inn i **Tekst**-feltet, vises *over* trinnteksten i oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="2ea91-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="2ea91-189">Denne plasseringen er egnet for tekst som du vil at brukeren leser før han eller hun fullfører trinnet.</span><span class="sxs-lookup"><span data-stu-id="2ea91-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="2ea91-190">Notater</span><span class="sxs-lookup"><span data-stu-id="2ea91-190">Notes</span></span>

<span data-ttu-id="2ea91-191">Teksten du skriver inn i **Merknader**-feltet, vises *under* trinnteksten i oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="2ea91-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="2ea91-192">Hvis brukeren skal lese merknadsteksten, må han/hun utvide trinnteksten i popup-vinduet.</span><span class="sxs-lookup"><span data-stu-id="2ea91-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="2ea91-193">Denne plasseringen er egnet for valgfritt lesemateriale eller annen informasjon som kan være nyttig for brukeren, men som brukeren ikke trenger for å fullføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="2ea91-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="2ea91-194">Hjelp i Retail Modern POS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="2ea91-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="2ea91-195">Hvis du vil vise dine egne oppgaveopptak i Hjelp-ruten i Retail Modern POS og Cloud POS, slik at de kan vises som tekst, må du lagre oppgaveopptakene i ditt eget Forretningsprosessmodeler-bibliotek og deretter oppdatere hjelpesystemparameterne slik at de peker mot Forretningsprosessmodeler-biblioteket ditt.</span><span class="sxs-lookup"><span data-stu-id="2ea91-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="2ea91-196">Hvis du vil ha mer informasjon, kan du se [Connecting the help system](../fin-and-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="2ea91-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="2ea91-197">Hjelp for Retail Modern POS og Cloud POS søker i LCS i sanntid.</span><span class="sxs-lookup"><span data-stu-id="2ea91-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="2ea91-198">Den søker gjennom alle BPM-biblioteker som er valgt i hjelpesystemparametere for Commerce, og viser de relevante resultatene.</span><span class="sxs-lookup"><span data-stu-id="2ea91-198">It searches across all the BPM libraries that are selected in the Commerce Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="2ea91-199">Du kan åpne **Hjelp**-menyen ved å klikke **Hjelp**-knappen (spørsmålstegn) øverst på skjermen og deretter skrive inn prosessnavnet ditt i søkeboksen og klikke på søkeknappen.</span><span class="sxs-lookup"><span data-stu-id="2ea91-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="2ea91-200">[![Hjelp-knappen](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="2ea91-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="2ea91-201">Når du klikker en oppgaveveiledning i søkeresultatene, kan du se trinnene som et hjelpeemne eller eksportere trinnene til et Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="2ea91-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="2ea91-202">Hjelp i Retail Modern POS og Cloud POS henter ikke frem oppgaveveiledninger i henhold til hvilket skjema du bruker eller hva du holder på med.</span><span class="sxs-lookup"><span data-stu-id="2ea91-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="2ea91-203">Du må skrive inn prosessnavnet i søkeboksen, og deretter klikke **Søk**.</span><span class="sxs-lookup"><span data-stu-id="2ea91-203">You have to type the process name in the search box and then click **Search**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]