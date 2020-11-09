---
title: Fremme en variasjon og fullføre et eksperiment
description: Dette emnet beskriver hvordan du fremmer en vellykket variasjon og fullfører et eksperiment i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097099"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="a3e9c-103">Fremme en variasjon og fullføre et eksperiment</span><span class="sxs-lookup"><span data-stu-id="a3e9c-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="a3e9c-104">Dette emnet beskriver hvordan du kan fremme variasjonen som produserte de best resultatene i eksperimentet, og hvordan du fullfører eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="a3e9c-105">Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a3e9c-106">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="a3e9c-107">[ ![Brukerreise for eksperimentering – se gjennom og fullføre](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a3e9c-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="a3e9c-108">Når du har [kjørt eksperimentet](experimentation-run-monitor.md) og samlet inn nok data til å avgjøre hvilken variasjon du vil bruke på det aktive området, kan du fremme variasjonen og avslutte eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="a3e9c-109">Fremme en variasjon</span><span class="sxs-lookup"><span data-stu-id="a3e9c-109">Promote a variation</span></span>
<span data-ttu-id="a3e9c-110">Bruk dataene og analysen som er relatert til eksperimentet i tredjepartstjenesten, til å avgjøre hvilken variant som oppnådde det beste resultatet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="a3e9c-111">Du kan deretter forfremme den ved å erstatte gjeldende innhold på det aktive området med den vinnende variasjonen, slik at det er tilgjengelig for alle som bruker nettstedet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="a3e9c-112">Følg denne fremgangsmåten for å forfremme den vinnende variasjonen.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="a3e9c-113">Velg **Eksperimenter** i den venstre navigasjonsruten i Commerce-områdebyggeren, og velg deretter eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="a3e9c-114">Velg **Fullfør eksperiment** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="a3e9c-115">I dialogboksen **Fullfør eksperiment** velger du **Se gjennom eksperimentdataene**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="a3e9c-116">Det åpnes en tredjepartstjeneste der du kan validere måledataene og avgjøre hvilken variant som er fungerte best.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="a3e9c-117">I dialogboksen **Fullfør eksperiment** i områdebygger, velger du den vinnende variasjonen og velger deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="a3e9c-118">Åpne tredjepartstjenesten, og stopp eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="a3e9c-119">Velg **Fullfør** i områdebygger for å overskrive den opprinnelige aktive siden og publisere den vinnende variasjonen, slik at den er tilgjengelig for alle som bruker nettstedet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="a3e9c-120">Hvis du velger å beholde gjeldende aktive side og ikke publisere en variasjon, velger du **Publiser den opprinnelige siden på nytt**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="a3e9c-121">Slette eksperimentet</span><span class="sxs-lookup"><span data-stu-id="a3e9c-121">Delete your experiment</span></span>
<span data-ttu-id="a3e9c-122">Selv om det ikke er nødvendig at du sletter et fullført eksperiment i Commerce, kan du velge å slette det for å spare plass eller rydde arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="a3e9c-123">Følg denne fremgangsmåten for å slette et eksperiment i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a3e9c-124">Velg **Eksperimenter** i den venstre navigasjonsruten, og velg deretter eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="a3e9c-125">Hvis eksperimentet fortsatt er aktivt, stopper du eksperimentet i tredjepartstjenesten før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="a3e9c-126">Velg **Opphev publisering** på kommandolinjen for å fjerne variasjonsinnholdet fra det aktive området.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="a3e9c-127">Velg **Slett** for å slette eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="a3e9c-128">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="a3e9c-128">Previous step</span></span>
[<span data-ttu-id="a3e9c-129">Kjøre og overvåke et eksperiment</span><span class="sxs-lookup"><span data-stu-id="a3e9c-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
