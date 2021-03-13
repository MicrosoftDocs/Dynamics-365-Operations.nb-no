---
title: Forhåndsvise og publisere et eksperiment
description: Dette emnet beskriver hvordan du forhåndsviser og publiserer et eksperiment fra Dynamics 365 Commerce.
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
ms.openlocfilehash: 32115378be00df771c6ff658da0c090446edf8b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009954"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="a020d-103">Forhåndsvise og publisere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="a020d-103">Preview and publish an experiment</span></span>

<span data-ttu-id="a020d-104">Dette emnet beskriver hvordan du forhåndsviser og publiserer eksperimentet i Dynamics 365 Commerce etter at du har [koblet til eksperimentet og redigert variasjonene](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="a020d-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="a020d-105">Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a020d-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a020d-106">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="a020d-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="a020d-107">[ ![Brukerreise for eksperimentering – forhåndsvise og publisere](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a020d-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="a020d-108">Forhåndsvise eksperimentvariasjonene</span><span class="sxs-lookup"><span data-stu-id="a020d-108">Preview your experiment variations</span></span>
<span data-ttu-id="a020d-109">Du kan forhåndsvise variasjonene og fortsette å redigere dem til de ser ut slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="a020d-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="a020d-110">Følg denne fremgangsmåten for å forhåndsvise eksperimentvariasjonene i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="a020d-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a020d-111">Fra rullegardinmenyen for variasjoner nedenfor kommandolinjen velger du innholdet du vil forhåndsvise.</span><span class="sxs-lookup"><span data-stu-id="a020d-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="a020d-112">På kommandolinjen velger du **Forhåndsvis**.</span><span class="sxs-lookup"><span data-stu-id="a020d-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="a020d-113">En forhåndsvisning av hvordan innholdet vil se ut når det publiseres.</span><span class="sxs-lookup"><span data-stu-id="a020d-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="a020d-114">Hvis du vil forhåndsvise en annen variasjon, velger du den fra rullegardinlisten for variasjon og velger **Forhåndsvisning** på nytt.</span><span class="sxs-lookup"><span data-stu-id="a020d-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="a020d-115">Publisere eksperimentet</span><span class="sxs-lookup"><span data-stu-id="a020d-115">Publish your experiment</span></span>
<span data-ttu-id="a020d-116">Hvis du ikke bruker en publiseringsgruppe til å planlegge når eksperimentet er aktivt og du vil publisere umiddelbart, velger du **Publiser** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="a020d-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="a020d-117">Alle variasjoner som hører til eksperimentet, blir publisert.</span><span class="sxs-lookup"><span data-stu-id="a020d-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="a020d-118">Hvis siden ikke har en publisert URL-adresse, må du først publisere URL-adressen eller den vil ikke være synlig for brukerne av nettstedet.</span><span class="sxs-lookup"><span data-stu-id="a020d-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="a020d-119">Hvis du vil ha mer informasjon, kan du se [Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="a020d-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="a020d-120">Bruke publiseringsgrupper til å planlegge når eksperimentet aktiveres</span><span class="sxs-lookup"><span data-stu-id="a020d-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="a020d-121">Varianter som er opprettet i områdebygger, kan planlegges for publisering ved hjelp av en publiseringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a020d-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="a020d-122">I en publiseringsgruppe kan du koble en side eller et fragment til eksperimentet ved å velge **Eksperimenter** i den venstre navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="a020d-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="a020d-123">Du kan også gjøre dette ved å velge **Sider** eller **Fragmenter** og følge instruksjonene i [Koble til et eksperiment og redigere variasjoner](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="a020d-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="a020d-124">Hvis du vil ha informasjon om publiseringsgrupper, kan du se [Arbeide med publiseringsgrupper](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="a020d-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="a020d-125">Når du bruker publiseringsgrupper med eksperimenter, er det noen viktige hensyn du må være oppmerksom på.</span><span class="sxs-lookup"><span data-stu-id="a020d-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="a020d-126">Når du legger til en side eller et fragment som kjører på den i en publiseringsgruppe, blir eksperimentet fjernet fra siden eller fragmentet i publiseringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="a020d-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="a020d-127">Eksperimenter som er koblet til sider på et aktivt område, er ikke tilgjengelige for sider i publiseringsgrupper og omvendt.</span><span class="sxs-lookup"><span data-stu-id="a020d-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="a020d-128">Sider der eksperimenter kjører på dem i et aktivt område, er på samme måte ikke tilgjengelige for andre eksperimenter i publiseringsgrupper og omvendt.</span><span class="sxs-lookup"><span data-stu-id="a020d-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="a020d-129">Når du publiserer eller planlegger en publiseringsgruppe, blir alt innholdet i publiseringsgruppen publisert, uansett om det finnes et eksperiment som er knyttet til publiseringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="a020d-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="a020d-130">Fordi en publiseringsgruppe beholdes etter at den er publisert på et aktivt område, vil eksperimenter i publiseringsgruppen også beholdes.</span><span class="sxs-lookup"><span data-stu-id="a020d-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="a020d-131">Derfor kan du ikke knytte andre eksperimenter til samme side eller fragment.</span><span class="sxs-lookup"><span data-stu-id="a020d-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="a020d-132">Du kan unngå denne begrensningen ved å slette alle publiseringsgrupper med eksperimenter som beholdes.</span><span class="sxs-lookup"><span data-stu-id="a020d-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="a020d-133">Hvis du vil slette et eksperiment i et aktivt område som også finnes i en publiseringsgruppe, må du først slette det fra publiseringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="a020d-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="a020d-134">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="a020d-134">Previous step</span></span>
[<span data-ttu-id="a020d-135">Koble til og redigere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="a020d-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="a020d-136">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="a020d-136">Next step</span></span>
[<span data-ttu-id="a020d-137">Kjør og Overvåk et eksperiment</span><span class="sxs-lookup"><span data-stu-id="a020d-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
