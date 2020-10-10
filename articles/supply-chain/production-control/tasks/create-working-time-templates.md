---
title: Opprette driftstidsmaler
description: Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5bd1b384fe66dd7d59b776bdf1154cc5b8262ce
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826530"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="4a22f-103">Opprette driftstidsmaler</span><span class="sxs-lookup"><span data-stu-id="4a22f-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a22f-104">Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="4a22f-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="4a22f-105">Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene.</span><span class="sxs-lookup"><span data-stu-id="4a22f-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="4a22f-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="4a22f-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="4a22f-107">Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.</span><span class="sxs-lookup"><span data-stu-id="4a22f-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="4a22f-108">Klikk Driftstidsmaler.</span><span class="sxs-lookup"><span data-stu-id="4a22f-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="4a22f-109">Opprette driftstidsmal</span><span class="sxs-lookup"><span data-stu-id="4a22f-109">Create working time template</span></span>
1. <span data-ttu-id="4a22f-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4a22f-110">Click New.</span></span>
2. <span data-ttu-id="4a22f-111">Skriv inn en verdi i feltet Driftstidsmal.</span><span class="sxs-lookup"><span data-stu-id="4a22f-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="4a22f-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a22f-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4a22f-113">Utvid delen Mandag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="4a22f-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a22f-114">Click Add.</span></span>
6. <span data-ttu-id="4a22f-115">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="4a22f-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="4a22f-116">Angi tidspunktet når arbeidet begynner om morgenen.</span><span class="sxs-lookup"><span data-stu-id="4a22f-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="4a22f-117">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="4a22f-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="4a22f-118">Angi tidspunktet når arbeidere tar lunsjpause.</span><span class="sxs-lookup"><span data-stu-id="4a22f-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="4a22f-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a22f-119">Click Add.</span></span>
9. <span data-ttu-id="4a22f-120">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="4a22f-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="4a22f-121">Angi tidspunktet når arbeidet fortsetter etter lunsj.</span><span class="sxs-lookup"><span data-stu-id="4a22f-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="4a22f-122">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="4a22f-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="4a22f-123">Angi slutten på arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="4a22f-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="4a22f-124">Replikere arbeidstider til alle ukedager</span><span class="sxs-lookup"><span data-stu-id="4a22f-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="4a22f-125">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-125">Click Copy day.</span></span>
    * <span data-ttu-id="4a22f-126">Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="4a22f-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a22f-127">Click OK.</span></span>
3. <span data-ttu-id="4a22f-128">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-128">Click Copy day.</span></span>
    * <span data-ttu-id="4a22f-129">Kopier arbeidstidsdefinisjonene fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="4a22f-130">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="4a22f-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a22f-131">Click OK.</span></span>
6. <span data-ttu-id="4a22f-132">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-132">Click Copy day.</span></span>
    * <span data-ttu-id="4a22f-133">Kopier arbeidstidsdefinisjonene fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="4a22f-134">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="4a22f-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a22f-135">Click OK.</span></span>
9. <span data-ttu-id="4a22f-136">Klikk Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-136">Click Copy day.</span></span>
    * <span data-ttu-id="4a22f-137">Kopier arbeidstidsdefinisjonene fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="4a22f-138">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="4a22f-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a22f-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="4a22f-140">Definere tidsrom for spesielle operasjoner</span><span class="sxs-lookup"><span data-stu-id="4a22f-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="4a22f-141">Utvid delen Fredag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="4a22f-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4a22f-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4a22f-143">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="4a22f-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="4a22f-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4a22f-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4a22f-145">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="4a22f-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="4a22f-146">Merke helgedager som lukket for plukking</span><span class="sxs-lookup"><span data-stu-id="4a22f-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="4a22f-147">Utvid delen Lørdag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="4a22f-148">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="4a22f-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="4a22f-149">Utvid delen Søndag.</span><span class="sxs-lookup"><span data-stu-id="4a22f-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="4a22f-150">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="4a22f-150">Select Yes in the Closed for pickup field.</span></span>

