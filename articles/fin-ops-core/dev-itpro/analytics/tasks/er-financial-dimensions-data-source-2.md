---
title: ER Bruke finansdimensjoner som en datakilde (del 2 - Modelltilordning)
description: Dette emnet beskriver hvordan du konfigurerer en ER-modell (Elektronisk rapportering) for å bruke finansdimensjoner som en datakilde for ER-rapporter. (Del 2)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02c730d08c411e736a7f8b9e7bad3d6a18cb8e6a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093243"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="6cb24-104">ER Bruke finansdimensjoner som en datakilde (del 2 - Modelltilordning)</span><span class="sxs-lookup"><span data-stu-id="6cb24-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6cb24-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="6cb24-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="6cb24-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="6cb24-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="6cb24-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 1: Utforme datamodell).</span><span class="sxs-lookup"><span data-stu-id="6cb24-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="6cb24-108">Legge til obligatoriske datakilder i modelltilordning</span><span class="sxs-lookup"><span data-stu-id="6cb24-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="6cb24-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="6cb24-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6cb24-110">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6cb24-111">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="6cb24-111">Click Designer.</span></span>
4. <span data-ttu-id="6cb24-112">Klikk på Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="6cb24-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="6cb24-113">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="6cb24-113">Click New.</span></span>
6. <span data-ttu-id="6cb24-114">Velg Oppføring i Definisjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="6cb24-115">Skriv inn Dimensjonsdatatilordning i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="6cb24-116">Skriv inn Dimensjonsdatatilordning i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="6cb24-117">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="6cb24-117">Click Save.</span></span>
10. <span data-ttu-id="6cb24-118">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="6cb24-118">Click Designer.</span></span>
11. <span data-ttu-id="6cb24-119">Velg Dynamics 365 for Operations\Tabell i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="6cb24-120">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="6cb24-120">Click Add root.</span></span>
13. <span data-ttu-id="6cb24-121">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="6cb24-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="6cb24-122">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="6cb24-123">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="6cb24-123">Click OK.</span></span>
16. <span data-ttu-id="6cb24-124">Velg Funksjoner\Detaljer for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="6cb24-125">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="6cb24-125">Click Add root.</span></span>
    * <span data-ttu-id="6cb24-126">Denne datakilden angir hvordan omfanget av finansdimensjoner defineres for en rapport som skal bruke denne modellen som datakilde.</span><span class="sxs-lookup"><span data-stu-id="6cb24-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="6cb24-127">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="6cb24-128">Velg Ja i feltet Be om dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="6cb24-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="6cb24-129">Velg Ja hvis du vil at brukeren skal kunne velge dimensjoner under kjøring i dialogboksskjemaet Bruker.</span><span class="sxs-lookup"><span data-stu-id="6cb24-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="6cb24-130">Hvis satt til Nei, brukes alle finansdimensjoner for den gjeldende forekomsten som standard.</span><span class="sxs-lookup"><span data-stu-id="6cb24-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="6cb24-131">Velg Juridisk enhet i feltet Valg av finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="6cb24-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="6cb24-132">Velg Alle for å la brukeren velge ønskede dimensjoner for gjeldende forekomst i oppslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="6cb24-133">Velg Juridisk enhet for å la brukeren velge dimensjoner for firmaet i oppslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="6cb24-134">Velg Dimensjon for å la brukeren velge dimensjoner ved hjelp av et enkelt dimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="6cb24-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="6cb24-135">Velg Ja i feltet Be om hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="6cb24-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="6cb24-136">Sett Be om hovedkonto til Ja for å tillate brukere å velge hovedkontoen som en del av listen med dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="6cb24-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="6cb24-137">Hvis satt til Nei, blir ikke hovedkontoen tatt med i listen over dimensjoner, og alternativet Er obligatorisk for hovedkonto aktiveres.</span><span class="sxs-lookup"><span data-stu-id="6cb24-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="6cb24-138">Hvis Er obligatorisk for hovedkonto settes til Ja, inkluderes hovedkontoen i listen over dimensjonere uavhengig av brukerens valg.</span><span class="sxs-lookup"><span data-stu-id="6cb24-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="6cb24-139">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="6cb24-139">Click OK.</span></span>
<span data-ttu-id="6cb24-140">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="6cb24-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="6cb24-141">Velg Dynamics 365 for Operations\Tabellposter i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="6cb24-142">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="6cb24-142">Click Add root.</span></span>
25. <span data-ttu-id="6cb24-143">Skriv inn LedgerJournal i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="6cb24-144">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="6cb24-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="6cb24-145">Skriv inn LedgerJournalTable i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="6cb24-146">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="6cb24-146">Click OK.</span></span>
<span data-ttu-id="6cb24-147">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="6cb24-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="6cb24-148">Tilordne datamodellelementer til datakilder som er lagt til</span><span class="sxs-lookup"><span data-stu-id="6cb24-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="6cb24-149">Utvid Journal i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="6cb24-150">Utvid Journal\Transaksjon i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="6cb24-151">Utvid Journal\Transaksjon\Dimensjonsdata i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="6cb24-152">Utvid Dimensjonsinnstilling i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="6cb24-153">Utvid LedgerJournal i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="6cb24-154">Utvid LedgerJournal\<Relasjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="6cb24-155">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="6cb24-156">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Bilag i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="6cb24-157">Velg Journal\Transaksjon\Bilag i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="6cb24-158">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-158">Click Bind.</span></span>
11. <span data-ttu-id="6cb24-159">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension) i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="6cb24-160">Merk at for alle referanser til finansdimensjoner som settes til, for eksempel LedgerDimension, er et tilsvarende datakildeelement tilgjengelig (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="6cb24-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="6cb24-161">Dette datakildeelementet tilbyr finansdimensjonene for dette dimensjonssettet som postens liste.</span><span class="sxs-lookup"><span data-stu-id="6cb24-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="6cb24-162">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension) i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="6cb24-163">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="6cb24-164">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="6cb24-165">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Definisjon i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="6cb24-166">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Definisjon\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="6cb24-167">Velg Journal\Transaksjon\Dimensjonsdata\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="6cb24-168">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-168">Click Bind.</span></span>
19. <span data-ttu-id="6cb24-169">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="6cb24-170">Velg Journal\Transaksjon\Dimensjonsdata\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="6cb24-171">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-171">Click Bind.</span></span>
22. <span data-ttu-id="6cb24-172">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="6cb24-173">Velg Journal\Transaksjon\Dimensjonsdata\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="6cb24-174">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-174">Click Bind.</span></span>
25. <span data-ttu-id="6cb24-175">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="6cb24-176">Velg Journal\Transaksjon\Dimensjonsdata i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="6cb24-177">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-177">Click Bind.</span></span>
<span data-ttu-id="6cb24-178">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="6cb24-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="6cb24-179">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Debet(AmountCurDebit) i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="6cb24-180">Velg Journal\Transaksjon\Debet i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="6cb24-181">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-181">Click Bind.</span></span>
31. <span data-ttu-id="6cb24-182">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Dato(TransDate) i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="6cb24-183">Velg Journal\Transaksjon\Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="6cb24-184">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-184">Click Bind.</span></span>
34. <span data-ttu-id="6cb24-185">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Valuta(CurrencyCode) i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="6cb24-186">Velg Journal\Transaksjon\Valuta i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="6cb24-187">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-187">Click Bind.</span></span>
37. <span data-ttu-id="6cb24-188">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Kredit(AmountCurCredit) i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="6cb24-189">Velg Journal\Transaksjon\Kredit i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="6cb24-190">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-190">Click Bind.</span></span>
40. <span data-ttu-id="6cb24-191">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="6cb24-192">Velg Journal\Transaksjon i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="6cb24-193">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-193">Click Bind.</span></span>
43. <span data-ttu-id="6cb24-194">Velg LedgerJournal\Journalpartinummer(JournalNum) i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="6cb24-195">Velg Journal\Parti i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="6cb24-196">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-196">Click Bind.</span></span>
46. <span data-ttu-id="6cb24-197">Velg LedgerJournal i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="6cb24-198">Velg Journal i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="6cb24-199">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-199">Click Bind.</span></span>
49. <span data-ttu-id="6cb24-200">Utvid Dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="6cb24-201">Utvid Dimensjoner\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="6cb24-202">Utvid Dimensjoner\Hovedkonto og dimensjoner\Definisjon i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="6cb24-203">Velg Dimensjoner\Hovedkonto og dimensjoner\Definisjon\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="6cb24-204">Velg Dimensjonsinnstilling\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="6cb24-205">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-205">Click Bind.</span></span>
55. <span data-ttu-id="6cb24-206">Velg Dimensjoner\Hovedkonto og dimensjoner\Definisjon\Rapportkolonnenavn i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="6cb24-207">Velg Dimensjonsinnstilling\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="6cb24-208">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-208">Click Bind.</span></span>
58. <span data-ttu-id="6cb24-209">Velg Dimensjoner\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="6cb24-210">Velg Dimensjonsinnstilling i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="6cb24-211">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6cb24-211">Click Bind.</span></span>
61. <span data-ttu-id="6cb24-212">Velg Firma i treet.</span><span class="sxs-lookup"><span data-stu-id="6cb24-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="6cb24-213">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="6cb24-213">Click Edit.</span></span>
63. <span data-ttu-id="6cb24-214">Angi Company.'find()'.'name()' i feltet expressionAsStringText.</span><span class="sxs-lookup"><span data-stu-id="6cb24-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="6cb24-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="6cb24-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="6cb24-216">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="6cb24-216">Click Save.</span></span>
<span data-ttu-id="6cb24-217">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="6cb24-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="6cb24-218">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6cb24-218">Close the page.</span></span>
66. <span data-ttu-id="6cb24-219">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="6cb24-219">Click Save.</span></span>
67. <span data-ttu-id="6cb24-220">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6cb24-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="6cb24-221">Fullføre versjonen av denne utkastmodellen</span><span class="sxs-lookup"><span data-stu-id="6cb24-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="6cb24-222">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6cb24-222">Close the page.</span></span>
2. <span data-ttu-id="6cb24-223">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6cb24-223">Close the page.</span></span>
3. <span data-ttu-id="6cb24-224">Klikk på Endre status.</span><span class="sxs-lookup"><span data-stu-id="6cb24-224">Click Change status.</span></span>
4. <span data-ttu-id="6cb24-225">Klikk på Fullført.</span><span class="sxs-lookup"><span data-stu-id="6cb24-225">Click Complete.</span></span>
5. <span data-ttu-id="6cb24-226">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="6cb24-226">Click OK.</span></span>
<span data-ttu-id="6cb24-227">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="6cb24-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
