---
title: Konfigurere hjelpeopplevelsen for Finance and Operations-apper
description: Dette emnet inneholder informasjon om komponentene i hjelpesystemet for noen Microsoft Dynamics 365-apper. Det forklarer også hvordan du kobler disse appene og gir et sammendrag av prosessen med å opprette tilpasset hjelp.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d000c3f801d382921a027c8ee259fd44ac5cdc80
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798286"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="6a79b-104">Konfigurere hjelpeopplevelsen for Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="6a79b-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a79b-105">I dette emnet vil du finne en oversikt over komponentene i hjelpesystemet for Finance and Operations-apper, for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6a79b-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6a79b-106">Emnet forklarer også hvordan du kobler disse komponentene og gir et sammendrag av prosessen med å opprette tilpasset hjelp.</span><span class="sxs-lookup"><span data-stu-id="6a79b-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="6a79b-107">Hjelpearkitektur</span><span class="sxs-lookup"><span data-stu-id="6a79b-107">Help architecture</span></span>

<span data-ttu-id="6a79b-108">Finance and Operations-apper omfatter begrepsmessige oversikter og andre emner som publiseres til nettstedet for [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="6a79b-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="6a79b-109">Du får tilgang til dette innholdet fra **Hjelp**-ruten i produktet.</span><span class="sxs-lookup"><span data-stu-id="6a79b-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="6a79b-110">Illustrasjonen nedenfor viser delene av hjelpesystemet.</span><span class="sxs-lookup"><span data-stu-id="6a79b-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="6a79b-111">[![Hjelpearkitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="6a79b-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="6a79b-112">Hjelpesystemet i produktet trekker ut artikler fra docs.microsoft.com og andre tilkoblede nettsteder.</span><span class="sxs-lookup"><span data-stu-id="6a79b-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="6a79b-113">Den henter også inn oppgaveveiledninger som er lagret i forretningsprosessmodelereren (BPM) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6a79b-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="6a79b-114">Legge til oppgaveveiledninger</span><span class="sxs-lookup"><span data-stu-id="6a79b-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="6a79b-115">fanen **Oppgaveveiledninger** er for øyeblikket ikke tilgjengelig i Human Resources eller Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a79b-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="6a79b-116">Oppgaveveiledningene i opplevelsen Komme i gang i Human Resources vil imidlertid fortsatt være tilgjengelige for å dekke grunnleggende funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="6a79b-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="6a79b-117">For både Human Resources og Commerce er prosedyremessig hjelp tilgjengelig på nettstedet for [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="6a79b-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="6a79b-118">På siden **Systemparametere** kan systemadministratorer konfigurere tilgang til de relevante oppgavelinjebibliotekene for en implementering.</span><span class="sxs-lookup"><span data-stu-id="6a79b-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="6a79b-119">Hvis du vil konfigurere Hjelp, må du logge på med en konto i samme leier som leieren der appen er distribuert.</span><span class="sxs-lookup"><span data-stu-id="6a79b-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="6a79b-120">Et LCS-biblioteket kan ikke kobles til fra en forekomst av appen som kjører på en virtuell harddisk (VHD).</span><span class="sxs-lookup"><span data-stu-id="6a79b-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="6a79b-121">[![Skjemaet Systemparametere med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="6a79b-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="6a79b-122">Hvis du vil konfigurere oppgavelinjer for en løsning, følger du denne fremgangsmåten på siden **Systemparametere**.</span><span class="sxs-lookup"><span data-stu-id="6a79b-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a79b-123">Første gang du åpner fanen **Hjelp**, må du koble til Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="6a79b-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="6a79b-124">Husk å velge koblingen i midten av skjemaet, vent på tilkoblingen, lukk dialogboksen og velg **OK** for å få tilgang til siden **Systemparametere**.</span><span class="sxs-lookup"><span data-stu-id="6a79b-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="6a79b-125">[![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png "Koble til LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="6a79b-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="6a79b-126">Velg Lifecycle Services-prosjektet du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="6a79b-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="6a79b-127">Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.</span><span class="sxs-lookup"><span data-stu-id="6a79b-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="6a79b-128">Angi visningsrekkefølge for BPM-bibliotekene.</span><span class="sxs-lookup"><span data-stu-id="6a79b-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="6a79b-129">Visningsrekkefølgen definerer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i **Hjelp**-ruten.</span><span class="sxs-lookup"><span data-stu-id="6a79b-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="6a79b-130">Etter at du har fullført disse trinnene, kan du åpne **Hjelp**-ruten og velge fanen **Oppgaveveiledninger**. Du ser nå oppgaveveiledningene som gjelder for siden du er på i Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="6a79b-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="6a79b-131">Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket.</span><span class="sxs-lookup"><span data-stu-id="6a79b-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="6a79b-132">Vise oversatte oppgaveveiledninger</span><span class="sxs-lookup"><span data-stu-id="6a79b-132">Showing translated task guides</span></span>

<span data-ttu-id="6a79b-133">Oversatte oppgaveveiledninger ble først lansert i APQC Unified Library fra mai 2016 og i Komme i gang-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="6a79b-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="6a79b-134">Hvis du vil vise lokalisert hjelp for oppgaveveiledning, må du sørge for at Dynamics 365-løsningen er koblet til biblioteket for mai 2016.</span><span class="sxs-lookup"><span data-stu-id="6a79b-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="6a79b-135">Brukere kan endre språket som en oppgaveveiledning vises i, ved å endre språkinnstillingene under **Alternativer** &gt; **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="6a79b-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="6a79b-136">Selv om mange oppgaveveiledninger er oversatt, viser klienten for øyeblikket ikke de oversatte navnene på oppgaveveiledningene.</span><span class="sxs-lookup"><span data-stu-id="6a79b-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="6a79b-137">I tillegg er oversettelser tilgjengelige i bibliotekte for mai 2016 bare for oppgaveveiledningene som ble lansert i februar 2016.</span><span class="sxs-lookup"><span data-stu-id="6a79b-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="6a79b-138">Microsoft vil publisere et oppdatert bibliotek som inkluderer flere oversettelser.</span><span class="sxs-lookup"><span data-stu-id="6a79b-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="6a79b-139">Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="6a79b-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="6a79b-140">Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="6a79b-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="6a79b-141">Legge til tilpasset Hjelp</span><span class="sxs-lookup"><span data-stu-id="6a79b-141">Adding custom Help</span></span>

<span data-ttu-id="6a79b-142">Du kan bruke oppgaveveiledninger til å opprette tilpasset Hjelp, eller du kan koble et tilpasset nettsted til **Hjelp**-ruten.</span><span class="sxs-lookup"><span data-stu-id="6a79b-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="6a79b-143">Opprette tilpasset Hjelp ved hjelp av oppgaveveiledninger</span><span class="sxs-lookup"><span data-stu-id="6a79b-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="6a79b-144">Du kan opprette tilpasset Hjelp for de støttede appene ved å opprette oppgaveregistreringer som gjenspeiler implementeringen, og deretter kan du lagre dem i et forretningsprosessbibliotek i LCS.</span><span class="sxs-lookup"><span data-stu-id="6a79b-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="6a79b-145">Du kan ikke opprette tilpassede oppgaveveiledninger for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6a79b-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="6a79b-146">Hvis du er partner og du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine.</span><span class="sxs-lookup"><span data-stu-id="6a79b-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="6a79b-147">Du kan også lage en kopi av det APQC-enhetlige biblioteket og deretter åpne oppgaveregistreringene i kopien, redigere dem og lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="6a79b-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="6a79b-148">Hvis du vil ha mer informasjon, kan du se [Ressurser for Oppgaveregistrering](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="6a79b-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="6a79b-149">Koble til et tilpasset hjelpeområde</span><span class="sxs-lookup"><span data-stu-id="6a79b-149">Connect a custom Help site</span></span>

<span data-ttu-id="6a79b-150">Finance and Operations-apper blir sjelden brukt i sin bruksklare form.</span><span class="sxs-lookup"><span data-stu-id="6a79b-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="6a79b-151">Løsningen er i stedet tilpasset og utvidet for å tilpasses organisasjonens behov.</span><span class="sxs-lookup"><span data-stu-id="6a79b-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="6a79b-152">Du kan også tilpasse og utvide hjelpeopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="6a79b-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="6a79b-153">Du kan for eksempel legge til tilpasset hjelp i **Hjelp**-ruten i produktet.</span><span class="sxs-lookup"><span data-stu-id="6a79b-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="6a79b-154">Microsoft tilbyr et verktøysett som hjelper deg med å distribuere og koble til tilpasset i **Hjelp**-ruten.</span><span class="sxs-lookup"><span data-stu-id="6a79b-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="6a79b-155">Hvis du vil ha informasjon om hvordan du kan sette opp en tilpasset hjelpløsning som er koblet til **Hjelp**-ruten, kan du se [Oversikt over tilpasset hjelp](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6a79b-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="6a79b-156">Hvis du vil samarbeide med Microsoft om verktøy og prosesser for å tilpasse hjelp, fyller du ut skjemaet på [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="6a79b-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="6a79b-157">Se også</span><span class="sxs-lookup"><span data-stu-id="6a79b-157">See also</span></span>

[<span data-ttu-id="6a79b-158">Hjelpesystem</span><span class="sxs-lookup"><span data-stu-id="6a79b-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="6a79b-159">Oversikt over tilpasset hjelp</span><span class="sxs-lookup"><span data-stu-id="6a79b-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="6a79b-160">Ressurser for Oppgaveregistrering</span><span class="sxs-lookup"><span data-stu-id="6a79b-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="6a79b-161">Lage dokumentasjon eller opplæring med Oppgaveregistrering</span><span class="sxs-lookup"><span data-stu-id="6a79b-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="6a79b-162">Tilpasset hjelp for GitHub-repositorium</span><span class="sxs-lookup"><span data-stu-id="6a79b-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  
