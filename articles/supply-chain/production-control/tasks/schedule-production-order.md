--- 
title: Planlegge en produksjonsordre
description: Denne prosedyren viser hvordan du planlegger en produksjonsordre.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 20e7ee023f39cc5d02b0f5b80fbb3ae3ad0c9774
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="schedule-a-production-order"></a><span data-ttu-id="255d3-103">Planlegge en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="255d3-103">Schedule a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="255d3-104">Denne prosedyren viser hvordan du planlegger en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="255d3-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="255d3-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="255d3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="255d3-106">Dette er den tredje prosedyren av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="255d3-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="255d3-107">Planlegge en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="255d3-107">Schedule a production order</span></span>
1. <span data-ttu-id="255d3-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="255d3-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="255d3-109">Velg en produksjonsordre med statusen Estimert.</span><span class="sxs-lookup"><span data-stu-id="255d3-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="255d3-110">Klikk Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="255d3-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="255d3-111">Klikk Planlegg jobber.</span><span class="sxs-lookup"><span data-stu-id="255d3-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="255d3-112">Parameterne for planlegging er definert på denne siden.</span><span class="sxs-lookup"><span data-stu-id="255d3-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="255d3-113">Du kan definere parameterne for bestemte brukere eller alle brukere.</span><span class="sxs-lookup"><span data-stu-id="255d3-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="255d3-114">Velg Fremover fra i dag i Planleggingsretning-feltet.</span><span class="sxs-lookup"><span data-stu-id="255d3-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="255d3-115">Angi en dato i Planleggingsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="255d3-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="255d3-116">Merk av for eller fjern merket for Begrenset kapasitet.</span><span class="sxs-lookup"><span data-stu-id="255d3-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="255d3-117">Merk av for eller fjern merket for Begrenset materiale.</span><span class="sxs-lookup"><span data-stu-id="255d3-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="255d3-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="255d3-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="255d3-119">Vise planleggingsresultatene</span><span class="sxs-lookup"><span data-stu-id="255d3-119">View the scheduling results</span></span>
1. <span data-ttu-id="255d3-120">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="255d3-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="255d3-121">Klikk Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="255d3-121">Click All jobs.</span></span>
    * <span data-ttu-id="255d3-122">Denne siden viser planlagte jobber som du nettopp har generert.</span><span class="sxs-lookup"><span data-stu-id="255d3-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="255d3-123">Vis eller skjul Planlegging-delen.</span><span class="sxs-lookup"><span data-stu-id="255d3-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="255d3-124">Du kan vise planlagt dato og klokkeslett på hurtigfanen Planlegging.</span><span class="sxs-lookup"><span data-stu-id="255d3-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="255d3-125">Klikk Forespørsler.</span><span class="sxs-lookup"><span data-stu-id="255d3-125">Click Inquiries.</span></span>
5. <span data-ttu-id="255d3-126">Klikk Kapasitetsbelastning.</span><span class="sxs-lookup"><span data-stu-id="255d3-126">Click Capacity load.</span></span>
    * <span data-ttu-id="255d3-127">Kapasitetsbelastning-siden viser kapasiteten som er reservert gjennom finplanlegging, totalt antall timer som er reservert for ressursen nå, og gjenværende antall timer som er tilgjengelig for finplanlegging av ressursen.</span><span class="sxs-lookup"><span data-stu-id="255d3-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="255d3-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="255d3-128">Close the page.</span></span>
7. <span data-ttu-id="255d3-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="255d3-129">Close the page.</span></span>


