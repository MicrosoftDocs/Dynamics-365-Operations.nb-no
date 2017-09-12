--- 
title: "Opprette en tidsplan for et område"
description: "Denne fremgangsmåten viser hvordan du planlegger produksjonsordrer som ennå ikke er startet for et område."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 775428bf84a752c03c492e764fa9ed576ab64fb8
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="4a111-103">Opprette en tidsplan for et område</span><span class="sxs-lookup"><span data-stu-id="4a111-103">Create a schedule for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a111-104">Denne fremgangsmåten viser hvordan du planlegger produksjonsordrer som ennå ikke er startet for et område.</span><span class="sxs-lookup"><span data-stu-id="4a111-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="4a111-105">USMF-demodatafirmaet brukes til å utføre denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="4a111-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="4a111-106">Identifisere produksjonsordrer som ikke er startet</span><span class="sxs-lookup"><span data-stu-id="4a111-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="4a111-107">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="4a111-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="4a111-108">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="4a111-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4a111-109">Du kan for eksempel filtrere på Område-feltet med verdien 1.</span><span class="sxs-lookup"><span data-stu-id="4a111-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="4a111-110">1 representerer et område i USMF.</span><span class="sxs-lookup"><span data-stu-id="4a111-110">1 represents a site in USMF.</span></span> <span data-ttu-id="4a111-111">Hvis du ikke bruker USMF, velger du et område fra firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="4a111-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="4a111-112">Åpne kolonnefilteret Status.</span><span class="sxs-lookup"><span data-stu-id="4a111-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="4a111-113">Bruk et filter på "Status"-feltet, med verdien "Planlagt", ved hjelp av filteroperatoren "er nøyaktig".</span><span class="sxs-lookup"><span data-stu-id="4a111-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="4a111-114">Opprette en tidsplan</span><span class="sxs-lookup"><span data-stu-id="4a111-114">Create a schedule</span></span>
1. <span data-ttu-id="4a111-115">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="4a111-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="4a111-116">Klikk Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4a111-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="4a111-117">Klikk Planlegg jobber.</span><span class="sxs-lookup"><span data-stu-id="4a111-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="4a111-118">Velg Bakover fra leveringsdato i Planleggingsretning-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a111-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="4a111-119">Velg Nei i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a111-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="4a111-120">Velg Nei i Begrenset materiale-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a111-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="4a111-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a111-121">Click OK.</span></span>
    * <span data-ttu-id="4a111-122">Dette kan ta en stund.</span><span class="sxs-lookup"><span data-stu-id="4a111-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="4a111-123">Vise resultatet av planlagte produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="4a111-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="4a111-124">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4a111-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4a111-125">Du kan merke en vilkårlig rad.</span><span class="sxs-lookup"><span data-stu-id="4a111-125">You can mark any row.</span></span>  
2. <span data-ttu-id="4a111-126">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4a111-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="4a111-127">Klikk Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="4a111-127">Click All jobs.</span></span>
    * <span data-ttu-id="4a111-128">På denne siden kan du se listen over jobber.</span><span class="sxs-lookup"><span data-stu-id="4a111-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="4a111-129">I kategorien Planlegging kan du se start- og sluttdato for en jobb.</span><span class="sxs-lookup"><span data-stu-id="4a111-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="4a111-130">Klikk Materialer.</span><span class="sxs-lookup"><span data-stu-id="4a111-130">Click Materials.</span></span>
    * <span data-ttu-id="4a111-131">På denne siden kan du se det forventede materialforbruket for operasjonene i produksjonsordren og gjeldende tilgjengelig lager.</span><span class="sxs-lookup"><span data-stu-id="4a111-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  


