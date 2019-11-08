---
title: Opprette aktivitetsrelasjon - Etterfølger
description: Flyten av aktiviteter i en lean produksjonsflyt er dokumentert gjennom aktivitetsrelasjoner.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07ebb7d2158964a5d8862df998fe470032a0d354
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550419"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="bf28c-103">Opprette aktivitetsrelasjon - Etterfølger</span><span class="sxs-lookup"><span data-stu-id="bf28c-103">Create activity relation - Successor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bf28c-104">Flyten av aktiviteter i en lean produksjonsflyt er dokumentert gjennom aktivitetsrelasjoner.</span><span class="sxs-lookup"><span data-stu-id="bf28c-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="bf28c-105">Denne registreringen viser hvordan du oppretter en aktivitetsrelasjon.</span><span class="sxs-lookup"><span data-stu-id="bf28c-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="bf28c-106">Forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="bf28c-106">Prerequisites:</span></span>

- <span data-ttu-id="bf28c-107">En produksjonsflyt og versjon i utkastmodus.</span><span class="sxs-lookup"><span data-stu-id="bf28c-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="bf28c-108">To aktiviteter som kommer etter hverandre i produksjonsflyten er opprettet, men ikke er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="bf28c-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="bf28c-109">Finne produksjonsflytversjonen</span><span class="sxs-lookup"><span data-stu-id="bf28c-109">Find the production flow version</span></span> 
1. <span data-ttu-id="bf28c-110">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="bf28c-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="bf28c-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bf28c-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bf28c-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bf28c-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bf28c-113">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bf28c-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="bf28c-114">Velg en utkastversjon i listen.</span><span class="sxs-lookup"><span data-stu-id="bf28c-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="bf28c-115">Aktivitetsrelasjoner kan legges til i både utkast eller aktive versjoner av en produksjonsflyt.</span><span class="sxs-lookup"><span data-stu-id="bf28c-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="bf28c-116">Åpne aktivitetsoversikten</span><span class="sxs-lookup"><span data-stu-id="bf28c-116">Open the activity overview</span></span>
1. <span data-ttu-id="bf28c-117">Klikk Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="bf28c-117">Click Activities.</span></span>
    * <span data-ttu-id="bf28c-118">Legg merke til at skjemaet viser alle aktiviteter for produksjonsflyten som er fordelt til versjonen av produksjonsflytene som du arbeider i.</span><span class="sxs-lookup"><span data-stu-id="bf28c-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="bf28c-119">Legg til en etterfølgende aktivitet</span><span class="sxs-lookup"><span data-stu-id="bf28c-119">Add a Successor</span></span>
1. <span data-ttu-id="bf28c-120">Klikk Legg til etterfølgende aktivitet.</span><span class="sxs-lookup"><span data-stu-id="bf28c-120">Click Add successor.</span></span>
2. <span data-ttu-id="bf28c-121">Klikk rullegardinknappen i feltet Aktivitet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="bf28c-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bf28c-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bf28c-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bf28c-123">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bf28c-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bf28c-124">Merk av for Begrensning.</span><span class="sxs-lookup"><span data-stu-id="bf28c-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="bf28c-125">Angi et tall i feltet Begrensningsverdi.</span><span class="sxs-lookup"><span data-stu-id="bf28c-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="bf28c-126">Begrensningstiden er tiden som skal planlegges mellom den planlagte slutten av den foregående (forfallsdato og -klokkeslett) og den planlagte starten for den etterfølgende.</span><span class="sxs-lookup"><span data-stu-id="bf28c-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="bf28c-127">Skriv inn en verdi i feltet Enheter.</span><span class="sxs-lookup"><span data-stu-id="bf28c-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="bf28c-128">Angi et tall i feltet Forhold for syklustid.</span><span class="sxs-lookup"><span data-stu-id="bf28c-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="bf28c-129">Hvis begge aktiviteter kjører på den samme takten, skal syklustidsforholdet være 1.</span><span class="sxs-lookup"><span data-stu-id="bf28c-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="bf28c-130">Hvis den foregående aktiviteten kjøres med den etterfølgende aktiviteten Dobbel hastighet, skal forholdet være 2.</span><span class="sxs-lookup"><span data-stu-id="bf28c-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="bf28c-131">Syklustidforholdene brukes til å beregne de individuelle syklustidene for produksjonsflytaktivitetene.</span><span class="sxs-lookup"><span data-stu-id="bf28c-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="bf28c-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bf28c-132">Click OK.</span></span>
10. <span data-ttu-id="bf28c-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bf28c-133">Close the page.</span></span>
11. <span data-ttu-id="bf28c-134">Klikk kategorien GridPanel.</span><span class="sxs-lookup"><span data-stu-id="bf28c-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="bf28c-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bf28c-135">Close the page.</span></span>
13. <span data-ttu-id="bf28c-136">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="bf28c-136">Refresh the page.</span></span>

