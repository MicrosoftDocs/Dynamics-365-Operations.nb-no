--- 
title: Definere kvalitetsordrer
description: "Denne fremgangsmåten viser hvordan du aktiverer en kvalitetsstyringsprosess der innkommende lager må kontrolleres umiddelbart etter ankomstregistrering."
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c36e35f45709d32db7bc1a625d4bcc30cf543fb0
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="39554-103">Definere kvalitetsordrer</span><span class="sxs-lookup"><span data-stu-id="39554-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39554-104">Denne fremgangsmåten viser hvordan du aktiverer en kvalitetsstyringsprosess der innkommende lager må kontrolleres umiddelbart etter ankomstregistrering.</span><span class="sxs-lookup"><span data-stu-id="39554-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="39554-105">Fremgangsmåten vil vanligvis utføres av en kvalitetssjef.</span><span class="sxs-lookup"><span data-stu-id="39554-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="39554-106">Prosessen omfatter oppretting av en kvalitetsgruppe, for å definere varene som skal testes, og en testgruppe for å gruppere testene som skal utføres, på varer i kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="39554-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="39554-107">Du kan kjøre denne veiledningen i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="39554-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="39554-108">Aktivere kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="39554-108">Enable quality management</span></span>
1. <span data-ttu-id="39554-109">Gå til Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="39554-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="39554-110">Klikk kategorien Kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="39554-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="39554-111">Sett alternativet Bruk kvalitetsstyring til Ja.</span><span class="sxs-lookup"><span data-stu-id="39554-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="39554-112">Klikk Rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="39554-112">Click Report setup.</span></span>
    * <span data-ttu-id="39554-113">Rapportoppsett for kvalitetsstyring er allerede definert i USMF.</span><span class="sxs-lookup"><span data-stu-id="39554-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="39554-114">Hvis dette ikke er gjort, kan du legge til nye linjer for de forskjellige rapporttypene og velg dokumenttypen som skal brukes for hver rapport.</span><span class="sxs-lookup"><span data-stu-id="39554-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="39554-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-115">Close the page.</span></span>
6. <span data-ttu-id="39554-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="39554-117">Opprette en test</span><span class="sxs-lookup"><span data-stu-id="39554-117">Create a test</span></span>
1. <span data-ttu-id="39554-118">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Tester.</span><span class="sxs-lookup"><span data-stu-id="39554-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="39554-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39554-119">Click New.</span></span>
3. <span data-ttu-id="39554-120">Skriv inn en verdi i Test-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="39554-121">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="39554-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="39554-122">Velg Alternativ i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="39554-123">I dette eksemplet velger vi "Alternativ" som vil gjøre det mulig å tilordne testresultatene basert på forhåndsdefinerte verdier.</span><span class="sxs-lookup"><span data-stu-id="39554-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="39554-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="39554-124">Click Save.</span></span>
7. <span data-ttu-id="39554-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="39554-126">Opprette testvariabler for å definere hvordan testresultater registreres</span><span class="sxs-lookup"><span data-stu-id="39554-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="39554-127">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Testvariabler.</span><span class="sxs-lookup"><span data-stu-id="39554-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="39554-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39554-128">Click New.</span></span>
3. <span data-ttu-id="39554-129">Skriv inn en verdi i Variabel-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="39554-130">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="39554-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="39554-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="39554-131">Click Save.</span></span>
6. <span data-ttu-id="39554-132">Klikk Resultater.</span><span class="sxs-lookup"><span data-stu-id="39554-132">Click Outcomes.</span></span>
7. <span data-ttu-id="39554-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39554-133">Click New.</span></span>
8. <span data-ttu-id="39554-134">Skriv inn en verdi i Resultat-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="39554-135">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="39554-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="39554-136">Velg Bestått i feltet Resultatstatus.</span><span class="sxs-lookup"><span data-stu-id="39554-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="39554-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="39554-137">Click Save.</span></span>
12. <span data-ttu-id="39554-138">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39554-138">Click New.</span></span>
13. <span data-ttu-id="39554-139">Skriv inn en verdi i Resultat-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="39554-140">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="39554-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="39554-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="39554-141">Click Save.</span></span>
16. <span data-ttu-id="39554-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-142">Close the page.</span></span>
17. <span data-ttu-id="39554-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="39554-144">Definere vareprøver</span><span class="sxs-lookup"><span data-stu-id="39554-144">Set up item sampling</span></span>
1. <span data-ttu-id="39554-145">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Vareprøve.</span><span class="sxs-lookup"><span data-stu-id="39554-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="39554-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39554-146">Click New.</span></span>
3. <span data-ttu-id="39554-147">Skriv inn en verdi i Vareprøve-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="39554-148">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="39554-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="39554-149">Angi et tall i Verdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="39554-150">Denne verdien er knyttet til spesifikasjonen av antall som er valgt i feltet ved siden av.</span><span class="sxs-lookup"><span data-stu-id="39554-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="39554-151">Vis eller skjul delen Prosess.</span><span class="sxs-lookup"><span data-stu-id="39554-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="39554-152">Merk av for eller fjern merket for Full blokkering..</span><span class="sxs-lookup"><span data-stu-id="39554-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="39554-153">Hvis du velger dette alternativet, blokkeres hele parti- eller ordrelinjeantallet eller hvis en test mislyktes.</span><span class="sxs-lookup"><span data-stu-id="39554-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="39554-154">Hvis du ikke merker den, blokkeres bare varene i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="39554-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="39554-155">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="39554-155">Click Save.</span></span>
9. <span data-ttu-id="39554-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="39554-157">Opprette en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="39554-157">Create a quality group</span></span>
1. <span data-ttu-id="39554-158">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Kvalitetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="39554-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="39554-159">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39554-159">Click New.</span></span>
3. <span data-ttu-id="39554-160">Skriv inn en verdi i Kvalitetsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="39554-161">Bruk et beskrivende navn som hjelper deg med å identifisere hvilken type varer gruppen inneholder (prøvekriterier).</span><span class="sxs-lookup"><span data-stu-id="39554-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="39554-162">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="39554-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="39554-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="39554-163">Click Save.</span></span>
6. <span data-ttu-id="39554-164">Klikk Legg til varer.</span><span class="sxs-lookup"><span data-stu-id="39554-164">Click Add items.</span></span>
7. <span data-ttu-id="39554-165">Velg varenummerraden.</span><span class="sxs-lookup"><span data-stu-id="39554-165">Select the Item number row</span></span>
    * <span data-ttu-id="39554-166">I dette eksemplet kjøres filtreringsfunksjonen basert på varenummeret.</span><span class="sxs-lookup"><span data-stu-id="39554-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="39554-167">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="39554-168">Skriv for eksempel T\* for å filtrere på varenumrene som begynner med T.</span><span class="sxs-lookup"><span data-stu-id="39554-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="39554-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="39554-169">Click OK.</span></span>
10. <span data-ttu-id="39554-170">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="39554-170">Click OK.</span></span>
11. <span data-ttu-id="39554-171">Klikk Varekvalitetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="39554-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="39554-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-172">Close the page.</span></span>
13. <span data-ttu-id="39554-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="39554-174">Opprette en testgruppe</span><span class="sxs-lookup"><span data-stu-id="39554-174">Create a test group</span></span>
1. <span data-ttu-id="39554-175">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Testgrupper.</span><span class="sxs-lookup"><span data-stu-id="39554-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="39554-176">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39554-176">Click New.</span></span>
3. <span data-ttu-id="39554-177">Skriv inn en verdi i Testgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="39554-178">Gi testgruppen et navn som hjelper deg med å huske hva slags tester som kjøres, og hvilke kvalitetsgruppe den skal være knyttet til.</span><span class="sxs-lookup"><span data-stu-id="39554-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="39554-179">Hvis den for eksempel skal brukes med en kvalitetsgruppe som velger varer som begynner med "T", du kan kalle den "T-varetester".</span><span class="sxs-lookup"><span data-stu-id="39554-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="39554-180">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="39554-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="39554-181">Velg vareprøvelinjen som du opprettet før, i Vareprøve-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="39554-182">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="39554-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="39554-183">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="39554-183">Click Add.</span></span>
8. <span data-ttu-id="39554-184">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="39554-185">Velg testen du opprettet tidligere, i Test-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="39554-186">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="39554-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="39554-187">Klikk kategorien Test.</span><span class="sxs-lookup"><span data-stu-id="39554-187">Click the Test tab.</span></span>
12. <span data-ttu-id="39554-188">Velg testvariabelen du opprettet tidligere, i Variabel-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="39554-189">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="39554-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="39554-190">Klikk rullegardinknappen i Standardresultat-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="39554-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="39554-191">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="39554-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="39554-192">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="39554-192">Click Save.</span></span>
17. <span data-ttu-id="39554-193">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="39554-194">Definere når kvalitetsordrer kan opprettes</span><span class="sxs-lookup"><span data-stu-id="39554-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="39554-195">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Kvalitetstilknytninger.</span><span class="sxs-lookup"><span data-stu-id="39554-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="39554-196">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39554-196">Click New.</span></span>
3. <span data-ttu-id="39554-197">Velg et alternativ i Referansetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="39554-198">Velg Gruppe i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="39554-199">I dette eksemplet skal vi velge "Gruppe" og bruke kvalitetsgruppen vi opprettet før.</span><span class="sxs-lookup"><span data-stu-id="39554-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="39554-200">Du kan også angi dette til "Tabell" for å angi varene manuelt, ellere velg "Alle" for å legge til alle varer i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="39554-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="39554-201">I Vare-feltet velger du kvalitetsgruppen som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="39554-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="39554-202">De tilgjengelige alternativene i Vare-feltet avhenger av hva du angir i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="39554-203">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="39554-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="39554-204">Vis eller skjul delen Prosess.</span><span class="sxs-lookup"><span data-stu-id="39554-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="39554-205">Velg et alternativ i Hendelsestype-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="39554-206">Dette er hendelsen som utløser testen.</span><span class="sxs-lookup"><span data-stu-id="39554-206">This is the event that triggers the test.</span></span> <span data-ttu-id="39554-207">Alternativene som er tilgjengelig her, avhenger av hvilken prosess du valgte i feltet Referansetype.</span><span class="sxs-lookup"><span data-stu-id="39554-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="39554-208">Velg et alternativ i Utførelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="39554-209">Vis eller skjul delen Kvalitetsordreprosess.</span><span class="sxs-lookup"><span data-stu-id="39554-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="39554-210">Klikk rullegardinknappen i feltet Hendelsesblokkering for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="39554-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="39554-211">Dette feltet viser listen over prosesser som det er mulig å blokkere hvis kvalitetsordren fremdeles er åpen.</span><span class="sxs-lookup"><span data-stu-id="39554-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="39554-212">Alternativene er avhengig av hva du valgte i feltet Hendelsestype.</span><span class="sxs-lookup"><span data-stu-id="39554-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="39554-213">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="39554-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="39554-214">Dette vil være avhengig av de tidligere valgte verdiene.</span><span class="sxs-lookup"><span data-stu-id="39554-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="39554-215">Velg om følgende prosesser må være blokkert mens du har åpne kvalitetsordrer som er koblet til en kildedokumentlinje.</span><span class="sxs-lookup"><span data-stu-id="39554-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="39554-216">Vis eller skjul delen Spesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="39554-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="39554-217">Velg testgruppen du opprettet tidligere, i Testgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="39554-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="39554-218">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="39554-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="39554-219">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="39554-219">Click Save.</span></span>
17. <span data-ttu-id="39554-220">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39554-220">Close the page.</span></span>


