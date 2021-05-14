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
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920935"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="6cf0b-103">Opprette driftstidsmaler</span><span class="sxs-lookup"><span data-stu-id="6cf0b-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6cf0b-104">Driftstidsmaler definerer arbeidstimene gjennom en uke og brukes til å generere arbeidstider for en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="6cf0b-105">Denne fremgangsmåten viser hvordan du definerer en driftstidsmal ved hjelp av egenskaper for planlegging av driftstider for kategorisering av arbeidstidsintervallene.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="6cf0b-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="6cf0b-107">Gå til **Arbeidsområder > Administrasjon av livssyklus for ressurs**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="6cf0b-108">Velg **Driftstidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="6cf0b-109">Opprette driftstidsmal</span><span class="sxs-lookup"><span data-stu-id="6cf0b-109">Create working time template</span></span>

1. <span data-ttu-id="6cf0b-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-110">Select **New**.</span></span>
1. <span data-ttu-id="6cf0b-111">I feltet **Driftstidsmal** skriver du inn en verdi.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="6cf0b-112">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="6cf0b-113">Utvid delen **Mandag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="6cf0b-114">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-114">Select **Add**.</span></span>
1. <span data-ttu-id="6cf0b-115">Angi et klokkeslett i feltet **Fra**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="6cf0b-116">Angi tidspunktet når arbeidet begynner om morgenen.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="6cf0b-117">Angi et klokkeslett i feltet **Til**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="6cf0b-118">Angi tidspunktet når arbeidere tar lunsjpause.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="6cf0b-119">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-119">Select **Add**.</span></span>
1. <span data-ttu-id="6cf0b-120">Angi et klokkeslett i feltet **Fra**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="6cf0b-121">Angi tidspunktet når arbeidet fortsetter etter lunsj.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="6cf0b-122">Angi et klokkeslett i feltet **Til**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="6cf0b-123">Angi slutten på arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="6cf0b-124">Replikere arbeidstider til alle ukedager</span><span class="sxs-lookup"><span data-stu-id="6cf0b-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="6cf0b-125">Velg **Kopier dag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="6cf0b-126">Kopier arbeidstidsdefinisjonene fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="6cf0b-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-127">Select **OK**.</span></span>
1. <span data-ttu-id="6cf0b-128">Velg **Kopier dag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="6cf0b-129">Kopier arbeidstidsdefinisjonene fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="6cf0b-130">Velg et alternativ i feltet **Til ukedag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="6cf0b-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-131">Select **OK**.</span></span>
1. <span data-ttu-id="6cf0b-132">Velg **Kopier dag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="6cf0b-133">Kopier arbeidstidsdefinisjonene fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="6cf0b-134">Velg et alternativ i feltet **Til ukedag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="6cf0b-135">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-135">Select **OK**.</span></span>
1. <span data-ttu-id="6cf0b-136">Velg **Kopier dag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="6cf0b-137">Kopier arbeidstidsdefinisjonene fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="6cf0b-138">Velg et alternativ i feltet **Til ukedag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="6cf0b-139">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="6cf0b-140">Definere tidsrom for spesielle operasjoner</span><span class="sxs-lookup"><span data-stu-id="6cf0b-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="6cf0b-141">Utvid delen **Fredag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="6cf0b-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="6cf0b-143">Angi eller velg en verdi i feltet **Egenskap**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="6cf0b-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="6cf0b-145">Angi eller velg en verdi i feltet **Egenskap**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="6cf0b-146">Merke helgedager som lukket for plukking</span><span class="sxs-lookup"><span data-stu-id="6cf0b-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="6cf0b-147">Utvid delen **Lørdag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="6cf0b-148">Velg *Ja* i feltet **Lukket for plukk**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="6cf0b-149">Utvid delen **Søndag**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="6cf0b-150">Velg *Ja* i feltet **Lukket for plukk**.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]