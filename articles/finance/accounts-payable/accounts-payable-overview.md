---
title: Oversikt over å konfigurere leverandør
description: Denne artikkelen beskriver sidene du bruker til å definer grunnleggende og valgfrie funksjoner for leverandører. Den beskriver også trinnene i oppsettet som du må fullføre før du begynner å definere leverandører.
author: abruer
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0edc2fcbde536e98fa3ce3567c2c8fdf3fc864ad
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188788"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="0e0c3-104">Oversikt over å konfigurere leverandør</span><span class="sxs-lookup"><span data-stu-id="0e0c3-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e0c3-105">Denne artikkelen beskriver sidene du bruker til å definer grunnleggende og valgfrie funksjoner for leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="0e0c3-106">Den beskriver også trinnene i oppsettet som du må fullføre før du begynner å definere leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

## <a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="0e0c3-107">Forutsetninger for oppsett av Leverandører</span><span class="sxs-lookup"><span data-stu-id="0e0c3-107">Prerequisites for Accounts payable setup</span></span>

<span data-ttu-id="0e0c3-108">Før du kan konfigurere Leverandører må du fullføre følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="0e0c3-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="0e0c3-109">I Økonomimodul:</span><span class="sxs-lookup"><span data-stu-id="0e0c3-109">In General ledger:</span></span>
    -   <span data-ttu-id="0e0c3-110">Hvis du planlegger bruk av betalingsjournaler, må du konfigurere betalingsjournaler.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="0e0c3-111">Hvis du planlegger å kjøre kursjusteringer, må du konfigurere valutakoder på siden Valutaer, konfigurere valutakurstyper på siden Valutakurstyper og konfigurere valutakurser på siden Valutakurser.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="0e0c3-112">I Kontant- og bankbetaling definerer du bankkontoer som skal brukes med betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="0e0c3-113">Konfigurasjonssider for Leverandører</span><span class="sxs-lookup"><span data-stu-id="0e0c3-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="0e0c3-114">Bruk de følgende sidene til å sette opp den grunnleggende funksjonaliteten i Leverandører for hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="0e0c3-115">Sidene vises i rekkefølgen som anbefales for oppsett.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="0e0c3-116">Du kan gjøre oppsettet enklere ved å opprette maler fra de første postene som opprettes.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="0e0c3-117">I en mal angis verdiene vanligvis i mange felt for å reflektere funksjonene som organisasjonen ønsker å implementere for en bestemt type leverandør.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="0e0c3-118">På siden Betalingsbetingelser definerer du betalingsbetingelsene du tilordner til salgsordrer, bestillinger, kunder og leverandører, og som bestemmer forfallsdatoer for fakturaers.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="0e0c3-119">Hvis du vil ha mer informasjon, kan du se [Definere leverandørbetalingsgebyrer](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="0e0c3-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="0e0c3-120">På siden Betalingsmåter - leverandører oppretter og vedlikeholder du informasjon om hvordan organisasjonen betaler sine leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="0e0c3-121">På siden Leverandørgrupper oppretter og vedlikeholder du grupper av leverandører som deler viktige parametere for postering, utligning og betaling, rapportering og prognoser.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="0e0c3-122">På siden Leverandørposteringsprofiler angir du hvordan leverandørtransaksjoner posteres til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="0e0c3-123">På siden Leverandørparametere angir du standardinnstillinger som brukes hvis ingen bestemt innstilling er angitt, parametere for forskjellige typer funksjonalitet og de ulike nummerseriene for Leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="0e0c3-124">På siden Skjemaoppsett definerer du formatet for forskjellige dokumenter som er knyttet til leverandører, og som firmaet bruker til å holde oversikt over mottak fra leverandører og til å registrere årsaker til betalingsflyten til leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="0e0c3-125">På siden leverandører oppretter og vedlikeholder du leverandørkontoer, og skattemyndighetene som organisasjonen din rapporterer merverdiavgift til.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="0e0c3-126">Valgfrie sider for leverandøroppsett</span><span class="sxs-lookup"><span data-stu-id="0e0c3-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="0e0c3-127">I tillegg til den grunnleggende funksjonaliteten har Leverandører andre funksjoner som du kan definere.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="0e0c3-128">De ekstra oppsettssidene organiseres etter funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="0e0c3-129">**Policyer**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-129">**Policies**</span></span>
-   <span data-ttu-id="0e0c3-130">På siden Leverandørfakturapolicy angir du leverandørfakturapolicyer.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="0e0c3-131">**Fakturakontroll**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-131">**Invoice matching**</span></span>

-   <span data-ttu-id="0e0c3-132">På siden Toleranse for fakturatotaler definerer du toleranser for fakturatotaler.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="0e0c3-133">Angi toveis og treveis kontrollpolicyer på Kontrollpolicy-siden.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="0e0c3-134">På siden Pristoleranser definerer du toleranser for enhetspriser.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="0e0c3-135">Angi toleransegrupper for varepriser på siden Pristoleransegrupper for vare.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="0e0c3-136">Angi toleransegrupper for leverandørpriser på siden Pristoleransegrupper for leverandør.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="0e0c3-137">På siden Toleranser for tillegg definerer du toleranser for tillegg.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="0e0c3-138">**Arbeidsflyt**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-138">**Workflow**</span></span>

-   <span data-ttu-id="0e0c3-139">På siden Arbeidsflyter for leverandørreskontro definerer du arbeidsflytkonfigurasjoner for journalgodkjenninger og innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="0e0c3-140">**Årsaker**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-140">**Reasons**</span></span>

-   <span data-ttu-id="0e0c3-141">På siden Leverandørårsaker definerer du årsakskoder.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="0e0c3-142">**Tillegg**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-142">**Charges**</span></span>

-   <span data-ttu-id="0e0c3-143">På siden Tilleggskode definerer du koder for tilleggene som skal brukes i bestillinger.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="0e0c3-144">På siden Leverandørtilleggsgruppe oppretter og vedlikeholder du tilleggsgrupper for leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="0e0c3-145">På siden Varetilleggsgrupper  oppretter og vedlikeholder du tilleggsgrupper for varer.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="0e0c3-146">På Automatiske gebyrer-siden definerer du gebyrene som tilordnes ordrer automatisk.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="0e0c3-147">**Tilleggsvarer**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-147">**Supplementary items**</span></span>

-   <span data-ttu-id="0e0c3-148">På Tilleggsvaregrupper - Leverandør -siden oppretter og vedlikeholder du tilleggsvaregrupper for leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="0e0c3-149">På Tilleggsvaregrupper - Lager -siden oppretter og vedlikeholder du tilleggsvaregrupper for varer.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="0e0c3-150">**Distribusjon**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-150">**Distribution**</span></span>

-   <span data-ttu-id="0e0c3-151">På Leveringsbetingelser-siden oppretter og vedlikeholder du betingelsene for en vares overføring fra selger til kjøper.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="0e0c3-152">På Leveringsmåter-siden oppretter og vedlikeholder du transportmåtene som brukes ved levering av en ordre fra selgeren til kjøperen.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="0e0c3-153">På Fraktsone-siden oppretter og vedlikeholder du identifikatorer og beskrivelser av mottaksadresser.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="0e0c3-154">**Skjemaer**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-154">**Forms**</span></span>

-   <span data-ttu-id="0e0c3-155">På Skjemamerknader-siden oppretter du standardteksten som skal vises på forskjellige sider.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="0e0c3-156">På Skjemasorteringsparametere-siden definerer du sorteringsrekkefølgen for rekvisisjoner, mottakslister, følgesedler og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="0e0c3-157">På Oppsett for utskriftsbehandling-siden definerer du utskriftsbehandlingsinformasjon for originaler og kopier av sider.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="0e0c3-158">**Betalinger**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-158">**Payments**</span></span>

-   <span data-ttu-id="0e0c3-159">På Kontantrabatt-siden definerer og administrer du betingelsene for å oppnå kontantrabatter.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="0e0c3-160">Kontantrabattkodene er knyttet til leverandører, og brukes på bestillinger.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="0e0c3-161">På Betalingsplaner-siden definerer du betalingsplaner som brukes til å administrere avdragsbetalinger til leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="0e0c3-162">På Betalingsdager-siden definerer du betalingsdagene som skal brukes til beregning av forfallsdager, og angir betalingsdager for en bestemt dag i uken eller måneden.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="0e0c3-163">På Betalingsgebyr-siden oppretter og vedlikeholder du betalingsgebyrer som er knyttet til leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="0e0c3-164">På Betalingsinstruksjon-siden oppretter og vedlikeholder du betalingsinstruksjoner.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="0e0c3-165">**Statistikk**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-165">**Statistics**</span></span>

-   <span data-ttu-id="0e0c3-166">På Definisjoner av aldersfordelingsperiode-siden setter du opp brukerdefinerte intervaller som brukes til å analysere modenhetsdistribusjon for leverandørkontoer.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="0e0c3-167">På Bransje-siden oppretter du bransjekoder (LOB) som er tilordnet til leverandører.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="0e0c3-168">**1099-avgift**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-168">**Tax 1099**</span></span>

-   <span data-ttu-id="0e0c3-169">På **1099-felt**-siden kontrollerer og oppdaterer du minimumsbeløpene som må rapporteres til det amerikanske skattevesenet, Internal Revenue Service (IRS), basert på de nyeste IRS-kravene.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="0e0c3-170">**Valgfritt oppsett for andre moduler**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="0e0c3-171">**Organisasjonsstyring**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-171">**Organization administration**</span></span>

-   <span data-ttu-id="0e0c3-172">På Nummerserier-siden definerer du nummerseriegrupper for fakturanumre.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="0e0c3-173">På de følgende sidene definerer du adresseinformasjon:</span><span class="sxs-lookup"><span data-stu-id="0e0c3-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="0e0c3-174">Adresseoppsett</span><span class="sxs-lookup"><span data-stu-id="0e0c3-174">Address setup</span></span>
    -   <span data-ttu-id="0e0c3-175">NAF-koder</span><span class="sxs-lookup"><span data-stu-id="0e0c3-175">NAF codes</span></span>
    -   <span data-ttu-id="0e0c3-176">Import av postnumre</span><span class="sxs-lookup"><span data-stu-id="0e0c3-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="0e0c3-177">**Økonomi**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-177">**General ledger**</span></span>

-   <span data-ttu-id="0e0c3-178">På Finansdimensjoner-siden definerer du finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="0e0c3-179">På de følgende sidene definerer du avgiftsinformasjon:</span><span class="sxs-lookup"><span data-stu-id="0e0c3-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="0e0c3-180">Mva-koder</span><span class="sxs-lookup"><span data-stu-id="0e0c3-180">Sales tax codes</span></span>
    -   <span data-ttu-id="0e0c3-181">Mva-grupper</span><span class="sxs-lookup"><span data-stu-id="0e0c3-181">Sales tax groups</span></span>
    -   <span data-ttu-id="0e0c3-182">Vare, mva-grupper</span><span class="sxs-lookup"><span data-stu-id="0e0c3-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="0e0c3-183">Kontogruppe</span><span class="sxs-lookup"><span data-stu-id="0e0c3-183">Account group</span></span>
    -   <span data-ttu-id="0e0c3-184">Mva-fritakskoder</span><span class="sxs-lookup"><span data-stu-id="0e0c3-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="0e0c3-185">Mva-jurisdiksjoner</span><span class="sxs-lookup"><span data-stu-id="0e0c3-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="0e0c3-186">Skattemyndigheter</span><span class="sxs-lookup"><span data-stu-id="0e0c3-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="0e0c3-187">Mva-utligningsperioder</span><span class="sxs-lookup"><span data-stu-id="0e0c3-187">Sales tax settlement periods</span></span>

<span data-ttu-id="0e0c3-188">**Kontant- og bankbehandling**</span><span class="sxs-lookup"><span data-stu-id="0e0c3-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="0e0c3-189">På siden Koder for betalingsformål definerer du sentralbankens formålskode.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]