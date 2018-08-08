--- 
title: Opprette driftstidsmaler
description: "Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: d9290dd363e5e617ec714f9b3ee8b71a21a61166
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="create-working-time-templates"></a><span data-ttu-id="accdb-103">Opprette driftstidsmaler</span><span class="sxs-lookup"><span data-stu-id="accdb-103">Create working time templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="accdb-104">Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="accdb-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="accdb-105">Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene.</span><span class="sxs-lookup"><span data-stu-id="accdb-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="accdb-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="accdb-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="accdb-107">Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.</span><span class="sxs-lookup"><span data-stu-id="accdb-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="accdb-108">Klikk Driftstidsmaler.</span><span class="sxs-lookup"><span data-stu-id="accdb-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="accdb-109">Opprette driftstidsmal</span><span class="sxs-lookup"><span data-stu-id="accdb-109">Create working time template</span></span>
1. <span data-ttu-id="accdb-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="accdb-110">Click New.</span></span>
2. <span data-ttu-id="accdb-111">Skriv inn en verdi i feltet Driftstidsmal.</span><span class="sxs-lookup"><span data-stu-id="accdb-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="accdb-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="accdb-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="accdb-113">Utvid delen Mandag.</span><span class="sxs-lookup"><span data-stu-id="accdb-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="accdb-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="accdb-114">Click Add.</span></span>
6. <span data-ttu-id="accdb-115">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="accdb-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="accdb-116">Angi tidspunktet når arbeidet begynner om morgenen.</span><span class="sxs-lookup"><span data-stu-id="accdb-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="accdb-117">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="accdb-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="accdb-118">Angi tidspunktet når arbeidere tar lunsjpause.</span><span class="sxs-lookup"><span data-stu-id="accdb-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="accdb-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="accdb-119">Click Add.</span></span>
9. <span data-ttu-id="accdb-120">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="accdb-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="accdb-121">Angi tidspunktet når arbeidet fortsetter etter lunsj.</span><span class="sxs-lookup"><span data-stu-id="accdb-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="accdb-122">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="accdb-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="accdb-123">Angi slutten på arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="accdb-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="accdb-124">Replikere arbeidstider til alle ukedager</span><span class="sxs-lookup"><span data-stu-id="accdb-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="accdb-125">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="accdb-125">Click Copy day.</span></span>
    * <span data-ttu-id="accdb-126">Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="accdb-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="accdb-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="accdb-127">Click OK.</span></span>
3. <span data-ttu-id="accdb-128">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="accdb-128">Click Copy day.</span></span>
    * <span data-ttu-id="accdb-129">Kopier arbeidstidsdefinisjonene fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="accdb-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="accdb-130">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="accdb-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="accdb-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="accdb-131">Click OK.</span></span>
6. <span data-ttu-id="accdb-132">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="accdb-132">Click Copy day.</span></span>
    * <span data-ttu-id="accdb-133">Kopier arbeidstidsdefinisjonene fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="accdb-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="accdb-134">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="accdb-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="accdb-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="accdb-135">Click OK.</span></span>
9. <span data-ttu-id="accdb-136">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="accdb-136">Click Copy day.</span></span>
    * <span data-ttu-id="accdb-137">Kopier arbeidstidsdefinisjonene fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="accdb-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="accdb-138">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="accdb-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="accdb-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="accdb-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="accdb-140">Definere tidsrom for spesielle operasjoner</span><span class="sxs-lookup"><span data-stu-id="accdb-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="accdb-141">Utvid delen Fredag.</span><span class="sxs-lookup"><span data-stu-id="accdb-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="accdb-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="accdb-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="accdb-143">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="accdb-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="accdb-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="accdb-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="accdb-145">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="accdb-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="accdb-146">Merke helgedager som lukket for plukking</span><span class="sxs-lookup"><span data-stu-id="accdb-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="accdb-147">Utvid delen Lørdag.</span><span class="sxs-lookup"><span data-stu-id="accdb-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="accdb-148">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="accdb-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="accdb-149">Utvid delen Søndag.</span><span class="sxs-lookup"><span data-stu-id="accdb-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="accdb-150">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="accdb-150">Select Yes in the Closed for pickup field.</span></span>


