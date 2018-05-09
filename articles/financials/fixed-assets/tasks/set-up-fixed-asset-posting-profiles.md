--- 
title: Definere posteringsprofiler for anleggsmidler
description: Denne oppgaveveiledninegn definerer posteringsprofiler for anleggsmiddel.
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d07df2c2779833485bd70240c47bb569622800f8
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="ba3a3-103">Definere posteringsprofiler for anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="ba3a3-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba3a3-104">Denne oppgaveveiledninegn definerer posteringsprofiler for anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="ba3a3-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="ba3a3-106">Eksemplene i oppgaveveiledningen er for en enkel posteringsprofil, men posteringsprofiler må opprettes for den bestemte kontoplanen og kravene til økonomisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="ba3a3-107">Gå til Anleggsmidler > Oppsett > Posteringsprofiler for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="ba3a3-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-108">Click New.</span></span>
3. <span data-ttu-id="ba3a3-109">Skriv inn en verdi i feltet Posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="ba3a3-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ba3a3-111">Du må opprette en posteringsprofil for hver transaksjonstype for anleggsmiddel som du vil bruke når du arbeider med anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="ba3a3-112">Denne oppgaveveiledningen starter med anskaffelsestransaksjonstypen.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="ba3a3-113">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-113">Click Add.</span></span>
6. <span data-ttu-id="ba3a3-114">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="ba3a3-115">Ved hjelp av Grupperinger-feltet kan du definere posteringsprofilen til tabellen (én konto konfigurert for hvert anleggsmiddel) eller gruppen (én konto er definert for hver anleggsmiddelgruppe).</span><span class="sxs-lookup"><span data-stu-id="ba3a3-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="ba3a3-116">I denne oppgaveveiledningen beholder jeg verdien "Alle" for alle anleggsmidler med det angitte tablået.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="ba3a3-117">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="ba3a3-118">Du kan angi en motkonto for anskaffelser eller la feltet stå tomt for å fylle det ut for den bestemte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="ba3a3-119">Velg "Skriv ned justering" i feltet Anskaffelsesjustering.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="ba3a3-120">For anskaffelsesjusteringstransaksjoner vil vi bruke de samme kontoene som brukes for anskaffelsestransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="ba3a3-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-121">Click Add.</span></span>
10. <span data-ttu-id="ba3a3-122">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="ba3a3-123">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="ba3a3-124">Du kan angi en motkonto for anskaffelsesjusteringer eller la feltet stå tomt for å fylle det ut for den bestemte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="ba3a3-125">Velg "Avskrivning" i Transaksjonstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="ba3a3-126">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-126">Click Add.</span></span>
14. <span data-ttu-id="ba3a3-127">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="ba3a3-128">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="ba3a3-129">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="ba3a3-130">Velg "Avskrivningsjustering" i Transaksjonstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="ba3a3-131">For avskrivningsjusteringstransaksjoner vil vi bruke de samme kontoene som brukes for avskrivingstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="ba3a3-132">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-132">Click Add.</span></span>
19. <span data-ttu-id="ba3a3-133">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="ba3a3-134">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="ba3a3-135">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="ba3a3-136">Velg "Avhendingssalg" i Transaksjonstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="ba3a3-137">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-137">Click Add.</span></span>
24. <span data-ttu-id="ba3a3-138">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="ba3a3-139">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="ba3a3-140">Du kan angi en motkonto for avhendinger eller la feltet stå tomt for å fylle det ut for den bestemte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="ba3a3-141">Velg "Avhending svinn" i Transaksjonstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="ba3a3-142">Vi vil bruke de samme kontoene for Avhendingssalg og Avhendingssvinn.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="ba3a3-143">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-143">Click Add.</span></span>
28. <span data-ttu-id="ba3a3-144">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="ba3a3-145">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="ba3a3-146">Du kan angi en motkonto for avhendinger eller la feltet stå tomt for å fylle det ut for den bestemte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="ba3a3-147">Utvid delen Avhending.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="ba3a3-148">Du må definere posteringsprofiler for avhending for både både salg og svinn.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="ba3a3-149">Vi starter med avhendingstransaksjoner for salg.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="ba3a3-150">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-150">Click Add.</span></span>
32. <span data-ttu-id="ba3a3-151">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="ba3a3-152">Velg "Anskaffelsesverdi" i feltet Poster verdi.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="ba3a3-153">Anskaffelsesverdien håndterer justeringsverdier for anskaffelse og anskaffelsesjustering for alle år.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="ba3a3-154">Du kan også definere kontoer for disse transaksjonstypene separat.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="ba3a3-155">Du kan angi avhendingsprosessen til å bruke forskjellige kontoer avhengig av om salget resulterer i tap eller vinning.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="ba3a3-156">Jeg vil angi Salgsverditypen til "Alle" for å bruke de samme kontoene for alle typer avhendinger.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="ba3a3-157">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="ba3a3-158">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="ba3a3-159">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-159">Click Add.</span></span>
37. <span data-ttu-id="ba3a3-160">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="ba3a3-161">I Poster verdi-feltet velger du Avskrivning (foregående år).</span><span class="sxs-lookup"><span data-stu-id="ba3a3-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="ba3a3-162">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="ba3a3-163">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="ba3a3-164">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-164">Click Add.</span></span>
41. <span data-ttu-id="ba3a3-165">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="ba3a3-166">I Poster verdi-feltet velger du "Avskrivning (inneværende år)".</span><span class="sxs-lookup"><span data-stu-id="ba3a3-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="ba3a3-167">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="ba3a3-168">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="ba3a3-169">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-169">Click Add.</span></span>
46. <span data-ttu-id="ba3a3-170">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="ba3a3-171">I Poster verdi-feltet velger du "Avskrivningsjusteringer (foregående år)".</span><span class="sxs-lookup"><span data-stu-id="ba3a3-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="ba3a3-172">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="ba3a3-173">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="ba3a3-174">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-174">Click Add.</span></span>
51. <span data-ttu-id="ba3a3-175">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="ba3a3-176">I Poster verdi-feltet velger du "Avskrivningsjusteringer (inneværende år)".</span><span class="sxs-lookup"><span data-stu-id="ba3a3-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="ba3a3-177">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="ba3a3-178">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="ba3a3-179">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-179">Click Add.</span></span>
56. <span data-ttu-id="ba3a3-180">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="ba3a3-181">Velg "Netto bokført verdi" i feltet Poster verdi.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="ba3a3-182">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="ba3a3-183">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="ba3a3-184">Velg "Svinn" i feltet Salg eller svinn.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="ba3a3-185">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-185">Click Add.</span></span>
62. <span data-ttu-id="ba3a3-186">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="ba3a3-187">Velg "Anskaffelsesverdi" i feltet Poster verdi.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="ba3a3-188">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="ba3a3-189">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="ba3a3-190">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-190">Click Add.</span></span>
67. <span data-ttu-id="ba3a3-191">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="ba3a3-192">I Poster verdi-feltet velger du Avskrivning (foregående år).</span><span class="sxs-lookup"><span data-stu-id="ba3a3-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="ba3a3-193">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="ba3a3-194">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="ba3a3-195">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-195">Click Add.</span></span>
71. <span data-ttu-id="ba3a3-196">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="ba3a3-197">I Poster verdi-feltet velger du "Avskrivning (inneværende år)".</span><span class="sxs-lookup"><span data-stu-id="ba3a3-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="ba3a3-198">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="ba3a3-199">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="ba3a3-200">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-200">Click Add.</span></span>
76. <span data-ttu-id="ba3a3-201">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="ba3a3-202">I Poster verdi-feltet velger du "Avskrivningsjusteringer (foregående år)".</span><span class="sxs-lookup"><span data-stu-id="ba3a3-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="ba3a3-203">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="ba3a3-204">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="ba3a3-205">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-205">Click Add.</span></span>
81. <span data-ttu-id="ba3a3-206">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="ba3a3-207">I Poster verdi-feltet velger du "Avskrivningsjusteringer (inneværende år)".</span><span class="sxs-lookup"><span data-stu-id="ba3a3-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="ba3a3-208">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="ba3a3-209">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="ba3a3-210">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-210">Click Add.</span></span>
86. <span data-ttu-id="ba3a3-211">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="ba3a3-212">Velg "Netto bokført verdi" i feltet Poster verdi.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="ba3a3-213">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="ba3a3-214">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba3a3-214">In the Offset account field, specify the desired values.</span></span>


