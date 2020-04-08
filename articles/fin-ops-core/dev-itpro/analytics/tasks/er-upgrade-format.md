---
title: ER Oppgradere formatet ved å ta i bruk en ny, grunnleggende versjon av dette formatet
description: De fremgangsmåten nedenfor forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan vedlikeholde en formatkonfigurasjon for elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52bc276a4a88971a7214fa09087cb1323b91aaf5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143285"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="9df49-103">ER Oppgradere formatet ved å ta i bruk en ny, grunnleggende versjon av dette formatet</span><span class="sxs-lookup"><span data-stu-id="9df49-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9df49-104">De fremgangsmåten nedenfor forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan vedlikeholde en formatkonfigurasjon for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="9df49-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="9df49-105">Denne fremgangsmåten beskriver hvordan en egendefinert versjon av et format kan opprettes basert på formatet som mottas fra en konfigurasjonsleverandør (CP).</span><span class="sxs-lookup"><span data-stu-id="9df49-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="9df49-106">Den forklarer også hvordan du bruker en ny, basisversjon av dette formatet.</span><span class="sxs-lookup"><span data-stu-id="9df49-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="9df49-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåtene "Opprette en konfigurasjonsleverandør og merke den som aktiv" og "Bruke opprettet formatet for å generere elektroniske betalingsdokumenter".</span><span class="sxs-lookup"><span data-stu-id="9df49-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="9df49-108">Denne fremgangsmåten kan utføres i firmaet GBSI.</span><span class="sxs-lookup"><span data-stu-id="9df49-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="9df49-109">Velge formatkonfigurasjon for tilpassing</span><span class="sxs-lookup"><span data-stu-id="9df49-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="9df49-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="9df49-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="9df49-111">I dette eksemplet fungerer eksempelfirmaet Litware, Inc. (https://www.litware.com) som en konfigurasjonsleverandør som støtter formatkonfigurasjoner for elektroniske betalinger for et bestemt land.</span><span class="sxs-lookup"><span data-stu-id="9df49-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="9df49-112">Eksempelfirmaet Proseware, Inc (http://www.proseware.com) fungerer som en kunde i formatkonfigurasjonen som Litware, Inc. har angitt</span><span class="sxs-lookup"><span data-stu-id="9df49-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="9df49-113">Proseware, Inc. bruker formater i bestemte områder i dette landet.</span><span class="sxs-lookup"><span data-stu-id="9df49-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="9df49-114">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="9df49-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9df49-115">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="9df49-115">Click Show filters.</span></span>
4. <span data-ttu-id="9df49-116">Bruk følgende filtre: Angi filterverdien "BACS (britisk fiktivt)" i Navn-feltet ved hjelp av filteroperatoren "begynner med".</span><span class="sxs-lookup"><span data-stu-id="9df49-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="9df49-117">Den valgte formatkonfigurajonen BBS (Storbritannia fiktiv) eies av leverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9df49-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="9df49-118">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="9df49-118">Click Show filters.</span></span>
6. <span data-ttu-id="9df49-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9df49-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9df49-120">Versjonen av formatet med statusen Fullført brukes av Proseware, Inc. for tilpassing.</span><span class="sxs-lookup"><span data-stu-id="9df49-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="9df49-121">Opprette en ny konfigurasjon for det egendefinerte formatet for elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="9df49-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="9df49-122">Proseware, Inc. mottatte versjon 1.1 av BBS-konfigurasjon (Storbritannia fiktiv) som inneholder det innledende formatet for å generere elektroniske betalingsdokumenter fra Litware, Inc. i henhold til deres serviceabonnement.</span><span class="sxs-lookup"><span data-stu-id="9df49-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="9df49-123">Proseware, Inc. vil begynne å bruke dette som standard for landet sitt, men noe tilpassing er nødvendig for å støtte bestemte områdekrav.</span><span class="sxs-lookup"><span data-stu-id="9df49-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="9df49-124">Proseware, Inc. vil også beholde muligheten til å oppgradere et egendefinert format når det kommer en ny versjon av det (med endringer for å støtte nye landspesifikke krav) fra Litware, Inc, og de vil utføre oppgraderingen med lavest mulig kostnad.</span><span class="sxs-lookup"><span data-stu-id="9df49-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="9df49-125">For å gjøre dette må Proseware, Inc. opprette en konfigurasjon ved hjelp av Litware, Inc. konfigurasjonen BBS (Storbritannia fiktiv) som grunnlag.</span><span class="sxs-lookup"><span data-stu-id="9df49-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="9df49-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9df49-126">Close the page.</span></span>
2. <span data-ttu-id="9df49-127">Velg Proseware, Inc. for å gjøre dette til en aktiv leverandør.</span><span class="sxs-lookup"><span data-stu-id="9df49-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="9df49-128">Klikk Angi som aktiv</span><span class="sxs-lookup"><span data-stu-id="9df49-128">Click Set active.</span></span>
4. <span data-ttu-id="9df49-129">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="9df49-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9df49-130">Vis Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9df49-131">Velg Betalinger (forenklet model)\BBS (Storbritannia fiktiv) i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="9df49-132">Velg konfigurasjonen BBS (Storbritannia fiktivt) fra Litware, Inc. Proseware, Inc. bruker versjon 1.1 som grunnlag for den tilpassede versjonen.</span><span class="sxs-lookup"><span data-stu-id="9df49-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="9df49-133">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9df49-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="9df49-134">Det lar deg opprette en ny konfigurasjon for et egendefinert betalingsformat.</span><span class="sxs-lookup"><span data-stu-id="9df49-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="9df49-135">I det nye feltet angir du Avled fra navnet: BBS (Storbritannia fiktiv), Litware, Inc..</span><span class="sxs-lookup"><span data-stu-id="9df49-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="9df49-136">Velg alternativet Avled for å bekrefte at bruken av BBS (Storbritannia fiktivt) som grunnlag for oppretting av den egendefinerte versjonen.</span><span class="sxs-lookup"><span data-stu-id="9df49-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="9df49-137">Skriv inn BBS (Storbritannia fiktiv egendefinert ) i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9df49-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="9df49-138">I Beskrivelse-feltet skriver du inn BACS-leverandørbetaling (fiktivt Storbritannia egendefinert).</span><span class="sxs-lookup"><span data-stu-id="9df49-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="9df49-139">Den aktive konfigurasjonsleverandøren (Proseware, Inc.) angis automatisk her.</span><span class="sxs-lookup"><span data-stu-id="9df49-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="9df49-140">Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="9df49-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="9df49-141">Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.</span><span class="sxs-lookup"><span data-stu-id="9df49-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="9df49-142">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="9df49-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="9df49-143">Tilpasse formatet for det elektroniske dokumentet</span><span class="sxs-lookup"><span data-stu-id="9df49-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="9df49-144">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="9df49-144">Click Designer.</span></span>
2. <span data-ttu-id="9df49-145">Klikk Vis/skjul.</span><span class="sxs-lookup"><span data-stu-id="9df49-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="9df49-146">Klikk Vis/skjul.</span><span class="sxs-lookup"><span data-stu-id="9df49-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="9df49-147">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="9df49-148">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9df49-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="9df49-149">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="9df49-150">I Navn-feltet skriver du IBAN.</span><span class="sxs-lookup"><span data-stu-id="9df49-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="9df49-151">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9df49-151">Click OK.</span></span>
9. <span data-ttu-id="9df49-152">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\IBAN i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="9df49-153">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9df49-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="9df49-154">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="9df49-155">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9df49-155">Click OK.</span></span>
13. <span data-ttu-id="9df49-156">Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="9df49-157">Angi 60 i feltet Maksimumslengde.</span><span class="sxs-lookup"><span data-stu-id="9df49-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="9df49-158">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="9df49-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="9df49-159">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="9df49-160">Utvid modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="9df49-161">Utvid modell\Betalinger\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="9df49-162">Utvid modell\Betalinger\Kreditor\Konto i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="9df49-163">I treet velger du modell\Betalinger\Kreditor\Konto\IBAN.</span><span class="sxs-lookup"><span data-stu-id="9df49-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="9df49-164">Velg Xml\Melding\Betalinger\Vare = modell.Betalinger\Leverandør\Bank\IBAN\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="9df49-165">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="9df49-165">Click Bind.</span></span>
23. <span data-ttu-id="9df49-166">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9df49-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="9df49-167">Validere det egendefinerte formatet</span><span class="sxs-lookup"><span data-stu-id="9df49-167">Validate the customized format</span></span>
1. <span data-ttu-id="9df49-168">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="9df49-168">Click Validate.</span></span>

    <span data-ttu-id="9df49-169">Validere oppsett for egendefinert format og endringer for datatilordning for å sikre at alle bindinger er i orden.</span><span class="sxs-lookup"><span data-stu-id="9df49-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="9df49-170">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9df49-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="9df49-171">Endre statusen for gjeldende versjon av egendefinert formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="9df49-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="9df49-172">Endre statusen for utformet formatkonfigurasjon fra Utkast til Fullført for å gjøre den tilgjengelig for generering av betalingsdokument.</span><span class="sxs-lookup"><span data-stu-id="9df49-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="9df49-173">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="9df49-173">Click Change status.</span></span>

    <span data-ttu-id="9df49-174">Legg merke til at gjeldende versjon av den valgte konfigurasjonen har statusen Utkast.</span><span class="sxs-lookup"><span data-stu-id="9df49-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9df49-175">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="9df49-175">Click Complete.</span></span>
3. <span data-ttu-id="9df49-176">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9df49-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9df49-177">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9df49-177">Click OK.</span></span>
5. <span data-ttu-id="9df49-178">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9df49-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9df49-179">Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="9df49-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="9df49-180">Dette betyr at det er versjon 1 av egendefinerte BBS-format (Storbritannia fiktivt egendefinert), som er basert på versjon 1 av BBS-format (Storbritannia fiktivt), som er basert på versjon 1 av datamodellen Betalinger (forenklet modell).</span><span class="sxs-lookup"><span data-stu-id="9df49-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="9df49-181">Teste det egendefinerte formatet for å generere betalingsfiler</span><span class="sxs-lookup"><span data-stu-id="9df49-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="9df49-182">Fullfør trinnene i fremgangsmåten "Bruke opprettet format for å generere elektroniske dokumenter for betalinger" i en parallel Finance and Operations-økt.</span><span class="sxs-lookup"><span data-stu-id="9df49-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="9df49-183">Velg BBS-formatet (Storbritannia fiktiv egendefinert) i parametere for elektronisk betalingmåte.</span><span class="sxs-lookup"><span data-stu-id="9df49-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="9df49-184">Kontroller at den opprettede betalingsfilen inneholder den nylig introduserte XML-noden som presenterer IBAN-kode i henhold til områdekrav.</span><span class="sxs-lookup"><span data-stu-id="9df49-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="9df49-185">Oppdatere den eksisterende landspesifikke konfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="9df49-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="9df49-186">Litware, Inc. må oppdatere BBS-konfigurasjonen (Storbritannia fiktiv) og bruke nye landkrav for administrasjon av formatet for det elektroniske dokumentet.</span><span class="sxs-lookup"><span data-stu-id="9df49-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="9df49-187">Senere vil dette tas med i en ny versjon av denne konfigurasjonen, som vil tilbys for serviceabonnenter, inkludert Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9df49-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="9df49-188">I virkelige relaterte prosesser for klargjøring av tjeneste kan hver versjon av BBS (Storbritannia fiktiv) importeres av Proseware, Inc. fra Litware, Inc. Litware, Inc. -konfigurasjonens LCS-repositorium.</span><span class="sxs-lookup"><span data-stu-id="9df49-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="9df49-189">I denne fremgangsmåten skal vi simuler dette ved å oppdatere BBS (Storbritannia fiktiv) på vegne av en tjenesteleverandør.</span><span class="sxs-lookup"><span data-stu-id="9df49-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="9df49-190">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9df49-190">Close the page.</span></span>
2. <span data-ttu-id="9df49-191">Velg Litware, inc-leverandør.</span><span class="sxs-lookup"><span data-stu-id="9df49-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="9df49-192">Klikk Angi som aktiv</span><span class="sxs-lookup"><span data-stu-id="9df49-192">Click Set active.</span></span>
4. <span data-ttu-id="9df49-193">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="9df49-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9df49-194">Vis Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9df49-195">Velg Betalinger (forenklet model)\BBS (Storbritannia fiktiv) i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="9df49-196">Utkastversjonen som eies av Litware, Inc.-BBS-leverandøren (Storbritannia fiktiv), velges for å vise endringer for å støtte nye landspesifikke krav.</span><span class="sxs-lookup"><span data-stu-id="9df49-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="9df49-197">Lokalisere basisformatet for det elektroniske dokumentet</span><span class="sxs-lookup"><span data-stu-id="9df49-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="9df49-198">Gå ut ifra at det finnes nye landsspesifikke krav som skal støttes av Litware, Inc:</span><span class="sxs-lookup"><span data-stu-id="9df49-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="9df49-199">En verdi for kreditorens SWIFT-bankkode i hver betalingstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="9df49-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="9df49-200">En grense på 100 tegn for lengden på tekst for leverandørens navn i filen som genereres.</span><span class="sxs-lookup"><span data-stu-id="9df49-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="9df49-201">Nye landspesifikke krav</span><span class="sxs-lookup"><span data-stu-id="9df49-201">New country-specific requirements</span></span>  
- <span data-ttu-id="9df49-202">Velg utkastversjonen av den ønskede konfigurasjonen for å introdusere nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="9df49-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="9df49-203">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="9df49-203">Click Designer.</span></span>
2. <span data-ttu-id="9df49-204">Klikk Vis/skjul.</span><span class="sxs-lookup"><span data-stu-id="9df49-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="9df49-205">Klikk Vis/skjul.</span><span class="sxs-lookup"><span data-stu-id="9df49-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="9df49-206">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="9df49-207">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9df49-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="9df49-208">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="9df49-209">I Navn-feltet skriver du inn SWIFT.</span><span class="sxs-lookup"><span data-stu-id="9df49-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="9df49-210">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9df49-210">Click OK.</span></span>
9. <span data-ttu-id="9df49-211">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\SWIFT i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="9df49-212">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9df49-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="9df49-213">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="9df49-214">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9df49-214">Click OK.</span></span>
13. <span data-ttu-id="9df49-215">Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="9df49-216">Angi 100 i feltet Maksimumslengde.</span><span class="sxs-lookup"><span data-stu-id="9df49-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="9df49-217">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="9df49-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="9df49-218">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="9df49-219">Utvid modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="9df49-220">Utvid modell\Betalinger\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="9df49-221">Utvid modell\Betalinger\Kreditor\Agent i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="9df49-222">I treet velger du modell\Betalinger\Kreditor\Agent\SWIFT.</span><span class="sxs-lookup"><span data-stu-id="9df49-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="9df49-223">Velg Xml\Melding\Betalinger\Vare = modell.Betalinger\Leverandør\Bank\SWIFT\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="9df49-224">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="9df49-224">Click Bind.</span></span>
23. <span data-ttu-id="9df49-225">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9df49-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="9df49-226">Validere det lokaliserte formatet</span><span class="sxs-lookup"><span data-stu-id="9df49-226">Validate the localized format</span></span>
1. <span data-ttu-id="9df49-227">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="9df49-227">Click Validate.</span></span>
2. <span data-ttu-id="9df49-228">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9df49-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="9df49-229">Endre statusen for gjeldende versjon av basisformatkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="9df49-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="9df49-230">Endre statusen for den oppdaterte grunnleggende formatkonfigurasjonen fra Utkast til Fullført for å gjøre den tilgjengelig for generering av betalingsdokumenter og oppdateringer av formatkonfigurasjoner som er avledet fra den.</span><span class="sxs-lookup"><span data-stu-id="9df49-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="9df49-231">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="9df49-231">Click Change status.</span></span>

    <span data-ttu-id="9df49-232">Legg merke til at gjeldende versjon av den valgte konfigurasjonen har statusen Utkast.</span><span class="sxs-lookup"><span data-stu-id="9df49-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9df49-233">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="9df49-233">Click Complete.</span></span>
3. <span data-ttu-id="9df49-234">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9df49-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9df49-235">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9df49-235">Click OK.</span></span>
5. <span data-ttu-id="9df49-236">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9df49-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="9df49-237">Endre basisversjonen for den egendefinerte formatkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="9df49-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="9df49-238">Proseware, Inc. blir informert om at en ny versjon 1.2 av BBS-konfigurasjon (Storbritannia fiktiv) er tilgjengelig for å generere elektroniske betalingsdokumenter i henhold til den nylig annonserte landspesifikke krav.</span><span class="sxs-lookup"><span data-stu-id="9df49-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="9df49-239">Proseware, Inc. vil begynne å bruke det som standard for landet.</span><span class="sxs-lookup"><span data-stu-id="9df49-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="9df49-240">For å gjøre dette må Proseware, Inc. endre den grunnleggende konfigurasjonsversjonen for den tilpassede BBS-konfigurasjonen (Storbritannia fiktiv egendefinert).</span><span class="sxs-lookup"><span data-stu-id="9df49-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="9df49-241">Bruk den nye versjon 1.2 i stedet for versjon 1.1 av BBS (Storbritannia fiktiv).</span><span class="sxs-lookup"><span data-stu-id="9df49-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="9df49-242">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="9df49-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9df49-243">Velg Proseware, Inc.-leverandøren for å merke den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="9df49-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="9df49-244">Klikk Angi som aktiv</span><span class="sxs-lookup"><span data-stu-id="9df49-244">Click Set active.</span></span>
4. <span data-ttu-id="9df49-245">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="9df49-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9df49-246">Vis Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9df49-247">Vis Betalinger (forenklet model)\BBS (Storbritannia fiktiv) i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="9df49-248">Velg Betalinger (forenklet model)\BBS (Storbritannia fiktiv)\BBS (Storbritannia fiktiv egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="9df49-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="9df49-249">Velge BBS-konfigurasjonen (Storbritannia fiktiv egendefinert), som eies av Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9df49-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="9df49-250">Bruk utkastversjonen av den valgte konfigurasjonen for å introdusere nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="9df49-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="9df49-251">Klikk Rebaser.</span><span class="sxs-lookup"><span data-stu-id="9df49-251">Click Rebase.</span></span>

    <span data-ttu-id="9df49-252">Velg den nye versjonen 1.2 av den grunnleggende konfigurasjonen som skal brukes som nytt grunnlag for oppdatering av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="9df49-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="9df49-253">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9df49-253">Click OK.</span></span>

    <span data-ttu-id="9df49-254">Vær oppmerksom på at det er oppdaget noen konflikter under sammenslåing av den egendefinerte versjonen og en ny grunnleggende versjon, som representerer noen formatendringer som ikke kan slås sammen automatisk.</span><span class="sxs-lookup"><span data-stu-id="9df49-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="9df49-255">Løse rebaseringskonflikter</span><span class="sxs-lookup"><span data-stu-id="9df49-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="9df49-256">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="9df49-256">Click Designer.</span></span>
    
    <span data-ttu-id="9df49-257">Vær oppmerksom på at endringer i leverandørens tekstlengdegrense ikke kunne løses automatisk.</span><span class="sxs-lookup"><span data-stu-id="9df49-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="9df49-258">Dette vises derfor i en konfliktliste.</span><span class="sxs-lookup"><span data-stu-id="9df49-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="9df49-259">Følgende alternativer er tilgjengelige for hver konflikt av typen Oppdatering: – Bruk en tidligere basisverdi (knappen øverst i rutenettet) for å vise forrige basisversjonsverdi (0 i vårt tilfelle).</span><span class="sxs-lookup"><span data-stu-id="9df49-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="9df49-260">- Bruk en basisverdi (knappen øverst i rutenettet) for å vise den nye basisversjonverdien (100 i vårt tilfelle).</span><span class="sxs-lookup"><span data-stu-id="9df49-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="9df49-261">- Behold en egen (egendefinert) verdi (60 i vårt tilfelle).</span><span class="sxs-lookup"><span data-stu-id="9df49-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="9df49-262">Klikk Bruk basisverdi for å bruke den landspesifikke grensen på 100 tegn for tekstlengden for leverandørens navn.</span><span class="sxs-lookup"><span data-stu-id="9df49-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="9df49-263">Merk at Proseware, Inc. og Litware, Inc. har egendefinerte og lokale versjoner av dette formatet som bruker IBAN- og SWIFT-koder med relaterte komponenter som slås sammen automatisk i administrasjonsformat.</span><span class="sxs-lookup"><span data-stu-id="9df49-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="9df49-264">Klikk Bruk basisverdi.</span><span class="sxs-lookup"><span data-stu-id="9df49-264">Click Apply base value.</span></span>

    <span data-ttu-id="9df49-265">Klikk Bruk basisverdi for å bruke den landspesifikke grensen på 100 tegn for leverandørnavn.</span><span class="sxs-lookup"><span data-stu-id="9df49-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="9df49-266">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9df49-266">Click Save.</span></span>

    <span data-ttu-id="9df49-267">Lagring av formatet fjerner løste konflikter fra listen over konflikter.</span><span class="sxs-lookup"><span data-stu-id="9df49-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="9df49-268">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9df49-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="9df49-269">Endre statusen for den nye versjonen av den egendefinerte formatkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="9df49-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="9df49-270">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="9df49-270">Click Change status.</span></span>

    <span data-ttu-id="9df49-271">Endre statusen for den oppdaterte, egendefinert formatkonfigurasjonen fra Utkast til Fullført.</span><span class="sxs-lookup"><span data-stu-id="9df49-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="9df49-272">Dette vil gjøre formatkonfigurasjonen tilgjengelig for generering av betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="9df49-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="9df49-273">Legg merke til at gjeldende versjon av den valgte konfigurasjonen har statusen Utkast.</span><span class="sxs-lookup"><span data-stu-id="9df49-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9df49-274">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="9df49-274">Click Complete.</span></span>
3. <span data-ttu-id="9df49-275">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9df49-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9df49-276">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9df49-276">Click OK.</span></span>

    <span data-ttu-id="9df49-277">Vær oppmerksom på at den opprettede konfigurasjonen lagres som fullført versjon 1.2.2: versjon 2 av det grunnleggende BBS-formatet (Storbritannia fiktiv egendefinert), som er basert på versjon 2 av det grunnleggende BBS-formatet (Storbritannia fiktiv), som er basert på versjon 1 av datamodellen Betalinger (forenklet modell).</span><span class="sxs-lookup"><span data-stu-id="9df49-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="9df49-278">Teste det egendefinerte formatet for generering av betalingsfiler</span><span class="sxs-lookup"><span data-stu-id="9df49-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="9df49-279">Fullfør trinnene i fremgangsmåten "Bruke opprettet format til å generere elektroniske dokumenter for betalinger" i en parallel Finance and Operations-økt.</span><span class="sxs-lookup"><span data-stu-id="9df49-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="9df49-280">Velg det opprettede BBS-formatet (Storbritannia fiktiv egendefinert) i parametere for elektronisk betalingmåte.</span><span class="sxs-lookup"><span data-stu-id="9df49-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="9df49-281">Kontroller at den opprettede betalingsfilen inneholder den nylig introduserte Proseware, Inc. XML-noden som presenterer IBAN-kontokode i henhold til områdekrav.</span><span class="sxs-lookup"><span data-stu-id="9df49-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="9df49-282">Filen skal også inneholde den nylig introduserte Litware, Inc. XML-noden som presenterer SWIFT-bankkode i henhold til landkrav.</span><span class="sxs-lookup"><span data-stu-id="9df49-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  

