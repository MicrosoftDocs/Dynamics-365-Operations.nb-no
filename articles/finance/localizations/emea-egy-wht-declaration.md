---
title: Deklarering av kildeskatt for Egypt
description: Dette emnet beskriver hvordan du konfigurerer og genererer deklareringer for kildeskatt for Egypt.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8c9aaa3868167806ce3189d724621991ec7e53eb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022817"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="3e018-103">Deklarering av kildeskatt for Egypt (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="3e018-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="3e018-104">Oversikt</span><span class="sxs-lookup"><span data-stu-id="3e018-104">Overview</span></span>
<span data-ttu-id="3e018-105">Dette emnet beskriver hvordan du kan sette opp og generere deklarering av forskuddsskatt og skjemaene 11 og 41 for deklarering av kildeskatt for juridiske enheter i Egypt</span><span class="sxs-lookup"><span data-stu-id="3e018-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="3e018-106">Alle egyptiske enheter må klargjøre skjema 41, som summerer alle skatter som oppbevares fra lokale leverandører og leverandører.</span><span class="sxs-lookup"><span data-stu-id="3e018-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="3e018-107">I tillegg til skjema 41 må skjema 11 genereres for detaljert å beskrive alle opptjente avgifter fra utenlandske leverandører.</span><span class="sxs-lookup"><span data-stu-id="3e018-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="3e018-108">Rapporten **Deklarering av kildeskatt** i Dynamics 365 Finance inkluderer følgende rapporter:</span><span class="sxs-lookup"><span data-stu-id="3e018-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="3e018-109">Deklareringsskjema nr.</span><span class="sxs-lookup"><span data-stu-id="3e018-109">Declaration form No.</span></span> <span data-ttu-id="3e018-110">41</span><span class="sxs-lookup"><span data-stu-id="3e018-110">41</span></span>
- <span data-ttu-id="3e018-111">Deklareringsskjema nr.</span><span class="sxs-lookup"><span data-stu-id="3e018-111">Declaration form No.</span></span> <span data-ttu-id="3e018-112">11</span><span class="sxs-lookup"><span data-stu-id="3e018-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="3e018-113">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="3e018-113">Prerequisites</span></span>
<span data-ttu-id="3e018-114">Primæradressen for den juridiske enheten må være i Egypt.</span><span class="sxs-lookup"><span data-stu-id="3e018-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="3e018-115">I arbeidsområdet **Funksjonsstyring** må følgende funksjon være aktivert:</span><span class="sxs-lookup"><span data-stu-id="3e018-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="3e018-116">**Global kildeskatt**</span><span class="sxs-lookup"><span data-stu-id="3e018-116">**Global withholding tax**</span></span>

<span data-ttu-id="3e018-117">Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsstyring.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="3e018-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="3e018-118">Gå til **Avgift** > **Oppsett** > **Parametere** > **Parametere for økonomimodul** og sett **Aktiver global kildeskatt** til **Ja** i fanen **Kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="3e018-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="3e018-119">I arbeidsområdet **Elektronisk rapportering** importerer du følgende formater for elektronisk rapportering fra repositoriet:</span><span class="sxs-lookup"><span data-stu-id="3e018-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="3e018-120">WHT-deklarering Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="3e018-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e018-121">Formatet ovenfor er basert på **mva-deklareringsmodellen** og bruker **tilordningen av mva-deklareringsmodellen**.</span><span class="sxs-lookup"><span data-stu-id="3e018-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="3e018-122">Denne tilleggskonfigurasjonen blir importert automatisk.</span><span class="sxs-lookup"><span data-stu-id="3e018-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="3e018-123">Hvis du vil ha mer informasjon om hvordan du importerer konfigurasjoner for elektronisk rapportering, kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="3e018-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="3e018-124">Laste ned konfigurasjoner for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3e018-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="3e018-125">Implementeringen av WHT-deklareringsskjemaene for Egypt er basert på konfigurasjoner for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="3e018-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="3e018-126">Hvis du vil ha mer informasjon om funksjonene og begrepene for rapportering som kan konfigureres, kan du se [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="3e018-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="3e018-127">For miljøer av produksjons- og brukergodkjenningstesting (UAT), følger du instruksjonene i emnet [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="3e018-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="3e018-128">Hvis du vil generere kildeskattdeklareringer i en egyptisk juridisk enhet, må du laste opp følgende konfigurasjoner:</span><span class="sxs-lookup"><span data-stu-id="3e018-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="3e018-129">Tax declaration model.version.82.xml eller nyere</span><span class="sxs-lookup"><span data-stu-id="3e018-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="3e018-130">Tax declaration model mapping.version.82.133.xml eller nyere</span><span class="sxs-lookup"><span data-stu-id="3e018-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="3e018-131">WHT Declaration Excel (EG).version.82.21 eller nyere</span><span class="sxs-lookup"><span data-stu-id="3e018-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="3e018-132">Etter at du har lastet ned ER-konfigurasjonene fra Lifecycle Services (LCS) eller det globale repositoriet, fullfører du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="3e018-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="3e018-133">Gå til arbeidsområdet **Elektronisk rapportering** og velg flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3e018-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="3e018-134">På siden **Konfigurasjoner** velger du **Exchange > Last fra XML-fil** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3e018-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="3e018-135">Last opp alle filene i den rekkefølgen de er oppført i de forrige oversiktene.</span><span class="sxs-lookup"><span data-stu-id="3e018-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="3e018-136">Når alle konfigurasjonene er lastet opp, skal konfigurasjonstreet være til stede i Finance.</span><span class="sxs-lookup"><span data-stu-id="3e018-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="3e018-137">Konfigurere programspesifikke parametere</span><span class="sxs-lookup"><span data-stu-id="3e018-137">Set up application-specific parameters</span></span>

<span data-ttu-id="3e018-138">Med det programspesifikke parameteralternativet kan brukere fastsette kriteriene for hvordan avgiftstransaksjonene klassifiseres og beregnes på hver linje i en generert rapport, avhengig av konfigurasjonen til **varegruppen for kildeskatt** eller andre kriterier som er fastsatt i oppslagsdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3e018-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="3e018-139">Skjema 41 for kildeskattdeklarering inkluderer en bestemt kolonne der kildeskattransaksjonen må klassifiseres i samsvar med skattemyndighetens klassifisering kalt **Rabattkodetype**.</span><span class="sxs-lookup"><span data-stu-id="3e018-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="3e018-140">I stedet for å inkludere disse nye klassifiseringene som nye oppføringsdata når transaksjonene posteres, bestemmes klassifiseringene basert på forskjellige oppslag som introduseres i **Konfigurasjoner** > **Konfigurere programspesifikke parametere** > **Oppsett** for å oppfylle kravene til kildeskattrapporter for Egypt.</span><span class="sxs-lookup"><span data-stu-id="3e018-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="3e018-141">Følgende konfigurasjon brukes til å klassifisere transaksjonene i rapporten skjema 41 for kildeskattdeklarering:</span><span class="sxs-lookup"><span data-stu-id="3e018-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="3e018-142">**DiscountTaxTypeLookup**-> Kolonne nr. 18</span><span class="sxs-lookup"><span data-stu-id="3e018-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="3e018-143">Fullfør fremgangsmåten nedenfor for å sette opp de ulike oppslagene som brukes til å generere WHT-deklarering og relaterte bøker.</span><span class="sxs-lookup"><span data-stu-id="3e018-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="3e018-144">I arbeidsområdet **Elektroniosk rapportering** velger du **Konfigurasjoner** > **Oppsett** for å identifisere hvordan transaksjoner blir klassifisert i rapporten for WHT-deklarering.</span><span class="sxs-lookup"><span data-stu-id="3e018-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="3e018-145">Velg den gjeldende versjonen, og velg oppslagsnavnet i hurtigfanen **Oppslag**.</span><span class="sxs-lookup"><span data-stu-id="3e018-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="3e018-146">For eksempel **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="3e018-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="3e018-147">Dette oppslaget identifiserer listen over rabattyper som kreves av skattemyndigheten.</span><span class="sxs-lookup"><span data-stu-id="3e018-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="3e018-148">I hurtigfanen **Betingelser** velger du **Legg til**, og i den nye linjen i kolonnen **Oppslagsresultat** velger du den relaterte linjen som representerer klassifiseringen i **Kolonne 18**.</span><span class="sxs-lookup"><span data-stu-id="3e018-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="3e018-149">I kolonnen **Varegruppe for kildeskatt** velger du den relaterte koden som brukes til å identifisere klassifiseringen.</span><span class="sxs-lookup"><span data-stu-id="3e018-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="3e018-150">For eksempel **Tillatt rabatt**.</span><span class="sxs-lookup"><span data-stu-id="3e018-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="3e018-151">Gjenta trinn 3 og 4 for alle tilgjengelige oppslag.</span><span class="sxs-lookup"><span data-stu-id="3e018-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="3e018-152">Velg **Legg til** på nytt for å ta med sluttpostlinjen, og velg **Ikke tilgjengelig** i kolonnen **Oppslagsresultat**.</span><span class="sxs-lookup"><span data-stu-id="3e018-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="3e018-153">I den gjenstående kolonnene velger du **Ikke tom**.</span><span class="sxs-lookup"><span data-stu-id="3e018-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="3e018-154">Konfigurere parametere for økonomimodul</span><span class="sxs-lookup"><span data-stu-id="3e018-154">Set up General ledger parameters</span></span>

<span data-ttu-id="3e018-155">Hvis du vil generere rapporter for WHT-deklareringsskjema i Microsoft Excel, definerer du et ER-format på siden **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="3e018-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="3e018-156">Gå til **Avgift** > **Oppsett** > **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="3e018-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="3e018-157">Velg **WHT-deklarering Excel (EG)** i feltet **Tilordning av format for WHT-deklarering** i fanen **Kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="3e018-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="3e018-158">Hvis du lar feltet stå tomt, genereres standard mva-rapport i SSRS-format.</span><span class="sxs-lookup"><span data-stu-id="3e018-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Deklareringsskjema](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="3e018-160">Generere skjemaene for kildeskattdeklarering</span><span class="sxs-lookup"><span data-stu-id="3e018-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="3e018-161">Prosessen med å klargjøre og sende et skjema for kildeskattdeklarering for en bestemt periode er basert på kildeskattransaksjonene som er postert under utligningen og postering av betalingsavgiftsjobben.</span><span class="sxs-lookup"><span data-stu-id="3e018-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="3e018-162">Hvis du vil ha mer informasjon om global kildeskatt, kan du se [Global kildeskatt](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3e018-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="3e018-163">Fullfør fremgangsmåten nedenfor for å generere mva-deklareringsrapporten.</span><span class="sxs-lookup"><span data-stu-id="3e018-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="3e018-164">Gå til **Avgift** > **Deklareringer** > **Kildeskatt** > \**Kildeskattbetaling*.</span><span class="sxs-lookup"><span data-stu-id="3e018-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="3e018-165">Velg utligningsperioden og velg deretter Fra-datoen for rapporten.</span><span class="sxs-lookup"><span data-stu-id="3e018-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="3e018-166">Angi transaksjonsdatoen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e018-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="3e018-167">I dialogboksen som åpnes, velger du en eller flere av skjematypene **Skjema nr. 41**, **Skjema nr. 11** eller **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="3e018-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="3e018-168">Hvis du velger **Ingen**, genereres standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="3e018-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="3e018-169">Velg språket.</span><span class="sxs-lookup"><span data-stu-id="3e018-169">Select the language.</span></span> <span data-ttu-id="3e018-170">Alle rapporter er oversatt i **en-us** og **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="3e018-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="3e018-171">Angi avdelingen og navnet på banken der mva-betalingen skal betales.</span><span class="sxs-lookup"><span data-stu-id="3e018-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="3e018-172">Velg forretningstypen, og angi deretter sjekk- og dokumentnumrene.</span><span class="sxs-lookup"><span data-stu-id="3e018-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="3e018-173">Angi enhetstypen.</span><span class="sxs-lookup"><span data-stu-id="3e018-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="3e018-174">Angi navnet på personen som er registrert for å tilordne skjemaet, og velg **OK** for å bekrefte rapportgenereringen.</span><span class="sxs-lookup"><span data-stu-id="3e018-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
