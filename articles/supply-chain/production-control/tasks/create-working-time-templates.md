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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e8e43900fd25f0051124d761dc7b06d4f9313a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006822"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="ec74e-103">Opprette driftstidsmaler</span><span class="sxs-lookup"><span data-stu-id="ec74e-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec74e-104">Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="ec74e-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="ec74e-105">Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene.</span><span class="sxs-lookup"><span data-stu-id="ec74e-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="ec74e-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="ec74e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="ec74e-107">Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.</span><span class="sxs-lookup"><span data-stu-id="ec74e-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="ec74e-108">Klikk på Driftstidsmaler.</span><span class="sxs-lookup"><span data-stu-id="ec74e-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="ec74e-109">Opprette driftstidsmal</span><span class="sxs-lookup"><span data-stu-id="ec74e-109">Create working time template</span></span>
1. <span data-ttu-id="ec74e-110">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="ec74e-110">Click New.</span></span>
2. <span data-ttu-id="ec74e-111">Skriv inn en verdi i feltet Driftstidsmal.</span><span class="sxs-lookup"><span data-stu-id="ec74e-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="ec74e-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ec74e-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ec74e-113">Utvid delen Mandag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="ec74e-114">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="ec74e-114">Click Add.</span></span>
6. <span data-ttu-id="ec74e-115">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="ec74e-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="ec74e-116">Angi tidspunktet når arbeidet begynner om morgenen.</span><span class="sxs-lookup"><span data-stu-id="ec74e-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="ec74e-117">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="ec74e-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="ec74e-118">Angi tidspunktet når arbeidere tar lunsjpause.</span><span class="sxs-lookup"><span data-stu-id="ec74e-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="ec74e-119">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="ec74e-119">Click Add.</span></span>
9. <span data-ttu-id="ec74e-120">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="ec74e-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="ec74e-121">Angi tidspunktet når arbeidet fortsetter etter lunsj.</span><span class="sxs-lookup"><span data-stu-id="ec74e-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="ec74e-122">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="ec74e-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="ec74e-123">Angi slutten på arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="ec74e-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="ec74e-124">Replikere arbeidstider til alle ukedager</span><span class="sxs-lookup"><span data-stu-id="ec74e-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="ec74e-125">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-125">Click Copy day.</span></span>
    * <span data-ttu-id="ec74e-126">Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="ec74e-127">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="ec74e-127">Click OK.</span></span>
3. <span data-ttu-id="ec74e-128">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-128">Click Copy day.</span></span>
    * <span data-ttu-id="ec74e-129">Kopier arbeidstidsdefinisjonene fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="ec74e-130">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="ec74e-131">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="ec74e-131">Click OK.</span></span>
6. <span data-ttu-id="ec74e-132">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-132">Click Copy day.</span></span>
    * <span data-ttu-id="ec74e-133">Kopier arbeidstidsdefinisjonene fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="ec74e-134">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="ec74e-135">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="ec74e-135">Click OK.</span></span>
9. <span data-ttu-id="ec74e-136">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-136">Click Copy day.</span></span>
    * <span data-ttu-id="ec74e-137">Kopier arbeidstidsdefinisjonene fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="ec74e-138">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="ec74e-139">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="ec74e-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="ec74e-140">Definere tidsrom for spesielle operasjoner</span><span class="sxs-lookup"><span data-stu-id="ec74e-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="ec74e-141">Utvid delen Fredag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="ec74e-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ec74e-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ec74e-143">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="ec74e-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="ec74e-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ec74e-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ec74e-145">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="ec74e-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="ec74e-146">Merke helgedager som lukket for plukking</span><span class="sxs-lookup"><span data-stu-id="ec74e-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="ec74e-147">Utvid delen Lørdag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="ec74e-148">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="ec74e-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="ec74e-149">Utvid delen Søndag.</span><span class="sxs-lookup"><span data-stu-id="ec74e-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="ec74e-150">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="ec74e-150">Select Yes in the Closed for pickup field.</span></span>

