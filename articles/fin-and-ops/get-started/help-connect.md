---
title: Koble til hjelpesystemet
description: Dette emnet beskriver komponentene i hjelpesystemet for Microsoft Dynamics 365 for Finance and Operations, og gir en oversikt over hvordan du kobler dem og et sammendrag over hvordan du oppretter egendefinert hjelp.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 87ca6afe817d27de12479f1b7d8155d11d800233
ms.openlocfilehash: a2ca5f5302751ad2c4ddc3c6921a8a9b6c2d57df
ms.contentlocale: nb-no
ms.lasthandoff: 12/04/2018

---

# <a name="connect-the-help-system"></a><span data-ttu-id="0676f-103">Koble til hjelpesystemet</span><span class="sxs-lookup"><span data-stu-id="0676f-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0676f-104">Dette emnet beskriver komponentene i hjelpesystemet for Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0676f-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="0676f-105">Det gir en oversikt over hvordan du kobler disse komponentene og et sammendrag av hvordan du oppretter egendefinert hjelp.</span><span class="sxs-lookup"><span data-stu-id="0676f-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="0676f-106">Hjelpearkitektur</span><span class="sxs-lookup"><span data-stu-id="0676f-106">Help architecture</span></span>
<span data-ttu-id="0676f-107">Illustrasjonen nedenfor viser delene av Finance and Operations-hjelpesystemet.</span><span class="sxs-lookup"><span data-stu-id="0676f-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="0676f-108">Det integrerte hjelpesystemet i produktet henter artikler fra Finance and Operations-nettstedet på https://docs.microsoft.com i tillegg til oppgaveveiledninger som er lagret i Forretningsprosessmodellereren i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0676f-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="0676f-109">Funksjonene som nevnes i diagrammet med en stjerne (\*), er planlagte, men er ennå ikke tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="0676f-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="0676f-110">[![Hjelpearkitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="0676f-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="0676f-111">Koble til hjelpesystemet</span><span class="sxs-lookup"><span data-stu-id="0676f-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="0676f-112">Kategorien **oppgaveveiledninger** er ikke tilgjengelig i Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0676f-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="0676f-113">Vi arbeider for å aktivere denne funksjonaliteten i fremtidige utgaver.</span><span class="sxs-lookup"><span data-stu-id="0676f-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="0676f-114">Oppgaveveiledningene i Kom i gang-delen i Talene vil fortsatt være tilgjengelig for å dekke grunnleggende funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="0676f-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="0676f-115">Prosedyrehjelp er også tilgjengelig på docs.microsoft.com-området ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for både Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="0676f-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>


<span data-ttu-id="0676f-116">Ved hjelp av siden **Systemparametere**, kobler systemadministratorer delene av hjelpesystemet for en implementering.</span><span class="sxs-lookup"><span data-stu-id="0676f-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="0676f-117">[![Skjemaet Systemparametere med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) På **Systemparametere**-siden følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="0676f-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0676f-118">Første gang du åpner kategorien **Hjelp**, må du koble til Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="0676f-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="0676f-119">Husk å klikke koblingen i midten av skjemaet, vent på tilkoblingen, lukk dialogboksen og klikk **OK** for å få tilgang til siden **Systemparametere**.[![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png "Koble til LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="0676f-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="0676f-120">Velg Lifecycle Services-prosjektet du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="0676f-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="0676f-121">Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.</span><span class="sxs-lookup"><span data-stu-id="0676f-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="0676f-122">For Finance and Operations, for Microsoft-innhold, velg det nyeste APQC Unified Library for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0676f-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="0676f-123">Vi vil gi ut et bibliotek for Retail i nær fremtid.</span><span class="sxs-lookup"><span data-stu-id="0676f-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="0676f-124">Du trenger ikke velge et bibliotek for Talent – tilkoblingen til riktig biblioteket blir opprettet for deg.</span><span class="sxs-lookup"><span data-stu-id="0676f-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="0676f-125">Angi visningsrekkefølge for BPM-bibliotekene.</span><span class="sxs-lookup"><span data-stu-id="0676f-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="0676f-126">Dette bestemmer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i **Hjelp**-ruten.</span><span class="sxs-lookup"><span data-stu-id="0676f-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="0676f-127">Etter at du har fullført disse trinnene, kan du åpne **Hjelp**-vinduet og klikke på **Oppgaveveiledning**-fanen. Du ser nå oppgavelinjene som gjelder for siden du er på for øyeblikket i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0676f-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="0676f-128">Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket.</span><span class="sxs-lookup"><span data-stu-id="0676f-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="0676f-129">Vise oversatte oppgaveveiledninger</span><span class="sxs-lookup"><span data-stu-id="0676f-129">Showing translated task guides</span></span>

<span data-ttu-id="0676f-130">Oversatte oppgaveveiledninger ble først levert i APQC Unified Library fra mai 2016, og Komme i gang-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="0676f-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="0676f-131">Hvis du vil vise lokaliserte oppgaveveiledninger i Finance and Operations, kontroller at du er koblet til biblioteket fra mai.</span><span class="sxs-lookup"><span data-stu-id="0676f-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="0676f-132">Språket som en oppgaveveiledning vises i, kontrolleres for hver bruker av språkinnstillingene under **Alternativer** &gt; **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="0676f-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0676f-133">Selv om mange oppgaveveiledninger er oversatt, viser ikke Finance and Operations-klienten de oversatte navnene på oppgaveveiledningene.</span><span class="sxs-lookup"><span data-stu-id="0676f-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="0676f-134">Bare oppgaveveiledninger som ble utgitt i februar 2016, er også tilgjengelige i oversettelse i mai-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="0676f-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="0676f-135">Vi vil publisere et oppdatert bibliotek med flere oversettelser.</span><span class="sxs-lookup"><span data-stu-id="0676f-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="0676f-136">Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="0676f-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="0676f-137">Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="0676f-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="0676f-138">Opprette egendefinert hjelp</span><span class="sxs-lookup"><span data-stu-id="0676f-138">Creating custom help</span></span>
<span data-ttu-id="0676f-139">Du kan bruke støttelinjer for å opprette egendefinert hjelp, eller du kan koble et webområde til Hjelp-ruten.</span><span class="sxs-lookup"><span data-stu-id="0676f-139">You can use task guides to create custom help, or connect a website to the Help pane.</span></span> 

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="0676f-140">Opprette egendefinert hjelp med oppgaveveiledninger</span><span class="sxs-lookup"><span data-stu-id="0676f-140">Create custom help with task guides</span></span>
<span data-ttu-id="0676f-141">Du kan opprette egendefinert hjelp for Finance and Operations og for Retail ved å opprette oppgaveregistreringer som gjenspeiler implementeringen, og lagre dem i et bibliotek for LCS-forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="0676f-141">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="0676f-142">Du kan ikke opprette egendefinerte oppgaveveiledninger for Talent.</span><span class="sxs-lookup"><span data-stu-id="0676f-142">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="0676f-143">For partnere, hvis du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine.</span><span class="sxs-lookup"><span data-stu-id="0676f-143">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="0676f-144">Du kan også lage en kopi av det globale APQC-enhetlige biblioteket og deretter åpne kopien din, åpne oppgaveregistreringer fra den, endre dem og lagre registreringene sammen med endringene.</span><span class="sxs-lookup"><span data-stu-id="0676f-144">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="0676f-145">Hvis du vil ha mer informasjon, se [Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="0676f-145">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="0676f-146">Koble til et tilpasset område</span><span class="sxs-lookup"><span data-stu-id="0676f-146">Connect a custom site</span></span>
<span data-ttu-id="0676f-147">Microsoft har en hvitbok og eksempelkode som beskriver hvordan du kan opprette og koble et område med tilpasset hjelp til Hjelp-ruten.</span><span class="sxs-lookup"><span data-stu-id="0676f-147">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="0676f-148">Hvis du vil ha mer informasjon,  kan du se:</span><span class="sxs-lookup"><span data-stu-id="0676f-148">For more information, see:</span></span> 
- [<span data-ttu-id="0676f-149">Lage egendefinert hjelp for Finance and Operations (hvitbok)</span><span class="sxs-lookup"><span data-stu-id="0676f-149">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="0676f-150">Egendefinert hjelp for GitHub-repositoriet</span><span class="sxs-lookup"><span data-stu-id="0676f-150">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)



<a name="additional-resources"></a><span data-ttu-id="0676f-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0676f-151">Additional resources</span></span>
--------

[<span data-ttu-id="0676f-152">Oversikt over Hjelp</span><span class="sxs-lookup"><span data-stu-id="0676f-152">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="0676f-153">Oversikt over oppgaveopptaker</span><span class="sxs-lookup"><span data-stu-id="0676f-153">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="0676f-154">Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring</span><span class="sxs-lookup"><span data-stu-id="0676f-154">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)





