---
title: Forbedre ytelsen for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT
description: Dette emnet beskriver hvordan du kan forbedre ytelsen til ER-løsninger (Electroinic Reporting) ved å legge til datakilder med parameterisert BEREGNET FELT.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a87098e82284a4951f3a4de050f6ba3f587fd20a
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760088"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="da79e-103">Forbedre ytelsen for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT</span><span class="sxs-lookup"><span data-stu-id="da79e-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da79e-104">I dette emnet finner du informasjon om hvordan du kan utføre [ytelsessporinger](trace-execution-er-troubleshoot-perf.md) av [Elektronisk rapportering (ER)](general-electronic-reporting.md) som kjøres, og deretter bruke informasjonen fra disse sporingene til å forbedre ytelsen ved å konfigurere en datakilde med parameterisert **beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="da79e-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="da79e-105">Som en del av prosessen med å utforme ER-konfigurasjoner for å generere forretningsdokumenter, definerer du metoden som brukes til å hente data fra appen og registrere den i de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="da79e-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="da79e-106">Ved å utforme en parameterisert ER-datakilde for typen **Beregnet felt**, kan du redusere antallet databasekall, og du kan redusere tiden og kostnadene betydelig slik at du får mer detaljert informasjon om ER-formatutføringen.</span><span class="sxs-lookup"><span data-stu-id="da79e-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="da79e-107">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="da79e-107">Prerequisites</span></span>

- <span data-ttu-id="da79e-108">Hvis du vil fullføre eksemplene i dette emnet, må du ha tilgang til følgende [roller](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="da79e-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="da79e-109">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="da79e-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="da79e-110">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="da79e-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="da79e-111">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="da79e-111">System administrator</span></span>

- <span data-ttu-id="da79e-112">Firmaet må settes til **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="da79e-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="da79e-113">Følg trinnene i [Tillegg 1](#appendix1) i dette emnet for å laste ned komponentene i Microsoft ER-eksempelløsningen som kreves for å fullføre eksemplene i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="da79e-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="da79e-114">Følg trinnene i [Tillegg 2](#appendix2) i dette emnet for å konfigurere minimumssettet med ER-parametere som kreves for å bruke ER-rammeverket til å forbedre ytelsen i Microsoft ER-eksempelløsningen.</span><span class="sxs-lookup"><span data-stu-id="da79e-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="da79e-115">Importere ER-eksempelløsningen</span><span class="sxs-lookup"><span data-stu-id="da79e-115">Import the sample ER solution</span></span>

<span data-ttu-id="da79e-116">Anta at du må utforme en ER-løsning for å generere en ny rapport som viser leverandørtransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="da79e-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="da79e-117">For øyeblikket finner du transaksjonene for en valgt leverandør på siden **Leverandørtransaksjoner** (gå til **Leverandører** \> **Leverandører** \> **Alle leverandører**, velg en leverandør, og deretter velger du **Transaksjoner** i gruppen **Transaksjoner** i kategorien **Leverandør** i handlingsruten).</span><span class="sxs-lookup"><span data-stu-id="da79e-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="da79e-118">Du vil imidlertid ha alle leverandørtransaksjoner sammen i ett elektronisk dokument i XML-format.</span><span class="sxs-lookup"><span data-stu-id="da79e-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="da79e-119">Denne løsningen vil bestå av flere ER-konfigurasjoner som inneholder den nødvendige datamodellen, modelltilordningen og formatkomponentene.</span><span class="sxs-lookup"><span data-stu-id="da79e-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="da79e-120">Det første trinnet er å importere ER-eksempelløsningen for å generere en leverandørtransaksjonsrapport.</span><span class="sxs-lookup"><span data-stu-id="da79e-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="da79e-121">Logg på forekomsten av Microsoft Dynamics 365 Finance som er klargjort for firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="da79e-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="da79e-122">I dette emnet skal du opprette og endre konfigurasjoner for eksempelfirmaet **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="da79e-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="da79e-123">Kontroller at denne konfigurasjonsleverandøren er lagt til i Finance-forekomsten og er merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="da79e-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="da79e-124">Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="da79e-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="da79e-125">I arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="da79e-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="da79e-126">På siden **Konfigurasjoner** importerer du ER-konfigurasjoner som du lastet ned som en forutsetning til Finance, i denne rekkefølgen: datamodell, modelltilordning, format.</span><span class="sxs-lookup"><span data-stu-id="da79e-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="da79e-127">For hver konfigurasjon følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="da79e-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="da79e-128">I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="da79e-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="da79e-129">Velg **Bla gjennom**, og velg den riktige filen for ER-konfigurasjonen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="da79e-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="da79e-130">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="da79e-130">Select **OK**.</span></span>

![Importerte konfigurasjoner på siden Konfigurasjoner](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="da79e-132">Gå gjennom ER-eksempelløsningen</span><span class="sxs-lookup"><span data-stu-id="da79e-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="da79e-133">Se gjennom modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="da79e-133">Review the model mapping</span></span>

1. <span data-ttu-id="da79e-134">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **modellen Ytelsesforbedring** og velger **tilordningen Ytelsesforbedring**.</span><span class="sxs-lookup"><span data-stu-id="da79e-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="da79e-135">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="da79e-136">På siden **Tilordning av modell til datakilde** velger du **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="da79e-137">Denne ER-modelltilordningen er utformet for å utføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="da79e-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="da79e-138">Hent listen over leverandørtransaksjoner som er lagret i VendTrans-tabellen (**Ttrans**-datakilde).</span><span class="sxs-lookup"><span data-stu-id="da79e-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="da79e-139">For hver transaksjon må du hente posten for en leverandør som transaksjonen er postert for (**\#Vend**-datakilde), fra tabellen VendTable.</span><span class="sxs-lookup"><span data-stu-id="da79e-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="da79e-140">Datakilden **\#Vend** er konfigurert til å hente den tilsvarende leverandørposten ved hjelp av den eksisterende mange-til-én-relasjonen **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="da79e-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="da79e-141">Modelltilordningen i denne konfigurasjonen implementerer basisdatamodellen for ER-formater som opprettes for denne modellen og som kjøres i Finance.</span><span class="sxs-lookup"><span data-stu-id="da79e-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="da79e-142">Derfor vil inneholdet i datakilden **Trans** bli eksponert for ER-formater, for eksempel abstrakte datakilder av typen **model**.</span><span class="sxs-lookup"><span data-stu-id="da79e-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Trans-datakilde på siden Modelltilordningsutforming](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="da79e-144">Lukk siden **Modelltilordningsutforming**.</span><span class="sxs-lookup"><span data-stu-id="da79e-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="da79e-145">Lukk siden **Tilordning av modell til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="da79e-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="da79e-146">Gjennomgangsformat</span><span class="sxs-lookup"><span data-stu-id="da79e-146">Review format</span></span>

1. <span data-ttu-id="da79e-147">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **modellen Ytelsesforbedring** og velger **formatet Ytelsesforbedring**.</span><span class="sxs-lookup"><span data-stu-id="da79e-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="da79e-148">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="da79e-149">På siden **Formatutforming** i kategorien **Tilordning** velger du **Vis/skjul**.</span><span class="sxs-lookup"><span data-stu-id="da79e-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="da79e-150">Vis elementene **Modell**, **Data** og **Transaksjon**.</span><span class="sxs-lookup"><span data-stu-id="da79e-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="da79e-151">Dette ER-formatet er utformet for å generere en leverandørtransaksjonsrapport i XML-format.</span><span class="sxs-lookup"><span data-stu-id="da79e-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Formatdatakilder og konfigurerte bindinger for formatelementer på siden Formatutforming](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="da79e-153">Lukk **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="da79e-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="da79e-154">Kjøre ER-eksempelløsningen for å spore kjøring</span><span class="sxs-lookup"><span data-stu-id="da79e-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="da79e-155">Anta at du er ferdig med å utforme den første versjonen av ER-løsningen.</span><span class="sxs-lookup"><span data-stu-id="da79e-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="da79e-156">Nå skal du teste løsningen i Finance-forekomsten og analysere kjøringsytelsen.</span><span class="sxs-lookup"><span data-stu-id="da79e-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="da79e-157">Aktivere ER-ytelsessporing</span><span class="sxs-lookup"><span data-stu-id="da79e-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="da79e-158">Velg **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="da79e-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="da79e-159">Følg fremgangsmåten il [Aktivere ER-ytelsessporing](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) for å generere en ytelsessporing mens et ER-format kjøres.</span><span class="sxs-lookup"><span data-stu-id="da79e-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Dialogboksen Brukerparametere](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="da79e-161">Kjør ER-formatet</span><span class="sxs-lookup"><span data-stu-id="da79e-161">Run the ER format</span></span>

1. <span data-ttu-id="da79e-162">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="da79e-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="da79e-163">På siden **Konfigurasjoner** i konfigurasjonstreet, velger du **Format for ytelsesforbedring**.</span><span class="sxs-lookup"><span data-stu-id="da79e-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="da79e-164">Velg **Kjør** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="da79e-165">Bruke ytelsessporing til å analysere ytelse for modelltilordning</span><span class="sxs-lookup"><span data-stu-id="da79e-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="da79e-166">På siden **Konfigurasjoner** i konfigurasjonstreet, velger du **Tilordning for ytelsesforbedring**.</span><span class="sxs-lookup"><span data-stu-id="da79e-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="da79e-167">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="da79e-168">På siden **Modelltilordninger** velger du **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="da79e-169">På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="da79e-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="da79e-170">Velg den siste sporingen som ble generert, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="da79e-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="da79e-171">Ny informasjon er nå tilgjengelig for noen datakildeelementer av gjeldende modelltilordning:</span><span class="sxs-lookup"><span data-stu-id="da79e-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="da79e-172">Den faktiske tiden som ble brukt til å hente data ved hjelp av datakilden</span><span class="sxs-lookup"><span data-stu-id="da79e-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="da79e-173">Den samme tiden som prosent av den totale tiden som ble brukt til å kjøre hele modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="da79e-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Informasjon om utføringstid på siden Modelltilordningsutforming](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="da79e-175">Rutenettet **Ytelsesstatistikk** viser at datakilden **Trans** kaller VendTrans-tabellen én gang.</span><span class="sxs-lookup"><span data-stu-id="da79e-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="da79e-176">Verdien **\[265\]\[Q:265\]** for datakilden **Trans** angir at 265 leverandørtransaksjoner er hentet fra apptabellen og returneres til datamodellen.</span><span class="sxs-lookup"><span data-stu-id="da79e-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="da79e-177">Rutenettet **Ytelsesstatistikk** viser også at gjeldende modelltilordning dupliserer databaseforespørsler når datakilden **\#Vend** kjøres.</span><span class="sxs-lookup"><span data-stu-id="da79e-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="da79e-178">Dupliseringen skjer av følgende årsaker:</span><span class="sxs-lookup"><span data-stu-id="da79e-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="da79e-179">Leverandørtabellen kalles to ganger for hver av de 265 omsluttede leverandørtransaksjonene, totalt 530 kall:</span><span class="sxs-lookup"><span data-stu-id="da79e-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="da79e-180">Det blir opprettet ett kall for å angi leverandørkontonummeret.</span><span class="sxs-lookup"><span data-stu-id="da79e-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="da79e-181">Det blir opprettet ett kall for å angi leverandørnavnet.</span><span class="sxs-lookup"><span data-stu-id="da79e-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="da79e-182">Leverandørtabellen kalles for hver repeterende leverandørtransaksjon, selv om de hentede transaksjonene bare er postert for fem leverandører.</span><span class="sxs-lookup"><span data-stu-id="da79e-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="da79e-183">Av de 530 kallene er 525 duplikater.</span><span class="sxs-lookup"><span data-stu-id="da79e-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="da79e-184">Følgende illustrasjon viser meldingen du mottar om duplikatoppringinger (databaseforespørsler).</span><span class="sxs-lookup"><span data-stu-id="da79e-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Melding om dupliserte databaseforespørsler på siden Modelltilordningsutforming](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="da79e-186">Av den samlede utføringstiden for modelltilordning (ca. åtte sekunder), må du legge merke til at mer enn 80 prosent (omtrent seks sekunder) har blitt brukt til å hente verdier fra apptabellen VendTable.</span><span class="sxs-lookup"><span data-stu-id="da79e-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="da79e-187">Denne prosentandelen er for stor for to attributter av fem leverandører, sammenlignet med informasjonsvolumet i apptabellen VendTrans.</span><span class="sxs-lookup"><span data-stu-id="da79e-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="da79e-188">Hvis du vil redusere antallet kall som gjøres for å få leverandørdetaljene for hver transaksjon, og for å forbedre ytelsen til modelltilordningen, kan du bruke hurtigbufring for datakilden **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="da79e-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="da79e-189">Datakilden **Trans\\\#Vend** blir bufret i området til gjeldende transaksjon for datakilden **Trans** ved kjøring.</span><span class="sxs-lookup"><span data-stu-id="da79e-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="da79e-190">Ved å bufre datakilden **\#Vend**, reduserer du antallet dupliserte kall fra 525 til 260, men eliminerer ikke dupliseringen fullstendig.</span><span class="sxs-lookup"><span data-stu-id="da79e-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="da79e-191">Hvis du vil eliminere duplisering fullstendig, kan du konfigurere en ny parameterdatakilde av typen **Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="da79e-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="da79e-192">Forbedre modelltilordningen basert på informasjon fra kjøringssporingen</span><span class="sxs-lookup"><span data-stu-id="da79e-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="da79e-193">Endre logikken til modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="da79e-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="da79e-194">Følg denne fremgangsmåten for å bruke bufring og en datakilde av typen **Beregnet felt** for å hindre dupliserte kall til databasen.</span><span class="sxs-lookup"><span data-stu-id="da79e-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="da79e-195">På siden **Konfigurasjoner** i konfigurasjonstreet, velger du **Tilordning for ytelsesforbedring**.</span><span class="sxs-lookup"><span data-stu-id="da79e-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="da79e-196">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="da79e-197">På siden **Modelltilordninger** velger du **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="da79e-198">På siden **Modelltilordningsutforming** følger du denne fremgangsmåten for å legge til en datakilde av typen **Tabellposter** for å få tilgang til poster i apptabellen VendTable:</span><span class="sxs-lookup"><span data-stu-id="da79e-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="da79e-199">I ruten **Datakildetyper** utvider du **Dynamics 365 for Operations** og velger **Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="da79e-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="da79e-200">Velg **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="da79e-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="da79e-201">Skriv inn **Vend** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="da79e-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="da79e-202">I **Tabell**-feltet angir du **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="da79e-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="da79e-203">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="da79e-203">Select **OK**.</span></span>

5. <span data-ttu-id="da79e-204">Du kan parameterisere kall til datakilder av typen **Beregnet felt** bare hvis disse datakildene befinner seg i en beholder.</span><span class="sxs-lookup"><span data-stu-id="da79e-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="da79e-205">Du bør derfor følge denne fremgangsmåten for å legge til en datakilde av typen **Tom beholder** for å oppbevare en ny parameterdatakilde av typen **Beregnet felt**:</span><span class="sxs-lookup"><span data-stu-id="da79e-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="da79e-206">I ruten **Datakildetyper** utvider du **Generelt** og velger **Tom beholder**.</span><span class="sxs-lookup"><span data-stu-id="da79e-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="da79e-207">Velg **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="da79e-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="da79e-208">Skriv inn **Box** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="da79e-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="da79e-209">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="da79e-209">Select **OK**.</span></span>

    ![Box-datakilde på siden Modelltilordningsutforming](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="da79e-211">Følg disse trinnene for å legge til en parameterdatakilde av typen **Beregnet felt**:</span><span class="sxs-lookup"><span data-stu-id="da79e-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="da79e-212">I ruten **Datakilder** velger du **Box**.</span><span class="sxs-lookup"><span data-stu-id="da79e-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="da79e-213">I ruten **Datakildetyper** utvider du **Funksjoner** og velger **Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="da79e-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="da79e-214">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="da79e-214">Select **Add**.</span></span>
    4. <span data-ttu-id="da79e-215">Skriv inn **Vend** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="da79e-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="da79e-216">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="da79e-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="da79e-217">På siden **Formeldesigner** velger du **Parametere** for å angi parameterne som må oppgis når datakilden kalles.</span><span class="sxs-lookup"><span data-stu-id="da79e-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="da79e-218">I dialogboksen **Parametere** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="da79e-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="da79e-219">I **Navn**-feltet angir du **parmVendAccNumber**.</span><span class="sxs-lookup"><span data-stu-id="da79e-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="da79e-220">Velg **Streng** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="da79e-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="da79e-221">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="da79e-221">Select **OK**.</span></span>
    11. <span data-ttu-id="da79e-222">I **Formel**-feltet angir du **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="da79e-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="da79e-223">Velg **Lagre**, og lukk siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="da79e-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="da79e-224">Velg **OK** for å legge til den nye datakilden.</span><span class="sxs-lookup"><span data-stu-id="da79e-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="da79e-225">Følg denne fremgangsmåten for å merke den tillagte datakilden som hurtigbufret under kjøringen:</span><span class="sxs-lookup"><span data-stu-id="da79e-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="da79e-226">I ruten **Datakilder** velger du **Box\\Vend**.</span><span class="sxs-lookup"><span data-stu-id="da79e-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="da79e-227">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="da79e-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da79e-228">Datakilden **Box\\Vend** vil bli bufret i omfanget for alle leverandørtransaksjoner for datakilden **Trans** under kjøring.</span><span class="sxs-lookup"><span data-stu-id="da79e-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="da79e-229">Følg denne fremgangsmåten for å oppdatere den nestede datakilden **Trans\\\#Vend** slik at den bruker datakilden **Box\\Vend**:</span><span class="sxs-lookup"><span data-stu-id="da79e-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="da79e-230">I **Datakilder**-ruten utvider du **Trans**.</span><span class="sxs-lookup"><span data-stu-id="da79e-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="da79e-231">Velg datakilden **Trans\\\#Vend**, og velg deretter **Rediger** \> **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="da79e-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="da79e-232">På siden **Formeldesigner** i feltet **Formel** angir du **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="da79e-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="da79e-233">Velg **Lagre**, og lukk deretter siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="da79e-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="da79e-234">Velg **OK** for å fullføre endringene i den valgte datakilden.</span><span class="sxs-lookup"><span data-stu-id="da79e-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="da79e-235">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="da79e-235">Select **Save**.</span></span>

    ![Vend-datakilde på siden Modelltilordningsutforming](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="da79e-237">Lukk siden **Modelltilordningsutforming**.</span><span class="sxs-lookup"><span data-stu-id="da79e-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="da79e-238">Lukk siden **Modelltilordninger**.</span><span class="sxs-lookup"><span data-stu-id="da79e-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="da79e-239">Fullføre den endrede versjonen av ER-modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="da79e-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="da79e-240">På siden **Konfigurasjoner** i hurtigkategorien **Versjoner**, velger du versjon **1.2** av konfigurasjonen **Tilordning for ytelsesforbedring**.</span><span class="sxs-lookup"><span data-stu-id="da79e-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="da79e-241">Velg **Endre status** \> **Fullfør**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="da79e-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="da79e-242">Kjøre den endrede ER-løsningen for å spore kjøring</span><span class="sxs-lookup"><span data-stu-id="da79e-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="da79e-243">Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.</span><span class="sxs-lookup"><span data-stu-id="da79e-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="da79e-244">Bruke ytelsessporing til å analysere justerniger for modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="da79e-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="da79e-245">På siden **Konfigurasjoner** i konfigurasjonstreet, velger du **Tilordning for ytelsesforbedring**.</span><span class="sxs-lookup"><span data-stu-id="da79e-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="da79e-246">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="da79e-247">På siden **Modelltilordninger** velger du **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="da79e-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="da79e-248">På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="da79e-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="da79e-249">Velg den siste sporingen som ble generert, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="da79e-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="da79e-250">Legg merke til at justeringene du har gjort i modelltilordningen, har eliminert duplikate spørringer til databasen.</span><span class="sxs-lookup"><span data-stu-id="da79e-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="da79e-251">Antall kall til databasetabeller og datakilder for denne modelltilordningen er også redusert.</span><span class="sxs-lookup"><span data-stu-id="da79e-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Sporingsinformasjon på siden Modelltilordningsutforming 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="da79e-253">Den totale utføringstiden er redusert omtrent 20 ganger (fra omtrent 8 sekunder til omtrent 400 millisekunder).</span><span class="sxs-lookup"><span data-stu-id="da79e-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="da79e-254">Derfor har ytelsen til hele ER-løsningen blitt forbedret.</span><span class="sxs-lookup"><span data-stu-id="da79e-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Sporingsinformasjon på siden Modelltilordningsutforming 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="da79e-256">Tillegg 1: Last ned komponentene i Microsoft ER-eksempelløsningen</span><span class="sxs-lookup"><span data-stu-id="da79e-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="da79e-257">Du må laste ned følgende filer og lagre dem lokalt.</span><span class="sxs-lookup"><span data-stu-id="da79e-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="da79e-258">Fil</span><span class="sxs-lookup"><span data-stu-id="da79e-258">File</span></span>                                        | <span data-ttu-id="da79e-259">Innhold</span><span class="sxs-lookup"><span data-stu-id="da79e-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="da79e-260">Ytelsesforbedringsmodell, versjon 1</span><span class="sxs-lookup"><span data-stu-id="da79e-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="da79e-261">Eksempel ER-datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="da79e-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="da79e-262">Tilordning for ytelsesforbedring, versjon.1.1</span><span class="sxs-lookup"><span data-stu-id="da79e-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="da79e-263">Eksempel ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="da79e-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="da79e-264">Format for ytelsesforbedring, versjon.1.1</span><span class="sxs-lookup"><span data-stu-id="da79e-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="da79e-265">Eksempel ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="da79e-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="da79e-266">Tillegg 2: Konfigurere ER-rammeverket</span><span class="sxs-lookup"><span data-stu-id="da79e-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="da79e-267">Før du kan begynne å bruke ER-rammeverket til å forbedre ytelsen til Microsoft ER-eksempelløsningen, må du konfigurere minimumssettet med ER-parametere.</span><span class="sxs-lookup"><span data-stu-id="da79e-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="da79e-268">Konfigurere ER-parametere</span><span class="sxs-lookup"><span data-stu-id="da79e-268">Configure ER parameters</span></span>

1. <span data-ttu-id="da79e-269">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="da79e-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="da79e-270">På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="da79e-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="da79e-271">På **Parametere for elektronisk rapportering**-siden, i **Generelt**-fanen angi **Aktiver utformingsmodus** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="da79e-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="da79e-272">Angi følgende parametere i fanen **Vedlegg**:</span><span class="sxs-lookup"><span data-stu-id="da79e-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="da79e-273">I **Konfigurasjoner**-feltet velger du **Fil**-typen for **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="da79e-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="da79e-274">I feltene **Jobbarkiv**, **Midlertidig**, **Grunnlinje** og **Annet** velger du **Fil**-typen.</span><span class="sxs-lookup"><span data-stu-id="da79e-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="da79e-275">Hvis du vil ha mer informasjon om ER-parametere, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="da79e-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="da79e-276">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="da79e-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="da79e-277">Hver ER-konfigurasjon som legges til, er merket som eid av en ER-konfigurasjonsleverandør.</span><span class="sxs-lookup"><span data-stu-id="da79e-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="da79e-278">ER-konfigurasjonsleverandøren som aktiveres i **Elektronisk rapportering**-arbeidsområdet, brukes til dette formålet.</span><span class="sxs-lookup"><span data-stu-id="da79e-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="da79e-279">Derfor må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet før du begynner å legge til eller redigere ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="da79e-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="da79e-280">Bare eieren av en ER-konfigurasjon kan redigere den.</span><span class="sxs-lookup"><span data-stu-id="da79e-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="da79e-281">Derfor, før en ER-konfigurasjon kan redigeres, må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="da79e-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="da79e-282">Se gjennom listen over ER-konfigurasjonsleverandører</span><span class="sxs-lookup"><span data-stu-id="da79e-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="da79e-283">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="da79e-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="da79e-284">På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="da79e-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="da79e-285">På **Konfigurasjonsleverandørtabell**-siden har hver leverandørpost et unikt navn og en unik URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="da79e-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="da79e-286">Se gjennom innholdet på denne siden.</span><span class="sxs-lookup"><span data-stu-id="da79e-286">Review the contents of this page.</span></span> <span data-ttu-id="da79e-287">Hvis en post for **Litware, Inc.** allerede finnes, hopper du over netste prosedyre, kalt [Legg til en ny ER-konfigurasjonsleverandør](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="da79e-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="da79e-288">Legg til en ny ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="da79e-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="da79e-289">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="da79e-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="da79e-290">På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="da79e-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="da79e-291">Velg **Ny** på siden **Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="da79e-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="da79e-292">I **Navn**-feltet angir du **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="da79e-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="da79e-293">I **Internett-adresse**-feltet angir du `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="da79e-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="da79e-294">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="da79e-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="da79e-295">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="da79e-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="da79e-296">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="da79e-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="da79e-297">På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Litware, Inc.**-flisen og deretter **Angi aktiv**.</span><span class="sxs-lookup"><span data-stu-id="da79e-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="da79e-298">Hvis du ha mer informasjon om ER-konfigurasjonsleverandører, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="da79e-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da79e-299">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="da79e-299">Additional resources</span></span>

- [<span data-ttu-id="da79e-300">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="da79e-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="da79e-301">Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer</span><span class="sxs-lookup"><span data-stu-id="da79e-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="da79e-302">Støtte for parameterkall fra ER-datakilder for Beregnet felt-typen</span><span class="sxs-lookup"><span data-stu-id="da79e-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)
