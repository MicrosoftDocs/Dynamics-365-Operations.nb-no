---
title: ER Bruke finansdimensjoner som en datakilde (del 2 - Modelltilordning)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.
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
ms.openlocfilehash: 3214ddb1e077d889fb7b785bee2554b96c3907ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681691"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="5d2b6-103">ER Bruke finansdimensjoner som en datakilde (del 2 - Modelltilordning)</span><span class="sxs-lookup"><span data-stu-id="5d2b6-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d2b6-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="5d2b6-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5d2b6-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 1: Utforme datamodell).</span><span class="sxs-lookup"><span data-stu-id="5d2b6-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="5d2b6-107">Legge til obligatoriske datakilder i modelltilordning</span><span class="sxs-lookup"><span data-stu-id="5d2b6-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="5d2b6-108">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5d2b6-109">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="5d2b6-110">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-110">Click Designer.</span></span>
4. <span data-ttu-id="5d2b6-111">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="5d2b6-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-112">Click New.</span></span>
6. <span data-ttu-id="5d2b6-113">Velg Oppføring i Definisjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="5d2b6-114">Skriv inn Dimensjonsdatatilordning i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="5d2b6-115">Skriv inn Dimensjonsdatatilordning i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="5d2b6-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-116">Click Save.</span></span>
10. <span data-ttu-id="5d2b6-117">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-117">Click Designer.</span></span>
11. <span data-ttu-id="5d2b6-118">Velg Dynamics 365 for Operations\Tabell i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="5d2b6-119">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-119">Click Add root.</span></span>
13. <span data-ttu-id="5d2b6-120">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="5d2b6-121">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="5d2b6-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-122">Click OK.</span></span>
16. <span data-ttu-id="5d2b6-123">Velg Funksjoner\Detaljer for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="5d2b6-124">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-124">Click Add root.</span></span>
    * <span data-ttu-id="5d2b6-125">Denne datakilden angir hvordan omfanget av finansdimensjoner defineres for en rapport som skal bruke denne modellen som datakilde.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="5d2b6-126">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="5d2b6-127">Velg Ja i feltet Be om dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="5d2b6-128">Velg Ja hvis du vil at brukeren skal kunne velge dimensjoner under kjøring i dialogboksskjemaet Bruker.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="5d2b6-129">Hvis satt til Nei, brukes alle finansdimensjoner for den gjeldende forekomsten som standard.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="5d2b6-130">Velg Juridisk enhet i feltet Valg av finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="5d2b6-131">Velg Alle for å la brukeren velge ønskede dimensjoner for gjeldende forekomst i oppslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="5d2b6-132">Velg Juridisk enhet for å la brukeren velge dimensjoner for firmaet i oppslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="5d2b6-133">Velg Dimensjon for å la brukeren velge dimensjoner ved hjelp av et enkelt dimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="5d2b6-134">Velg Ja i feltet Be om hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="5d2b6-135">Sett Be om hovedkonto til Ja for å tillate brukere å velge hovedkontoen som en del av listen med dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-135">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="5d2b6-136">Hvis satt til Nei, blir ikke hovedkontoen tatt med i listen over dimensjoner, og alternativet Er obligatorisk for hovedkonto aktiveres.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-136">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="5d2b6-137">Hvis Er obligatorisk for hovedkonto settes til Ja, inkluderes hovedkontoen i listen over dimensjonere uavhengig av brukerens valg.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-137">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="5d2b6-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-138">Click OK.</span></span>
<span data-ttu-id="5d2b6-139">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="5d2b6-139">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="5d2b6-140">Velg Dynamics 365 for Operations\Tabellposter i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-140">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="5d2b6-141">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-141">Click Add root.</span></span>
25. <span data-ttu-id="5d2b6-142">Skriv inn LedgerJournal i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-142">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="5d2b6-143">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-143">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="5d2b6-144">Skriv inn LedgerJournalTable i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-144">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="5d2b6-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-145">Click OK.</span></span>
<span data-ttu-id="5d2b6-146">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="5d2b6-146">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="5d2b6-147">Tilordne datamodellelementer til datakilder som er lagt til</span><span class="sxs-lookup"><span data-stu-id="5d2b6-147">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="5d2b6-148">Utvid Journal i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-148">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="5d2b6-149">Utvid Journal\Transaksjon i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-149">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="5d2b6-150">Utvid Journal\Transaksjon\Dimensjonsdata i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-150">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="5d2b6-151">Utvid Dimensjonsinnstilling i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-151">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="5d2b6-152">Utvid LedgerJournal i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-152">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="5d2b6-153">Utvid LedgerJournal\<Relasjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-153">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="5d2b6-154">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-154">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="5d2b6-155">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Bilag i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-155">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="5d2b6-156">Velg Journal\Transaksjon\Bilag i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-156">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="5d2b6-157">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-157">Click Bind.</span></span>
11. <span data-ttu-id="5d2b6-158">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension) i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-158">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="5d2b6-159">Merk at for alle referanser til finansdimensjoner som settes til, for eksempel LedgerDimension, er et tilsvarende datakildeelement tilgjengelig (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="5d2b6-159">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="5d2b6-160">Dette datakildeelementet tilbyr finansdimensjonene for dette dimensjonssettet som postens liste.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-160">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="5d2b6-161">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension) i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="5d2b6-162">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="5d2b6-163">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="5d2b6-164">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Definisjon i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="5d2b6-165">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Definisjon\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-165">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="5d2b6-166">Velg Journal\Transaksjon\Dimensjonsdata\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-166">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="5d2b6-167">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-167">Click Bind.</span></span>
19. <span data-ttu-id="5d2b6-168">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-168">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="5d2b6-169">Velg Journal\Transaksjon\Dimensjonsdata\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-169">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="5d2b6-170">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-170">Click Bind.</span></span>
22. <span data-ttu-id="5d2b6-171">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-171">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="5d2b6-172">Velg Journal\Transaksjon\Dimensjonsdata\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-172">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="5d2b6-173">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-173">Click Bind.</span></span>
25. <span data-ttu-id="5d2b6-174">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-174">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="5d2b6-175">Velg Journal\Transaksjon\Dimensjonsdata i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-175">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="5d2b6-176">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-176">Click Bind.</span></span>
<span data-ttu-id="5d2b6-177">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="5d2b6-177">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="5d2b6-178">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Debet(AmountCurDebit) i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="5d2b6-179">Velg Journal\Transaksjon\Debet i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-179">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="5d2b6-180">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-180">Click Bind.</span></span>
31. <span data-ttu-id="5d2b6-181">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Dato(TransDate) i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="5d2b6-182">Velg Journal\Transaksjon\Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-182">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="5d2b6-183">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-183">Click Bind.</span></span>
34. <span data-ttu-id="5d2b6-184">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Valuta(CurrencyCode) i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="5d2b6-185">Velg Journal\Transaksjon\Valuta i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-185">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="5d2b6-186">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-186">Click Bind.</span></span>
37. <span data-ttu-id="5d2b6-187">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Kredit(AmountCurCredit) i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="5d2b6-188">Velg Journal\Transaksjon\Kredit i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-188">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="5d2b6-189">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-189">Click Bind.</span></span>
40. <span data-ttu-id="5d2b6-190">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-190">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="5d2b6-191">Velg Journal\Transaksjon i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-191">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="5d2b6-192">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-192">Click Bind.</span></span>
43. <span data-ttu-id="5d2b6-193">Velg LedgerJournal\Journalpartinummer(JournalNum) i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-193">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="5d2b6-194">Velg Journal\Parti i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-194">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="5d2b6-195">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-195">Click Bind.</span></span>
46. <span data-ttu-id="5d2b6-196">Velg LedgerJournal i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-196">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="5d2b6-197">Velg Journal i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-197">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="5d2b6-198">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-198">Click Bind.</span></span>
49. <span data-ttu-id="5d2b6-199">Utvid Dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-199">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="5d2b6-200">Utvid Dimensjoner\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-200">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="5d2b6-201">Utvid Dimensjoner\Hovedkonto og dimensjoner\Definisjon i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-201">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="5d2b6-202">Velg Dimensjoner\Hovedkonto og dimensjoner\Definisjon\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="5d2b6-203">Velg Dimensjonsinnstilling\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-203">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="5d2b6-204">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-204">Click Bind.</span></span>
55. <span data-ttu-id="5d2b6-205">Velg Dimensjoner\Hovedkonto og dimensjoner\Definisjon\Rapportkolonnenavn i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-205">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="5d2b6-206">Velg Dimensjonsinnstilling\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-206">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="5d2b6-207">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-207">Click Bind.</span></span>
58. <span data-ttu-id="5d2b6-208">Velg Dimensjoner\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-208">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="5d2b6-209">Velg Dimensjonsinnstilling i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-209">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="5d2b6-210">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-210">Click Bind.</span></span>
61. <span data-ttu-id="5d2b6-211">Velg Firma i treet.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-211">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="5d2b6-212">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-212">Click Edit.</span></span>
63. <span data-ttu-id="5d2b6-213">Angi Company.'find()'.'name()' i feltet expressionAsStringText.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-213">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="5d2b6-214">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="5d2b6-214">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="5d2b6-215">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-215">Click Save.</span></span>
<span data-ttu-id="5d2b6-216">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="5d2b6-216">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="5d2b6-217">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-217">Close the page.</span></span>
66. <span data-ttu-id="5d2b6-218">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-218">Click Save.</span></span>
67. <span data-ttu-id="5d2b6-219">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-219">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="5d2b6-220">Fullføre versjonen av denne utkastmodellen</span><span class="sxs-lookup"><span data-stu-id="5d2b6-220">Complete this draft model's version</span></span>
1. <span data-ttu-id="5d2b6-221">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-221">Close the page.</span></span>
2. <span data-ttu-id="5d2b6-222">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-222">Close the page.</span></span>
3. <span data-ttu-id="5d2b6-223">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-223">Click Change status.</span></span>
4. <span data-ttu-id="5d2b6-224">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-224">Click Complete.</span></span>
5. <span data-ttu-id="5d2b6-225">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5d2b6-225">Click OK.</span></span>
<span data-ttu-id="5d2b6-226">![Siden ER-utforming av modelltilordning](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="5d2b6-226">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
