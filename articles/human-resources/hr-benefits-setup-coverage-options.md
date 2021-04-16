---
title: Opprette dekningsalternativer
description: Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6d304b0cf65c7833ebc7f21323efc59540289de8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803687"
---
# <a name="create-coverage-options"></a><span data-ttu-id="03a2b-103">Opprette dekningsalternativer</span><span class="sxs-lookup"><span data-stu-id="03a2b-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="03a2b-104">Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program.</span><span class="sxs-lookup"><span data-stu-id="03a2b-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="03a2b-105">Dekningsalternativer kan for eksempel inkludere **Bare ansatte** for en medisinsk plan, eller **2x lønn** for en forsikringsplan for livstid.</span><span class="sxs-lookup"><span data-stu-id="03a2b-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="03a2b-106">Når det er definert, kan du bruke alternativer for fordelsdekning på nytt.</span><span class="sxs-lookup"><span data-stu-id="03a2b-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="03a2b-107">Du kan knytte et alternativ til én eller flere planer.</span><span class="sxs-lookup"><span data-stu-id="03a2b-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="03a2b-108">Når du har definert dekningsalternativer, knytter du dekningsalternativene til en fordelsplantype.</span><span class="sxs-lookup"><span data-stu-id="03a2b-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="03a2b-109">Plantypen knyttes deretter til en fordelsplan eller et program.</span><span class="sxs-lookup"><span data-stu-id="03a2b-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="03a2b-110">Dekningsalternativer som er knyttet til en plantype, er tilgjengelige for alle planer som opprettes med denne plantypen.</span><span class="sxs-lookup"><span data-stu-id="03a2b-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="03a2b-111">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Dekningsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="03a2b-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="03a2b-112">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="03a2b-112">Select **New**.</span></span>

3. <span data-ttu-id="03a2b-113">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="03a2b-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="03a2b-114">Felt</span><span class="sxs-lookup"><span data-stu-id="03a2b-114">Field</span></span> | <span data-ttu-id="03a2b-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="03a2b-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="03a2b-116">**Dekningsalternativ**</span><span class="sxs-lookup"><span data-stu-id="03a2b-116">**Coverage option**</span></span> | <span data-ttu-id="03a2b-117">Et unikt navn på dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="03a2b-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="03a2b-118">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="03a2b-118">**Description**</span></span> | <span data-ttu-id="03a2b-119">En beskrivelse av dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="03a2b-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="03a2b-120">**Dekningskode**</span><span class="sxs-lookup"><span data-stu-id="03a2b-120">**Coverage code**</span></span> | <span data-ttu-id="03a2b-121">Dekningskoder som tilordner minimums- og maksimumsbeløp for hver enkelt berettigede, dekkede persontype.</span><span class="sxs-lookup"><span data-stu-id="03a2b-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="03a2b-122">En dekningskode angir hvem som er dekket av eller hvor mye dekning som er tillatt for en plantype.</span><span class="sxs-lookup"><span data-stu-id="03a2b-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="03a2b-123">Du kan uttrykke dekningsbeløpet som et valutabeløp eller en prosent.</span><span class="sxs-lookup"><span data-stu-id="03a2b-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="03a2b-124">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="03a2b-124">For example:</span></span></br></br><span data-ttu-id="03a2b-125">- **Emp+1** – for å være kvalifisert må den ansatte ha én avhengig valgt (hvis flere er valgt, er de ikke lenger kvalifisert).</span><span class="sxs-lookup"><span data-stu-id="03a2b-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="03a2b-126">- **Emp+familie** – for å være kvalifisert må den ansatte ha minst to avhengige valgt.</span><span class="sxs-lookup"><span data-stu-id="03a2b-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="03a2b-127">**Maksimalt antall**</span><span class="sxs-lookup"><span data-stu-id="03a2b-127">**Maximum number**</span></span> | <span data-ttu-id="03a2b-128">Det maksimale antall avhengige.</span><span class="sxs-lookup"><span data-stu-id="03a2b-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="03a2b-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="03a2b-129">**Status**</span></span> | <span data-ttu-id="03a2b-130">Statusen for dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="03a2b-130">The status of the coverage option.</span></span> <span data-ttu-id="03a2b-131">Hvis statusen for dekningsalternativet er satt til Inaktiv, kan ikke dekningsalternativet velges på plantyper.</span><span class="sxs-lookup"><span data-stu-id="03a2b-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="03a2b-132">**Prosent**</span><span class="sxs-lookup"><span data-stu-id="03a2b-132">**Percent**</span></span> | <span data-ttu-id="03a2b-133">Prosentbeløpet.</span><span class="sxs-lookup"><span data-stu-id="03a2b-133">The percent amount.</span></span> <span data-ttu-id="03a2b-134">Dette feltet er bare aktivt hvis % x lønn ble valgt i Dekningskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="03a2b-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="03a2b-135">**Divisor**</span><span class="sxs-lookup"><span data-stu-id="03a2b-135">**Divisor**</span></span> | <span data-ttu-id="03a2b-136">Divisoren som skal brukes i beregningen når du velger dekningskoden % x lønn.</span><span class="sxs-lookup"><span data-stu-id="03a2b-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="03a2b-137">**Minste prosentandel**</span><span class="sxs-lookup"><span data-stu-id="03a2b-137">**Percent minimum**</span></span> | <span data-ttu-id="03a2b-138">Minimumsprosenten når du velger kode for prosentdekning.</span><span class="sxs-lookup"><span data-stu-id="03a2b-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="03a2b-139">**Størst prosentandel**</span><span class="sxs-lookup"><span data-stu-id="03a2b-139">**Percent maximum**</span></span> | <span data-ttu-id="03a2b-140">Maksimumsprosenten når du velger kode for prosentdekning.</span><span class="sxs-lookup"><span data-stu-id="03a2b-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="03a2b-141">Under **Alternativer for rettighet for personlig kontakt** knytter du det aktuelle rettighetsalternativet for personlige kontakter til hvert dekningsalternativ.</span><span class="sxs-lookup"><span data-stu-id="03a2b-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="03a2b-142">Under **Selvbetjening** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="03a2b-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="03a2b-143">Felt</span><span class="sxs-lookup"><span data-stu-id="03a2b-143">Field</span></span> | <span data-ttu-id="03a2b-144">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="03a2b-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="03a2b-145">**Tillat bidragsbeløp fra ansatt**</span><span class="sxs-lookup"><span data-stu-id="03a2b-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="03a2b-146">Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler.</span><span class="sxs-lookup"><span data-stu-id="03a2b-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="03a2b-147">Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på fordeler selvbetjent.</span><span class="sxs-lookup"><span data-stu-id="03a2b-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="03a2b-148">**Tillat dekningsbeløp fra ansatt**</span><span class="sxs-lookup"><span data-stu-id="03a2b-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="03a2b-149">Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler.</span><span class="sxs-lookup"><span data-stu-id="03a2b-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="03a2b-150">Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="03a2b-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="03a2b-151">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="03a2b-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]