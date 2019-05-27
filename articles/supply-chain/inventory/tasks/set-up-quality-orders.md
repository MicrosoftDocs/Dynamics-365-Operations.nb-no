---
title: Definere kvalitetsordrer
description: Denne fremgangsmåten viser hvordan du aktiverer en kvalitetsstyringsprosess der innkommende lager må kontrolleres umiddelbart etter ankomstregistrering.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a073de7bdfd2ef597c09a8066ff2b6a7721ca62
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561323"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="afeeb-103">Definere kvalitetsordrer</span><span class="sxs-lookup"><span data-stu-id="afeeb-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="afeeb-104">Denne fremgangsmåten viser hvordan du aktiverer en kvalitetsstyringsprosess der innkommende lager må kontrolleres umiddelbart etter ankomstregistrering.</span><span class="sxs-lookup"><span data-stu-id="afeeb-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="afeeb-105">Fremgangsmåten vil vanligvis utføres av en kvalitetssjef.</span><span class="sxs-lookup"><span data-stu-id="afeeb-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="afeeb-106">Prosessen omfatter oppretting av en kvalitetsgruppe, for å definere varene som skal testes, og en testgruppe for å gruppere testene som skal utføres, på varer i kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="afeeb-107">Du kan kjøre denne veiledningen i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="afeeb-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="afeeb-108">Aktivere kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="afeeb-108">Enable quality management</span></span>
1. <span data-ttu-id="afeeb-109">Gå til Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="afeeb-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="afeeb-110">Klikk kategorien Kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="afeeb-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="afeeb-111">Sett alternativet Bruk kvalitetsstyring til Ja.</span><span class="sxs-lookup"><span data-stu-id="afeeb-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="afeeb-112">Klikk Rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="afeeb-112">Click Report setup.</span></span>
    * <span data-ttu-id="afeeb-113">Rapportoppsett for kvalitetsstyring er allerede definert i USMF.</span><span class="sxs-lookup"><span data-stu-id="afeeb-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="afeeb-114">Hvis dette ikke er gjort, kan du legge til nye linjer for de forskjellige rapporttypene og velg dokumenttypen som skal brukes for hver rapport.</span><span class="sxs-lookup"><span data-stu-id="afeeb-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="afeeb-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-115">Close the page.</span></span>
6. <span data-ttu-id="afeeb-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="afeeb-117">Opprette en test</span><span class="sxs-lookup"><span data-stu-id="afeeb-117">Create a test</span></span>
1. <span data-ttu-id="afeeb-118">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Tester.</span><span class="sxs-lookup"><span data-stu-id="afeeb-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="afeeb-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="afeeb-119">Click New.</span></span>
3. <span data-ttu-id="afeeb-120">Skriv inn en verdi i Test-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="afeeb-121">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="afeeb-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="afeeb-122">Velg Alternativ i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="afeeb-123">I dette eksemplet velger vi "Alternativ" som vil gjøre det mulig å tilordne testresultatene basert på forhåndsdefinerte verdier.</span><span class="sxs-lookup"><span data-stu-id="afeeb-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="afeeb-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="afeeb-124">Click Save.</span></span>
7. <span data-ttu-id="afeeb-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="afeeb-126">Opprette testvariabler for å definere hvordan testresultater registreres</span><span class="sxs-lookup"><span data-stu-id="afeeb-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="afeeb-127">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Testvariabler.</span><span class="sxs-lookup"><span data-stu-id="afeeb-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="afeeb-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="afeeb-128">Click New.</span></span>
3. <span data-ttu-id="afeeb-129">Skriv inn en verdi i Variabel-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="afeeb-130">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="afeeb-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="afeeb-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="afeeb-131">Click Save.</span></span>
6. <span data-ttu-id="afeeb-132">Klikk Resultater.</span><span class="sxs-lookup"><span data-stu-id="afeeb-132">Click Outcomes.</span></span>
7. <span data-ttu-id="afeeb-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="afeeb-133">Click New.</span></span>
8. <span data-ttu-id="afeeb-134">Skriv inn en verdi i Resultat-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="afeeb-135">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="afeeb-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="afeeb-136">Velg Bestått i feltet Resultatstatus.</span><span class="sxs-lookup"><span data-stu-id="afeeb-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="afeeb-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="afeeb-137">Click Save.</span></span>
12. <span data-ttu-id="afeeb-138">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="afeeb-138">Click New.</span></span>
13. <span data-ttu-id="afeeb-139">Skriv inn en verdi i Resultat-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="afeeb-140">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="afeeb-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="afeeb-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="afeeb-141">Click Save.</span></span>
16. <span data-ttu-id="afeeb-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-142">Close the page.</span></span>
17. <span data-ttu-id="afeeb-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="afeeb-144">Definere vareprøver</span><span class="sxs-lookup"><span data-stu-id="afeeb-144">Set up item sampling</span></span>
1. <span data-ttu-id="afeeb-145">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Vareprøve.</span><span class="sxs-lookup"><span data-stu-id="afeeb-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="afeeb-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="afeeb-146">Click New.</span></span>
3. <span data-ttu-id="afeeb-147">Skriv inn en verdi i Vareprøve-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="afeeb-148">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="afeeb-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="afeeb-149">Angi et tall i Verdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="afeeb-150">Denne verdien er knyttet til spesifikasjonen av antall som er valgt i feltet ved siden av.</span><span class="sxs-lookup"><span data-stu-id="afeeb-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="afeeb-151">Vis eller skjul delen Prosess.</span><span class="sxs-lookup"><span data-stu-id="afeeb-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="afeeb-152">Merk av for eller fjern merket for Full blokkering..</span><span class="sxs-lookup"><span data-stu-id="afeeb-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="afeeb-153">Hvis du velger dette alternativet, blokkeres hele parti- eller ordrelinjeantallet eller hvis en test mislyktes.</span><span class="sxs-lookup"><span data-stu-id="afeeb-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="afeeb-154">Hvis du ikke merker den, blokkeres bare varene i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="afeeb-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="afeeb-155">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="afeeb-155">Click Save.</span></span>
9. <span data-ttu-id="afeeb-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="afeeb-157">Opprette en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="afeeb-157">Create a quality group</span></span>
1. <span data-ttu-id="afeeb-158">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Kvalitetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="afeeb-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="afeeb-159">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="afeeb-159">Click New.</span></span>
3. <span data-ttu-id="afeeb-160">Skriv inn en verdi i Kvalitetsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="afeeb-161">Bruk et beskrivende navn som hjelper deg med å identifisere hvilken type varer gruppen inneholder (prøvekriterier).</span><span class="sxs-lookup"><span data-stu-id="afeeb-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="afeeb-162">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="afeeb-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="afeeb-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="afeeb-163">Click Save.</span></span>
6. <span data-ttu-id="afeeb-164">Klikk Legg til varer.</span><span class="sxs-lookup"><span data-stu-id="afeeb-164">Click Add items.</span></span>
7. <span data-ttu-id="afeeb-165">Velg varenummerraden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-165">Select the Item number row</span></span>
    * <span data-ttu-id="afeeb-166">I dette eksemplet kjøres filtreringsfunksjonen basert på varenummeret.</span><span class="sxs-lookup"><span data-stu-id="afeeb-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="afeeb-167">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="afeeb-168">Skriv for eksempel T\* for å filtrere på varenumrene som begynner med T.</span><span class="sxs-lookup"><span data-stu-id="afeeb-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="afeeb-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="afeeb-169">Click OK.</span></span>
10. <span data-ttu-id="afeeb-170">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="afeeb-170">Click OK.</span></span>
11. <span data-ttu-id="afeeb-171">Klikk Varekvalitetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="afeeb-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="afeeb-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-172">Close the page.</span></span>
13. <span data-ttu-id="afeeb-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="afeeb-174">Opprette en testgruppe</span><span class="sxs-lookup"><span data-stu-id="afeeb-174">Create a test group</span></span>
1. <span data-ttu-id="afeeb-175">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Testgrupper.</span><span class="sxs-lookup"><span data-stu-id="afeeb-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="afeeb-176">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="afeeb-176">Click New.</span></span>
3. <span data-ttu-id="afeeb-177">Skriv inn en verdi i Testgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="afeeb-178">Gi testgruppen et navn som hjelper deg med å huske hva slags tester som kjøres, og hvilke kvalitetsgruppe den skal være knyttet til.</span><span class="sxs-lookup"><span data-stu-id="afeeb-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="afeeb-179">Hvis den for eksempel skal brukes med en kvalitetsgruppe som velger varer som begynner med "T", du kan kalle den "T-varetester".</span><span class="sxs-lookup"><span data-stu-id="afeeb-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="afeeb-180">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="afeeb-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="afeeb-181">Velg vareprøvelinjen som du opprettet før, i Vareprøve-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="afeeb-182">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="afeeb-183">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="afeeb-183">Click Add.</span></span>
8. <span data-ttu-id="afeeb-184">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="afeeb-185">Velg testen du opprettet tidligere, i Test-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="afeeb-186">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="afeeb-187">Klikk kategorien Test.</span><span class="sxs-lookup"><span data-stu-id="afeeb-187">Click the Test tab.</span></span>
12. <span data-ttu-id="afeeb-188">Velg testvariabelen du opprettet tidligere, i Variabel-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="afeeb-189">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="afeeb-190">Klikk rullegardinknappen i Standardresultat-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="afeeb-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="afeeb-191">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="afeeb-192">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="afeeb-192">Click Save.</span></span>
17. <span data-ttu-id="afeeb-193">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="afeeb-194">Definere når kvalitetsordrer kan opprettes</span><span class="sxs-lookup"><span data-stu-id="afeeb-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="afeeb-195">Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Kvalitetstilknytninger.</span><span class="sxs-lookup"><span data-stu-id="afeeb-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="afeeb-196">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="afeeb-196">Click New.</span></span>
3. <span data-ttu-id="afeeb-197">Velg et alternativ i Referansetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="afeeb-198">Velg Gruppe i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="afeeb-199">I dette eksemplet skal vi velge "Gruppe" og bruke kvalitetsgruppen vi opprettet før.</span><span class="sxs-lookup"><span data-stu-id="afeeb-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="afeeb-200">Du kan også angi dette til "Tabell" for å angi varene manuelt, ellere velg "Alle" for å legge til alle varer i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="afeeb-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="afeeb-201">I Vare-feltet velger du kvalitetsgruppen som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="afeeb-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="afeeb-202">De tilgjengelige alternativene i Vare-feltet avhenger av hva du angir i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="afeeb-203">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="afeeb-204">Vis eller skjul delen Prosess.</span><span class="sxs-lookup"><span data-stu-id="afeeb-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="afeeb-205">Velg et alternativ i Hendelsestype-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="afeeb-206">Dette er hendelsen som utløser testen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-206">This is the event that triggers the test.</span></span> <span data-ttu-id="afeeb-207">Alternativene som er tilgjengelig her, avhenger av hvilken prosess du valgte i feltet Referansetype.</span><span class="sxs-lookup"><span data-stu-id="afeeb-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="afeeb-208">Velg et alternativ i Utførelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="afeeb-209">Vis eller skjul delen Kvalitetsordreprosess.</span><span class="sxs-lookup"><span data-stu-id="afeeb-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="afeeb-210">Klikk rullegardinknappen i feltet Hendelsesblokkering for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="afeeb-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="afeeb-211">Dette feltet viser listen over prosesser som det er mulig å blokkere hvis kvalitetsordren fremdeles er åpen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="afeeb-212">Alternativene er avhengig av hva du valgte i feltet Hendelsestype.</span><span class="sxs-lookup"><span data-stu-id="afeeb-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="afeeb-213">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="afeeb-214">Dette vil være avhengig av de tidligere valgte verdiene.</span><span class="sxs-lookup"><span data-stu-id="afeeb-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="afeeb-215">Velg om følgende prosesser må være blokkert mens du har åpne kvalitetsordrer som er koblet til en kildedokumentlinje.</span><span class="sxs-lookup"><span data-stu-id="afeeb-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="afeeb-216">Vis eller skjul delen Spesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="afeeb-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="afeeb-217">Velg testgruppen du opprettet tidligere, i Testgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="afeeb-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="afeeb-218">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="afeeb-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="afeeb-219">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="afeeb-219">Click Save.</span></span>
17. <span data-ttu-id="afeeb-220">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="afeeb-220">Close the page.</span></span>

