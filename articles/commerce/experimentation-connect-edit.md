---
title: Koble til et eksperiment og redigere variasjoner
description: Dette emnet beskriver hvordan du kobler et eksperiment i en tredjepartstjeneste til Dynamics 365 Commerce, og hvordan du redigerer variasjoner for eksperimentet.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2a33897d01dd98d446c2fb49e417abd9db9f403a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010030"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="19cfd-103">Koble til et eksperiment og redigere variasjoner</span><span class="sxs-lookup"><span data-stu-id="19cfd-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="19cfd-104">Dette emnet beskriver hvordan du kobler til eksperimentet i Commerce og gjør endringer i variasjonene slik at de justeres med hypotesen.</span><span class="sxs-lookup"><span data-stu-id="19cfd-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="19cfd-105">Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="19cfd-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="19cfd-106">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="19cfd-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="19cfd-107">[ ![Brukerreise for eksperimentering – koble til og redigere](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="19cfd-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="19cfd-108">Når du har [konfigurert eksperimentet](experimentation-setup.md) i en tredjepartstjeneste, kobler du eksperimentet til i Dynamics 365 Commerce og redigerer eksperimentvariasjonene.</span><span class="sxs-lookup"><span data-stu-id="19cfd-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="19cfd-109">Planleggingshensyn</span><span class="sxs-lookup"><span data-stu-id="19cfd-109">Planning considerations</span></span>

<span data-ttu-id="19cfd-110">Før du kobler til eksperimentet i Commerce, må du ta noen beslutninger som påvirker hvordan innholdet administreres i Commerce.</span><span class="sxs-lookup"><span data-stu-id="19cfd-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="19cfd-111">Bestemme omfanget av eksperimentet ditt</span><span class="sxs-lookup"><span data-stu-id="19cfd-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="19cfd-112">Når du kobler til et eksperiment, blir du bedt om å definere omfanget av eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="19cfd-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="19cfd-113">Eksperimenter er definert som omfanget **delvis** eller **hele**</span><span class="sxs-lookup"><span data-stu-id="19cfd-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="19cfd-114">Velg **delvis** hvis du vil utføre et eksperiment på en bestemt del av en side.</span><span class="sxs-lookup"><span data-stu-id="19cfd-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="19cfd-115">Hvis du velger dette alternativet, må du identifisere hvilke moduler som er inkludert i eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="19cfd-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="19cfd-116">Endringer som gjøres i deler av standardsiden eller -fragmentet som ikke er relatert til eksperimentet, synkroniseres automatisk på tvers av variasjoner.</span><span class="sxs-lookup"><span data-stu-id="19cfd-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="19cfd-117">Velg **hele** hvis du vil utføre et eksperiment på en hel side eller et helt fragment.</span><span class="sxs-lookup"><span data-stu-id="19cfd-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="19cfd-118">Det opprettes separate kopier av standardsiden eller -fragmentet.</span><span class="sxs-lookup"><span data-stu-id="19cfd-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="19cfd-119">Du trenger ikke velge hvilke moduler som skal tas med i eksperimentet, fordi hele redigeringsflaten kan endres.</span><span class="sxs-lookup"><span data-stu-id="19cfd-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="19cfd-120">Du kan legge til, slette og ordne modulene på nytt etter behov.</span><span class="sxs-lookup"><span data-stu-id="19cfd-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="19cfd-121">Hvis det imidlertid gjøres endringer i standardsiden eller -fragmentet som eksperimentet er tilknyttet, må disse endringene synkroniseres manuelt på tvers av alle variasjoner.</span><span class="sxs-lookup"><span data-stu-id="19cfd-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="19cfd-122">Hvis du knytter eksperimentet til en side som bruker et oppsett, kan du bare angi omfanget **hele** for eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="19cfd-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="19cfd-123">Bestem om du vil planlegge når eksperimentet publiseres</span><span class="sxs-lookup"><span data-stu-id="19cfd-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="19cfd-124">Hvis du vil planlegge når eksperimentet publiseres til ditt eget område, må du passe på at innholdet du vil knytte til eksperimentet, er tilgjengelig i en publiseringsgruppe *før* du kobler til eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="19cfd-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="19cfd-125">Hvis du vil ha mer informasjon om publiseringsgrupper, kan du se [Arbeide med publiseringsgrupper](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="19cfd-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="19cfd-126">Koble til eksperimentet</span><span class="sxs-lookup"><span data-stu-id="19cfd-126">Connect your experiment</span></span>
<span data-ttu-id="19cfd-127">Hvis du vil koble til eksperimentet, starter du veiviser **Koble til eksperiment**.</span><span class="sxs-lookup"><span data-stu-id="19cfd-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="19cfd-128">Veiviseren leder deg gjennom trinnene som kreves for å koble til eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="19cfd-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="19cfd-129">Når du fullfører veiviseren, er eksperimentet ditt tilkoblet, og variasjonene er opprettet og klare til redigering.</span><span class="sxs-lookup"><span data-stu-id="19cfd-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="19cfd-130">Følg denne fremgangsmåten for å komme i gang med å koble til eksperimentet i Commerce-områdebyggeren:</span><span class="sxs-lookup"><span data-stu-id="19cfd-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="19cfd-131">Hvis du vil starte veiviseren **Koble til eksperiment**, velger du **Eksperimenter** i den venstre navigasjonsruten, og deretter velger du **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="19cfd-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="19cfd-132">Alternativt kan du få tilgang til veiviseren fra en side eller et fragmentredigeringsprogram ved å redigere den og velge **Koble til eksperiment** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="19cfd-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="19cfd-133">En side kan bare kobles til ett eksperiment om gangen.</span><span class="sxs-lookup"><span data-stu-id="19cfd-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="19cfd-134">Hvis du vil koble en side til et annet eksperiment, må du først slette eksperimentet som siden for øyeblikket er koblet til.</span><span class="sxs-lookup"><span data-stu-id="19cfd-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="19cfd-135">Velg siden eller fragmentet du vil kjøre eksperimentet på.</span><span class="sxs-lookup"><span data-stu-id="19cfd-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="19cfd-136">Angi eksperimentomfanget til **delvis** eller **hele**, basert på valget ditt i delen [Bestemme omfanget av eksperimentet ditt](#determine-the-scope-of-your-experiment) ovenfor.</span><span class="sxs-lookup"><span data-stu-id="19cfd-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="19cfd-137">Funksjonsflaggene for **Eksperimenter på sider eller fragmenter** må være aktivert hvis du vil eksperimentere på en hel side eller et helt fragment.</span><span class="sxs-lookup"><span data-stu-id="19cfd-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="19cfd-138">Hvis du vil ha mer informasjon, kan du se emnet [Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="19cfd-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="19cfd-139">Velg **Generer varianter og avslutt veiviser** i det siste trinnet i veiviseren.</span><span class="sxs-lookup"><span data-stu-id="19cfd-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="19cfd-140">Variasjoner blir opprettet for eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="19cfd-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="19cfd-141">Redigere variasjonene</span><span class="sxs-lookup"><span data-stu-id="19cfd-141">Edit your variations</span></span>
<span data-ttu-id="19cfd-142">Når du avslutter veiviseren, blir det opprettet variasjoner for deg.</span><span class="sxs-lookup"><span data-stu-id="19cfd-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="19cfd-143">Deretter skal du redigere variasjonene slik at de gjenspeiler valgene du må kontrollere i hypotesen for eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="19cfd-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="19cfd-144">Velg én av følgende fremgangsmåter som tilsvarer omfanget du velger for eksperimentet, i [Bestemme omfanget av eksperimentet ditt](#determine-the-scope-of-your-experiment) ovenfor.</span><span class="sxs-lookup"><span data-stu-id="19cfd-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="19cfd-145">Redigere variasjoner for eksperiment med omfanget delvis</span><span class="sxs-lookup"><span data-stu-id="19cfd-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="19cfd-146">Følg disse trinnene hvis du har definert omfanget for eksperimentet som **delvis** i veiviseren **Koble til eksperiment**.</span><span class="sxs-lookup"><span data-stu-id="19cfd-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="19cfd-147">I redigeringsvisning bruker du rullegardinmenyen for variasjoner nedenfor kommandolinjen til å redigere hver variant basert på den opprinnelige hypotesen.</span><span class="sxs-lookup"><span data-stu-id="19cfd-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="19cfd-148">Du kan også opprette en kontroll eller basisvariasjon ved å la én av variasjonene være uendret.</span><span class="sxs-lookup"><span data-stu-id="19cfd-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="19cfd-149">Velg modulen det skal eksperimenteres på, Velg ellipsen (...), og velg deretter **Legg til eksperiment**.</span><span class="sxs-lookup"><span data-stu-id="19cfd-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="19cfd-150">Redigere variasjoner for eksperiment med omfanget hele</span><span class="sxs-lookup"><span data-stu-id="19cfd-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="19cfd-151">Hvis du har definert omfanget av eksperimentet som **hele** i veiviseren **Koble til eksperiment**, kan du i redigeringsvisning bruke rullegardinmenyen for variasjoner under kommandolinjen til å redigere hver variant basert på den opprinnelige hypotesen.</span><span class="sxs-lookup"><span data-stu-id="19cfd-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="19cfd-152">I begge tilfeller kan du også opprette en kontroll eller basisvariasjon ved å la én av variasjonene være uendret.</span><span class="sxs-lookup"><span data-stu-id="19cfd-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="19cfd-153">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="19cfd-153">Previous step</span></span>
[<span data-ttu-id="19cfd-154">Definer et eksperiment</span><span class="sxs-lookup"><span data-stu-id="19cfd-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="19cfd-155">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="19cfd-155">Next step</span></span>
[<span data-ttu-id="19cfd-156">Forhåndsvise og publisere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="19cfd-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
