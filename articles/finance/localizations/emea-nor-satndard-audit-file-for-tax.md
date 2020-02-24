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
ms.openlocfilehash: d4147632ccaf490bbfa75faab777f900782c26f4
ms.sourcegitcommit: de715b7fda2f1548f2f443b9e0f6d09f5b881d61
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2020
ms.locfileid: "3033930"
---
# <a name="standard-audit-file-for-tax-saf-t-for-norway"></a><span data-ttu-id="e6ef7-103">Standard revisjonsfil for avgift (SAF-T) for Norge</span><span class="sxs-lookup"><span data-stu-id="e6ef7-103">Standard Audit File for Tax (SAF-T) for Norway</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6ef7-104">Dette emnet inneholder landsspesifikk informasjon om hvordan du setter opp standard revisjonsfil for avgift (SAF-T) for juridiske enheter som har en primæradresse i Norge.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-104">This topic includes country-specific information about how to set up the Standard Audit File for Tax (SAF-T) for legal entities that have their primary address in Norway.</span></span>

## <a name="introduction"></a><span data-ttu-id="e6ef7-105">Innledning</span><span class="sxs-lookup"><span data-stu-id="e6ef7-105">Introduction</span></span>

<span data-ttu-id="e6ef7-106">Fra og med januar 2020 er alle selskaper i Norge pålagt av Skatteetaten å gi SAF-T finansielle data.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-106">Beginning January 2020, all companies in Norway are required by the Norwegian Tax Administration to provide SAF-T Financial data.</span></span> <span data-ttu-id="e6ef7-107">Dette kravet er i samsvar med versjon 1.4 av dokumentasjonen, som ble publisert den 8. juli 2019, og versjon 1.3 av den tekniske dokumentasjonen, som ble publisert den 23. mars 2018, i form av en XML-rapport.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-107">This requirement is in accordance with version 1.4 of the documentation, which was published on July 8, 2019, and version 1.3 of the technical documentation, which was published on March 23, 2018, in the form of an XML report.</span></span> <span data-ttu-id="e6ef7-108">Publiseringen av disse delene av dokumentasjonen sammenfaller med versjon 1.1 av "norsk SAF-T økonomiske data" XML Schema Definition (XSD)-skjema som ble utviklet av SAF-T-arbeidsgruppen, Skatteetaten, og basert på "OECD-standard revisjonsfil - Avgifter 2.00,"som ble modifisert 2. februar 2018.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-108">The publication of these pieces of documentation coincided with version 1.1 of the "Norwegian SAF-T Financial data" XML Schema Definition (XSD) schema that was developed by the SAF-T Working group, Skatteetaten, and based on "OECD Standard Audit File - Taxation 2.00," which was modified on February 2, 2018.</span></span>

## <a name="overview"></a><span data-ttu-id="e6ef7-109">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e6ef7-109">Overview</span></span>

<span data-ttu-id="e6ef7-110">For å støtte rapporten **Norsk SAF-T økonomiske data** må Microsoft Dynamics 365 Finance-programmet være en av følgende versjoner eller senere.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-110">To support the **Norwegian SAF-T Financial data** report, your Microsoft Dynamics 365 Finance application must be one of the following versions or later.</span></span>

| <span data-ttu-id="e6ef7-111">Versjon av Finance</span><span class="sxs-lookup"><span data-stu-id="e6ef7-111">Version of Finance</span></span> | <span data-ttu-id="e6ef7-112">Build-nummer</span><span class="sxs-lookup"><span data-stu-id="e6ef7-112">Build number</span></span>       |
|--------------------|--------------------|
| <span data-ttu-id="e6ef7-113">10.0.6</span><span class="sxs-lookup"><span data-stu-id="e6ef7-113">10.0.6</span></span>             | <span data-ttu-id="e6ef7-114">10.0.234.**20020**</span><span class="sxs-lookup"><span data-stu-id="e6ef7-114">10.0.234.**20020**</span></span> |
| <span data-ttu-id="e6ef7-115">10.0.7</span><span class="sxs-lookup"><span data-stu-id="e6ef7-115">10.0.7</span></span>             | <span data-ttu-id="e6ef7-116">10.0.283.**10012**</span><span class="sxs-lookup"><span data-stu-id="e6ef7-116">10.0.283.**10012**</span></span> |
| <span data-ttu-id="e6ef7-117">10.0.8</span><span class="sxs-lookup"><span data-stu-id="e6ef7-117">10.0.8</span></span>             | <span data-ttu-id="e6ef7-118">10.0.319.**12**</span><span class="sxs-lookup"><span data-stu-id="e6ef7-118">10.0.319.**12**</span></span>    |
| <span data-ttu-id="e6ef7-119">10.0.9</span><span class="sxs-lookup"><span data-stu-id="e6ef7-119">10.0.9</span></span>             | <span data-ttu-id="e6ef7-120">10.0.328.**20020**</span><span class="sxs-lookup"><span data-stu-id="e6ef7-120">10.0.328.**20020**</span></span> |

<span data-ttu-id="e6ef7-121">Når Finance-programversjonen er egnet, importerer du følgende versjoner eller senere av disse konfigurasjonene for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e6ef7-121">When your Finance application version is suitable, import the following versions or later of these Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

| <span data-ttu-id="e6ef7-122">ER-konfigurasjonsnavn</span><span class="sxs-lookup"><span data-stu-id="e6ef7-122">ER configuration name</span></span>              | <span data-ttu-id="e6ef7-123">Konfigurasjonstype</span><span class="sxs-lookup"><span data-stu-id="e6ef7-123">Configuration type</span></span> | <span data-ttu-id="e6ef7-124">Versjon</span><span class="sxs-lookup"><span data-stu-id="e6ef7-124">Version</span></span> |
|------------------------------------|--------------------|---------|
| <span data-ttu-id="e6ef7-125">Standard revisjonsfil (SAF-T)</span><span class="sxs-lookup"><span data-stu-id="e6ef7-125">Standard Audit File (SAF-T)</span></span>        | <span data-ttu-id="e6ef7-126">Modell</span><span class="sxs-lookup"><span data-stu-id="e6ef7-126">Model</span></span>              | <span data-ttu-id="e6ef7-127">32</span><span class="sxs-lookup"><span data-stu-id="e6ef7-127">32</span></span>      |
| <span data-ttu-id="e6ef7-128">SAF-T økonomiske datamodelltilordning</span><span class="sxs-lookup"><span data-stu-id="e6ef7-128">SAF-T Financial data model mapping</span></span> | <span data-ttu-id="e6ef7-129">Modelltilordning</span><span class="sxs-lookup"><span data-stu-id="e6ef7-129">Model mapping</span></span>      | <span data-ttu-id="e6ef7-130">32.30</span><span class="sxs-lookup"><span data-stu-id="e6ef7-130">32.30</span></span>   |
| <span data-ttu-id="e6ef7-131">SAF-T-format (NO)</span><span class="sxs-lookup"><span data-stu-id="e6ef7-131">SAF-T Format (NO)</span></span>                  | <span data-ttu-id="e6ef7-132">Format (eksport)</span><span class="sxs-lookup"><span data-stu-id="e6ef7-132">Format (exporting)</span></span> | <span data-ttu-id="e6ef7-133">32.41</span><span class="sxs-lookup"><span data-stu-id="e6ef7-133">32.41</span></span>   |

<span data-ttu-id="e6ef7-134">Importer de nyeste versjonene av konfigurasjonene.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-134">Import the latest versions of the configurations.</span></span> <span data-ttu-id="e6ef7-135">Versjonsbeskrivelsen inneholder vanligvis nummeret til Microsoft Knowledge Base-artikkelen (KB) som forklarer endringene som konfigurasjonsversjonen introduserte.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-135">The version description usually includes the number of the Microsoft Knowledge Base (KB) article that explains the changes that the configuration version introduced.</span></span>

> [!NOTE]
> <span data-ttu-id="e6ef7-136">Når du er ferdig med å importere alle ER-konfigurasjoner fra tabellen ovenfor, kan du angi alternativet **Standard for modelltilordning** til **Ja** for konfigurasjonen **SAF-T økonomiske datamodelltilordning**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-136">After you've finished importing all the ER configurations from the preceding table, set the **Default for model mapping** option to **Yes** for the **SAF-T Financial data model mapping** configuration.</span></span>
>
> ![Standardalternativ for modelltilordning er satt til Ja](media/nor-saf-default-model-mapping.jpg)


![Last opp og legg til-knappen](media/nor-saf-default-model-mapping.jpg)

<span data-ttu-id="e6ef7-139">Hvis du vil ha mer informasjon om hvordan du laster ned ER-konfigurasjoner fra Microsoft Dynamics Lifecycle Services (LCS), kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="e6ef7-139">For more information about how to download ER configurations from Microsoft Dynamics Lifecycle Services (LCS), see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>


## <a name="setup"></a><span data-ttu-id="e6ef7-140">Oppsett</span><span class="sxs-lookup"><span data-stu-id="e6ef7-140">Setup</span></span>

<span data-ttu-id="e6ef7-141">Hvis du vil begynne å bruke rapporten **Norsk SAF-T økonomiske data** i Finance, må du fullføre følgende oppsett:</span><span class="sxs-lookup"><span data-stu-id="e6ef7-141">To start to use the **Norwegian SAF-T Financial data** report in Finance, you must complete the following setup:</span></span>

- <span data-ttu-id="e6ef7-142">**Parametere for økonomimodul:** Definer ER-formatet på siden **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-142">**General ledger parameters:** Set up the ER format on the **General ledgers parameters** page.</span></span>
- <span data-ttu-id="e6ef7-143">**Mva-koder:** Knytt mva-koder til norske standard mva-koder for merverdiavgift (mva.).</span><span class="sxs-lookup"><span data-stu-id="e6ef7-143">**Sales tax codes:** Associate sales tax codes with Norwegian standard value-added tax (VAT) tax codes.</span></span>
- <span data-ttu-id="e6ef7-144">**Hovedkontoer:** Knytt hovedkontoer til norske standardkontoer.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-144">**Main accounts:** Associate main accounts with Norwegian standard accounts.</span></span>

<span data-ttu-id="e6ef7-145">Delene nedenfor forklarer hvordan du gjør hver del av dette oppsettet.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-145">The following sections explain how to do each part of this setup.</span></span>

### <a name="general-ledger-parameters"></a><span data-ttu-id="e6ef7-146">Parametere for økonomimodul</span><span class="sxs-lookup"><span data-stu-id="e6ef7-146">General ledger parameters</span></span>

1. <span data-ttu-id="e6ef7-147">I Finance går du til **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-147">In Finance, go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="e6ef7-148">På siden **Parametere for økonomimodul**, i kategorien **Standard revisjonsfil for avgift (SAF-T)** i feltet **Standard revisjonsfil for avgift (SAF-T)**, velger du **SAF-T-format (NO)**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-148">On the **General ledger parameters** page, on the **Standard Audit File for Tax (SAF-T)** tab, in the **Standard Audit File for Tax (SAF-T)** field, select **SAF-T Format (NO)**.</span></span>

![Feltet Standard revisjonsfil for avgift (SAF-T) på siden parametere for økonomimodul](media/nor-saf-gl-parameters.jpg)

### <a name="sales-tax-codes"></a><span data-ttu-id="e6ef7-150">Mva-koder</span><span class="sxs-lookup"><span data-stu-id="e6ef7-150">Sales tax codes</span></span>

<span data-ttu-id="e6ef7-151">Som dokumentasjonen forklarer, i Norsk SAF-T økonomiske data, må mva-koder som brukes i Finance, være knyttet til norske standard mva-koder (\<StandardTaxCode\>) for SAF-T-rapportering.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-151">As the documentation explains, in Norwegian SAF-T Financial data, sales tax codes that are used in Finance must be associated with Norwegian standard VAT tax codes (\<StandardTaxCode\>) for the purpose of SAF-T reporting.</span></span> <span data-ttu-id="e6ef7-152">Norske standard mva-koder er tilgjengelige på <https://github.com/Skatteetaten/saf-t>.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-152">The Norwegian standard VAT tax codes are available at <https://github.com/Skatteetaten/saf-t>.</span></span>

<span data-ttu-id="e6ef7-153">Hvis du vil knytte mva-koder som brukes i Finance, med norske standard mva-koder, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-153">To associate sales tax codes that are used in Finance with Norwegian standard VAT tax codes, follow these steps.</span></span>

1. <span data-ttu-id="e6ef7-154">I Finance går du til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-154">In Finance, go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="e6ef7-155">På siden **Mva-kode** velger du **Mva-kode**-posten, og deretter, på handlingsruten i kategorien **Mva-kode** i gruppen **Mva-kode**, velger du **Eksterne koder**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-155">On the **Sales tax code** page, select the **Sales tax code** record, and then, on the Action Pane, on the **Sales tax code** tab, in the **Sales tax code** group, select **External codes**.</span></span>

    ![Eksterne koder-knappen i handlingsruten på siden for mva-kode](media/nor-saf-standard-tax-codes.jpg)

3. <span data-ttu-id="e6ef7-157">På **Eksterne koder**-siden angir du norske standard mva-koder som skal brukes for den valgte posten for mva-koden, for SAF-T-rapportering.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-157">On the **External codes** page, specify the Norwegian standard VAT tax codes that should be used for the selected sales tax code record for the purpose of SAF-T reporting.</span></span>

### <a name="main-accounts"></a><span data-ttu-id="e6ef7-158">Hovedkontoer</span><span class="sxs-lookup"><span data-stu-id="e6ef7-158">Main accounts</span></span>

<span data-ttu-id="e6ef7-159">Som dokumentasjonen forklarer, i Norsk SAF-T økonomiske data, må hovedkontoer som brukes i Finance, være knyttet til norske standardkontoer for SAF-T-rapportering.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-159">As the documentation explains, in Norwegian SAF-T Financial data, main accounts that are used in Finance must be associated with Norwegian standard accounts for the purpose of SAF-T reporting.</span></span> <span data-ttu-id="e6ef7-160">Norske standardkontoer er tilgjengelige på <https://github.com/Skatteetaten/saf-t>.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-160">The Norwegian standard accounts are available at <https://github.com/Skatteetaten/saf-t>.</span></span>


<span data-ttu-id="e6ef7-161">Fra og med **versjon 54.61** støtter det elektroniske rapporteringsformatet **“SAF-T-format (NO)”** oppsettet av **Standardkontoer** for selskapets **Hovedkontoer** ved å benytte **Applikasjonsspesifikke parametere**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-161">Starting from **version 54.61**, the electronic reporting format **“SAF-T Format (NO)”** supports the setup of **Standard accounts** for the **Main accounts** of the company by using **Application specific parameters**.</span></span>

<span data-ttu-id="e6ef7-162">Hvis du vil knytte **Hovedkontoer** som brukes i Finans, til norske standardkontoer via **Applikasjonsspesifikke parametere**, følger du trinnene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="e6ef7-162">To associate **Main accounts** that are used in Finance with Norwegian standard accounts via **Application specific parameters** follow the following steps:</span></span>

1. <span data-ttu-id="e6ef7-163">Åpne **Elektronisk rapportering**-arbeidsområdet, gå til konfigurasjonstreet og velg det elektroniske rapporteringsformatet **“SAF-T-format (NO)”**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-163">Open the **Electronic reporting** workspace, in the configuration tree, select the **“SAF-T Format (NO)”** electronic reporting format.</span></span> 
2. <span data-ttu-id="e6ef7-164">Kontroller at selskapet du arbeider med, er selskapet du vil definere **Applikasjonsspesifikke parametere** for.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-164">Make sure that company you are working is the company for which you want to set up the **Application specific parameters**.</span></span>
3. <span data-ttu-id="e6ef7-165">På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-165">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
4. <span data-ttu-id="e6ef7-166">Velg versjonen av formatet som du vil bruke på venstre side av siden **Applikasjonsspesifikke parametere**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-166">Select the version of the format that you want to use on the left side of the **Application specific parameters** page.</span></span>
5. <span data-ttu-id="e6ef7-167">I **Oppslag**-hurtigfanen velger du **StandardMainAccount_Lookup** og spesifiserer deretter kriteriene på **Betingelser**-hurtigfanen ved å legge til linjer for hver **Resultat**-verdi som må brukes i det valgte selskapet.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-167">On the **Lookup** FastTab, select **StandardMainAccount_Lookup**, and then specify criteria on the **Conditions** FastTab by adding lines for each **Result** value which must be used in the selected company.</span></span> <span data-ttu-id="e6ef7-168">Hvis flere **Hovedkontoer** i det valgte selskapet må resultere i samme **Standardkonto**, legger du til en separat linje for hver **Hovedkonto** og spesifiserer samme **Standardkonto** for hver.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-168">If several **Main accounts** in the selected company must result the same **Standard account**, add a separate line for each **Main account** and specify the same **Standard account** for each one.</span></span>
6. <span data-ttu-id="e6ef7-169">Velg verdien **Ikke aktuelt** som den siste betingelsen i listen.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-169">Select the value, **NA** as the last condition in the list.</span></span> <span data-ttu-id="e6ef7-170">Den må være satt til **\*Ikke tom\*** i **Hovedkonto**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-170">It must be set to **\*Not blank\*** in **Main account** column.</span></span> <span data-ttu-id="e6ef7-171">Verifiser verdien i **Linje**-kolonnen for at **"Ikke aktuelt"** er den siste betingelsen i tabellen.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-171">Verify the value in the **Line** column that **“NA”** is the last condition in the table.</span></span>
7. <span data-ttu-id="e6ef7-172">Når du er ferdig med å sette opp betingelser, endrer du verdien i **Tilstand**-feltet til **Fullført**, lagrer endringene og lukker siden.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-172">When you've finished setting up conditions, change the value of the **State** field to **Completed**, save your changes, and close the page.</span></span>

![Standardkonto-feltet på siden Hovedkontoer](media/nor-saf-standard-main-accounts-appsppar.jpg)

<span data-ttu-id="e6ef7-174">Du kan enkelt eksportere oppsettet av applikasjonsspesifikke parametere fra én versjon av en rapport og importere det til en annen versjon ved å velge **Eksporter** eller **Importer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-174">You can easily export the setup of application-specific parameters from one version of a report and import it into another version by selecting **Export** or **Import** on the Action Pane.</span></span> <span data-ttu-id="e6ef7-175">Du kan også eksportere oppsettet fra én rapport og importere det til samme rapport i et annet selskap hvis hovedkontoene er de samme i begge selskapene.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-175">You can also export the setup from one report and import it into the same report in another company if the Main accounts are the same in both companies.</span></span>

## <a name="generate-the-norwegian-saf-t-financial-data-report"></a><span data-ttu-id="e6ef7-176">Generer rapporten Norsk SAF-T økonomiske data</span><span class="sxs-lookup"><span data-stu-id="e6ef7-176">Generate the Norwegian SAF-T Financial data report</span></span>

<span data-ttu-id="e6ef7-177">Hvis du vil generere rapporten **Norsk SAF-T økonomiske data**, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-177">To generate the **Norwegian SAF-T Financial data** report, follow these steps.</span></span>

1. <span data-ttu-id="e6ef7-178">I Finance går du til **Økonomimodul** \> **Forespørsler og rapporter** \> **Standard revisjonsfil for avgift (SAF-T)** \> **Standard revisjonsfil for avgift (SAF-T)**.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-178">In Finance, go to **General ledger** \> **Inquiries and reports** \> **Standard Audit File for Tax (SAF-T)** \> **Standard Audit File for Tax (SAF-T)**.</span></span>
2. <span data-ttu-id="e6ef7-179">Angi start- og sluttdatoene for perioden du vil generere rapporten for, i **Fra dato**- og **Til dato**-feltene i dialogboksen for rapporten.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-179">In the dialog box for the report, in the **From date** and **To date** fields, specify the start and end dates of the period that you want to generate the report for.</span></span>
3. <span data-ttu-id="e6ef7-180">Merk av for **Kunder**, **Leverandører** og **Finansdimensjoner** for å ta med alle postene fra de relaterte tabellene i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-180">Select the check boxes for **Customers**, **Vendors**, and **Financial dimensions** to include all the records from the related tables on the report.</span></span>

    <span data-ttu-id="e6ef7-181">Hvis det ikke er merket av for **Kunder** og **Leverandører**, vil rapporten bare inkludere kunder og leverandører i firmaet som det var transaksjoner for i rapporteringsperioden, og kunder og leverandører som har en saldo som ikke er null.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-181">If the **Customers** and **Vendors** check boxes are cleared, the report will include only those customers and vendors of your company that there were transactions for in the reporting period, and customers and vendors that have a non-zero balance.</span></span>
    
    <span data-ttu-id="e6ef7-182">Hvis det ikke er merket av for **Finansdimensjoner**, vil bare finansdimensjonene som ble brukt i transaksjoner i løpet av rapporteringsperioden, rapporteres i **\<MasterFiles\>**-noden i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-182">If the **Financial dimensions** check box is cleared, only those financial dimensions that were used in transactions during the reporting period will be reported in the **\<MasterFiles\>** node of the report.</span></span>

4. <span data-ttu-id="e6ef7-183">I feltet **Personalnummer** velger du en ansatt for å legge til den ansatte i **\<Bruker-ID\>**-noden i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-183">In the **Personnel number** field, select an employee to add the employee to the **\<UserID\>** node of the report.</span></span> <span data-ttu-id="e6ef7-184">Denne noden rapporterer IDen til brukeren som genererte revisjonsfilen.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-184">This node reports the ID of the user who generated the audit file.</span></span>

<span data-ttu-id="e6ef7-185">Du kan også bruke filtre for feltene **Hovedkontoer** og **Oppføring i økonomijournal** ved hjelp av hurtigfanen **Poster som skal inkluderes** i dialogboksen for rapporten.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-185">You can also apply filters for the **Main accounts** and **General journal entry** fields by using **Records to include** FastTab in the dialog box for the report.</span></span>

## <a name="report-naming-and-splitting"></a><span data-ttu-id="e6ef7-186">Navngivning og oppdeling av rapporter</span><span class="sxs-lookup"><span data-stu-id="e6ef7-186">Report naming and splitting</span></span>

<span data-ttu-id="e6ef7-187">Dokumentasjonen for norske SAF-T økonomiske data krever følgende navngivingsstruktur for XML-rapportene som genereres:</span><span class="sxs-lookup"><span data-stu-id="e6ef7-187">The documentation for Norwegian SAF-T Financial data requires the following naming structure for the XML reports that are generated:</span></span>

<span data-ttu-id="e6ef7-188">\<SAF-T-eksporttype\>\_\<organisasjonsnummer for leverandøren som dataene representerer\>\_\<dato og klokkeslett (ååååmmddtt24tmise\>\_\<filnummer for totalt antall filer\>.xml</span><span class="sxs-lookup"><span data-stu-id="e6ef7-188">\<SAF-T export type\>\_\<organization number of the vendor that the data represents\>\_\<date and time(yyyymmddhh24hmise\>\_\<file number of total files\>.xml</span></span> 

<span data-ttu-id="e6ef7-189">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="e6ef7-189">Here is an example:</span></span>

<span data-ttu-id="e6ef7-190">SAF-T Financial\_999999999\_20160401235911\_1\_12.xml</span><span class="sxs-lookup"><span data-stu-id="e6ef7-190">SAF-T Financial\_999999999\_20160401235911\_1\_12.xml</span></span>

<span data-ttu-id="e6ef7-191">Her er en forklaring på delene av dette filnavnet:</span><span class="sxs-lookup"><span data-stu-id="e6ef7-191">Here is an explanation of the parts of this file name:</span></span>

- <span data-ttu-id="e6ef7-192">**SAF-T Financial** angir SAF-T-typen fil.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-192">**SAF-T Financial** states the SAF-T type of file.</span></span>
- <span data-ttu-id="e6ef7-193">**999999999** representerer organisasjonsnummeret som tilhører eieren av dataene.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-193">**999999999** represents the organization number that belongs to the owner of the data.</span></span>
- <span data-ttu-id="e6ef7-194">**20160401235911** representerer datoen og klokkeslettet da filen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-194">**20160401235911** represents the date and time when the file was created.</span></span> <span data-ttu-id="e6ef7-195">(En 24-timers klokke brukes for klokkeslettet.)</span><span class="sxs-lookup"><span data-stu-id="e6ef7-195">(A 24-hour clock is used for the time.)</span></span>
- <span data-ttu-id="e6ef7-196">**1\_12** representerer fil 1 av 12 totalt antall filer i eksporten (det vil si i samme valg).</span><span class="sxs-lookup"><span data-stu-id="e6ef7-196">**1\_12** represents file 1 out of 12 total files in the export (that is, in the same selection).</span></span>

<span data-ttu-id="e6ef7-197">Volumet til en enkelt XML-fil må være mindre enn 2 gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="e6ef7-197">The volume of a single XML file must be less than 2 gigabytes (GB).</span></span> <span data-ttu-id="e6ef7-198">Hver enkelt XML-fil som sendes, må valideres mot skjemaet.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-198">Every individual XML file that is submitted must be validated against the schema.</span></span> <span data-ttu-id="e6ef7-199">Alle \<MasterFiles\>-noder må være i den første filen, og de tilknyttede transaksjonene må være i de påfølgende filene (antallet av disse filene er fleksibelt).</span><span class="sxs-lookup"><span data-stu-id="e6ef7-199">All \<MasterFiles\> nodes must be in the first file, and the associated transactions must be in the subsequent files (the number of these files is flexible).</span></span>

<span data-ttu-id="e6ef7-200">Tabellen nedenfor viser et eksempelutvalg av ett regnskapsår som har 12 perioder.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-200">The following table shows a sample selection of one accounting year that has 12 periods.</span></span> <span data-ttu-id="e6ef7-201">For hver periode er det én fil som inneholder transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-201">For each period, there is one file that contains transactions.</span></span>

| <span data-ttu-id="e6ef7-202">Filnummer</span><span class="sxs-lookup"><span data-stu-id="e6ef7-202">File number</span></span> | <span data-ttu-id="e6ef7-203">Innhold i revisjonsfilen</span><span class="sxs-lookup"><span data-stu-id="e6ef7-203">Contents of the audit file</span></span>                     |
|-------------|------------------------------------------------|
| <span data-ttu-id="e6ef7-204">1</span><span class="sxs-lookup"><span data-stu-id="e6ef7-204">1</span></span>           | <span data-ttu-id="e6ef7-205">\<Topptekst\> og \<MasterFiles\>-noder</span><span class="sxs-lookup"><span data-stu-id="e6ef7-205">\<Header\> and \<MasterFiles\> nodes</span></span>           |
| <span data-ttu-id="e6ef7-206">2–13</span><span class="sxs-lookup"><span data-stu-id="e6ef7-206">2–13</span></span>        | <span data-ttu-id="e6ef7-207">\<Topptekst\> og \<GeneralLedgerEntries\>-noder</span><span class="sxs-lookup"><span data-stu-id="e6ef7-207">\<Header\> and \<GeneralLedgerEntries\> nodes</span></span>  |

<span data-ttu-id="e6ef7-208">Det kan være maksimalt 10 XML-filer i samme zip-arkiv.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-208">There can be a maximum of 10 XML files in the same zip archive.</span></span>

<span data-ttu-id="e6ef7-209">I samsvar med disse kravene er ER-formatet **SAF-T-format (NO)** implementert for å automatisk dele den resulterende rapporten i XML-format, basert på følgende forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="e6ef7-209">In accordance with these requirements, the **SAF-T Format (NO)** ER format is implemented to automatically split the resulting report in XML format, based on the following assumptions:</span></span>

- <span data-ttu-id="e6ef7-210">Det maksimale volumet for den resulterende XML-rapporten er 2 000 000 kilobyte (kB) (det vil si 2 GB).</span><span class="sxs-lookup"><span data-stu-id="e6ef7-210">The maximum volume of the resulting XML report is 2,000,000 kilobytes (KB) (that is, 2 GB).</span></span>
- <span data-ttu-id="e6ef7-211">Alle XML-filene bruker følgende navngivningsstruktur:</span><span class="sxs-lookup"><span data-stu-id="e6ef7-211">All the XML files use the following naming structure:</span></span>

    <span data-ttu-id="e6ef7-212">\<SAF-T-eksporttype\>\_\<organisasjonsnummer for leverandøren som dataene representerer\>\_\<dato og klokkeslett(ååååmmddtt24tmise\></span><span class="sxs-lookup"><span data-stu-id="e6ef7-212">\<SAF-T export type\>\_\<organization number of the vendor that the data represents\>\_\<date and time(yyyymmddhh24hmise\></span></span>

- <span data-ttu-id="e6ef7-213">Alle XML-filer er inkludert i ett zip-arkiv.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-213">All the XML files are included in one zip archive.</span></span>
- <span data-ttu-id="e6ef7-214">Hver enkelt XML-fil valideres mot skjemaet.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-214">Each individual XML file is validated against the schema.</span></span>

<span data-ttu-id="e6ef7-215">Når rapporten er generert, hvis det genereres mer enn én XML-fil, må brukeren manuelt nummerere de genererte filene i zip-arkivet ved å legge til **\_\<filnummeret for totalt antall filer\>** i filnavnene.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-215">After the report is generated, if more than one XML file is generated, the user must manually number the generated files in the zip archive by adding **\_\<file number of total files\>** to the file names.</span></span> <span data-ttu-id="e6ef7-216">Brukeren må likeledes sikre at det ikke mer enn 10 XML-filer i det samme zip-arkivet.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-216">The user must also make sure that there are no more than 10 XML files in the same zip archive.</span></span> <span data-ttu-id="e6ef7-217">Hvis det er mer enn 10 XML-filer i et arkiv, må brukeren manuelt dele det opp i flere arkiver, som hver har maksimalt 10 XML-filer.</span><span class="sxs-lookup"><span data-stu-id="e6ef7-217">If there are more than 10 XML files in an archive, the user must manually split it into several archives, each of which has a maximum of 10 XML files.</span></span>
