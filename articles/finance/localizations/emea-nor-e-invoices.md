---
title: Elektroniske fakturaer for kunde i Norge
description: Dette emnet forklarer hvordan du konfigurerer og elektroniske fakturaer for kunder i Norge.
author: ilkond
manager: AnnBe
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: ilyako
ms.search.validFrom: 2019-11-01
ms.dyn365.ops.version: 10.0.08
ms.openlocfilehash: dca356b38c5ef61bf6719a698ad1ebbab7143e56
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002884"
---
# <a name="customer-electronic-invoices-in-norway"></a><span data-ttu-id="86f2d-103">Elektroniske fakturaer for kunde i Norge</span><span class="sxs-lookup"><span data-stu-id="86f2d-103">Customer electronic invoices in Norway</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86f2d-104">For å oppnå samsvar med EU-direktiv 2014/55/EU har formatet **EHF Billing 3.0** for elektroniske fakturaer som gjelder spesifikt for Norge, blitt implementert basert på spesifikasjonen [PEPPOL Billing 3.0](https://docs.peppol.eu/poacc/billing/3.0/).</span><span class="sxs-lookup"><span data-stu-id="86f2d-104">For compliance with European Union Directive 2014/55/EU, the Norway-specific **EHF Billing 3.0** format for electronic invoices has been implemented based on the [PEPPOL Billing 3.0](https://docs.peppol.eu/poacc/billing/3.0/) specification.</span></span>

<span data-ttu-id="86f2d-105">Dette emnet inneholder informasjon om hvordan du konfigurerer og utsteder elektroniske fakturaer i Norge.</span><span class="sxs-lookup"><span data-stu-id="86f2d-105">This topic provides information about how to configure and issue customer electronic invoices in Norway.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="86f2d-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="86f2d-106">Prerequisites</span></span>

<span data-ttu-id="86f2d-107">Primæradressen for den juridiske enheten må være i Norge.</span><span class="sxs-lookup"><span data-stu-id="86f2d-107">The primary address of the legal entity must be in Norway.</span></span>

## <a name="import-electronic-reporting-configurations"></a><span data-ttu-id="86f2d-108">Importere konfigurasjoner for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="86f2d-108">Import Electronic reporting configurations</span></span>

<span data-ttu-id="86f2d-109">I arbeidsområdet **Elektronisk rapportering** importerer du følgende ER-formater (elektronisk rapportering) fra repositoriet:</span><span class="sxs-lookup"><span data-stu-id="86f2d-109">In the **Electronic reporting** workspace, import the following Electronic reporting (ER) formats from the repository:</span></span>

- <span data-ttu-id="86f2d-110">OIOUBL Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="86f2d-110">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="86f2d-111">OIOUBL Prosjektfaktura</span><span class="sxs-lookup"><span data-stu-id="86f2d-111">OIOUBL Project invoice</span></span>
- <span data-ttu-id="86f2d-112">OIOUBL Salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="86f2d-112">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="86f2d-113">OIOUBL Prosjektkreditnota</span><span class="sxs-lookup"><span data-stu-id="86f2d-113">OIOUBL Project credit note</span></span>

> [!NOTE]
> <span data-ttu-id="86f2d-114">Disse formatene er basert på konfigurasjonen **Fakturamodell** og bruker konfigurasjonen **Fakturamodelltilordning**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-114">These formats are based on the **Invoice model** configuration and use the **Invoice model mapping** configuration.</span></span> <span data-ttu-id="86f2d-115">Alle nødvendige tilleggskonfigurasjoner importeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="86f2d-115">All required additional configurations are automatically imported.</span></span>

<span data-ttu-id="86f2d-116">Hvis du vil ha mer informasjon om hvordan du importerer ER-konfigurasjoner, kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="86f2d-116">For more information about how to import ER configurations, see [Download Electronic reporting configurations from Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>

### <a name="reference-the-imported-er-format-configurations"></a><span data-ttu-id="86f2d-117">Referere til de importerte ER-formatkonfigurasjonene</span><span class="sxs-lookup"><span data-stu-id="86f2d-117">Reference the imported ER format configurations</span></span>

1. <span data-ttu-id="86f2d-118">Gå til **Kunder** \> **Oppsett** \> **Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="86f2d-119">Velg de importerte formatene for elektroniske dokumenter i hurtigfanen **Elektronisk rapportering** i fanen **Elektroniske dokumenter**:</span><span class="sxs-lookup"><span data-stu-id="86f2d-119">On the **Electronic documents** tab, on the **Electronic reporting** FastTab, select the imported formats for electronic documents:</span></span>

    - <span data-ttu-id="86f2d-120">**Salgs- og fritekstfaktura:** OIOUBL Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="86f2d-120">**Sales and Free text invoice:** OIOUBL Sales invoice</span></span>
    - <span data-ttu-id="86f2d-121">**Salgs- og fritekstkreditnota:** OIOUBL Salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="86f2d-121">**Sales and Free text credit note:** OIOUBL Sales credit note</span></span>
    - <span data-ttu-id="86f2d-122">**Prosjektfaktura:** OIOUBL Prosjektfaktura</span><span class="sxs-lookup"><span data-stu-id="86f2d-122">**Project invoice:** OIOUBL Project invoice</span></span>
    - <span data-ttu-id="86f2d-123">**Prosjektkreditnota:** OIOUBL Prosjektkreditnota</span><span class="sxs-lookup"><span data-stu-id="86f2d-123">**Project credit note:** OIOUBL Project credit note</span></span>

![Formater for elektroniske dokumenter](media/emea-nor-ger-configs.jpg)

## <a name="configure-parameters"></a><span data-ttu-id="86f2d-125">Konfigurere parametere</span><span class="sxs-lookup"><span data-stu-id="86f2d-125">Configure parameters</span></span>

### <a name="configure-legal-entity-parameters"></a><span data-ttu-id="86f2d-126">Konfigurere parametere for juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="86f2d-126">Configure legal entity parameters</span></span>

1. <span data-ttu-id="86f2d-127">Gå til **Organisasjonsstyring** \> **Organisasjoner** \> **Juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-127">Go to **Organization administration** \> **Organizations** \> **Legal entities**.</span></span>
2. <span data-ttu-id="86f2d-128">I feltet **Mva-nummer** i hurtigfanen **Avgiftsregistrering** angir du mva-nummeret for firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="86f2d-128">On the **Tax registration** FastTab, in the **Tax registration number** field, enter the company's value-added tax (VAT) number.</span></span>
3. <span data-ttu-id="86f2d-129">I hurtigfanen **Registreringsnumre** setter du alternativet **Skriv ut Foretaksregisteret på salgsdokumenter** for Norge til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-129">On the **Registration numbers** FastTab, set the **Print Foretaksregisteret on sales documents** option for Norway to **Yes**.</span></span>
4. <span data-ttu-id="86f2d-130">Angi firmaets organisasjonsnummeret i **Registreringsnummer**-feltet i hurtigfanen **Bankkontoinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-130">On the **Bank account information** FastTab, in the **Routing number** field, enter the company's organization number.</span></span>
5. <span data-ttu-id="86f2d-131">I **Bankkonto**-feltet angir du firmaets bankkontonummer.</span><span class="sxs-lookup"><span data-stu-id="86f2d-131">In the **Bank account** field, enter the company's bank account number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86f2d-132">Firmaets bankkonto må allerede være opprettet i **Kontant- og bankbehandling** \> **Bankkontoer** \> **Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-132">The company bank account must already be set up at **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>

### <a name="configure-customer-parameters"></a><span data-ttu-id="86f2d-133">Konfigurere kundeparametere</span><span class="sxs-lookup"><span data-stu-id="86f2d-133">Configure customer parameters</span></span>

1. <span data-ttu-id="86f2d-134">Gå til **Kunder** \> **Kunder** \> **Alle kunder**, og velg en kunde.</span><span class="sxs-lookup"><span data-stu-id="86f2d-134">Go to **Accounts receivable** \> **Customers** \> **All customers**, and select a customer.</span></span>
2. <span data-ttu-id="86f2d-135">I hurtigfanen **Faktura og levering** setter du alternativet **eFaktura** til **Ja** for å aktivere generering av elektroniske fakturaer.</span><span class="sxs-lookup"><span data-stu-id="86f2d-135">On the **Invoice and delivery** FastTab, set the **eInvoice** option to **Yes** to enable electronic invoices to be generated.</span></span>
3. <span data-ttu-id="86f2d-136">Sett alternativet **Vedlegg til eFaktura** til **Ja** for å legge en PDF-kopi av den utskrivbare fakturaen ved den elektroniske fakturaen.</span><span class="sxs-lookup"><span data-stu-id="86f2d-136">Set the **eInvoice attachment** option to **Yes** to attach a PDF copy of the printable invoice to the electronic invoice.</span></span>
4. <span data-ttu-id="86f2d-137">I feltet **Avgiftsfritaksnummer** skriver du inn kundens MVA-fritaksnummer.</span><span class="sxs-lookup"><span data-stu-id="86f2d-137">In the **Tax exempt number** field, enter the customer's VAT exempt number.</span></span>

![Kundeparametere](media/emea-nor-ger-customer.jpg)

### <a name="units-of-measure-configuration"></a><span data-ttu-id="86f2d-139">Konfigurasjon av måleenheter</span><span class="sxs-lookup"><span data-stu-id="86f2d-139">Units of measure configuration</span></span>

1. <span data-ttu-id="86f2d-140">Gå til **Organisasjonsstyring** \> **Oppsett** \> **Enheter** \> **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-140">Go to **Organization administration** \> **Setup** \> **Units** \> **Units**.</span></span>
2. <span data-ttu-id="86f2d-141">Velg en enhets-ID i listen, og velg deretter **Eksterne koder**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-141">Select a unit ID in the list, and then select **External codes**.</span></span>
3. <span data-ttu-id="86f2d-142">I **Kode**-feltet i **Oversikt**-delen på siden **Eksterne koder** angir du en kode som svarer til den valgte enhets-ID-en.</span><span class="sxs-lookup"><span data-stu-id="86f2d-142">On the **External codes** page, in the **Overview** section, in the **Code** field, enter a code that corresponds to the selected unit ID.</span></span>
4. <span data-ttu-id="86f2d-143">I **Verdi**-feltet i **Verdi**-delen angir du den eksterne koden som skal brukes som enhetskode for internasjonal handel.</span><span class="sxs-lookup"><span data-stu-id="86f2d-143">In **Value** section, in **Value** field, enter the external code that should be used as the units of measure code for international trade.</span></span> <span data-ttu-id="86f2d-144">Denne koden anbefales av [FNs økonomiske kommisjon for Europa (UNECE)](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNECERec20/).</span><span class="sxs-lookup"><span data-stu-id="86f2d-144">This code is recommended by the [United Nations Economic Commission for Europe (UN/ECE)](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNECERec20/).</span></span>

![Konfigurasjon av måleenheter](media/emea-nor-ger-units.jpg)

### <a name="sales-tax-codes-transformation"></a><span data-ttu-id="86f2d-146">Transformasjon av mva-koder</span><span class="sxs-lookup"><span data-stu-id="86f2d-146">Sales tax codes transformation</span></span>

<span data-ttu-id="86f2d-147">Når du genererer elektroniske fakturaer, blir satsene for mva-koder analysert og transformert til [kategorier som samsvarer med UNCL5305](https://docs.peppol.eu/pracc/catalogue/1.0/codelist/UNCL5305/).</span><span class="sxs-lookup"><span data-stu-id="86f2d-147">When you generate electronic invoices, the sales tax code rates are analyzed and transformed into [UNCL5305-compliant categories](https://docs.peppol.eu/pracc/catalogue/1.0/codelist/UNCL5305/).</span></span> <span data-ttu-id="86f2d-148">Følgende logikk brukes:</span><span class="sxs-lookup"><span data-stu-id="86f2d-148">The following logic is used:</span></span>

- <span data-ttu-id="86f2d-149">Når det gjelder alle avgiftssatser som ikke er null, brukes **S**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="86f2d-149">For all non-zero tax rates, the **S** category is used.</span></span>
- <span data-ttu-id="86f2d-150">Når det gjelder alle nullavgiftssatser, brukes enten kategorien **E** eller **Z**, avhengig av hvilken rapporteringskode som er konfigurert for avgiftsfritt salg.</span><span class="sxs-lookup"><span data-stu-id="86f2d-150">For all zero tax rates, either the **E** category or the **Z** category is used, depending on the reporting code that is configured for tax-free sales.</span></span>

### <a name="customer-requisition"></a><span data-ttu-id="86f2d-151">Kunderekvisisjon</span><span class="sxs-lookup"><span data-stu-id="86f2d-151">Customer requisition</span></span>

<span data-ttu-id="86f2d-152">Når du registrerer fritekstfakturaer, fakturaer som er basert på salgsordrer, eller prosjektfakturaer, må du angi en kunderekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="86f2d-152">When you register free text invoices, invoices that are based on sales orders, or project invoices, you must enter a customer requisition.</span></span> <span data-ttu-id="86f2d-153">Du kan også legge til en valgfri kundereferanse.</span><span class="sxs-lookup"><span data-stu-id="86f2d-153">You can also add an optional customer reference.</span></span>

#### <a name="free-text-invoices"></a><span data-ttu-id="86f2d-154">Fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="86f2d-154">Free text invoices</span></span>

1. <span data-ttu-id="86f2d-155">Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-155">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="86f2d-156">Opprett en ny faktura, eller velg en eksisterende faktura.</span><span class="sxs-lookup"><span data-stu-id="86f2d-156">Create a new invoice, or select an existing invoice.</span></span>
3. <span data-ttu-id="86f2d-157">I **Referanser**-delen i hurtigfanen **Kunde** i **Hode**-visningen angir du verdier i feltene **Kunderekvisisjon** og **Kundereferanse**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-157">In the **Header** view, on the **Customer** FastTab, in the **References** section, enter values in the **Customer requisition** and **Customer reference** fields.</span></span>

#### <a name="sales-orders"></a><span data-ttu-id="86f2d-158">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="86f2d-158">Sales orders</span></span>

1. <span data-ttu-id="86f2d-159">Gå til **Kunder** \> **Ordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-159">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="86f2d-160">Opprett en ny salgsordre, eller velg en eksisterende salgsordre.</span><span class="sxs-lookup"><span data-stu-id="86f2d-160">Create a new sales order, or select an existing sales order.</span></span> 
3. <span data-ttu-id="86f2d-161">I **Referanser**-delen i hurtigfanen **Generelt** i **Hode**-visningen angir du verdier i feltene **Kunderekvisisjon** og **Kundereferanse**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-161">In the **Header** view, on the **General** FastTab, in the **References** section, enter values in the **Customer requisition** and **Customer reference** fields.</span></span>

#### <a name="project-invoices"></a><span data-ttu-id="86f2d-162">Prosjektfakturaer</span><span class="sxs-lookup"><span data-stu-id="86f2d-162">Project invoices</span></span>

1. <span data-ttu-id="86f2d-163">Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-163">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="86f2d-164">Opprett en prosjektkontrakt, eller velg en eksisterende prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="86f2d-164">Create a new project contract, or select an existing project contract.</span></span>
3. <span data-ttu-id="86f2d-165">I hurtigfanen **Finansieringskilder** velger eller oppretter du en finansieringskilde av typen **Kunde**, og deretter velger du **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-165">On **Funding sources** FastTab, select or create a funding source of the **Customer** type, and then select **Details**.</span></span>

    ![Finansieringskilder](media/emea-nor-ger-proj-contracts.jpg)

4. <span data-ttu-id="86f2d-167">I **Referanser**-delen i hurtigfanen **Andre** på siden **Finansieringskildedetaljer** angir du standardverdier for kontrakten i feltene **Kunderekvisisjon** og **Kundereferanse**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-167">On the **Funding source details** page, on the **Other** FastTab, in **References** section, in the **Customer requisition** and **Customer reference** fields, enter default values for the contract.</span></span> <span data-ttu-id="86f2d-168">Du kan også angi prosjektspesifikke verdier i de tilsvarende feltene i hurtigfanen **E-faktura**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-168">Alternatively, you can enter project-specific values in the corresponding fields on the **E-invoice** FastTab.</span></span>

    ![Prosjektreferanser](media/emea-nor-ger-proj-refs.jpg)

5. <span data-ttu-id="86f2d-170">Følg denne fremgangsmåten for å angi verdier for kunderekvisisjon og referanse direkte på prosjektfakturaforslaget:</span><span class="sxs-lookup"><span data-stu-id="86f2d-170">To enter customer requisition and reference values directly on the project invoice proposal, follow these steps:</span></span>

    1. <span data-ttu-id="86f2d-171">Gå til **Prosjektstyring og regnskap** \> **Prosjektfakturaer** \> **Fakturaforslag for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-171">Go to **Project management and accounting** \> **Projects invoices** \> **Project invoice proposals**.</span></span>
    2. <span data-ttu-id="86f2d-172">Opprett et nytt fakturaforslag, eller velg et eksisterende fakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="86f2d-172">Create a new invoice proposal, or select an existing invoice proposal.</span></span>
    3. <span data-ttu-id="86f2d-173">I **E-faktura**-delen i hurtigfanen **Hode for fakturaforslag** angir du verdier i feltene **Kunderekvisisjon** og **Kundereferanse**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-173">On the **Invoice proposal header** FastTab, in the **e-Invoice** section, enter values in **Customer requisition** and **Customer reference** fields.</span></span>

    ![Prosjektforslag](media/emea-nor-ger-proj-prop.jpg)

### <a name="customer-accounting-code-registration"></a><span data-ttu-id="86f2d-175">Registrering av kunderegnskapskode</span><span class="sxs-lookup"><span data-stu-id="86f2d-175">Customer accounting code registration</span></span>

<span data-ttu-id="86f2d-176">Du kan registrere kunderegnskapskoder når du arbeider med fritekstfakturaer, fakturaer som er basert på salgsordrer, eller prosjektfakturaer.</span><span class="sxs-lookup"><span data-stu-id="86f2d-176">You can enter customer accounting codes when you work with free text invoices, invoices that are based on sales orders, or project invoices.</span></span>

#### <a name="free-text-invoices"></a><span data-ttu-id="86f2d-177">Fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="86f2d-177">Free text invoices</span></span>

1. <span data-ttu-id="86f2d-178">Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-178">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="86f2d-179">Opprett en ny faktura, eller velg en eksisterende faktura.</span><span class="sxs-lookup"><span data-stu-id="86f2d-179">Create a new invoice, or select an existing invoice.</span></span> 
3. <span data-ttu-id="86f2d-180">I feltet **Dimensjonskonto** i **E-faktura**-delen i hurtigfanen **Generelt** i **Hode**-visningen angir du regnskapskoden for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="86f2d-180">In the **Header** view, on the **General** FastTab, in the **e-Invoice** section, in the **Dimension account** field, enter the accounting code for the invoice.</span></span> 
4. <span data-ttu-id="86f2d-181">Hvis du vil ha en separat regnskapskode for hver fakturalinje, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="86f2d-181">To have a separate accounting code for each invoice line, follow these steps:</span></span>

    1. <span data-ttu-id="86f2d-182">Sett alternativet **Linjespesifikk** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-182">Set the **Line-specific** option to **Yes**.</span></span>
    2. <span data-ttu-id="86f2d-183">Gå til **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="86f2d-183">Switch to the **Lines** view.</span></span>
    3. <span data-ttu-id="86f2d-184">I **Dimensjonskonto**-feltet i fanen **Generelt** i hurtigfanen **Linjedetaljer** angir du en linjebestemt regnskapskode for hver fakturalinje.</span><span class="sxs-lookup"><span data-stu-id="86f2d-184">On the **Line details** FastTab, on the **General** tab, in the **Dimension account** field, enter a line-specific accounting code for each invoice line.</span></span>

    ![Linjebestemt regnskapskode for en fritekstfaktura](media/emea-nor-ger-fti-cost.jpg)

#### <a name="sales-orders"></a><span data-ttu-id="86f2d-186">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="86f2d-186">Sales orders</span></span>

1. <span data-ttu-id="86f2d-187">Gå til **Kunder** \> **Ordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-187">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="86f2d-188">Opprett en ny salgsordre, eller velg en eksisterende salgsordre.</span><span class="sxs-lookup"><span data-stu-id="86f2d-188">Create a new sales order, or select an existing sales order.</span></span>
3. <span data-ttu-id="86f2d-189">I feltet **Dimensjonskonto** i **E-faktura**-delen i hurtigfanen **Generelt** i **Hode**-visningen angir du regnskapskoden for ordren.</span><span class="sxs-lookup"><span data-stu-id="86f2d-189">In the **Header** view, on the **General** FastTab, in the **e-Invoice** section, in the **Dimension account** field, enter the accounting code for the order.</span></span>
4. <span data-ttu-id="86f2d-190">Hvis du vil ha en separat regnskapskode for hver ordrelinje, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="86f2d-190">To have a separate accounting code for each order line, follow these steps:</span></span>

    1. <span data-ttu-id="86f2d-191">Sett alternativet **Linjespesifikk** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-191">Set the **Line-specific** option to **Yes**.</span></span>
    2. <span data-ttu-id="86f2d-192">Gå til **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="86f2d-192">Switch to the **Lines** view.</span></span>
    3. <span data-ttu-id="86f2d-193">I **Dimensjonskonto**-feltet i fanen **Generelt** i hurtigfanen **Linjedetaljer** angir du en linjebestemt regnskapskode for hver ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="86f2d-193">On the **Line details** FastTab, on the **General** tab, in the **Dimension account** field, enter a line-specific accounting code for each order line.</span></span>

#### <a name="project-invoices"></a><span data-ttu-id="86f2d-194">Prosjektfakturaer</span><span class="sxs-lookup"><span data-stu-id="86f2d-194">Project invoices</span></span>

1. <span data-ttu-id="86f2d-195">Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-195">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="86f2d-196">Opprett en prosjektkontrakt, eller velg en eksisterende prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="86f2d-196">Create a new project contract, or select an existing project contract.</span></span>
3. <span data-ttu-id="86f2d-197">I hurtigfanen **Finansieringskilder** oppretter eller velger du en finansieringskilde av typen **Kunde**, og deretter velger du **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-197">On **Funding sources** FastTab, create or select a funding source of the **Customer** type, and then select **Details**.</span></span>
4. <span data-ttu-id="86f2d-198">I **Dimensjonskonto**-feltet i hurtigfanen **E-faktura** på siden **Finansieringskildedetaljer** angir du den prosjektspesifikke standard regnskapskoden.</span><span class="sxs-lookup"><span data-stu-id="86f2d-198">On **Funding source details** page, on the **E-invoice** FastTab, in the **Dimension account** field, enter the project-specific default accounting code.</span></span>

    ![Prosjektspesifikk regnskapskode](media/emea-nor-ger-proj-cost.jpg)

5. <span data-ttu-id="86f2d-200">Hvis du vil angi kunderegnskapskoder direkte i prosjektfakturaforslag, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="86f2d-200">To enter customer accounting codes directly in project invoice proposals, follow these steps:</span></span>

    1. <span data-ttu-id="86f2d-201">Gå til **Prosjektstyring og regnskap** \> **Prosjektfakturaer** \> **Fakturaforslag for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-201">Go to **Project management and accounting** \> **Projects invoices** \> **Project invoice proposals**.</span></span>
    2. <span data-ttu-id="86f2d-202">Opprett et nytt fakturaforslag, eller velg et eksisterende fakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="86f2d-202">Create a new invoice proposal, or select an existing invoice proposal.</span></span>
    3. <span data-ttu-id="86f2d-203">I feltet **Dimensjonskonto** i **E-faktura**-delen i hurtigfanen **Generelt** i Hode-visningen angir du regnskapskoden for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="86f2d-203">On the **Invoice proposal header** FastTab, in the **e-Invoice** section, in the **Dimension account** field, enter the accounting code.</span></span>

6. <span data-ttu-id="86f2d-204">Hvis du vil ha en separat regnskapskode for hver transaksjonslinje, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="86f2d-204">To have a separate accounting code for each transaction line, follow these steps:</span></span>

    1. <span data-ttu-id="86f2d-205">Sett alternativet **Linjespesifikk** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-205">Set the **Line-specific** option to **Yes**.</span></span>
    2. <span data-ttu-id="86f2d-206">I **Dimensjonskonto**-feltet i hurtigfanen **Transaksjoner for fakturaforslag** angir du en linjebestemt regnskapskode for hver transaksjonslinje.</span><span class="sxs-lookup"><span data-stu-id="86f2d-206">On the **Invoice proposal transactions** FastTab, in the **Dimension account** field, enter a line-specific accounting code for each transaction line.</span></span>

    ![Transaksjonslinjebestemt regnskapskode](media/emea-nor-ger-proj-prop-cost.jpg)

## <a name="export-customer-electronic-invoices"></a><span data-ttu-id="86f2d-208">Eksportere elektroniske fakturaer for kunde</span><span class="sxs-lookup"><span data-stu-id="86f2d-208">Export customer electronic invoices</span></span>

### <a name="send-e-invoices"></a><span data-ttu-id="86f2d-209">Sende e-fakturaer</span><span class="sxs-lookup"><span data-stu-id="86f2d-209">Send e-invoices</span></span>

<span data-ttu-id="86f2d-210">Når en faktura posteres, kan du generere en elektronisk faktura ved å velge **Send** \> **Original** for den valgte fakturaen.</span><span class="sxs-lookup"><span data-stu-id="86f2d-210">When an invoice is posted, you can generate an electronic invoice by selecting **Send** \> **Original** for the selected invoice.</span></span>

![Sende en e-faktura](media/emea-nor-ger-einvoice.jpg)

### <a name="view-e-invoices"></a><span data-ttu-id="86f2d-212">Vise e-fakturaer</span><span class="sxs-lookup"><span data-stu-id="86f2d-212">View e-invoices</span></span>

<span data-ttu-id="86f2d-213">Hvis du vil spørre om XML-filene for elektroniske fakturaer som er generert, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="86f2d-213">To inquire about the XML files of electronic invoices that have been generated, follow these steps.</span></span>

1. <span data-ttu-id="86f2d-214">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjobber**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-214">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>
2. <span data-ttu-id="86f2d-215">Velg en jobb, og velg deretter **Vis filer**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-215">Select a job, and then select **Show files**.</span></span>

    ![Vis filer-knappen](media/emea-nor-ger-einvoice-open.jpg)

3. <span data-ttu-id="86f2d-217">Velg **Åpne** for å laste ned filen som inneholder den elektroniske fakturaen.</span><span class="sxs-lookup"><span data-stu-id="86f2d-217">Select **Open** to download the file that contains the electronic invoice.</span></span>

<span data-ttu-id="86f2d-218">Hvis generering av de elektroniske fakturaene mislykkes på grunn av feil, velger du **Vis logg** \> **Meldingsdetaljer** for å vise flere detaljer om feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="86f2d-218">If generation of the electronic invoices fails because of errors, select **Show log** \> **Message details** to view more details about the error message.</span></span>

![Meldingsdetaljer](media/emea-nor-ger-einvoice-log.jpg)

### <a name="send-e-invoices-to-er-destinations"></a><span data-ttu-id="86f2d-220">Sende e-fakturaer til ER-mål</span><span class="sxs-lookup"><span data-stu-id="86f2d-220">Send e-invoices to ER destinations</span></span>

<span data-ttu-id="86f2d-221">Du kan konfigurere ER-målene for elektroniske fakturaformater.</span><span class="sxs-lookup"><span data-stu-id="86f2d-221">You can set up ER destinations for electronic invoice formats.</span></span> <span data-ttu-id="86f2d-222">I dette tilfellet blir utdata-XML-filer som inneholder elektroniske fakturaer, automatisk sendt til de definerte målene like etter at fakturaene er postert.</span><span class="sxs-lookup"><span data-stu-id="86f2d-222">In this case, output XML files that contain electronic invoices will automatically be sent to the defined destinations immediately after the invoices are posted.</span></span> <span data-ttu-id="86f2d-223">Når du posterer fakturaene, må du aktivere parameteren **Skriv ut faktura**.</span><span class="sxs-lookup"><span data-stu-id="86f2d-223">When you post the invoices, you must turn on the **Print invoice** parameter.</span></span>

<span data-ttu-id="86f2d-224">Hvis du vil ha mer informasjon om hvordan du konfigurerer ER-mål, kan du se [Mål for elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="86f2d-224">For more information about ER destinations, see [Electronic reporting destinations](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-destinations.md).</span></span>
