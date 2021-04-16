---
title: Fremme en variasjon og fullføre et eksperiment
description: Dette emnet beskriver hvordan du fremmer en vellykket variasjon og fullfører et eksperiment i Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0ea0fc8d50c25312b184ec1d3bd613695870d121
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792565"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="29fbf-103">Fremme en variasjon og fullføre et eksperiment</span><span class="sxs-lookup"><span data-stu-id="29fbf-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="29fbf-104">Dette emnet beskriver hvordan du kan fremme variasjonen som produserte de best resultatene i eksperimentet, og hvordan du fullfører eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="29fbf-105">Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="29fbf-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="29fbf-106">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="29fbf-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="29fbf-107">[ ![Brukerreise for eksperimentering – se gjennom og fullføre](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="29fbf-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="29fbf-108">Når du har [kjørt eksperimentet](experimentation-run-monitor.md) og samlet inn nok data til å avgjøre hvilken variasjon du vil bruke på det aktive området, kan du fremme variasjonen og avslutte eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="29fbf-109">Fremme en variasjon</span><span class="sxs-lookup"><span data-stu-id="29fbf-109">Promote a variation</span></span>
<span data-ttu-id="29fbf-110">Bruk dataene og analysen som er relatert til eksperimentet i tredjepartstjenesten, til å avgjøre hvilken variant som oppnådde det beste resultatet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="29fbf-111">Du kan deretter forfremme den ved å erstatte gjeldende innhold på det aktive området med den vinnende variasjonen, slik at det er tilgjengelig for alle som bruker nettstedet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="29fbf-112">Følg denne fremgangsmåten for å forfremme den vinnende variasjonen.</span><span class="sxs-lookup"><span data-stu-id="29fbf-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="29fbf-113">Velg **Eksperimenter** i den venstre navigasjonsruten i Commerce-områdebyggeren, og velg deretter eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="29fbf-114">Velg **Fullfør eksperiment** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="29fbf-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="29fbf-115">I dialogboksen **Fullfør eksperiment** velger du **Se gjennom eksperimentdataene**.</span><span class="sxs-lookup"><span data-stu-id="29fbf-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="29fbf-116">Det åpnes en tredjepartstjeneste der du kan validere måledataene og avgjøre hvilken variant som er fungerte best.</span><span class="sxs-lookup"><span data-stu-id="29fbf-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="29fbf-117">I dialogboksen **Fullfør eksperiment** i områdebygger, velger du den vinnende variasjonen og velger deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="29fbf-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="29fbf-118">Åpne tredjepartstjenesten, og stopp eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="29fbf-119">Velg **Fullfør** i områdebygger for å overskrive den opprinnelige aktive siden og publisere den vinnende variasjonen, slik at den er tilgjengelig for alle som bruker nettstedet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="29fbf-120">Hvis du velger å beholde gjeldende aktive side og ikke publisere en variasjon, velger du **Publiser den opprinnelige siden på nytt**.</span><span class="sxs-lookup"><span data-stu-id="29fbf-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="29fbf-121">Slette eksperimentet</span><span class="sxs-lookup"><span data-stu-id="29fbf-121">Delete your experiment</span></span>
<span data-ttu-id="29fbf-122">Selv om det ikke er nødvendig at du sletter et fullført eksperiment i Commerce, kan du velge å slette det for å spare plass eller rydde arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="29fbf-123">Følg denne fremgangsmåten for å slette et eksperiment i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="29fbf-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="29fbf-124">Velg **Eksperimenter** i den venstre navigasjonsruten, og velg deretter eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="29fbf-125">Hvis eksperimentet fortsatt er aktivt, stopper du eksperimentet i tredjepartstjenesten før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="29fbf-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="29fbf-126">Velg **Opphev publisering** på kommandolinjen for å fjerne variasjonsinnholdet fra det aktive området.</span><span class="sxs-lookup"><span data-stu-id="29fbf-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="29fbf-127">Velg **Slett** for å slette eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="29fbf-128">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="29fbf-128">Previous step</span></span>
[<span data-ttu-id="29fbf-129">Kjøre og overvåke et eksperiment</span><span class="sxs-lookup"><span data-stu-id="29fbf-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]