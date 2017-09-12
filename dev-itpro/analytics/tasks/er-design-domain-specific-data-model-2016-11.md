--- 
title: Utforme en domenespesifikk datamodell for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en datamodell for elektroniske betalingsdokumenter."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3349d4e910cf1a97eb099aaa7d1155732be3a21f
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a><span data-ttu-id="06efc-103">Utforme en domenespesifikk datamodell for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="06efc-103">Design a domain-specific data model for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06efc-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en datamodell for elektroniske betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="06efc-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="06efc-105">Denne datamodellen brukes senere som en datakilde når du oppretter formatet for betalingsdokumentene.</span><span class="sxs-lookup"><span data-stu-id="06efc-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="06efc-106">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="06efc-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="06efc-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="06efc-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="06efc-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="06efc-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="06efc-109">Velg konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="06efc-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="06efc-110">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="06efc-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="06efc-111">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="06efc-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="06efc-112">Du vil opprette en konfigurasjon som inneholder en datamodell for elektroniske betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="06efc-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="06efc-113">Denne datamodellen brukes senere som en datakilde når du oppretter formatet for betalingsdokumentene.</span><span class="sxs-lookup"><span data-stu-id="06efc-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="06efc-114">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="06efc-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="06efc-115">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="06efc-116">I Navn-feltet skriver du inn Betalinger (forenklet modell).</span><span class="sxs-lookup"><span data-stu-id="06efc-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="06efc-117">Betalinger (forenklet modell)</span><span class="sxs-lookup"><span data-stu-id="06efc-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="06efc-118">Skriv inn Konfigurasjon for betalingsmodell i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="06efc-119">Konfigurasjon for betalingsmodell</span><span class="sxs-lookup"><span data-stu-id="06efc-119">Payment model configuration</span></span>  
    * <span data-ttu-id="06efc-120">Den aktive konfigurasjonsleverandøren angis automatisk her.</span><span class="sxs-lookup"><span data-stu-id="06efc-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="06efc-121">Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="06efc-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="06efc-122">Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.</span><span class="sxs-lookup"><span data-stu-id="06efc-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="06efc-123">Klikk Opprett konfigurasjon for å fullføre oppgaven for konfigurasjonsopprettelse</span><span class="sxs-lookup"><span data-stu-id="06efc-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="06efc-124">Opprett en datamodell</span><span class="sxs-lookup"><span data-stu-id="06efc-124">Create a data model</span></span>
    * <span data-ttu-id="06efc-125">Du oppretter en ny datamodell for den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="06efc-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="06efc-126">Denne konfigurasjonsversjonen får statusen Utkast.</span><span class="sxs-lookup"><span data-stu-id="06efc-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="06efc-127">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="06efc-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="06efc-128">Definere strukturen for en part som deltar i en betalingsprosessen</span><span class="sxs-lookup"><span data-stu-id="06efc-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="06efc-129">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="06efc-130">I Navn-feltet skriver du inn Part.</span><span class="sxs-lookup"><span data-stu-id="06efc-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="06efc-131">Part</span><span class="sxs-lookup"><span data-stu-id="06efc-131">Party</span></span>  
3. <span data-ttu-id="06efc-132">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-132">Click Add.</span></span>
4. <span data-ttu-id="06efc-133">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="06efc-134">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="06efc-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="06efc-135">Navn</span><span class="sxs-lookup"><span data-stu-id="06efc-135">Name</span></span>  
6. <span data-ttu-id="06efc-136">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="06efc-137">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-137">Click Add.</span></span>
8. <span data-ttu-id="06efc-138">I Søk-feltet skriver du inn Part.</span><span class="sxs-lookup"><span data-stu-id="06efc-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="06efc-139">Part</span><span class="sxs-lookup"><span data-stu-id="06efc-139">Party</span></span>  
9. <span data-ttu-id="06efc-140">Klikk Søk etter forrige.</span><span class="sxs-lookup"><span data-stu-id="06efc-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="06efc-141">Definer bankstrukturen for denne modellen</span><span class="sxs-lookup"><span data-stu-id="06efc-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="06efc-142">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="06efc-143">Skriv inn Agent i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="06efc-144">Agent</span><span class="sxs-lookup"><span data-stu-id="06efc-144">Agent</span></span>  
3. <span data-ttu-id="06efc-145">Velg Post i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="06efc-146">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-146">Click Add.</span></span>
5. <span data-ttu-id="06efc-147">Angi Finansinstitusjon (for eksempel en bank) som betjener en konto for parten (debitoren/kreditoren), i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="06efc-148">Finansinstitusjon (for eksempel en bank) som betjener en konto for parten (debitoren/kreditoren).</span><span class="sxs-lookup"><span data-stu-id="06efc-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="06efc-149">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="06efc-150">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="06efc-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="06efc-151">Navn</span><span class="sxs-lookup"><span data-stu-id="06efc-151">Name</span></span>  
8. <span data-ttu-id="06efc-152">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="06efc-153">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-153">Click Add.</span></span>
10. <span data-ttu-id="06efc-154">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="06efc-155">I Navn-feltet skriver du inn SWIFT.</span><span class="sxs-lookup"><span data-stu-id="06efc-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="06efc-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="06efc-156">SWIFT</span></span>  
12. <span data-ttu-id="06efc-157">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-157">Click Add.</span></span>
13. <span data-ttu-id="06efc-158">Skriv inn Bankidentifikasjonskode i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="06efc-159">Bankens identifikasjonskode</span><span class="sxs-lookup"><span data-stu-id="06efc-159">Bank identification code</span></span>  
14. <span data-ttu-id="06efc-160">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="06efc-161">Skriv inn RoutingNumber i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="06efc-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="06efc-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="06efc-162">RoutingNumber</span></span>  
16. <span data-ttu-id="06efc-163">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-163">Click Add.</span></span>
17. <span data-ttu-id="06efc-164">Skriv inn Registreringsnummer i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="06efc-165">Organisasjonsnummer</span><span class="sxs-lookup"><span data-stu-id="06efc-165">Routing number</span></span>  
18. <span data-ttu-id="06efc-166">Klikk Søk etter forrige.</span><span class="sxs-lookup"><span data-stu-id="06efc-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="06efc-167">Definer bankkontostrukturen for denne modellen</span><span class="sxs-lookup"><span data-stu-id="06efc-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="06efc-168">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="06efc-169">I Navn-feltet skriver du inn Konto.</span><span class="sxs-lookup"><span data-stu-id="06efc-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="06efc-170">Konto</span><span class="sxs-lookup"><span data-stu-id="06efc-170">Account</span></span>  
3. <span data-ttu-id="06efc-171">Velg Post i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="06efc-172">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-172">Click Add.</span></span>
5. <span data-ttu-id="06efc-173">I Beskrivelse-feltet skriver du inn Identifikasjon av en konto for en part i en finansinstitusjon (for eksempel en bank).</span><span class="sxs-lookup"><span data-stu-id="06efc-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="06efc-174">Identifikasjon av en konto for en part i en finansinstitusjon (for eksempel en bank).</span><span class="sxs-lookup"><span data-stu-id="06efc-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="06efc-175">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="06efc-176">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="06efc-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="06efc-177">Valuta</span><span class="sxs-lookup"><span data-stu-id="06efc-177">Currency</span></span>  
8. <span data-ttu-id="06efc-178">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="06efc-179">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-179">Click Add.</span></span>
10. <span data-ttu-id="06efc-180">Skriv inn Valutakode i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="06efc-181">Valutakode</span><span class="sxs-lookup"><span data-stu-id="06efc-181">Currency code</span></span>  
11. <span data-ttu-id="06efc-182">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="06efc-183">I Navn-feltet skriver du inn Nummer.</span><span class="sxs-lookup"><span data-stu-id="06efc-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="06efc-184">Tall</span><span class="sxs-lookup"><span data-stu-id="06efc-184">Number</span></span>  
13. <span data-ttu-id="06efc-185">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-185">Click Add.</span></span>
14. <span data-ttu-id="06efc-186">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="06efc-187">I Navn-feltet skriver du IBAN.</span><span class="sxs-lookup"><span data-stu-id="06efc-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="06efc-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="06efc-188">IBAN</span></span>  
16. <span data-ttu-id="06efc-189">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-189">Click Add.</span></span>
17. <span data-ttu-id="06efc-190">Angi Internasjonalt bankkontonummer i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="06efc-191">Internasjonalt bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="06efc-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="06efc-192">Definere betalingsmeldingsstrukturen for betalingstype for kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="06efc-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="06efc-193">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="06efc-194">I feltet Ny node som en for angir du Modellrot.</span><span class="sxs-lookup"><span data-stu-id="06efc-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="06efc-195">I Navn-feltet skriver du inn CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="06efc-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="06efc-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="06efc-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="06efc-197">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-197">Click Add.</span></span>
5. <span data-ttu-id="06efc-198">I Søk-feltet skriver du inn CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="06efc-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="06efc-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="06efc-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="06efc-200">Klikk Søk etter forrige.</span><span class="sxs-lookup"><span data-stu-id="06efc-200">Click Find previous.</span></span>
7. <span data-ttu-id="06efc-201">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="06efc-202">Skriv inn MessageIdentification i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="06efc-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="06efc-203">MessageIdentification</span></span>  
9. <span data-ttu-id="06efc-204">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-204">Click Add.</span></span>
10. <span data-ttu-id="06efc-205">I Beskrivelse-feltet angir du Punkt-til-punkt-referansen, som tilordnet av instruksjonsparten (og sendt til den neste parten) for å identifisere en melding.</span><span class="sxs-lookup"><span data-stu-id="06efc-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="06efc-206">Punkt-til-punkt-referansen, som tilordnet av instruksjonsparten (og sendt til den neste parten) for å identifisere en melding.</span><span class="sxs-lookup"><span data-stu-id="06efc-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="06efc-207">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="06efc-208">Skriv inn ProcessingDateTime i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="06efc-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="06efc-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="06efc-210">Velg DateTime i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="06efc-211">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-211">Click Add.</span></span>
15. <span data-ttu-id="06efc-212">I Beskrivelse-feltet angir du Datoen og klokkeslettet da betalingsmeldingen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="06efc-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="06efc-213">Datoen og klokkeslettet da betalingsmeldingen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="06efc-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="06efc-214">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="06efc-215">Definer betalingstransaksjonsstrukturen for denne modellen.</span><span class="sxs-lookup"><span data-stu-id="06efc-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="06efc-216">Skriv inn Betalinger i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="06efc-217">Betalinger</span><span class="sxs-lookup"><span data-stu-id="06efc-217">Payments</span></span>  
18. <span data-ttu-id="06efc-218">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="06efc-219">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-219">Click Add.</span></span>
20. <span data-ttu-id="06efc-220">I Beskrivelse-feltet angir du Betalingslinjer for gjeldende melding.</span><span class="sxs-lookup"><span data-stu-id="06efc-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="06efc-221">Betalingslinjer for gjeldende melding</span><span class="sxs-lookup"><span data-stu-id="06efc-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="06efc-222">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="06efc-223">I Navn-feltet skriver du inn Kreditor.</span><span class="sxs-lookup"><span data-stu-id="06efc-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="06efc-224">Kreditor</span><span class="sxs-lookup"><span data-stu-id="06efc-224">Creditor</span></span>  
23. <span data-ttu-id="06efc-225">Velg Post i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="06efc-226">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-226">Click Add.</span></span>
25. <span data-ttu-id="06efc-227">I Beskrivelse-feltet angir du Parten som et pengebeløp forfaller for.</span><span class="sxs-lookup"><span data-stu-id="06efc-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="06efc-228">Parten som et pengebeløp forfaller for.</span><span class="sxs-lookup"><span data-stu-id="06efc-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="06efc-229">Klikk Bytt varereferanse.</span><span class="sxs-lookup"><span data-stu-id="06efc-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="06efc-230">I Søk-feltet skriver du inn Part.</span><span class="sxs-lookup"><span data-stu-id="06efc-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="06efc-231">Part</span><span class="sxs-lookup"><span data-stu-id="06efc-231">Party</span></span>  
28. <span data-ttu-id="06efc-232">Klikk Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="06efc-232">Click Find next.</span></span>
29. <span data-ttu-id="06efc-233">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="06efc-233">Click OK.</span></span>
30. <span data-ttu-id="06efc-234">Skriv inn Betalinger i Søk-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="06efc-235">Betalinger</span><span class="sxs-lookup"><span data-stu-id="06efc-235">Payments</span></span>  
31. <span data-ttu-id="06efc-236">Klikk Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="06efc-236">Click Find next.</span></span>
32. <span data-ttu-id="06efc-237">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="06efc-238">I Navn-feltet skriver du inn Debitor.</span><span class="sxs-lookup"><span data-stu-id="06efc-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="06efc-239">Debitor</span><span class="sxs-lookup"><span data-stu-id="06efc-239">Debtor</span></span>  
34. <span data-ttu-id="06efc-240">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-240">Click Add.</span></span>
35. <span data-ttu-id="06efc-241">I Beskrivelse-feltet angir du Part som skylder et pengebeløp til den (ultimate) kreditoren.</span><span class="sxs-lookup"><span data-stu-id="06efc-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="06efc-242">Part som skylder et pengebeløp til den (ultimate) kreditoren.</span><span class="sxs-lookup"><span data-stu-id="06efc-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="06efc-243">Klikk Bytt varereferanse.</span><span class="sxs-lookup"><span data-stu-id="06efc-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="06efc-244">I Søk-feltet skriver du inn Part.</span><span class="sxs-lookup"><span data-stu-id="06efc-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="06efc-245">Part</span><span class="sxs-lookup"><span data-stu-id="06efc-245">Party</span></span>  
38. <span data-ttu-id="06efc-246">Klikk Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="06efc-246">Click Find next.</span></span>
39. <span data-ttu-id="06efc-247">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="06efc-247">Click OK.</span></span>
40. <span data-ttu-id="06efc-248">Klikk Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="06efc-248">Click Find next.</span></span>
41. <span data-ttu-id="06efc-249">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="06efc-250">Skriv inn Beskrivelse i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="06efc-251">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="06efc-251">Description</span></span>  
43. <span data-ttu-id="06efc-252">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="06efc-253">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-253">Click Add.</span></span>
45. <span data-ttu-id="06efc-254">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="06efc-255">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="06efc-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="06efc-256">Valuta</span><span class="sxs-lookup"><span data-stu-id="06efc-256">Currency</span></span>  
47. <span data-ttu-id="06efc-257">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-257">Click Add.</span></span>
48. <span data-ttu-id="06efc-258">Skriv inn Valutakode i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="06efc-259">Valutakode</span><span class="sxs-lookup"><span data-stu-id="06efc-259">Currency code</span></span>  
49. <span data-ttu-id="06efc-260">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="06efc-261">Skriv inn TransactionDate i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="06efc-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="06efc-262">TransactionDate</span></span>  
51. <span data-ttu-id="06efc-263">Velg Dato i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="06efc-264">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-264">Click Add.</span></span>
53. <span data-ttu-id="06efc-265">Angi Transaksjonsdato i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="06efc-266">Transaksjonsdato</span><span class="sxs-lookup"><span data-stu-id="06efc-266">Transaction date</span></span>  
54. <span data-ttu-id="06efc-267">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="06efc-268">Skriv inn InstructedAmount i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="06efc-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="06efc-269">InstructedAmount</span></span>  
56. <span data-ttu-id="06efc-270">Velg Faktisk i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="06efc-271">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-271">Click Add.</span></span>
58. <span data-ttu-id="06efc-272">I Beskrivelse-feltet angir du Beløpet som skal flyttes mellom debitor og kreditor før fradrag av tillegg.</span><span class="sxs-lookup"><span data-stu-id="06efc-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="06efc-273">Beløpet bør uttrykkes i valutaen som er bestilt av den første parten.</span><span class="sxs-lookup"><span data-stu-id="06efc-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="06efc-274">Beløpet som skal flyttes mellom debitor og kreditor før fradrag av tillegg.</span><span class="sxs-lookup"><span data-stu-id="06efc-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="06efc-275">Beløpet bør uttrykkes i valutaen som er bestilt av den første parten.</span><span class="sxs-lookup"><span data-stu-id="06efc-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="06efc-276">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="06efc-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="06efc-277">I Navn-feltet skriver du inn End2EndID.</span><span class="sxs-lookup"><span data-stu-id="06efc-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="06efc-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="06efc-278">End2EndID</span></span>  
61. <span data-ttu-id="06efc-279">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="06efc-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="06efc-280">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="06efc-280">Click Add.</span></span>
63. <span data-ttu-id="06efc-281">I Beskrivelse-feltet skriver du Den unike identifikasjonen som er tilordnet av initialiseringsparten.</span><span class="sxs-lookup"><span data-stu-id="06efc-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="06efc-282">Denne identifikasjonen sendes, forblir uendret, gjennom hele kjeden ende-til-ende.</span><span class="sxs-lookup"><span data-stu-id="06efc-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="06efc-283">Den unike identifikasjonen som er tilordnet av initialiseringsparten.</span><span class="sxs-lookup"><span data-stu-id="06efc-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="06efc-284">Denne identifikasjonen sendes, forblir uendret, gjennom hele kjeden ende-til-ende.</span><span class="sxs-lookup"><span data-stu-id="06efc-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="06efc-285">Skriv inn PaymentModel i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="06efc-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="06efc-286">Navnet på PaymentModel justerer med forhåndsdefinerte grensesnitt for betalingsskjemaer.</span><span class="sxs-lookup"><span data-stu-id="06efc-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="06efc-287">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="06efc-287">Click Save.</span></span>
66. <span data-ttu-id="06efc-288">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="06efc-288">Close the page.</span></span>


