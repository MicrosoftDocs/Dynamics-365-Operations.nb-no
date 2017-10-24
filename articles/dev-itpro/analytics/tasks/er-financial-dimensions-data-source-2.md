--- 
title: "Tilordne modeller for å bruke finansdimensjoner som en datakilde for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a3eafa7b66dcc0c2481d7eeaf98bed7f58e4be33
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="cbf66-103">Tilordne modeller for å bruke finansdimensjoner som en datakilde for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="cbf66-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbf66-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="cbf66-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="cbf66-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="cbf66-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="cbf66-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 1: Utforme datamodell).</span><span class="sxs-lookup"><span data-stu-id="cbf66-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="cbf66-107">Legge til obligatoriske datakilder i modelltilordning</span><span class="sxs-lookup"><span data-stu-id="cbf66-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="cbf66-108">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="cbf66-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="cbf66-109">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="cbf66-110">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="cbf66-110">Click Designer.</span></span>
4. <span data-ttu-id="cbf66-111">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="cbf66-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="cbf66-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="cbf66-112">Click New.</span></span>
6. <span data-ttu-id="cbf66-113">Velg Oppføring i Definisjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="cbf66-114">Skriv inn Dimensjonsdatatilordning i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="cbf66-115">Skriv inn Dimensjonsdatatilordning i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="cbf66-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="cbf66-116">Click Save.</span></span>
10. <span data-ttu-id="cbf66-117">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="cbf66-117">Click Designer.</span></span>
11. <span data-ttu-id="cbf66-118">I treet velger du Dynamics 365 for Operations\Tabell.</span><span class="sxs-lookup"><span data-stu-id="cbf66-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="cbf66-119">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="cbf66-119">Click Add root.</span></span>
13. <span data-ttu-id="cbf66-120">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="cbf66-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="cbf66-121">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="cbf66-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cbf66-122">Click OK.</span></span>
16. <span data-ttu-id="cbf66-123">Velg Funksjoner\Detaljer for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="cbf66-124">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="cbf66-124">Click Add root.</span></span>
    * <span data-ttu-id="cbf66-125">Denne datakilden angir hvordan omfanget av finansdimensjoner defineres for en rapport som skal bruke denne modellen som datakilde.</span><span class="sxs-lookup"><span data-stu-id="cbf66-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="cbf66-126">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="cbf66-127">Velg Ja i feltet Be om dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="cbf66-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="cbf66-128">Velg Ja hvis du vil at brukeren skal kunne velge dimensjoner under kjøring i dialogboksskjemaet Bruker.</span><span class="sxs-lookup"><span data-stu-id="cbf66-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="cbf66-129">Hvis satt til Nei, brukes alle finansdimensjoner for den gjeldende forekomsten som standard.</span><span class="sxs-lookup"><span data-stu-id="cbf66-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="cbf66-130">Velg Juridisk enhet i feltet Valg av finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="cbf66-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="cbf66-131">Velg Alle for å la brukeren velge ønskede dimensjoner for gjeldende forekomst i oppslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="cbf66-132">Velg Juridisk enhet for å la brukeren velge dimensjoner for firmaet i oppslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="cbf66-133">Velg Dimensjon for å la brukeren velge dimensjoner ved hjelp av et enkelt dimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="cbf66-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="cbf66-134">Velg Ja i feltet Be om hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="cbf66-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="cbf66-135">Sett Be om hovedkonto til Ja for å tillate brukere å velge hovedkontoen som en del av listen med dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="cbf66-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="cbf66-136">Hvis satt til Nei, blir ikke hovedkontoen tatt med i listen over dimensjoner, og alternativet Er obligatorisk for hovedkonto aktiveres.</span><span class="sxs-lookup"><span data-stu-id="cbf66-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="cbf66-137">Hvis Er obligatorisk for hovedkonto settes til Ja, inkluderes hovedkontoen i listen over dimensjonere uavhengig av brukerens valg.</span><span class="sxs-lookup"><span data-stu-id="cbf66-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="cbf66-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cbf66-138">Click OK.</span></span>
23. <span data-ttu-id="cbf66-139">I treet velger du Dynamics 365 for Operations\Tabellposter.</span><span class="sxs-lookup"><span data-stu-id="cbf66-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="cbf66-140">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="cbf66-140">Click Add root.</span></span>
25. <span data-ttu-id="cbf66-141">Skriv inn LedgerJournal i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="cbf66-142">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="cbf66-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="cbf66-143">Skriv inn LedgerJournalTable i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="cbf66-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cbf66-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="cbf66-145">Tilordne datamodellelementer til datakilder som er lagt til</span><span class="sxs-lookup"><span data-stu-id="cbf66-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="cbf66-146">Utvid Journal i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="cbf66-147">Utvid Journal\Transaksjon i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="cbf66-148">Utvid Journal\Transaksjon\Dimensjonsdata i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="cbf66-149">Utvid Dimensjonsinnstilling i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="cbf66-150">Utvid LedgerJournal i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="cbf66-151">Utvid LedgerJournal\<Relasjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="cbf66-152">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="cbf66-153">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Bilag i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="cbf66-154">Velg Journal\Transaksjon\Bilag i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="cbf66-155">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-155">Click Bind.</span></span>
11. <span data-ttu-id="cbf66-156">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension) i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="cbf66-157">Merk at for alle referanser til finansdimensjoner som settes til, for eksempel LedgerDimension, er et tilsvarende datakildeelement tilgjengelig (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="cbf66-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="cbf66-158">Dette datakildeelementet tilbyr finansdimensjonene for dette dimensjonssettet som postens liste.</span><span class="sxs-lookup"><span data-stu-id="cbf66-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="cbf66-159">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension) i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="cbf66-160">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="cbf66-161">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="cbf66-162">Utvid LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Definisjon i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="cbf66-163">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Definisjon\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="cbf66-164">Velg Journal\Transaksjon\Dimensjonsdata\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="cbf66-165">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-165">Click Bind.</span></span>
19. <span data-ttu-id="cbf66-166">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="cbf66-167">Velg Journal\Transaksjon\Dimensjonsdata\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="cbf66-168">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-168">Click Bind.</span></span>
22. <span data-ttu-id="cbf66-169">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner\Verdi\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="cbf66-170">Velg Journal\Transaksjon\Dimensjonsdata\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="cbf66-171">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-171">Click Bind.</span></span>
25. <span data-ttu-id="cbf66-172">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="cbf66-173">Velg Journal\Transaksjon\Dimensjonsdata i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="cbf66-174">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-174">Click Bind.</span></span>
28. <span data-ttu-id="cbf66-175">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Debet(AmountCurDebit) i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="cbf66-176">Velg Journal\Transaksjon\Debet i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="cbf66-177">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-177">Click Bind.</span></span>
31. <span data-ttu-id="cbf66-178">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Dato(TransDate) i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="cbf66-179">Velg Journal\Transaksjon\Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="cbf66-180">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-180">Click Bind.</span></span>
34. <span data-ttu-id="cbf66-181">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Valuta(CurrencyCode) i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="cbf66-182">Velg Journal\Transaksjon\Valuta i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="cbf66-183">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-183">Click Bind.</span></span>
37. <span data-ttu-id="cbf66-184">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans\Kredit(AmountCurCredit) i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="cbf66-185">Velg Journal\Transaksjon\Kredit i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="cbf66-186">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-186">Click Bind.</span></span>
40. <span data-ttu-id="cbf66-187">Velg LedgerJournal\<Relasjoner\LedgerJournalTrans i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="cbf66-188">Velg Journal\Transaksjon i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="cbf66-189">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-189">Click Bind.</span></span>
43. <span data-ttu-id="cbf66-190">Velg LedgerJournal\Journalpartinummer(JournalNum) i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="cbf66-191">Velg Journal\Parti i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="cbf66-192">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-192">Click Bind.</span></span>
46. <span data-ttu-id="cbf66-193">Velg LedgerJournal i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="cbf66-194">Velg Journal i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="cbf66-195">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-195">Click Bind.</span></span>
49. <span data-ttu-id="cbf66-196">Utvid Dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="cbf66-197">Utvid Dimensjoner\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="cbf66-198">Utvid Dimensjoner\Hovedkonto og dimensjoner\Definisjon i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="cbf66-199">Velg Dimensjoner\Hovedkonto og dimensjoner\Definisjon\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="cbf66-200">Velg Dimensjonsinnstilling\Kode i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="cbf66-201">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-201">Click Bind.</span></span>
55. <span data-ttu-id="cbf66-202">Velg Dimensjoner\Hovedkonto og dimensjoner\Definisjon\Rapportkolonnenavn i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="cbf66-203">Velg Dimensjonsinnstilling\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="cbf66-204">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-204">Click Bind.</span></span>
58. <span data-ttu-id="cbf66-205">Velg Dimensjoner\Hovedkonto og dimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="cbf66-206">Velg Dimensjonsinnstilling i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="cbf66-207">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="cbf66-207">Click Bind.</span></span>
61. <span data-ttu-id="cbf66-208">Velg Firma i treet.</span><span class="sxs-lookup"><span data-stu-id="cbf66-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="cbf66-209">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="cbf66-209">Click Edit.</span></span>
63. <span data-ttu-id="cbf66-210">Angi Company.'find()'.'name()' i feltet expressionAsStringText.</span><span class="sxs-lookup"><span data-stu-id="cbf66-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="cbf66-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="cbf66-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="cbf66-212">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="cbf66-212">Click Save.</span></span>
65. <span data-ttu-id="cbf66-213">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cbf66-213">Close the page.</span></span>
66. <span data-ttu-id="cbf66-214">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="cbf66-214">Click Save.</span></span>
67. <span data-ttu-id="cbf66-215">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cbf66-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="cbf66-216">Fullføre versjonen av denne utkastmodellen</span><span class="sxs-lookup"><span data-stu-id="cbf66-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="cbf66-217">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cbf66-217">Close the page.</span></span>
2. <span data-ttu-id="cbf66-218">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cbf66-218">Close the page.</span></span>
3. <span data-ttu-id="cbf66-219">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="cbf66-219">Click Change status.</span></span>
4. <span data-ttu-id="cbf66-220">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="cbf66-220">Click Complete.</span></span>
5. <span data-ttu-id="cbf66-221">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cbf66-221">Click OK.</span></span>


