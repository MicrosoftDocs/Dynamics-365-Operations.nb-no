---
title: Opprette driftstidsmaler
description: Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c82126d64954f8691571b80ab97b198d58a9e2cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837716"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="00728-103">Opprette driftstidsmaler</span><span class="sxs-lookup"><span data-stu-id="00728-103">Create working time templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00728-104">Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="00728-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="00728-105">Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene.</span><span class="sxs-lookup"><span data-stu-id="00728-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="00728-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="00728-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="00728-107">Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.</span><span class="sxs-lookup"><span data-stu-id="00728-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="00728-108">Klikk Driftstidsmaler.</span><span class="sxs-lookup"><span data-stu-id="00728-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="00728-109">Opprette driftstidsmal</span><span class="sxs-lookup"><span data-stu-id="00728-109">Create working time template</span></span>
1. <span data-ttu-id="00728-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="00728-110">Click New.</span></span>
2. <span data-ttu-id="00728-111">Skriv inn en verdi i feltet Driftstidsmal.</span><span class="sxs-lookup"><span data-stu-id="00728-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="00728-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="00728-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="00728-113">Utvid delen Mandag.</span><span class="sxs-lookup"><span data-stu-id="00728-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="00728-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="00728-114">Click Add.</span></span>
6. <span data-ttu-id="00728-115">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="00728-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="00728-116">Angi tidspunktet når arbeidet begynner om morgenen.</span><span class="sxs-lookup"><span data-stu-id="00728-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="00728-117">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="00728-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="00728-118">Angi tidspunktet når arbeidere tar lunsjpause.</span><span class="sxs-lookup"><span data-stu-id="00728-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="00728-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="00728-119">Click Add.</span></span>
9. <span data-ttu-id="00728-120">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="00728-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="00728-121">Angi tidspunktet når arbeidet fortsetter etter lunsj.</span><span class="sxs-lookup"><span data-stu-id="00728-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="00728-122">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="00728-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="00728-123">Angi slutten på arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="00728-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="00728-124">Replikere arbeidstider til alle ukedager</span><span class="sxs-lookup"><span data-stu-id="00728-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="00728-125">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="00728-125">Click Copy day.</span></span>
    * <span data-ttu-id="00728-126">Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="00728-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="00728-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00728-127">Click OK.</span></span>
3. <span data-ttu-id="00728-128">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="00728-128">Click Copy day.</span></span>
    * <span data-ttu-id="00728-129">Kopier arbeidstidsdefinisjonene fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="00728-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="00728-130">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="00728-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="00728-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00728-131">Click OK.</span></span>
6. <span data-ttu-id="00728-132">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="00728-132">Click Copy day.</span></span>
    * <span data-ttu-id="00728-133">Kopier arbeidstidsdefinisjonene fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="00728-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="00728-134">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="00728-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="00728-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00728-135">Click OK.</span></span>
9. <span data-ttu-id="00728-136">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="00728-136">Click Copy day.</span></span>
    * <span data-ttu-id="00728-137">Kopier arbeidstidsdefinisjonene fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="00728-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="00728-138">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="00728-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="00728-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00728-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="00728-140">Definere tidsrom for spesielle operasjoner</span><span class="sxs-lookup"><span data-stu-id="00728-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="00728-141">Utvid delen Fredag.</span><span class="sxs-lookup"><span data-stu-id="00728-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="00728-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="00728-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="00728-143">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="00728-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="00728-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="00728-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="00728-145">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="00728-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="00728-146">Merke helgedager som lukket for plukking</span><span class="sxs-lookup"><span data-stu-id="00728-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="00728-147">Utvid delen Lørdag.</span><span class="sxs-lookup"><span data-stu-id="00728-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="00728-148">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="00728-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="00728-149">Utvid delen Søndag.</span><span class="sxs-lookup"><span data-stu-id="00728-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="00728-150">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="00728-150">Select Yes in the Closed for pickup field.</span></span>

