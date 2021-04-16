---
title: Opprette driftstidsmaler
description: Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1885aba11b5c6878cc9dca615cea98b77b4df63f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811588"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="3496d-103">Opprette driftstidsmaler</span><span class="sxs-lookup"><span data-stu-id="3496d-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3496d-104">Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="3496d-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="3496d-105">Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene.</span><span class="sxs-lookup"><span data-stu-id="3496d-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="3496d-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="3496d-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="3496d-107">Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.</span><span class="sxs-lookup"><span data-stu-id="3496d-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="3496d-108">Klikk på Driftstidsmaler.</span><span class="sxs-lookup"><span data-stu-id="3496d-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="3496d-109">Opprette driftstidsmal</span><span class="sxs-lookup"><span data-stu-id="3496d-109">Create working time template</span></span>
1. <span data-ttu-id="3496d-110">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3496d-110">Click New.</span></span>
2. <span data-ttu-id="3496d-111">Skriv inn en verdi i feltet Driftstidsmal.</span><span class="sxs-lookup"><span data-stu-id="3496d-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="3496d-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3496d-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3496d-113">Utvid delen Mandag.</span><span class="sxs-lookup"><span data-stu-id="3496d-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="3496d-114">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3496d-114">Click Add.</span></span>
6. <span data-ttu-id="3496d-115">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="3496d-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="3496d-116">Angi tidspunktet når arbeidet begynner om morgenen.</span><span class="sxs-lookup"><span data-stu-id="3496d-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="3496d-117">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="3496d-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="3496d-118">Angi tidspunktet når arbeidere tar lunsjpause.</span><span class="sxs-lookup"><span data-stu-id="3496d-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="3496d-119">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3496d-119">Click Add.</span></span>
9. <span data-ttu-id="3496d-120">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="3496d-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="3496d-121">Angi tidspunktet når arbeidet fortsetter etter lunsj.</span><span class="sxs-lookup"><span data-stu-id="3496d-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="3496d-122">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="3496d-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="3496d-123">Angi slutten på arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="3496d-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="3496d-124">Replikere arbeidstider til alle ukedager</span><span class="sxs-lookup"><span data-stu-id="3496d-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="3496d-125">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="3496d-125">Click Copy day.</span></span>
    * <span data-ttu-id="3496d-126">Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="3496d-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="3496d-127">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3496d-127">Click OK.</span></span>
3. <span data-ttu-id="3496d-128">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="3496d-128">Click Copy day.</span></span>
    * <span data-ttu-id="3496d-129">Kopier arbeidstidsdefinisjonene fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="3496d-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="3496d-130">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="3496d-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="3496d-131">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3496d-131">Click OK.</span></span>
6. <span data-ttu-id="3496d-132">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="3496d-132">Click Copy day.</span></span>
    * <span data-ttu-id="3496d-133">Kopier arbeidstidsdefinisjonene fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="3496d-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="3496d-134">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="3496d-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="3496d-135">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3496d-135">Click OK.</span></span>
9. <span data-ttu-id="3496d-136">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="3496d-136">Click Copy day.</span></span>
    * <span data-ttu-id="3496d-137">Kopier arbeidstidsdefinisjonene fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="3496d-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="3496d-138">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="3496d-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="3496d-139">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3496d-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="3496d-140">Definere tidsrom for spesielle operasjoner</span><span class="sxs-lookup"><span data-stu-id="3496d-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="3496d-141">Utvid delen Fredag.</span><span class="sxs-lookup"><span data-stu-id="3496d-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="3496d-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3496d-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3496d-143">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="3496d-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="3496d-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3496d-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3496d-145">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="3496d-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="3496d-146">Merke helgedager som lukket for plukking</span><span class="sxs-lookup"><span data-stu-id="3496d-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="3496d-147">Utvid delen Lørdag.</span><span class="sxs-lookup"><span data-stu-id="3496d-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="3496d-148">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="3496d-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="3496d-149">Utvid delen Søndag.</span><span class="sxs-lookup"><span data-stu-id="3496d-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="3496d-150">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="3496d-150">Select Yes in the Closed for pickup field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]