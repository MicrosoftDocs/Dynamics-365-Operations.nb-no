---
title: Standard revisjonsfil for avgift (SAF-T) for Norge
description: Dette emnet forklarer hvordan du setter opp og generere standard revisjonsfil for avgift (SAF-T) for juridiske enheter som har en primær postadresse i Norge.
author: LizaGolub
ms.author: v-elgolu
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
manager: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Norway
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c5f3d5c7f4f2fb01027450dbb6545c86eb6a6723
ms.sourcegitcommit: c1101d34299c189c30287e034d389da213ca9878
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2921139"
---
# <a name="standard-audit-file-for-tax-saf-t-for-norway"></a><span data-ttu-id="eac09-103">Standard revisjonsfil for avgift (SAF-T) for Norge</span><span class="sxs-lookup"><span data-stu-id="eac09-103">Standard Audit File for Tax (SAF-T) for Norway</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eac09-104">Dette emnet inneholder landsspesifikk informasjon om hvordan du setter opp standard revisjonsfil for avgift (SAF-T) for juridiske enheter som har en primæradresse i Norge.</span><span class="sxs-lookup"><span data-stu-id="eac09-104">This topic includes country-specific information about how to set up the Standard Audit File for Tax (SAF-T) for legal entities that have their primary address in Norway.</span></span>

## <a name="introduction"></a><span data-ttu-id="eac09-105">Innledning</span><span class="sxs-lookup"><span data-stu-id="eac09-105">Introduction</span></span>

<span data-ttu-id="eac09-106">Fra og med januar 2020 er alle selskaper i Norge pålagt av Skatteetaten å gi SAF-T finansielle data.</span><span class="sxs-lookup"><span data-stu-id="eac09-106">Beginning January 2020, all companies in Norway are required by the Norwegian Tax Administration to provide SAF-T Financial data.</span></span> <span data-ttu-id="eac09-107">Dette kravet er i samsvar med versjon 1.4 av dokumentasjonen, som ble publisert den 8. juli 2019, og versjon 1.3 av den tekniske dokumentasjonen, som ble publisert den 23. mars 2018, i form av en XML-rapport.</span><span class="sxs-lookup"><span data-stu-id="eac09-107">This requirement is in accordance with version 1.4 of the documentation, which was published on July 8, 2019, and version 1.3 of the technical documentation, which was published on March 23, 2018, in the form of an XML report.</span></span> <span data-ttu-id="eac09-108">Publiseringen av disse delene av dokumentasjonen sammenfaller med versjon 1.1 av "norsk SAF-T økonomiske data" XML Schema Definition (XSD)-skjema som ble utviklet av SAF-T-arbeidsgruppen, Skatteetaten, og basert på "OECD-standard revisjonsfil - Avgifter 2.00,"som ble modifisert 2. februar 2018.</span><span class="sxs-lookup"><span data-stu-id="eac09-108">The publication of these pieces of documentation coincided with version 1.1 of the "Norwegian SAF-T Financial data" XML Schema Definition (XSD) schema that was developed by the SAF-T Working group, Skatteetaten, and based on "OECD Standard Audit File - Taxation 2.00," which was modified on February 2, 2018.</span></span>

## <a name="overview"></a><span data-ttu-id="eac09-109">Oversikt</span><span class="sxs-lookup"><span data-stu-id="eac09-109">Overview</span></span>

<span data-ttu-id="eac09-110">For å støtte rapporten **Norsk SAF-T økonomiske data** må Microsoft Dynamics 365 Finance-programmet være en av følgende versjoner eller senere.</span><span class="sxs-lookup"><span data-stu-id="eac09-110">To support the **Norwegian SAF-T Financial data** report, your Microsoft Dynamics 365 Finance application must be one of the following versions or later.</span></span>

| <span data-ttu-id="eac09-111">Versjon av Finance</span><span class="sxs-lookup"><span data-stu-id="eac09-111">Version of Finance</span></span> | <span data-ttu-id="eac09-112">Build-nummer</span><span class="sxs-lookup"><span data-stu-id="eac09-112">Build number</span></span>       |
|--------------------|--------------------|
| <span data-ttu-id="eac09-113">10.0.6</span><span class="sxs-lookup"><span data-stu-id="eac09-113">10.0.6</span></span>             | <span data-ttu-id="eac09-114">10.0.234.**20020**</span><span class="sxs-lookup"><span data-stu-id="eac09-114">10.0.234.**20020**</span></span> |
| <span data-ttu-id="eac09-115">10.0.7</span><span class="sxs-lookup"><span data-stu-id="eac09-115">10.0.7</span></span>             | <span data-ttu-id="eac09-116">10.0.283.**10012**</span><span class="sxs-lookup"><span data-stu-id="eac09-116">10.0.283.**10012**</span></span> |
| <span data-ttu-id="eac09-117">10.0.8</span><span class="sxs-lookup"><span data-stu-id="eac09-117">10.0.8</span></span>             | <span data-ttu-id="eac09-118">10.0.319.**12**</span><span class="sxs-lookup"><span data-stu-id="eac09-118">10.0.319.**12**</span></span>    |
| <span data-ttu-id="eac09-119">10.0.9</span><span class="sxs-lookup"><span data-stu-id="eac09-119">10.0.9</span></span>             | <span data-ttu-id="eac09-120">10.0.328.**20020**</span><span class="sxs-lookup"><span data-stu-id="eac09-120">10.0.328.**20020**</span></span> |

<span data-ttu-id="eac09-121">Når Finance-programversjonen er egnet, importerer du følgende versjoner eller senere av disse konfigurasjonene for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="eac09-121">When your Finance application version is suitable, import the following versions or later of these Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

| <span data-ttu-id="eac09-122">ER-konfigurasjonsnavn</span><span class="sxs-lookup"><span data-stu-id="eac09-122">ER configuration name</span></span>              | <span data-ttu-id="eac09-123">Konfigurasjonstype</span><span class="sxs-lookup"><span data-stu-id="eac09-123">Configuration type</span></span> | <span data-ttu-id="eac09-124">Versjon</span><span class="sxs-lookup"><span data-stu-id="eac09-124">Version</span></span> |
|------------------------------------|--------------------|---------|
| <span data-ttu-id="eac09-125">Standard revisjonsfil (SAF-T)</span><span class="sxs-lookup"><span data-stu-id="eac09-125">Standard Audit File (SAF-T)</span></span>        | <span data-ttu-id="eac09-126">Modell</span><span class="sxs-lookup"><span data-stu-id="eac09-126">Model</span></span>              | <span data-ttu-id="eac09-127">32</span><span class="sxs-lookup"><span data-stu-id="eac09-127">32</span></span>      |
| <span data-ttu-id="eac09-128">SAF-T økonomiske datamodelltilordning</span><span class="sxs-lookup"><span data-stu-id="eac09-128">SAF-T Financial data model mapping</span></span> | <span data-ttu-id="eac09-129">Modelltilordning</span><span class="sxs-lookup"><span data-stu-id="eac09-129">Model mapping</span></span>      | <span data-ttu-id="eac09-130">32.30</span><span class="sxs-lookup"><span data-stu-id="eac09-130">32.30</span></span>   |
| <span data-ttu-id="eac09-131">SAF-T-format (NO)</span><span class="sxs-lookup"><span data-stu-id="eac09-131">SAF-T Format (NO)</span></span>                  | <span data-ttu-id="eac09-132">Format (eksport)</span><span class="sxs-lookup"><span data-stu-id="eac09-132">Format (exporting)</span></span> | <span data-ttu-id="eac09-133">32.41</span><span class="sxs-lookup"><span data-stu-id="eac09-133">32.41</span></span>   |

<span data-ttu-id="eac09-134">Importer de nyeste versjonene av konfigurasjonene.</span><span class="sxs-lookup"><span data-stu-id="eac09-134">Import the latest versions of the configurations.</span></span> <span data-ttu-id="eac09-135">Versjonsbeskrivelsen inneholder vanligvis nummeret til Microsoft Knowledge Base-artikkelen (KB) som forklarer endringene som konfigurasjonsversjonen introduserte.</span><span class="sxs-lookup"><span data-stu-id="eac09-135">The version description usually includes the number of the Microsoft Knowledge Base (KB) article that explains the changes that the configuration version introduced.</span></span>

> [!NOTE]
> <span data-ttu-id="eac09-136">Når du er ferdig med å importere alle ER-konfigurasjoner fra tabellen ovenfor, kan du angi alternativet **Standard for modelltilordning** til **Ja** for konfigurasjonen **SAF-T økonomiske datamodelltilordning**.</span><span class="sxs-lookup"><span data-stu-id="eac09-136">After you've finished importing all the ER configurations from the preceding table, set the **Default for model mapping** option to **Yes** for the **SAF-T Financial data model mapping** configuration.</span></span>
>
> ![Standardalternativ for modelltilordning er satt til Ja](media/nor-saf-default-model-mapping.jpg)

<span data-ttu-id="eac09-138">Hvis du vil ha mer informasjon om hvordan du laster ned ER-konfigurasjoner fra LCS, se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="eac09-138">For more information about how to download ER configurations from LCS, see [Download Electronic reporting configurations from Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>

## <a name="setup"></a><span data-ttu-id="eac09-139">Oppsett</span><span class="sxs-lookup"><span data-stu-id="eac09-139">Setup</span></span>

<span data-ttu-id="eac09-140">Hvis du vil begynne å bruke rapporten **Norsk SAF-T økonomiske data** i Finance, må du fullføre følgende oppsett:</span><span class="sxs-lookup"><span data-stu-id="eac09-140">To start to use the **Norwegian SAF-T Financial data** report in Finance, you must complete the following setup:</span></span>

- <span data-ttu-id="eac09-141">**Parametere for økonomimodul:** Definer ER-formatet på siden **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="eac09-141">**General ledger parameters:** Set up the ER format on the **General ledgers parameters** page.</span></span>
- <span data-ttu-id="eac09-142">**Mva-koder:** Knytt mva-koder til norske standard mva-koder for merverdiavgift (mva.).</span><span class="sxs-lookup"><span data-stu-id="eac09-142">**Sales tax codes:** Associate sales tax codes with Norwegian standard value-added tax (VAT) tax codes.</span></span>
- <span data-ttu-id="eac09-143">**Hovedkontoer:** Knytt hovedkontoer til norske standardkontoer.</span><span class="sxs-lookup"><span data-stu-id="eac09-143">**Main accounts:** Associate main accounts with Norwegian standard accounts.</span></span>

<span data-ttu-id="eac09-144">Delene nedenfor forklarer hvordan du gjør hver del av dette oppsettet.</span><span class="sxs-lookup"><span data-stu-id="eac09-144">The following sections explain how to do each part of this setup.</span></span>

### <a name="general-ledger-parameters"></a><span data-ttu-id="eac09-145">Parametere for økonomimodul</span><span class="sxs-lookup"><span data-stu-id="eac09-145">General ledger parameters</span></span>

1. <span data-ttu-id="eac09-146">I Finance går du til **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="eac09-146">In Finance, go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="eac09-147">På siden **Parametere for økonomimodul**, i kategorien **Standard revisjonsfil for avgift (SAF-T)** i feltet **Standard revisjonsfil for avgift (SAF-T)**, velger du **SAF-T-format (NO)**.</span><span class="sxs-lookup"><span data-stu-id="eac09-147">On the **General ledger parameters** page, on the **Standard Audit File for Tax (SAF-T)** tab, in the **Standard Audit File for Tax (SAF-T)** field, select **SAF-T Format (NO)**.</span></span>

![Feltet Standard revisjonsfil for avgift (SAF-T) på siden parametere for økonomimodul](media/nor-saf-gl-parameters.jpg)

### <a name="sales-tax-codes"></a><span data-ttu-id="eac09-149">Mva-koder</span><span class="sxs-lookup"><span data-stu-id="eac09-149">Sales tax codes</span></span>

<span data-ttu-id="eac09-150">Som dokumentasjonen forklarer, i Norsk SAF-T økonomiske data, må mva-koder som brukes i Finance, være knyttet til norske standard mva-koder (\<StandardTaxCode\>) for SAF-T-rapportering.</span><span class="sxs-lookup"><span data-stu-id="eac09-150">As the documentation explains, in Norwegian SAF-T Financial data, sales tax codes that are used in Finance must be associated with Norwegian standard VAT tax codes (\<StandardTaxCode\>) for the purpose of SAF-T reporting.</span></span> <span data-ttu-id="eac09-151">Norske standard mva-koder er tilgjengelige på <https://github.com/Skatteetaten/saf-t>.</span><span class="sxs-lookup"><span data-stu-id="eac09-151">The Norwegian standard VAT tax codes are available at <https://github.com/Skatteetaten/saf-t>.</span></span>

<span data-ttu-id="eac09-152">Hvis du vil knytte mva-koder som brukes i Finance, med norske standard mva-koder, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="eac09-152">To associate sales tax codes that are used in Finance with Norwegian standard VAT tax codes, follow these steps.</span></span>

1. <span data-ttu-id="eac09-153">I Finance går du til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.</span><span class="sxs-lookup"><span data-stu-id="eac09-153">In Finance, go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="eac09-154">På siden **Mva-kode** velger du **Mva-kode**-posten, og deretter, på handlingsruten i kategorien **Mva-kode** i gruppen **Mva-kode**, velger du **Eksterne koder**.</span><span class="sxs-lookup"><span data-stu-id="eac09-154">On the **Sales tax code** page, select the **Sales tax code** record, and then, on the Action Pane, on the **Sales tax code** tab, in the **Sales tax code** group, select **External codes**.</span></span>

    ![Eksterne koder-knappen i handlingsruten på siden for mva-kode](media/nor-saf-standard-tax-codes.jpg)

3. <span data-ttu-id="eac09-156">På **Eksterne koder**-siden angir du norske standard mva-koder som skal brukes for den valgte posten for mva-koden, for SAF-T-rapportering.</span><span class="sxs-lookup"><span data-stu-id="eac09-156">On the **External codes** page, specify the Norwegian standard VAT tax codes that should be used for the selected sales tax code record for the purpose of SAF-T reporting.</span></span>

### <a name="main-accounts"></a><span data-ttu-id="eac09-157">Hovedkontoer</span><span class="sxs-lookup"><span data-stu-id="eac09-157">Main accounts</span></span>

<span data-ttu-id="eac09-158">Som dokumentasjonen forklarer, i Norsk SAF-T økonomiske data, må hovedkontoer som brukes i Finance, være knyttet til norske standardkontoer for SAF-T-rapportering.</span><span class="sxs-lookup"><span data-stu-id="eac09-158">As the documentation explains, in Norwegian SAF-T Financial data, main accounts that are used in Finance must be associated with Norwegian standard accounts for the purpose of SAF-T reporting.</span></span> <span data-ttu-id="eac09-159">Norske standardkontoer er tilgjengelige på <https://github.com/Skatteetaten/saf-t>.</span><span class="sxs-lookup"><span data-stu-id="eac09-159">The Norwegian standard accounts are available at <https://github.com/Skatteetaten/saf-t>.</span></span>

<span data-ttu-id="eac09-160">Hvis du vil knytte hovedkontoer som brukes i Finance, med norske standardkontoer, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="eac09-160">To associate main accounts that are used in Finance with Norwegian standard accounts, follow these steps.</span></span>

1. <span data-ttu-id="eac09-161">I Finance går du til **Økonomimodul** \> **Kontoplan** \> **Kontoer** \> **Hovedkontoer**.</span><span class="sxs-lookup"><span data-stu-id="eac09-161">In Finance, go to **General ledger** \> **Chart of accounts** \> **Accounts** \> **Main accounts**.</span></span>
2. <span data-ttu-id="eac09-162">På siden **Hovedkontoer** velger du **Hovedkonto**-oppføringen, og deretter velger du **Rediger**i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eac09-162">On the **Main accounts** page, select the **Main account** record, and then, on the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="eac09-163">På hurtigfanen **Generelt**, i delen **Standard finanskonto** i feltet **Standardkonto**, velger du **Standardkonto**.</span><span class="sxs-lookup"><span data-stu-id="eac09-163">On the **General** FastTab, in the **Standard general ledger account** section, in the **Standard account** field, select **Standard account**.</span></span>

![Standardkonto-feltet på siden Hovedkontoer](media/nor-saf-standard-main-accounts.jpg)

<span data-ttu-id="eac09-165">Du må definere alle standardkontoene på siden **Standard finanskontoer** før du kan velge dem for en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="eac09-165">You must define all the standard accounts on the **Standard general ledger accounts** page before you can select them for a main account.</span></span> <span data-ttu-id="eac09-166">Hvis du vil ha rask tilgang til siden **Standard finanskontoer** fra siden **Hovedkontoer**, høyreklikker du **Standardkonto**-feltet, og deretter velger du **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="eac09-166">To quickly access the **Standard general ledger accounts** page from the **Main accounts** page, right-click the **Standard account** field, and then select **View details**.</span></span>

![Kommandoen Vis detaljer på hurtigmenyen for feltet Standardkonto](media/nor-saf-standard-main-account-setup.jpg)

## <a name="generate-the-norwegian-saf-t-financial-data-report"></a><span data-ttu-id="eac09-168">Generer rapporten Norsk SAF-T økonomiske data</span><span class="sxs-lookup"><span data-stu-id="eac09-168">Generate the Norwegian SAF-T Financial data report</span></span>

<span data-ttu-id="eac09-169">Hvis du vil generere rapporten **Norsk SAF-T økonomiske data**, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="eac09-169">To generate the **Norwegian SAF-T Financial data** report, follow these steps.</span></span>

1. <span data-ttu-id="eac09-170">I Finance går du til **Økonomimodul** \> **Forespørsler og rapporter** \> **Standard revisjonsfil for avgift (SAF-T)** \> **Standard revisjonsfil for avgift (SAF-T)**.</span><span class="sxs-lookup"><span data-stu-id="eac09-170">In Finance, go to **General ledger** \> **Inquiries and reports** \> **Standard Audit File for Tax (SAF-T)** \> **Standard Audit File for Tax (SAF-T)**.</span></span>
2. <span data-ttu-id="eac09-171">Angi start- og sluttdatoene for perioden du vil generere rapporten for, i **Fra dato**- og **Til dato**-feltene i dialogboksen for rapporten.</span><span class="sxs-lookup"><span data-stu-id="eac09-171">In the dialog box for the report, in the **From date** and **To date** fields, specify the start and end dates of the period that you want to generate the report for.</span></span>
3. <span data-ttu-id="eac09-172">Merk av for **Kunder**, **Leverandører** og **Finansdimensjoner** for å ta med alle postene fra de relaterte tabellene i rapporten.</span><span class="sxs-lookup"><span data-stu-id="eac09-172">Select the check boxes for **Customers**, **Vendors**, and **Financial dimensions** to include all the records from the related tables on the report.</span></span>

    <span data-ttu-id="eac09-173">Hvis det ikke er merket av for **Kunder** og **Leverandører**, vil rapporten bare inkludere kunder og leverandører i firmaet som det var transaksjoner for i rapporteringsperioden, og kunder og leverandører som har en saldo som ikke er null.</span><span class="sxs-lookup"><span data-stu-id="eac09-173">If the **Customers** and **Vendors** check boxes are cleared, the report will include only those customers and vendors of your company that there were transactions for in the reporting period, and customers and vendors that have a non-zero balance.</span></span>
    
    <span data-ttu-id="eac09-174">Hvis det ikke er merket av for **Finansdimensjoner**, vil bare finansdimensjonene som ble brukt i transaksjoner i løpet av rapporteringsperioden, rapporteres i **\<MasterFiles\>**-noden i rapporten.</span><span class="sxs-lookup"><span data-stu-id="eac09-174">If the **Financial dimensions** check box is cleared, only those financial dimensions that were used in transactions during the reporting period will be reported in the **\<MasterFiles\>** node of the report.</span></span>

4. <span data-ttu-id="eac09-175">I feltet **Personalnummer** velger du en ansatt for å legge til den ansatte i **\<Bruker-ID\>**-noden i rapporten.</span><span class="sxs-lookup"><span data-stu-id="eac09-175">In the **Personnel number** field, select an employee to add the employee to the **\<UserID\>** node of the report.</span></span> <span data-ttu-id="eac09-176">Denne noden rapporterer IDen til brukeren som genererte revisjonsfilen.</span><span class="sxs-lookup"><span data-stu-id="eac09-176">This node reports the ID of the user who generated the audit file.</span></span>

<span data-ttu-id="eac09-177">Du kan også bruke filtre for feltene **Hovedkontoer** og **Oppføring i økonomijournal** ved hjelp av hurtigfanen **Poster som skal inkluderes** i dialogboksen for rapporten.</span><span class="sxs-lookup"><span data-stu-id="eac09-177">You can also apply filters for the **Main accounts** and **General journal entry** fields by using **Records to include** FastTab in the dialog box for the report.</span></span>

## <a name="report-naming-and-splitting"></a><span data-ttu-id="eac09-178">Navngivning og oppdeling av rapporter</span><span class="sxs-lookup"><span data-stu-id="eac09-178">Report naming and splitting</span></span>

<span data-ttu-id="eac09-179">Dokumentasjonen for norske SAF-T økonomiske data krever følgende navngivingsstruktur for XML-rapportene som genereres:</span><span class="sxs-lookup"><span data-stu-id="eac09-179">The documentation for Norwegian SAF-T Financial data requires the following naming structure for the XML reports that are generated:</span></span>

<span data-ttu-id="eac09-180">\<SAF-T-eksporttype\>\_\<organisasjonsnummer for leverandøren som dataene representerer\>\_\<dato og klokkeslett (ååååmmddtt24tmise\>\_\<filnummer for totalt antall filer\>.xml</span><span class="sxs-lookup"><span data-stu-id="eac09-180">\<SAF-T export type\>\_\<organization number of the vendor that the data represents\>\_\<date and time(yyyymmddhh24hmise\>\_\<file number of total files\>.xml</span></span> 

<span data-ttu-id="eac09-181">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="eac09-181">Here is an example:</span></span>

<span data-ttu-id="eac09-182">SAF-T Financial\_999999999\_20160401235911\_1\_12.xml</span><span class="sxs-lookup"><span data-stu-id="eac09-182">SAF-T Financial\_999999999\_20160401235911\_1\_12.xml</span></span>

<span data-ttu-id="eac09-183">Her er en forklaring på delene av dette filnavnet:</span><span class="sxs-lookup"><span data-stu-id="eac09-183">Here is an explanation of the parts of this file name:</span></span>

- <span data-ttu-id="eac09-184">**SAF-T Financial** angir SAF-T-typen fil.</span><span class="sxs-lookup"><span data-stu-id="eac09-184">**SAF-T Financial** states the SAF-T type of file.</span></span>
- <span data-ttu-id="eac09-185">**999999999** representerer organisasjonsnummeret som tilhører eieren av dataene.</span><span class="sxs-lookup"><span data-stu-id="eac09-185">**999999999** represents the organization number that belongs to the owner of the data.</span></span>
- <span data-ttu-id="eac09-186">**20160401235911** representerer datoen og klokkeslettet da filen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="eac09-186">**20160401235911** represents the date and time when the file was created.</span></span> <span data-ttu-id="eac09-187">(En 24-timers klokke brukes for klokkeslettet.)</span><span class="sxs-lookup"><span data-stu-id="eac09-187">(A 24-hour clock is used for the time.)</span></span>
- <span data-ttu-id="eac09-188">**1\_12** representerer fil 1 av 12 totalt antall filer i eksporten (det vil si i samme valg).</span><span class="sxs-lookup"><span data-stu-id="eac09-188">**1\_12** represents file 1 out of 12 total files in the export (that is, in the same selection).</span></span>

<span data-ttu-id="eac09-189">Volumet til en enkelt XML-fil må være mindre enn 2 gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="eac09-189">The volume of a single XML file must be less than 2 gigabytes (GB).</span></span> <span data-ttu-id="eac09-190">Hver enkelt XML-fil som sendes, må valideres mot skjemaet.</span><span class="sxs-lookup"><span data-stu-id="eac09-190">Every individual XML file that is submitted must be validated against the schema.</span></span> <span data-ttu-id="eac09-191">Alle \<MasterFiles\>-noder må være i den første filen, og de tilknyttede transaksjonene må være i de påfølgende filene (antallet av disse filene er fleksibelt).</span><span class="sxs-lookup"><span data-stu-id="eac09-191">All \<MasterFiles\> nodes must be in the first file, and the associated transactions must be in the subsequent files (the number of these files is flexible).</span></span>

<span data-ttu-id="eac09-192">Tabellen nedenfor viser et eksempelutvalg av ett regnskapsår som har 12 perioder.</span><span class="sxs-lookup"><span data-stu-id="eac09-192">The following table shows a sample selection of one accounting year that has 12 periods.</span></span> <span data-ttu-id="eac09-193">For hver periode er det én fil som inneholder transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="eac09-193">For each period, there is one file that contains transactions.</span></span>

| <span data-ttu-id="eac09-194">Filnummer</span><span class="sxs-lookup"><span data-stu-id="eac09-194">File number</span></span> | <span data-ttu-id="eac09-195">Innhold i revisjonsfilen</span><span class="sxs-lookup"><span data-stu-id="eac09-195">Contents of the audit file</span></span>                     |
|-------------|------------------------------------------------|
| <span data-ttu-id="eac09-196">1</span><span class="sxs-lookup"><span data-stu-id="eac09-196">1</span></span>           | <span data-ttu-id="eac09-197">\<Topptekst\> og \<MasterFiles\>-noder</span><span class="sxs-lookup"><span data-stu-id="eac09-197">\<Header\> and \<MasterFiles\> nodes</span></span>           |
| <span data-ttu-id="eac09-198">2–13</span><span class="sxs-lookup"><span data-stu-id="eac09-198">2–13</span></span>        | <span data-ttu-id="eac09-199">\<Topptekst\> og \<GeneralLedgerEntries\>-noder</span><span class="sxs-lookup"><span data-stu-id="eac09-199">\<Header\> and \<GeneralLedgerEntries\> nodes</span></span>  |

<span data-ttu-id="eac09-200">Det kan være maksimalt 10 XML-filer i samme zip-arkiv.</span><span class="sxs-lookup"><span data-stu-id="eac09-200">There can be a maximum of 10 XML files in the same zip archive.</span></span>

<span data-ttu-id="eac09-201">I samsvar med disse kravene er ER-formatet **SAF-T-format (NO)** implementert for å automatisk dele den resulterende rapporten i XML-format, basert på følgende forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="eac09-201">In accordance with these requirements, the **SAF-T Format (NO)** ER format is implemented to automatically split the resulting report in XML format, based on the following assumptions:</span></span>

- <span data-ttu-id="eac09-202">Det maksimale volumet for den resulterende XML-rapporten er 2 000 000 kilobyte (kB) (det vil si 2 GB).</span><span class="sxs-lookup"><span data-stu-id="eac09-202">The maximum volume of the resulting XML report is 2,000,000 kilobytes (KB) (that is, 2 GB).</span></span>
- <span data-ttu-id="eac09-203">Alle XML-filene bruker følgende navngivningsstruktur:</span><span class="sxs-lookup"><span data-stu-id="eac09-203">All the XML files use the following naming structure:</span></span>

    <span data-ttu-id="eac09-204">\<SAF-T-eksporttype\>\_\<organisasjonsnummer for leverandøren som dataene representerer\>\_\<dato og klokkeslett(ååååmmddtt24tmise\></span><span class="sxs-lookup"><span data-stu-id="eac09-204">\<SAF-T export type\>\_\<organization number of the vendor that the data represents\>\_\<date and time(yyyymmddhh24hmise\></span></span>

- <span data-ttu-id="eac09-205">Alle XML-filer er inkludert i ett zip-arkiv.</span><span class="sxs-lookup"><span data-stu-id="eac09-205">All the XML files are included in one zip archive.</span></span>
- <span data-ttu-id="eac09-206">Hver enkelt XML-fil valideres mot skjemaet.</span><span class="sxs-lookup"><span data-stu-id="eac09-206">Each individual XML file is validated against the schema.</span></span>

<span data-ttu-id="eac09-207">Når rapporten er generert, hvis det genereres mer enn én XML-fil, må brukeren manuelt nummerere de genererte filene i zip-arkivet ved å legge til **\_\<filnummeret for totalt antall filer\>** i filnavnene.</span><span class="sxs-lookup"><span data-stu-id="eac09-207">After the report is generated, if more than one XML file is generated, the user must manually number the generated files in the zip archive by adding **\_\<file number of total files\>** to the file names.</span></span> <span data-ttu-id="eac09-208">Brukeren må likeledes sikre at det ikke mer enn 10 XML-filer i det samme zip-arkivet.</span><span class="sxs-lookup"><span data-stu-id="eac09-208">The user must also make sure that there are no more than 10 XML files in the same zip archive.</span></span> <span data-ttu-id="eac09-209">Hvis det er mer enn 10 XML-filer i et arkiv, må brukeren manuelt dele det opp i flere arkiver, som hver har maksimalt 10 XML-filer.</span><span class="sxs-lookup"><span data-stu-id="eac09-209">If there are more than 10 XML files in an archive, the user must manually split it into several archives, each of which has a maximum of 10 XML files.</span></span>
