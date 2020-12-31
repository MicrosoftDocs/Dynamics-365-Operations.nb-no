---
title: ER Utforme domenespesifikk datamodell
description: De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en datamodell for elektroniske betalingsdokumenter.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268f661079b80551b36ad2e1877615d878350051
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681955"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="4a558-103">ER Utforme domenespesifikk datamodell</span><span class="sxs-lookup"><span data-stu-id="4a558-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a558-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en datamodell for elektroniske betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="4a558-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="4a558-105">Denne datamodellen brukes senere som en datakilde når du oppretter formatet for betalingsdokumentene.</span><span class="sxs-lookup"><span data-stu-id="4a558-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="4a558-106">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="4a558-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="4a558-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="4a558-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="4a558-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="4a558-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="4a558-109">Velg konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="4a558-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="4a558-110">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="4a558-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="4a558-111">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="4a558-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="4a558-112">Du vil opprette en konfigurasjon som inneholder en datamodell for elektroniske betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="4a558-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="4a558-113">Denne datamodellen brukes senere som en datakilde når du oppretter formatet for betalingsdokumentene.</span><span class="sxs-lookup"><span data-stu-id="4a558-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="4a558-114">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="4a558-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="4a558-115">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="4a558-116">I Navn-feltet skriver du inn Betalinger (forenklet modell).</span><span class="sxs-lookup"><span data-stu-id="4a558-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="4a558-117">Skriv inn Konfigurasjon for betalingsmodell i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="4a558-118">Den aktive konfigurasjonsleverandøren angis automatisk her.</span><span class="sxs-lookup"><span data-stu-id="4a558-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="4a558-119">Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="4a558-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="4a558-120">Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.</span><span class="sxs-lookup"><span data-stu-id="4a558-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="4a558-121">Klikk Opprett konfigurasjon for å fullføre oppgaven for konfigurasjonsopprettelse</span><span class="sxs-lookup"><span data-stu-id="4a558-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="4a558-122">Opprett en datamodell</span><span class="sxs-lookup"><span data-stu-id="4a558-122">Create a data model</span></span>
<span data-ttu-id="4a558-123">Du oppretter en ny datamodell for den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="4a558-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="4a558-124">Denne konfigurasjonsversjonen får statusen Utkast.</span><span class="sxs-lookup"><span data-stu-id="4a558-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="4a558-125">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="4a558-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="4a558-126">Definere strukturen for en part som deltar i en betalingsprosessen</span><span class="sxs-lookup"><span data-stu-id="4a558-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="4a558-127">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="4a558-128">I Navn-feltet skriver du inn Part.</span><span class="sxs-lookup"><span data-stu-id="4a558-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="4a558-129">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-129">Click Add.</span></span>
4. <span data-ttu-id="4a558-130">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="4a558-131">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="4a558-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="4a558-132">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="4a558-133">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-133">Click Add.</span></span>
8. <span data-ttu-id="4a558-134">I Søk-feltet skriver du inn Part.</span><span class="sxs-lookup"><span data-stu-id="4a558-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="4a558-135">Klikk Søk etter forrige.</span><span class="sxs-lookup"><span data-stu-id="4a558-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="4a558-136">Definer bankstrukturen for denne modellen</span><span class="sxs-lookup"><span data-stu-id="4a558-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="4a558-137">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="4a558-138">Skriv inn Agent i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="4a558-139">Velg Post i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="4a558-140">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-140">Click Add.</span></span>
5. <span data-ttu-id="4a558-141">Angi Finansinstitusjon (for eksempel en bank) som betjener en konto for parten (debitoren/kreditoren), i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="4a558-142">Finansinstitusjon (for eksempel en bank) som betjener en konto for parten (debitoren/kreditoren).</span><span class="sxs-lookup"><span data-stu-id="4a558-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="4a558-143">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="4a558-144">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="4a558-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="4a558-145">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="4a558-146">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-146">Click Add.</span></span>
10. <span data-ttu-id="4a558-147">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="4a558-148">I Navn-feltet skriver du inn SWIFT.</span><span class="sxs-lookup"><span data-stu-id="4a558-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="4a558-149">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-149">Click Add.</span></span>
13. <span data-ttu-id="4a558-150">Skriv inn Bankidentifikasjonskode i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="4a558-151">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="4a558-152">Skriv inn RoutingNumber i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="4a558-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="4a558-153">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-153">Click Add.</span></span>
17. <span data-ttu-id="4a558-154">Skriv inn Registreringsnummer i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="4a558-155">Klikk Søk etter forrige.</span><span class="sxs-lookup"><span data-stu-id="4a558-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="4a558-156">Definer bankkontostrukturen for denne modellen</span><span class="sxs-lookup"><span data-stu-id="4a558-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="4a558-157">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="4a558-158">I Navn-feltet skriver du inn Konto.</span><span class="sxs-lookup"><span data-stu-id="4a558-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="4a558-159">Velg Post i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="4a558-160">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-160">Click Add.</span></span>
5. <span data-ttu-id="4a558-161">I Beskrivelse-feltet skriver du inn Identifikasjon av en konto for en part i en finansinstitusjon (for eksempel en bank).</span><span class="sxs-lookup"><span data-stu-id="4a558-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="4a558-162">Identifikasjon av en konto for en part i en finansinstitusjon (for eksempel en bank).</span><span class="sxs-lookup"><span data-stu-id="4a558-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="4a558-163">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="4a558-164">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="4a558-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="4a558-165">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="4a558-166">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-166">Click Add.</span></span>
10. <span data-ttu-id="4a558-167">Skriv inn Valutakode i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="4a558-168">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="4a558-169">I Navn-feltet skriver du inn Nummer.</span><span class="sxs-lookup"><span data-stu-id="4a558-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="4a558-170">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-170">Click Add.</span></span>
14. <span data-ttu-id="4a558-171">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="4a558-172">I Navn-feltet skriver du IBAN.</span><span class="sxs-lookup"><span data-stu-id="4a558-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="4a558-173">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-173">Click Add.</span></span>
17. <span data-ttu-id="4a558-174">Angi Internasjonalt bankkontonummer i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="4a558-175">Definere betalingsmeldingsstrukturen for betalingstype for kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="4a558-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="4a558-176">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="4a558-177">I feltet Ny node som en for angir du Modellrot.</span><span class="sxs-lookup"><span data-stu-id="4a558-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="4a558-178">I Navn-feltet skriver du inn CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="4a558-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="4a558-179">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-179">Click Add.</span></span>
5. <span data-ttu-id="4a558-180">I Søk-feltet skriver du inn CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="4a558-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="4a558-181">Klikk Søk etter forrige.</span><span class="sxs-lookup"><span data-stu-id="4a558-181">Click Find previous.</span></span>
7. <span data-ttu-id="4a558-182">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="4a558-183">Skriv inn MessageIdentification i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="4a558-184">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-184">Click Add.</span></span>
10. <span data-ttu-id="4a558-185">I Beskrivelse-feltet angir du Punkt-til-punkt-referansen, som tilordnet av instruksjonsparten (og sendt til den neste parten) for å identifisere en melding.</span><span class="sxs-lookup"><span data-stu-id="4a558-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="4a558-186">Punkt-til-punkt-referansen, som tilordnet av instruksjonsparten (og sendt til den neste parten) for å identifisere en melding.</span><span class="sxs-lookup"><span data-stu-id="4a558-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="4a558-187">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="4a558-188">Skriv inn ProcessingDateTime i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="4a558-189">Velg DateTime i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="4a558-190">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-190">Click Add.</span></span>
15. <span data-ttu-id="4a558-191">I Beskrivelse-feltet angir du Datoen og klokkeslettet da betalingsmeldingen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="4a558-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="4a558-192">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="4a558-193">Definer betalingstransaksjonsstrukturen for denne modellen.</span><span class="sxs-lookup"><span data-stu-id="4a558-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="4a558-194">Skriv inn Betalinger i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="4a558-195">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="4a558-196">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-196">Click Add.</span></span>
20. <span data-ttu-id="4a558-197">I Beskrivelse-feltet angir du Betalingslinjer for gjeldende melding.</span><span class="sxs-lookup"><span data-stu-id="4a558-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="4a558-198">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="4a558-199">I Navn-feltet skriver du inn Kreditor.</span><span class="sxs-lookup"><span data-stu-id="4a558-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="4a558-200">Velg Post i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="4a558-201">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-201">Click Add.</span></span>
25. <span data-ttu-id="4a558-202">I Beskrivelse-feltet angir du Parten som et pengebeløp forfaller for.</span><span class="sxs-lookup"><span data-stu-id="4a558-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="4a558-203">Klikk Bytt varereferanse.</span><span class="sxs-lookup"><span data-stu-id="4a558-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="4a558-204">I Søk-feltet skriver du inn Part.</span><span class="sxs-lookup"><span data-stu-id="4a558-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="4a558-205">Klikk Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="4a558-205">Click Find next.</span></span>
29. <span data-ttu-id="4a558-206">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a558-206">Click OK.</span></span>
30. <span data-ttu-id="4a558-207">Skriv inn Betalinger i Søk-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="4a558-208">Klikk Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="4a558-208">Click Find next.</span></span>
32. <span data-ttu-id="4a558-209">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="4a558-210">I Navn-feltet skriver du inn Debitor.</span><span class="sxs-lookup"><span data-stu-id="4a558-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="4a558-211">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-211">Click Add.</span></span>
35. <span data-ttu-id="4a558-212">I Beskrivelse-feltet angir du Part som skylder et pengebeløp til den (ultimate) kreditoren.</span><span class="sxs-lookup"><span data-stu-id="4a558-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="4a558-213">Klikk Bytt varereferanse.</span><span class="sxs-lookup"><span data-stu-id="4a558-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="4a558-214">I Søk-feltet skriver du inn Part.</span><span class="sxs-lookup"><span data-stu-id="4a558-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="4a558-215">Klikk Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="4a558-215">Click Find next.</span></span>
39. <span data-ttu-id="4a558-216">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a558-216">Click OK.</span></span>
40. <span data-ttu-id="4a558-217">Klikk Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="4a558-217">Click Find next.</span></span>
41. <span data-ttu-id="4a558-218">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="4a558-219">Skriv inn Beskrivelse i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="4a558-220">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="4a558-221">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-221">Click Add.</span></span>
45. <span data-ttu-id="4a558-222">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="4a558-223">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="4a558-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="4a558-224">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-224">Click Add.</span></span>
48. <span data-ttu-id="4a558-225">Skriv inn Valutakode i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="4a558-226">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="4a558-227">Skriv inn TransactionDate i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="4a558-228">Velg Dato i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="4a558-229">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-229">Click Add.</span></span>
53. <span data-ttu-id="4a558-230">Angi Transaksjonsdato i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="4a558-231">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="4a558-232">Skriv inn InstructedAmount i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="4a558-233">Velg Faktisk i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="4a558-234">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-234">Click Add.</span></span>
58. <span data-ttu-id="4a558-235">I Beskrivelse-feltet angir du Beløpet som skal flyttes mellom debitor og kreditor før fradrag av tillegg.</span><span class="sxs-lookup"><span data-stu-id="4a558-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="4a558-236">Beløpet bør uttrykkes i valutaen som er bestilt av den første parten.</span><span class="sxs-lookup"><span data-stu-id="4a558-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="4a558-237">Beløpet som skal flyttes mellom debitor og kreditor før fradrag av tillegg.</span><span class="sxs-lookup"><span data-stu-id="4a558-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="4a558-238">Beløpet bør uttrykkes i valutaen som er bestilt av den første parten.</span><span class="sxs-lookup"><span data-stu-id="4a558-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="4a558-239">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a558-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="4a558-240">I Navn-feltet skriver du inn End2EndID.</span><span class="sxs-lookup"><span data-stu-id="4a558-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="4a558-241">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a558-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="4a558-242">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4a558-242">Click Add.</span></span>
63. <span data-ttu-id="4a558-243">I Beskrivelse-feltet skriver du Den unike identifikasjonen som er tilordnet av initialiseringsparten.</span><span class="sxs-lookup"><span data-stu-id="4a558-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="4a558-244">Denne identifikasjonen sendes, forblir uendret, gjennom hele kjeden ende-til-ende.</span><span class="sxs-lookup"><span data-stu-id="4a558-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="4a558-245">Skriv inn PaymentModel i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="4a558-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="4a558-246">Navnet på PaymentModel justerer med forhåndsdefinerte grensesnitt for betalingsskjemaer.</span><span class="sxs-lookup"><span data-stu-id="4a558-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="4a558-247">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4a558-247">Click Save.</span></span>
66. <span data-ttu-id="4a558-248">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4a558-248">Close the page.</span></span>

