---
title: Opprette dekningsalternativer
description: Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8690dbe00c2316ccf745f5222c3cbaa9c3379f85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419940"
---
# <a name="create-coverage-options"></a><span data-ttu-id="ee4a0-103">Opprette dekningsalternativer</span><span class="sxs-lookup"><span data-stu-id="ee4a0-103">Create coverage options</span></span>

<span data-ttu-id="ee4a0-104">Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="ee4a0-105">Dekningsalternativer kan for eksempel inkludere **Bare ansatte** for en medisinsk plan, eller **2x lønn** for en forsikringsplan for livstid.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="ee4a0-106">Når det er definert, kan du bruke alternativer for fordelsdekning på nytt.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="ee4a0-107">Du kan knytte et alternativ til én eller flere planer.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="ee4a0-108">Når du har definert dekningsalternativer, knytter du dekningsalternativene til en fordelsplantype.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="ee4a0-109">Plantypen knyttes deretter til en fordelsplan eller et program.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="ee4a0-110">Dekningsalternativer som er knyttet til en plantype, er tilgjengelige for alle planer som opprettes med denne plantypen.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="ee4a0-111">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Dekningsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="ee4a0-112">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-112">Select **New**.</span></span>

3. <span data-ttu-id="ee4a0-113">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ee4a0-114">Felt</span><span class="sxs-lookup"><span data-stu-id="ee4a0-114">Field</span></span> | <span data-ttu-id="ee4a0-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ee4a0-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ee4a0-116">**Dekningsalternativ**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-116">**Coverage option**</span></span> | <span data-ttu-id="ee4a0-117">Et unikt navn på dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="ee4a0-118">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-118">**Description**</span></span> | <span data-ttu-id="ee4a0-119">En beskrivelse av dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="ee4a0-120">**Dekningskode**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-120">**Coverage code**</span></span> | <span data-ttu-id="ee4a0-121">Dekningskoder som tilordner minimums- og maksimumsbeløp for hver enkelt berettigede, dekkede persontype.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="ee4a0-122">En dekningskode angir hvem som er dekket av eller hvor mye dekning som er tillatt for en plantype.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="ee4a0-123">Du kan uttrykke dekningsbeløpet som et valutabeløp eller en prosent.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="ee4a0-124">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-124">For example:</span></span></br></br><span data-ttu-id="ee4a0-125">- **Emp+1** – for å være kvalifisert må den ansatte ha én avhengig valgt (hvis flere er valgt, er de ikke lenger kvalifisert).</span><span class="sxs-lookup"><span data-stu-id="ee4a0-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="ee4a0-126">- **Emp+familie** – for å være kvalifisert må den ansatte ha minst to avhengige valgt.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="ee4a0-127">**Maksimalt antall**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-127">**Maximum number**</span></span> | <span data-ttu-id="ee4a0-128">Det maksimale antall avhengige.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="ee4a0-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-129">**Status**</span></span> | <span data-ttu-id="ee4a0-130">Statusen for dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-130">The status of the coverage option.</span></span> <span data-ttu-id="ee4a0-131">Hvis statusen for dekningsalternativet er satt til Inaktiv, kan ikke dekningsalternativet velges på plantyper.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="ee4a0-132">**Prosent**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-132">**Percent**</span></span> | <span data-ttu-id="ee4a0-133">Prosentbeløpet.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-133">The percent amount.</span></span> <span data-ttu-id="ee4a0-134">Dette feltet er bare aktivt hvis % x lønn ble valgt i Dekningskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="ee4a0-135">**Divisor**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-135">**Divisor**</span></span> | <span data-ttu-id="ee4a0-136">Divisoren som skal brukes i beregningen når du velger dekningskoden % x lønn.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="ee4a0-137">**Minste prosentandel**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-137">**Percent minimum**</span></span> | <span data-ttu-id="ee4a0-138">Minimumsprosenten når du velger kode for prosentdekning.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="ee4a0-139">**Størst prosentandel**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-139">**Percent maximum**</span></span> | <span data-ttu-id="ee4a0-140">Maksimumsprosenten når du velger kode for prosentdekning.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="ee4a0-141">Under **Alternativer for rettighet for personlig kontakt** knytter du det aktuelle rettighetsalternativet for personlige kontakter til hvert dekningsalternativ.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="ee4a0-142">Under **Selvbetjening** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="ee4a0-143">Felt</span><span class="sxs-lookup"><span data-stu-id="ee4a0-143">Field</span></span> | <span data-ttu-id="ee4a0-144">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ee4a0-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ee4a0-145">**Tillat bidragsbeløp fra ansatt**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="ee4a0-146">Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="ee4a0-147">Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på fordeler selvbetjent.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="ee4a0-148">**Tillat dekningsbeløp fra ansatt**</span><span class="sxs-lookup"><span data-stu-id="ee4a0-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="ee4a0-149">Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="ee4a0-150">Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="ee4a0-151">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-151">Select **Save**.</span></span> 
