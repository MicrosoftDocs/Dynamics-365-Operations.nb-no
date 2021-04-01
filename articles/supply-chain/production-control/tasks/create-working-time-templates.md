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
ms.openlocfilehash: 9829e91500abf8cba3f7cbfe2f89863cb2b1f4c4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257369"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="f8506-103">Opprette driftstidsmaler</span><span class="sxs-lookup"><span data-stu-id="f8506-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8506-104">Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="f8506-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="f8506-105">Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene.</span><span class="sxs-lookup"><span data-stu-id="f8506-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="f8506-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="f8506-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="f8506-107">Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.</span><span class="sxs-lookup"><span data-stu-id="f8506-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="f8506-108">Klikk på Driftstidsmaler.</span><span class="sxs-lookup"><span data-stu-id="f8506-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="f8506-109">Opprette driftstidsmal</span><span class="sxs-lookup"><span data-stu-id="f8506-109">Create working time template</span></span>
1. <span data-ttu-id="f8506-110">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f8506-110">Click New.</span></span>
2. <span data-ttu-id="f8506-111">Skriv inn en verdi i feltet Driftstidsmal.</span><span class="sxs-lookup"><span data-stu-id="f8506-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="f8506-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f8506-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f8506-113">Utvid delen Mandag.</span><span class="sxs-lookup"><span data-stu-id="f8506-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="f8506-114">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="f8506-114">Click Add.</span></span>
6. <span data-ttu-id="f8506-115">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="f8506-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="f8506-116">Angi tidspunktet når arbeidet begynner om morgenen.</span><span class="sxs-lookup"><span data-stu-id="f8506-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="f8506-117">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="f8506-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="f8506-118">Angi tidspunktet når arbeidere tar lunsjpause.</span><span class="sxs-lookup"><span data-stu-id="f8506-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="f8506-119">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="f8506-119">Click Add.</span></span>
9. <span data-ttu-id="f8506-120">Angi et klokkeslett i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="f8506-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="f8506-121">Angi tidspunktet når arbeidet fortsetter etter lunsj.</span><span class="sxs-lookup"><span data-stu-id="f8506-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="f8506-122">Angi et klokkeslett i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="f8506-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="f8506-123">Angi slutten på arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="f8506-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="f8506-124">Replikere arbeidstider til alle ukedager</span><span class="sxs-lookup"><span data-stu-id="f8506-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="f8506-125">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="f8506-125">Click Copy day.</span></span>
    * <span data-ttu-id="f8506-126">Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="f8506-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="f8506-127">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f8506-127">Click OK.</span></span>
3. <span data-ttu-id="f8506-128">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="f8506-128">Click Copy day.</span></span>
    * <span data-ttu-id="f8506-129">Kopier arbeidstidsdefinisjonene fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="f8506-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="f8506-130">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="f8506-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="f8506-131">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f8506-131">Click OK.</span></span>
6. <span data-ttu-id="f8506-132">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="f8506-132">Click Copy day.</span></span>
    * <span data-ttu-id="f8506-133">Kopier arbeidstidsdefinisjonene fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="f8506-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="f8506-134">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="f8506-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="f8506-135">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f8506-135">Click OK.</span></span>
9. <span data-ttu-id="f8506-136">Klikk på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="f8506-136">Click Copy day.</span></span>
    * <span data-ttu-id="f8506-137">Kopier arbeidstidsdefinisjonene fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="f8506-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="f8506-138">Velg et alternativ i feltet Til ukedag.</span><span class="sxs-lookup"><span data-stu-id="f8506-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="f8506-139">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f8506-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="f8506-140">Definere tidsrom for spesielle operasjoner</span><span class="sxs-lookup"><span data-stu-id="f8506-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="f8506-141">Utvid delen Fredag.</span><span class="sxs-lookup"><span data-stu-id="f8506-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="f8506-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f8506-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f8506-143">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="f8506-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="f8506-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f8506-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f8506-145">Angi eller velg en verdi i feltet Egenskap.</span><span class="sxs-lookup"><span data-stu-id="f8506-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="f8506-146">Merke helgedager som lukket for plukking</span><span class="sxs-lookup"><span data-stu-id="f8506-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="f8506-147">Utvid delen Lørdag.</span><span class="sxs-lookup"><span data-stu-id="f8506-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="f8506-148">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="f8506-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="f8506-149">Utvid delen Søndag.</span><span class="sxs-lookup"><span data-stu-id="f8506-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="f8506-150">Velg Ja i feltet Lukket for plukk.</span><span class="sxs-lookup"><span data-stu-id="f8506-150">Select Yes in the Closed for pickup field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]