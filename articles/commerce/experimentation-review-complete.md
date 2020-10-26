---
title: Fremme en variasjon og fullføre et eksperiment
description: Dette emnet beskriver hvordan du fremmer en vellykket variasjon og fullfører et eksperiment i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930256"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="0fa50-103">Fremme en variasjon og fullføre et eksperiment</span><span class="sxs-lookup"><span data-stu-id="0fa50-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="0fa50-104">Dette emnet beskriver hvordan du kan fremme variasjonen som produserte de best resultatene i eksperimentet, og hvordan du fullfører eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="0fa50-105">Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0fa50-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0fa50-106">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="0fa50-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="0fa50-107">[ ![Brukerreise for eksperimentering – se gjennom og fullføre](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0fa50-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="0fa50-108">Når du har [kjørt eksperimentet](experimentation-run-monitor.md) og samlet inn nok data til å avgjøre hvilken variasjon du vil bruke på det aktive området, kan du fremme variasjonen og avslutte eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="0fa50-109">Fremme en variasjon</span><span class="sxs-lookup"><span data-stu-id="0fa50-109">Promote a variation</span></span>
<span data-ttu-id="0fa50-110">Bruk dataene og analysen som er relatert til eksperimentet i tredjepartstjenesten, til å avgjøre hvilken variant som oppnådde det beste resultatet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="0fa50-111">Hvis du vil erstatte gjeldende innhold på det aktive området med den vinnende variasjonen, slik at det er tilgjengelig for alle som bruker nettstedet, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="0fa50-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="0fa50-112">Gå til kategorien **Eksperimenter** i områdebygger, og velg eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="0fa50-113">Velg **Fullfør eksperimente** på linjen øverst.</span><span class="sxs-lookup"><span data-stu-id="0fa50-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="0fa50-114">På dialogboksmenyen **Fullfør eksperiment** velger du **Se gjennom eksperimentdataene** .</span><span class="sxs-lookup"><span data-stu-id="0fa50-114">In the **Complete the experiment** dialog menu, select **Review the experiment data** .</span></span> <span data-ttu-id="0fa50-115">Det åpnes en tredjepartstjeneste der du kan validere måledataene og avgjøre hvilken variant som er fungerte best.</span><span class="sxs-lookup"><span data-stu-id="0fa50-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="0fa50-116">På dialogboksmenyen **Fullfør eksperiment** i områdebygger, velger du den vinnende variasjonen og velger deretter **Neste** .</span><span class="sxs-lookup"><span data-stu-id="0fa50-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next** .</span></span>
1. <span data-ttu-id="0fa50-117">Åpne tredjepartstjenesten, og stopp eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="0fa50-118">Velg **Fullfør** i områdebygger for å overskrive den opprinnelige aktive siden og publisere den vinnende variasjonen, slik at den er tilgjengelig for alle som bruker nettstedet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="0fa50-119">Hvis du velger å beholde gjeldende aktive side og ikke publisere en variasjon, velger du **Publiser den opprinnelige siden på nytt** .</span><span class="sxs-lookup"><span data-stu-id="0fa50-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page** .</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="0fa50-120">Slette eksperimentet</span><span class="sxs-lookup"><span data-stu-id="0fa50-120">Delete your experiment</span></span>
<span data-ttu-id="0fa50-121">Selv om det ikke er nødvendig at du sletter et fullført eksperiment i Commerce, kan du velge å slette det for å spare plass eller rydde arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="0fa50-122">Gjør følgende for å slette et eksperiment:</span><span class="sxs-lookup"><span data-stu-id="0fa50-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="0fa50-123">Gå til kategorien **Eksperimenter** i områdebygger, og velg eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="0fa50-124">Hvis eksperimentet fortsatt er aktivt, stopper du eksperimentet i tredjepartstjenesten før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="0fa50-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="0fa50-125">Velg **Opphev publisering** på kommandolinjen for å fjerne variasjonsinnholdet fra det aktive området.</span><span class="sxs-lookup"><span data-stu-id="0fa50-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="0fa50-126">Velg **Slett** på kommandolinjen for å slette eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0fa50-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="0fa50-127">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="0fa50-127">Previous step</span></span>
[<span data-ttu-id="0fa50-128">Kjør og Overvåk et eksperiment</span><span class="sxs-lookup"><span data-stu-id="0fa50-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
