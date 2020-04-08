---
title: Bruke konfigurasjoner for modelltilordning for aggregerte beregninger på databasenivået
description: Denne fremgangsmåten gir informasjon om hvordan du utformer en ny konfigurasjon for ER-modelltilordning (elektronisk rapportering) og bruker innebygde ER-funksjoner for effektive aggregerte beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0912b620fc70f8ed33e336da9ecefacd1f4e376e
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143183"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a><span data-ttu-id="ac572-103">Bruke konfigurasjoner for modelltilordning for aggregerte beregninger på databasenivået</span><span class="sxs-lookup"><span data-stu-id="ac572-103">Use model mapping configurations for aggregate calculations at the database level</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac572-104">Denne fremgangsmåten gir informasjon om hvordan du utformer en ny konfigurasjon for ER-modelltilordning (elektronisk rapportering) og bruker innebygde ER-funksjoner for effektive aggregerte beregninger.</span><span class="sxs-lookup"><span data-stu-id="ac572-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="ac572-105">I denne prosedyren skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ac572-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="ac572-106">Denne fremgangsmåten er opprettet for brukere med rollen som Systemansvarlig eller Utvikler av elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="ac572-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="ac572-107">Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett.</span><span class="sxs-lookup"><span data-stu-id="ac572-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="ac572-108">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten ER forbedrer effektiviteten til aggregerte beregninger ved å utføre dem på databasenivå (del 1: Klargjøre konfigurasjoner).</span><span class="sxs-lookup"><span data-stu-id="ac572-108">To complete these steps, you must first complete the steps in the procedure, "ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations)."</span></span>

1. <span data-ttu-id="ac572-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="ac572-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ac572-110">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="ac572-111">Velg Intrastat-modell\Intrastat-eksempeltilordning i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="ac572-112">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="ac572-112">Click Designer.</span></span>
5. <span data-ttu-id="ac572-113">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="ac572-113">Click Designer.</span></span>
6. <span data-ttu-id="ac572-114">Velg Dynamics 365 for Operations\Tabellposter i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="ac572-115">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="ac572-115">Click Add root.</span></span>
    * <span data-ttu-id="ac572-116">Legg til en ny datakilde som representerer postene du vil gruppere.</span><span class="sxs-lookup"><span data-stu-id="ac572-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="ac572-117">Skriv inn Transaksjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ac572-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="ac572-118">Transaksjoner</span><span class="sxs-lookup"><span data-stu-id="ac572-118">Transactions</span></span>  
9. <span data-ttu-id="ac572-119">Skriv inn Intrastat i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="ac572-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="ac572-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="ac572-120">Intrastat</span></span>  
10. <span data-ttu-id="ac572-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ac572-121">Click OK.</span></span>
11. <span data-ttu-id="ac572-122">Velg Funksjoner\Grupper etter i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="ac572-123">Denne datakildetypen brukes til å introdusere en ny datakilde under kjøring for å gruppere poster og beregne nødvendige aggregeringer.</span><span class="sxs-lookup"><span data-stu-id="ac572-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="ac572-124">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="ac572-124">Click Add root.</span></span>
13. <span data-ttu-id="ac572-125">Skriv inn TransactionsGroups i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ac572-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="ac572-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="ac572-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="ac572-127">Klikk Rediger gruppe etter.</span><span class="sxs-lookup"><span data-stu-id="ac572-127">Click Edit group by.</span></span>
15. <span data-ttu-id="ac572-128">Velg Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="ac572-129">Velg den tillagte datakilden av typen "Postliste" som representerer postene du vil gruppere.</span><span class="sxs-lookup"><span data-stu-id="ac572-129">Select the added data source of the 'Record list' type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="ac572-130">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="ac572-130">Click Add field to.</span></span>
17. <span data-ttu-id="ac572-131">Klikk Hva skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="ac572-131">Click What to group.</span></span>
18. <span data-ttu-id="ac572-132">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="ac572-133">I treet velger du Transaksjoner\Retning.</span><span class="sxs-lookup"><span data-stu-id="ac572-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="ac572-134">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="ac572-134">Click Add field to.</span></span>
21. <span data-ttu-id="ac572-135">Klikk Grupperte felt.</span><span class="sxs-lookup"><span data-stu-id="ac572-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="ac572-136">Velg feltet for å angi grupperingsnivået.</span><span class="sxs-lookup"><span data-stu-id="ac572-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="ac572-137">Avhengig av valget returnerer datakilden under kjøring så mange grupper med transaksjoner som det finnes retningskoder som skal oppfylles i Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="ac572-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="ac572-138">Velg Transaksjoner\Invoice amount(AmountMST) i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="ac572-139">Velg feltet for å angi kilden for aggregeringsberegning.</span><span class="sxs-lookup"><span data-stu-id="ac572-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="ac572-140">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="ac572-140">Click Add field to.</span></span>
24. <span data-ttu-id="ac572-141">Klikk Aggregeringsfelt.</span><span class="sxs-lookup"><span data-stu-id="ac572-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="ac572-142">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ac572-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="ac572-143">Velg Sum i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="ac572-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="ac572-144">Velg aggregeringstypen.</span><span class="sxs-lookup"><span data-stu-id="ac572-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="ac572-145">Skriv inn SumOfAmountMST i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ac572-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="ac572-146">Angi navnet på denne aggregeringen i den konfigurerte datakilden.</span><span class="sxs-lookup"><span data-stu-id="ac572-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="ac572-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ac572-147">Click Save.</span></span>
    * <span data-ttu-id="ac572-148">Legg merke til at "Utførelse på"-feltet angir at denne grupperingen skal utføres under kjøring i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ac572-148">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="ac572-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ac572-149">Close the page.</span></span>
30. <span data-ttu-id="ac572-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ac572-150">Click OK.</span></span>
31. <span data-ttu-id="ac572-151">Utvid Totaler i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="ac572-152">Utvid TransactionsGroups i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="ac572-153">Utvid TransactionsGroups\aggregert i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="ac572-154">Velg TransactionsGroups\aggregert\SumOfAmountMST i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="ac572-155">Velg 'Totaler\Total fakturaverdi(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')' i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="ac572-156">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ac572-156">Click Bind.</span></span>
    * <span data-ttu-id="ac572-157">Basert på denne innstillingen vil denne datakilden beregne summen av verdiene i feltet "AmountMST" for hver gruppe med transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ac572-157">Based on this setting, this data source will calculate the sum of values of the 'AmountMST' field for each groups of transactions.</span></span> <span data-ttu-id="ac572-158">Denne aggregeringsberegningen vil være tilgjengelig som elementet TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="ac572-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="ac572-159">Utvid TransactionsGroups i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="ac572-160">Velg TransactionsGroups i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="ac572-161">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="ac572-161">Click Edit.</span></span>
40. <span data-ttu-id="ac572-162">Klikk Rediger gruppe etter.</span><span class="sxs-lookup"><span data-stu-id="ac572-162">Click Edit group by.</span></span>
41. <span data-ttu-id="ac572-163">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="ac572-164">Velg Transaksjoner\Invoice amount(AmountMST) i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="ac572-165">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="ac572-165">Click Add field to.</span></span>
44. <span data-ttu-id="ac572-166">Klikk Aggregeringsfelt.</span><span class="sxs-lookup"><span data-stu-id="ac572-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="ac572-167">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ac572-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="ac572-168">Velg Maks i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="ac572-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="ac572-169">Skriv inn MaxOfAmountMST i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ac572-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="ac572-170">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ac572-170">Click Save.</span></span>
    * <span data-ttu-id="ac572-171">Utførelsen av GROUPBY-datakilder kan for øyeblikket oversettes til SQL-databasenivået med noen begrensninger.</span><span class="sxs-lookup"><span data-stu-id="ac572-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="ac572-172">Oversettelse kan utføres for datakildene av typen "Postliste" eller datakilder representert som et uttrykk ved hjelp av FILTER-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="ac572-172">Translation can be done for either data sources of the 'Record list' type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="ac572-173">Den kan også gjøres når bare én aggregering er konfigurert for ett enkelt felt for grupperingspostene.</span><span class="sxs-lookup"><span data-stu-id="ac572-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="ac572-174">Legg merke til at selv om mer enn én aggregering ble konfigurert for feltet AmountMST, angir "Utførelse på"-feltet fremdeles at denne grupperingen vil bli utført under kjøring i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ac572-174">Note that even though more than one aggregation was configured for the AmountMST field, the 'Execution at' field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="ac572-175">Dette er fordi bare én aggregering er bundet til datamodellelementet og skal brukes under kjøring til å hente data fra denne datakilden.</span><span class="sxs-lookup"><span data-stu-id="ac572-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="ac572-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ac572-176">Close the page.</span></span>
50. <span data-ttu-id="ac572-177">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ac572-177">Click OK.</span></span>
51. <span data-ttu-id="ac572-178">Utvid TransactionsGroups i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="ac572-179">Utvid TransactionsGroups\aggregert i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="ac572-180">Velg 'TransactionsGroups\aggregert\MaxOfAmountMST' i treet</span><span class="sxs-lookup"><span data-stu-id="ac572-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="ac572-181">Velg 'Totaler\Total statistisk verdi(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')' i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="ac572-182">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ac572-182">Click Bind.</span></span>
56. <span data-ttu-id="ac572-183">Utvid TransactionsGroups i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="ac572-184">Velg TransactionsGroups i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="ac572-185">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="ac572-185">Click Edit.</span></span>
59. <span data-ttu-id="ac572-186">Klikk Rediger gruppe etter.</span><span class="sxs-lookup"><span data-stu-id="ac572-186">Click Edit group by.</span></span>
    * <span data-ttu-id="ac572-187">Legg merke til at "Utførelse på"-feltet angir at denne grupperingen vil bli utført under kjøring i minnet fordi begge aggregeringene for det samme feltet er bundet til datamodellelementene.</span><span class="sxs-lookup"><span data-stu-id="ac572-187">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="ac572-188">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="ac572-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="ac572-189">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="ac572-189">Click Delete.</span></span>
62. <span data-ttu-id="ac572-190">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="ac572-190">Click Yes.</span></span>
63. <span data-ttu-id="ac572-191">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="ac572-191">Click Delete.</span></span>
64. <span data-ttu-id="ac572-192">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="ac572-192">Click Yes.</span></span>
65. <span data-ttu-id="ac572-193">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="ac572-193">Click Add field to.</span></span>
66. <span data-ttu-id="ac572-194">Klikk Hva skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="ac572-194">Click What to group.</span></span>
67. <span data-ttu-id="ac572-195">Utvid 'Artikkelpost(Intrastat)' i treet.</span><span class="sxs-lookup"><span data-stu-id="ac572-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="ac572-196">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ac572-196">Click Save.</span></span>
    * <span data-ttu-id="ac572-197">Legg merke til at "Utførelse på"-feltet angir at denne grupperingen vil bli utført under kjøring i minnet selv om det ikke er definert noen aggregeringer og den valgte datakilden av typen Tabellposter refererer til den samme Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="ac572-197">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of 'Table records' type refers to the same 'Intrastat' table.</span></span> <span data-ttu-id="ac572-198">Dette skyldes at datakilden inneholder enkelte beregnede felt som ennå ikke kan oversettes til SQL-databasenivået.</span><span class="sxs-lookup"><span data-stu-id="ac572-198">This is because the data source contains some calculated fields which can't yet be translated to the SQL database level.</span></span>  

