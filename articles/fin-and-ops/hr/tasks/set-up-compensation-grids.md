--- 
title: Konfigurer kompensasjonsrutenett
description: "Kompensasjonsrutenett brukes til å definere og vedlikeholde lønn-strukturer for faste kompensasjonsplaner."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompGridView
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 139c4e2adbf5029f8084c7c934a05def04cd31ca
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="254df-103">Konfigurer kompensasjonsrutenett</span><span class="sxs-lookup"><span data-stu-id="254df-103">Set up compensation grids</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="254df-104">Kompensasjonsrutenett brukes til å definere og vedlikeholde lønn-strukturer for faste kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="254df-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="254df-105">Kompensasjonsrutenett kan deles mellom flere planer eller kopieres når du oppretter en ny kompensasjonsplan.</span><span class="sxs-lookup"><span data-stu-id="254df-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="254df-106">Før du oppretter et kompensasjonsrutenett må nivåer og referansepunkt være definert.</span><span class="sxs-lookup"><span data-stu-id="254df-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="254df-107">Dette eksemplet oppretter en ny klasse-type for kompensasjonsrutenettet ved hjelp av demodata for nivåene og referansepunktene.</span><span class="sxs-lookup"><span data-stu-id="254df-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="254df-108">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="254df-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="254df-109">Definere informasjon om kompensasjonsrutenettet</span><span class="sxs-lookup"><span data-stu-id="254df-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="254df-110">Gå til Personale > Kompensasjon > Fast kompensasjon > Kompensasjonsrutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="254df-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="254df-111">Click New.</span></span>
3. <span data-ttu-id="254df-112">Skriv inn en verdi i feltet Rutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="254df-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="254df-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="254df-114">Velg et alternativ i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="254df-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="254df-115">Angi eller velg en verdi i feltet Referanseoppsett.</span><span class="sxs-lookup"><span data-stu-id="254df-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="254df-116">Angi eller velg en verdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="254df-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="254df-117">Skriv inn en verdi i Valuta-feltet.</span><span class="sxs-lookup"><span data-stu-id="254df-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="254df-118">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="254df-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="254df-119">Legge til nivåer i kompensasjonsstrukturen</span><span class="sxs-lookup"><span data-stu-id="254df-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="254df-120">Klikk Kompensasjonsstruktur.</span><span class="sxs-lookup"><span data-stu-id="254df-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="254df-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="254df-122">Angi eller velg en verdi i feltet Nivå.</span><span class="sxs-lookup"><span data-stu-id="254df-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="254df-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="254df-123">Click New.</span></span>
5. <span data-ttu-id="254df-124">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="254df-125">Angi eller velg en verdi i feltet Nivå.</span><span class="sxs-lookup"><span data-stu-id="254df-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="254df-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="254df-126">Click New.</span></span>
8. <span data-ttu-id="254df-127">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="254df-128">Angi eller velg en verdi i feltet Nivå.</span><span class="sxs-lookup"><span data-stu-id="254df-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="254df-129">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="254df-129">Click New.</span></span>
11. <span data-ttu-id="254df-130">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="254df-131">Angi eller velg en verdi i feltet Nivå.</span><span class="sxs-lookup"><span data-stu-id="254df-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="254df-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="254df-132">Click New.</span></span>
14. <span data-ttu-id="254df-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="254df-134">Angi eller velg en verdi i feltet Nivå.</span><span class="sxs-lookup"><span data-stu-id="254df-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="254df-135">Fylle ut kompensasjonsstrukturen med verdier</span><span class="sxs-lookup"><span data-stu-id="254df-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="254df-136">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="254df-137">Nå kan kompensasjonsverdiene settes inn manuelt i hvert felt i tabellen, eller masseendringsfunksjonaliteten kan brukes til å enkelt fylle ut flere felt og utføre enkle beregninger.</span><span class="sxs-lookup"><span data-stu-id="254df-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="254df-138">Klikk Masseendring.</span><span class="sxs-lookup"><span data-stu-id="254df-138">Click Mass change.</span></span>
    * <span data-ttu-id="254df-139">Vi vil først bruke verdien for midtpunktet i det første nivået for dette rutenettet på alle feltene i tabellen.</span><span class="sxs-lookup"><span data-stu-id="254df-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="254df-140">Dette vil være grunnlaget for kompensasjonsmatrisen.</span><span class="sxs-lookup"><span data-stu-id="254df-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="254df-141">Velg et alternativ i feltet Justeringstype.</span><span class="sxs-lookup"><span data-stu-id="254df-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="254df-142">Angi et tall i Justeringsbeløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="254df-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="254df-143">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="254df-144">Klikk Bruk på rutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="254df-145">Nå skal vi bruke masseendringsfunksjonen til å øke beløpene i hvert etterfølgende nivå med en bestemt prosent eller beløp.</span><span class="sxs-lookup"><span data-stu-id="254df-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="254df-146">I dette eksemplet skal hver klasse en 12,5 % spredning mellom midtpunktene.</span><span class="sxs-lookup"><span data-stu-id="254df-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="254df-147">Velg et alternativ i feltet Justeringstype.</span><span class="sxs-lookup"><span data-stu-id="254df-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="254df-148">Angi et tall i Justeringsbeløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="254df-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="254df-149">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="254df-150">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="254df-151">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="254df-152">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="254df-153">Klikk Bruk på rutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="254df-154">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="254df-155">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="254df-156">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="254df-157">Klikk Bruk på rutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="254df-158">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="254df-159">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="254df-160">Klikk Bruk på rutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="254df-161">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="254df-162">Klikk Bruk på rutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="254df-163">Nå skal vi bruke masseendringsfunksjonen til å justere Minimum og maksimum referansepunkt for hvert nivå.</span><span class="sxs-lookup"><span data-stu-id="254df-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="254df-164">Dette eksemplet bruker en 50 % spredning slik Minimum referansepunkt blir justert -20 % og maksimalt blir justert +20 %.</span><span class="sxs-lookup"><span data-stu-id="254df-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="254df-165">Angi et tall i Justeringsbeløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="254df-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="254df-166">Angi eller velg en verdi i feltet Referansepunkt.</span><span class="sxs-lookup"><span data-stu-id="254df-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="254df-167">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="254df-168">Klikk Bruk på rutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="254df-169">Angi et tall i Justeringsbeløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="254df-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="254df-170">Angi eller velg en verdi i feltet Referansepunkt.</span><span class="sxs-lookup"><span data-stu-id="254df-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="254df-171">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="254df-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="254df-172">Klikk Bruk på rutenett.</span><span class="sxs-lookup"><span data-stu-id="254df-172">Click Apply to grid.</span></span>


