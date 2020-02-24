---
title: Koble til hjelpesystemet
description: Dette emnet beskriver komponentene i hjelpesystemet for Finance and Operations-apper, og gir en oversikt over hvordan du kobler dem og et sammendrag over hvordan du oppretter egendefinert hjelp.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006178"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="0d3c7-103">Koble til hjelpesystemet</span><span class="sxs-lookup"><span data-stu-id="0d3c7-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d3c7-104">Dette emnet beskriver komponentene i hjelpesystemet for Finance and Operations-apper, for eksempel Dynamics 365 Finance, Supply Chain Management, Commerce og Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span></span> <span data-ttu-id="0d3c7-105">Det gir en oversikt over hvordan du kobler disse komponentene og et sammendrag av hvordan du oppretter egendefinert hjelp.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="0d3c7-106">Hjelpearkitektur</span><span class="sxs-lookup"><span data-stu-id="0d3c7-106">Help architecture</span></span>

<span data-ttu-id="0d3c7-107">Illustrasjonen nedenfor viser delene av hjelpesystemet.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="0d3c7-108">Det integrerte hjelpesystemet i produktet henter artikler fra https://docs.microsoft.com i tillegg til oppgaveveiledninger som er lagret i Forretningsprosessmodellereren i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0d3c7-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="0d3c7-109">Funksjonene som nevnes i diagrammet med en stjerne (\*), er planlagte, men er ennå ikke tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="0d3c7-110">[![Hjelpearkitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="0d3c7-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="0d3c7-111">Koble til hjelpesystemet</span><span class="sxs-lookup"><span data-stu-id="0d3c7-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="0d3c7-112">Kategorien **Oppgaveveiledninger** er ikke tilgjengelig for øyeblikket i Dynamics 365 Human Resources eller Handel.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-112">The **Task guides** tab is currently not available in Dynamics 365 Human Resources or Commerce.</span></span> <span data-ttu-id="0d3c7-113">Vi arbeider for å aktivere denne funksjonaliteten i fremtidige utgaver.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="0d3c7-114">Oppgaveveiledningene i Kom i gang-delen i Human Resources vil fortsatt være tilgjengelig for å dekke grunnleggende funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-114">The Task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="0d3c7-115">Prosedyrehjelp er også tilgjengelig på nettstedet docs.microsoft.com for Human Resources og Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-115">Procedural help is also available on the docs.microsoft.com site for both Human Resources and Commerce.</span></span>

<span data-ttu-id="0d3c7-116">Ved hjelp av siden **Systemparametere**, kobler systemadministratorer delene av hjelpesystemet for en implementering.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="0d3c7-117">[![Skjemaet Systemparametere med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="0d3c7-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="0d3c7-118">Følge denne fremgangsmåten på siden **Systemparametere**:</span><span class="sxs-lookup"><span data-stu-id="0d3c7-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d3c7-119">Første gang du åpner kategorien **Hjelp**, må du koble til Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="0d3c7-120">Husk å klikke koblingen i midten av skjemaet, vent på tilkoblingen, lukk dialogboksen og klikk **OK** for å få tilgang til **Systemparametere**-siden.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="0d3c7-121">[![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png "Koble til LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="0d3c7-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="0d3c7-122">Velg Lifecycle Services-prosjektet du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="0d3c7-123">Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="0d3c7-124">Angi visningsrekkefølge for BPM-bibliotekene.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="0d3c7-125">Dette bestemmer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i **Hjelp**-ruten.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="0d3c7-126">Etter at du har fullført disse trinnene, kan du åpne **Hjelp**-ruten og klikke på **Oppgaveveiledninger**-fanen. Du ser nå oppgaveveiledningene som gjelder for siden du er på i Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="0d3c7-127">Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="0d3c7-128">Vise oversatte oppgaveveiledninger</span><span class="sxs-lookup"><span data-stu-id="0d3c7-128">Showing translated task guides</span></span>

<span data-ttu-id="0d3c7-129">Oversatte oppgaveveiledninger ble først levert i APQC Unified Library fra mai 2016, og Komme i gang-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="0d3c7-130">Hvis du vil vise lokaliserte oppgaveveiledninger i Finance and Operations-apper, kontroller at du er koblet til biblioteket fra mai.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="0d3c7-131">Språket som en oppgaveveiledning vises i, kontrolleres for hver bruker av språkinnstillingene under **Alternativer** &gt; **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="0d3c7-132">Selv om mange oppgaveveiledninger er oversatt, viser ikke klienten de oversatte navnene på oppgaveveiledningene.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="0d3c7-133">Bare oppgaveveiledninger som ble utgitt i februar 2016, er også tilgjengelige i oversettelse i mai-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="0d3c7-134">Vi vil publisere et oppdatert bibliotek med flere oversettelser.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="0d3c7-135">Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="0d3c7-136">Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="0d3c7-137">Opprette egendefinert hjelp</span><span class="sxs-lookup"><span data-stu-id="0d3c7-137">Creating custom help</span></span>

<span data-ttu-id="0d3c7-138">Du kan bruke støttelinjer for å opprette egendefinert hjelp, eller du kan koble et webområde til Hjelp-ruten.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="0d3c7-139">Opprette egendefinert hjelp med oppgaveveiledninger</span><span class="sxs-lookup"><span data-stu-id="0d3c7-139">Create custom help with task guides</span></span>

<span data-ttu-id="0d3c7-140">Du kan opprette egendefinert hjelp for Supply Chain Management og for Handel ved å opprette oppgaveregistreringer som gjenspeiler implementeringen, og lagre dem i et bibliotek for LCS-forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-140">You can create custom help for Finance, Supply Chain Management, and Commerce by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="0d3c7-141">Du kan ikke opprette tilpassede oppgaveveiledninger for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-141">You cannot create custom task guides for Human Resources.</span></span>

<span data-ttu-id="0d3c7-142">For partnere, hvis du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="0d3c7-143">Du kan også lage en kopi av det globale APQC-enhetlige biblioteket og deretter åpne kopien din, åpne oppgaveregistreringer fra den, endre dem og lagre registreringene sammen med endringene.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="0d3c7-144">Hvis du vil ha mer informasjon, kan du se [Ressurser for Oppgaveregistrering](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="0d3c7-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="0d3c7-145">Koble til et tilpasset område</span><span class="sxs-lookup"><span data-stu-id="0d3c7-145">Connect a custom site</span></span>

<span data-ttu-id="0d3c7-146">Microsoft har en hvitbok og eksempelkode som beskriver hvordan du kan opprette og koble et område med tilpasset hjelp til Hjelp-ruten.</span><span class="sxs-lookup"><span data-stu-id="0d3c7-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="0d3c7-147">Hvis du vil ha mer informasjon,  kan du se:</span><span class="sxs-lookup"><span data-stu-id="0d3c7-147">For more information, see:</span></span>

- [<span data-ttu-id="0d3c7-148">Opprette tilpasset hjelp for Finance and Operations-apper (hvitbok)</span><span class="sxs-lookup"><span data-stu-id="0d3c7-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="0d3c7-149">Egendefinert hjelp for GitHub-repositoriet</span><span class="sxs-lookup"><span data-stu-id="0d3c7-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="0d3c7-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0d3c7-150">Additional resources</span></span>

[<span data-ttu-id="0d3c7-151">Hjelpesystem</span><span class="sxs-lookup"><span data-stu-id="0d3c7-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="0d3c7-152">Ressurser for Oppgaveregistrering</span><span class="sxs-lookup"><span data-stu-id="0d3c7-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="0d3c7-153">Lage dokumentasjon eller opplæring med Oppgaveopptaker</span><span class="sxs-lookup"><span data-stu-id="0d3c7-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
