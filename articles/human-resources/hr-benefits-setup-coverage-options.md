---
title: Opprette dekningsalternativer
description: ''
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010016"
---
# <a name="create-coverage-options"></a><span data-ttu-id="c4572-102">Opprette dekningsalternativer</span><span class="sxs-lookup"><span data-stu-id="c4572-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c4572-103">Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program, for eksempel Bare ansatte for en medisinsk plan, eller 2x lønn for en forsikringsplan for livstid.</span><span class="sxs-lookup"><span data-stu-id="c4572-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="c4572-104">Når det er definert, kan fordelsdekningsalternativene brukes på nytt, og det er mulig å knytte et alternativ til én eller flere planer.</span><span class="sxs-lookup"><span data-stu-id="c4572-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="c4572-105">Når dekningsalternativene er definert, knytter du dekningsalternativene til en fordelsplantype.</span><span class="sxs-lookup"><span data-stu-id="c4572-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="c4572-106">Plantypen knyttes deretter til en fordelsplan eller et program.</span><span class="sxs-lookup"><span data-stu-id="c4572-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="c4572-107">Dekningsalternativer som er knyttet til en plantype, vil være tilgjengelige for alle planer som opprettes med denne plantypen.</span><span class="sxs-lookup"><span data-stu-id="c4572-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="c4572-108">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Dekningsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="c4572-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="c4572-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c4572-109">Select **New**.</span></span>

3. <span data-ttu-id="c4572-110">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="c4572-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c4572-111">Felt</span><span class="sxs-lookup"><span data-stu-id="c4572-111">Field</span></span> | <span data-ttu-id="c4572-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4572-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c4572-113">**Dekningsalternativ**</span><span class="sxs-lookup"><span data-stu-id="c4572-113">**Coverage option**</span></span> | <span data-ttu-id="c4572-114">Et unikt navn på dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="c4572-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="c4572-115">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="c4572-115">**Description**</span></span> | <span data-ttu-id="c4572-116">En beskrivelse av dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="c4572-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="c4572-117">**Dekningskode**</span><span class="sxs-lookup"><span data-stu-id="c4572-117">**Coverage code**</span></span> | <span data-ttu-id="c4572-118">Dekningskoder som tilordner minimums- og maksimumsbeløp for hver enkelt berettigede, dekkede persontype.</span><span class="sxs-lookup"><span data-stu-id="c4572-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="c4572-119">En dekningskode angir hvem som er dekket av eller hvor mye dekning som er tillatt for en plantype.</span><span class="sxs-lookup"><span data-stu-id="c4572-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="c4572-120">Du kan uttrykke dekningsbeløpet som et valutabeløp eller en prosent.</span><span class="sxs-lookup"><span data-stu-id="c4572-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="c4572-121">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="c4572-121">For example:</span></span></br></br><span data-ttu-id="c4572-122">- **Emp+1** – for å være kvalifisert må den ansatte ha én avhengig valgt (hvis flere er valgt, er de ikke lenger kvalifisert).</span><span class="sxs-lookup"><span data-stu-id="c4572-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="c4572-123">- **Emp+familie** – for å være kvalifisert må den ansatte ha minst to avhengige valgt.</span><span class="sxs-lookup"><span data-stu-id="c4572-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="c4572-124">**Maksimalt antall**</span><span class="sxs-lookup"><span data-stu-id="c4572-124">**Maximum number**</span></span> | <span data-ttu-id="c4572-125">Det maksimale antall avhengige.</span><span class="sxs-lookup"><span data-stu-id="c4572-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="c4572-126">**Status**</span><span class="sxs-lookup"><span data-stu-id="c4572-126">**Status**</span></span> | <span data-ttu-id="c4572-127">Statusen for dekningsalternativet.</span><span class="sxs-lookup"><span data-stu-id="c4572-127">The status of the coverage option.</span></span> <span data-ttu-id="c4572-128">Hvis statusen for dekningsalternativet er satt til Inaktiv, kan ikke dekningsalternativet velges på plantyper.</span><span class="sxs-lookup"><span data-stu-id="c4572-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="c4572-129">**Prosent**</span><span class="sxs-lookup"><span data-stu-id="c4572-129">**Percent**</span></span> | <span data-ttu-id="c4572-130">Prosentbeløpet.</span><span class="sxs-lookup"><span data-stu-id="c4572-130">The percent amount.</span></span> <span data-ttu-id="c4572-131">Dette feltet er bare aktivt hvis % x lønn ble valgt i Dekningskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="c4572-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="c4572-132">**Divisor**</span><span class="sxs-lookup"><span data-stu-id="c4572-132">**Divisor**</span></span> | <span data-ttu-id="c4572-133">Divisoren som skal brukes i beregningen når du velger dekningskoden % x lønn.</span><span class="sxs-lookup"><span data-stu-id="c4572-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="c4572-134">**Minste prosentandel**</span><span class="sxs-lookup"><span data-stu-id="c4572-134">**Percent minimum**</span></span> | <span data-ttu-id="c4572-135">Minimumsprosenten når du velger kode for prosentdekning.</span><span class="sxs-lookup"><span data-stu-id="c4572-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="c4572-136">**Størst prosentandel**</span><span class="sxs-lookup"><span data-stu-id="c4572-136">**Percent maximum**</span></span> | <span data-ttu-id="c4572-137">Maksimumsprosenten når du velger kode for prosentdekning.</span><span class="sxs-lookup"><span data-stu-id="c4572-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="c4572-138">Under **Alternativer for rettighet for personlig kontakt** knytter du det aktuelle rettighetsalternativet for personlige kontakter til hvert dekningsalternativ.</span><span class="sxs-lookup"><span data-stu-id="c4572-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="c4572-139">Under **Selvbetjening** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="c4572-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="c4572-140">Felt</span><span class="sxs-lookup"><span data-stu-id="c4572-140">Field</span></span> | <span data-ttu-id="c4572-141">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4572-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c4572-142">**Tillat bidragsbeløp fra ansatt**</span><span class="sxs-lookup"><span data-stu-id="c4572-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="c4572-143">Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler.</span><span class="sxs-lookup"><span data-stu-id="c4572-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="c4572-144">Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på fordeler selvbetjent.</span><span class="sxs-lookup"><span data-stu-id="c4572-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="c4572-145">**Tillat dekningsbeløp fra ansatt**</span><span class="sxs-lookup"><span data-stu-id="c4572-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="c4572-146">Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler.</span><span class="sxs-lookup"><span data-stu-id="c4572-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="c4572-147">Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="c4572-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="c4572-148">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c4572-148">Select **Save**.</span></span> 
