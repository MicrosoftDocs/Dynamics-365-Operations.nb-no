---
title: Opprette dekningsalternativer
description: Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program, for eksempel Bare ansatte for en medisinsk plan, eller 2x lønn for en forsikringsplan for livstid.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092712"
---
# <a name="create-coverage-options"></a><span data-ttu-id="97e8c-103">Opprette dekningsalternativer</span><span class="sxs-lookup"><span data-stu-id="97e8c-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="97e8c-104">Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program, for eksempel Bare ansatte for en medisinsk plan, eller 2x lønn for en forsikringsplan for livstid.</span><span class="sxs-lookup"><span data-stu-id="97e8c-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="97e8c-105">Når det er definert, kan fordelsdekningsalternativene brukes på nytt, og det er mulig å knytte et alternativ til én eller flere planer.</span><span class="sxs-lookup"><span data-stu-id="97e8c-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="97e8c-106">Når dekningsalternativene er definert, knytter du dekningsalternativene til en fordelsplantype.</span><span class="sxs-lookup"><span data-stu-id="97e8c-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="97e8c-107">Plantypen knyttes deretter til en fordelsplan eller et program.</span><span class="sxs-lookup"><span data-stu-id="97e8c-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="97e8c-108">Dekningsalternativer som er knyttet til en plantype, vil være tilgjengelige for alle planer som opprettes med denne plantypen.</span><span class="sxs-lookup"><span data-stu-id="97e8c-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="97e8c-109">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Dekningsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="97e8c-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="97e8c-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="97e8c-110">Select **New**.</span></span>

3. <span data-ttu-id="97e8c-111">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="97e8c-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="97e8c-112">Felt</span><span class="sxs-lookup"><span data-stu-id="97e8c-112">Field</span></span> | <span data-ttu-id="97e8c-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="97e8c-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="97e8c-114">**Dekningsalternativ**</span><span class="sxs-lookup"><span data-stu-id="97e8c-114">**Coverage option**</span></span> | <span data-ttu-id="97e8c-115">Et unikt navn på dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="97e8c-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="97e8c-116">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="97e8c-116">**Description**</span></span> | <span data-ttu-id="97e8c-117">En beskrivelse av dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="97e8c-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="97e8c-118">**Dekningskode**</span><span class="sxs-lookup"><span data-stu-id="97e8c-118">**Coverage code**</span></span> | <span data-ttu-id="97e8c-119">Dekningskoder som tilordner minimums- og maksimumsbeløp for hver enkelt berettigede, dekkede persontype.</span><span class="sxs-lookup"><span data-stu-id="97e8c-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="97e8c-120">En dekningskode angir hvem som er dekket av eller hvor mye dekning som er tillatt for en plantype.</span><span class="sxs-lookup"><span data-stu-id="97e8c-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="97e8c-121">Du kan uttrykke dekningsbeløpet som et valutabeløp eller en prosent.</span><span class="sxs-lookup"><span data-stu-id="97e8c-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="97e8c-122">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="97e8c-122">For example:</span></span></br></br><span data-ttu-id="97e8c-123">- **Emp+1** – for å være kvalifisert må den ansatte ha én avhengig valgt (hvis flere er valgt, er de ikke lenger kvalifisert).</span><span class="sxs-lookup"><span data-stu-id="97e8c-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="97e8c-124">- **Emp+familie** – for å være kvalifisert må den ansatte ha minst to avhengige valgt.</span><span class="sxs-lookup"><span data-stu-id="97e8c-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="97e8c-125">**Maksimalt antall**</span><span class="sxs-lookup"><span data-stu-id="97e8c-125">**Maximum number**</span></span> | <span data-ttu-id="97e8c-126">Det maksimale antall avhengige.</span><span class="sxs-lookup"><span data-stu-id="97e8c-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="97e8c-127">**Status**</span><span class="sxs-lookup"><span data-stu-id="97e8c-127">**Status**</span></span> | <span data-ttu-id="97e8c-128">Statusen for dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="97e8c-128">The status of the coverage option.</span></span> <span data-ttu-id="97e8c-129">Hvis statusen for dekningsalternativet er satt til Inaktiv, kan ikke dekningsalternativet velges på plantyper.</span><span class="sxs-lookup"><span data-stu-id="97e8c-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="97e8c-130">**Prosent**</span><span class="sxs-lookup"><span data-stu-id="97e8c-130">**Percent**</span></span> | <span data-ttu-id="97e8c-131">Prosentbeløpet.</span><span class="sxs-lookup"><span data-stu-id="97e8c-131">The percent amount.</span></span> <span data-ttu-id="97e8c-132">Dette feltet er bare aktivt hvis % x lønn ble valgt i Dekningskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="97e8c-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="97e8c-133">**Divisor**</span><span class="sxs-lookup"><span data-stu-id="97e8c-133">**Divisor**</span></span> | <span data-ttu-id="97e8c-134">Divisoren som skal brukes i beregningen når du velger dekningskoden % x lønn.</span><span class="sxs-lookup"><span data-stu-id="97e8c-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="97e8c-135">**Minste prosentandel**</span><span class="sxs-lookup"><span data-stu-id="97e8c-135">**Percent minimum**</span></span> | <span data-ttu-id="97e8c-136">Minimumsprosenten når du velger kode for prosentdekning.</span><span class="sxs-lookup"><span data-stu-id="97e8c-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="97e8c-137">**Størst prosentandel**</span><span class="sxs-lookup"><span data-stu-id="97e8c-137">**Percent maximum**</span></span> | <span data-ttu-id="97e8c-138">Maksimumsprosenten når du velger kode for prosentdekning.</span><span class="sxs-lookup"><span data-stu-id="97e8c-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="97e8c-139">Under **Alternativer for rettighet for personlig kontakt** knytter du det aktuelle rettighetsalternativet for personlige kontakter til hvert dekningsalternativ.</span><span class="sxs-lookup"><span data-stu-id="97e8c-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="97e8c-140">Under **Selvbetjening** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="97e8c-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="97e8c-141">Felt</span><span class="sxs-lookup"><span data-stu-id="97e8c-141">Field</span></span> | <span data-ttu-id="97e8c-142">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="97e8c-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="97e8c-143">**Tillat bidragsbeløp fra ansatt**</span><span class="sxs-lookup"><span data-stu-id="97e8c-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="97e8c-144">Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler.</span><span class="sxs-lookup"><span data-stu-id="97e8c-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="97e8c-145">Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på fordeler selvbetjent.</span><span class="sxs-lookup"><span data-stu-id="97e8c-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="97e8c-146">**Tillat dekningsbeløp fra ansatt**</span><span class="sxs-lookup"><span data-stu-id="97e8c-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="97e8c-147">Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler.</span><span class="sxs-lookup"><span data-stu-id="97e8c-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="97e8c-148">Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="97e8c-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="97e8c-149">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="97e8c-149">Select **Save**.</span></span> 
