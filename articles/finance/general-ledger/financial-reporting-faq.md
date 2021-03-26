---
title: Vanlige spørsmål om finansrapportering
description: Dette emnet viser spørsmål som er knyttet til finansrapportering som andre brukere har hatt.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249314"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="6b7c6-103">Vanlige spørsmål om finansrapportering</span><span class="sxs-lookup"><span data-stu-id="6b7c6-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="6b7c6-104">Dette emnet viser spørsmål som er knyttet til finansrapportering som andre brukere har hatt.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="6b7c6-105">Hvordan begrenser jeg tilgang til en rapport med tresikkerhet?</span><span class="sxs-lookup"><span data-stu-id="6b7c6-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="6b7c6-106">Scenario: Demonstrasjonsfirmaet USMF har en balanserapport som de ikke vil at alle regnskapsrapporteringsbrukere skal kunne se i D365.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="6b7c6-107">Løsning: Du kan bruke tresikkerhet til å begrense tilgang til en rapport, slik at bare bestemte brukere får tilgang til rapporten.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="6b7c6-108">Logg på Rapportutforming for finansrapportering</span><span class="sxs-lookup"><span data-stu-id="6b7c6-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="6b7c6-109">Opprett en ny tredefinisjon (Fil | Ny | Tredefinisjon) a.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="6b7c6-110">Dobbeltklikk på linjen **Sammendrag** i kolonnen **Enhetssikkerhet**.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="6b7c6-111">i.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-111">i.</span></span>    <span data-ttu-id="6b7c6-112">Klikk på Brukere og grupper.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="6b7c6-113">1. Velg brukerne eller gruppen som vil ha tilgang til denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="6b7c6-114">[![brukerskjermbilde](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="6b7c6-115">[![sikkerhetsskjermbilde](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="6b7c6-116">b.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-116">b.</span></span>    <span data-ttu-id="6b7c6-117">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-117">Click **Save**.</span></span>
  
<span data-ttu-id="6b7c6-118">[![Lagre-knapp](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="6b7c6-119">I rapportdefinisjonen legger du til den nye tredefinisjonen</span><span class="sxs-lookup"><span data-stu-id="6b7c6-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="6b7c6-120">[![tredefinisjonsskjema](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="6b7c6-121">A.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-121">A.</span></span>  <span data-ttu-id="6b7c6-122">Mens du er i tredefinisjonen klikker du på Innstilling og merker av for Inkluder alle enheter under Valg av rapporteringsenhet</span><span class="sxs-lookup"><span data-stu-id="6b7c6-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="6b7c6-123">[![skjema for valg av rapporteringsenhet](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="6b7c6-124">**Før:** [![før skjermbilde](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="6b7c6-125">**Etter:** [![etter skjermbilde](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="6b7c6-126">Merk: Årsaken til meldingen ovenfor er at brukeren ikke har tilgang til rapporten etter bruk av enhetssikkerhet</span><span class="sxs-lookup"><span data-stu-id="6b7c6-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="6b7c6-127">Hvordan finner jeg ut hvilke kontoer som ikke samsvarer med saldoene i D365?</span><span class="sxs-lookup"><span data-stu-id="6b7c6-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="6b7c6-128">Når du har en rapport som ikke samsvarer med det du forventer i D365, er det noen trinn du kan gå gjennom for å identifisere disse kontoene og avvikene.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="6b7c6-129">I Rapportutforming for finansrapportering</span><span class="sxs-lookup"><span data-stu-id="6b7c6-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="6b7c6-130">Opprett en ny raddefinisjon a.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="6b7c6-131">Klikk på Rediger | Sett inn rader fra dimensjoner i.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="6b7c6-132">Velg MainAccount [![Velg Hovedskjermbilde_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="6b7c6-133">ii.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-133">ii.</span></span> <span data-ttu-id="6b7c6-134">Klikk på Ok b.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-134">Click Ok b.</span></span>    <span data-ttu-id="6b7c6-135">Lagre raddefinisjonen</span><span class="sxs-lookup"><span data-stu-id="6b7c6-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="6b7c6-136">Opprette en ny kolonnedefinisjon     [![Opprette en ny kolonnedefinisjon](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="6b7c6-137">Opprett en ny rapportdefinisjon a.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="6b7c6-138">Klikk på Innstillinger og fjern merket for [![Innstillinger-skjema](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="6b7c6-139">Generer rapporten.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="6b7c6-140">Eksporter rapporten til Excel.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="6b7c6-141">I D365:</span><span class="sxs-lookup"><span data-stu-id="6b7c6-141">In D365:</span></span> 
1.  <span data-ttu-id="6b7c6-142">Klikk på Økonomimodul | Forespørsler og rapporter | Råbalanse a.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="6b7c6-143">Parametere i.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-143">Parameters i.</span></span>  <span data-ttu-id="6b7c6-144">Fra-dato: Start på regnskapsår ii.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="6b7c6-145">Til-dato: Datoen da du genererte rapporten for iii.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="6b7c6-146">Finansdimensjonssettet Hovedkontosett [![Hovedkontoskjema](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="6b7c6-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="6b7c6-147">b.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-147">b.</span></span>    <span data-ttu-id="6b7c6-148">Klikk på Beregn</span><span class="sxs-lookup"><span data-stu-id="6b7c6-148">Click Calculate</span></span>

2.  <span data-ttu-id="6b7c6-149">Eksporter rapporten til Excel</span><span class="sxs-lookup"><span data-stu-id="6b7c6-149">Export the report to Excel</span></span>

<span data-ttu-id="6b7c6-150">Du skal nå kunne kopiere dataene fra FR Excel-rapporten til D365-råbalanserapporten og sammenligne sluttsaldokolonnene.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]