---
title: Støtte for parameterkall fra ER-datakilder for Beregnet felt-typen
description: Dette emnet inneholder informasjon om hvordan du bruker Beregnet felt-typen for ER-datakilder.
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 897133a27f9d3da2f576ce675c0949f824cde881
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749495"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="54234-103">Støtte for parameterkall fra ER-datakilder for Beregnet felt-typen</span><span class="sxs-lookup"><span data-stu-id="54234-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54234-104">Dette emnet beskriver hvordan du kan utforme en datakilde for elektronisk rapportering (ER) ved hjelp **Beregnet felt**-typen.</span><span class="sxs-lookup"><span data-stu-id="54234-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="54234-105">Denne datakilden kan inneholde et ER-uttrykk som, når det kjøres, kan kontrolleres av verdiene til parameterargumentene som er konfigurert i en binding som kaller opp denne datakilden.</span><span class="sxs-lookup"><span data-stu-id="54234-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="54234-106">Ved å konfigurere parametriske kall for en slik datakilde, kan du gjenbruke én enkelt datakilde i mange bindinger, noe som reduserer det totale antallet datakilder som må konfigureres i ER-modelltilordninger eller ER-formater.</span><span class="sxs-lookup"><span data-stu-id="54234-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="54234-107">Den forenkler også den konfigurerte ER-komponenten, noe som reduserer vedlikeholdskostnadene og kostnadene for bruk av andre forbrukere.</span><span class="sxs-lookup"><span data-stu-id="54234-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="54234-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="54234-108">Prerequisites</span></span>
<span data-ttu-id="54234-109">Hvis du vil fullføre eksemplene i dette emnet, må du ha følgende tilgang:</span><span class="sxs-lookup"><span data-stu-id="54234-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="54234-110">Tilgang til én av disse rollene:</span><span class="sxs-lookup"><span data-stu-id="54234-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="54234-111">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="54234-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="54234-112">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="54234-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="54234-113">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="54234-113">System administrator</span></span>

- <span data-ttu-id="54234-114">Tilgang til Regulatory Configuration Services (RCS) som er klargjort for samme leietaker som Finance and Operations, for én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="54234-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="54234-115">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="54234-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="54234-116">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="54234-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="54234-117">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="54234-117">System administrator</span></span>

<span data-ttu-id="54234-118">Du må også laste ned og lagre følgende filer lokalt.</span><span class="sxs-lookup"><span data-stu-id="54234-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="54234-119">**Innhold**</span><span class="sxs-lookup"><span data-stu-id="54234-119">**Content**</span></span>                           | <span data-ttu-id="54234-120">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="54234-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54234-121">Eksempel ER-datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="54234-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="54234-122">Modell for å lære om parameterkall.versjon.1.XML</span><span class="sxs-lookup"><span data-stu-id="54234-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="54234-123">Eksempel ER-metadatakonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="54234-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="54234-124">Metadata for å lære om parameterkall.versjon.1.XML</span><span class="sxs-lookup"><span data-stu-id="54234-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="54234-125">Eksempel ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="54234-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="54234-126">Tilordning for å lære om parameterkall.versjon.1.1.XML</span><span class="sxs-lookup"><span data-stu-id="54234-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="54234-127">Eksempel ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="54234-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="54234-128">Format for å lære om parameterkall.versjon.1.1.XML</span><span class="sxs-lookup"><span data-stu-id="54234-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="54234-129">Logge på RCS-forekomsten</span><span class="sxs-lookup"><span data-stu-id="54234-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="54234-130">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet, Litware, Inc. Først må du fullføre disse trinnene i RCS i fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="54234-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="54234-131">Velg **Elektronisk rapportering** på standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="54234-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="54234-132">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="54234-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="54234-133">Importer de nedlastede konfigurasjonene til RCS i følgende rekkefølge: datamodell, metadata, modelltilordning, format.</span><span class="sxs-lookup"><span data-stu-id="54234-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="54234-134">Fullfør trinnene nedenfor for hver ER-konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="54234-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="54234-135">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="54234-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="54234-136">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="54234-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="54234-137">Velg **Bla gjennom**, og velg deretter den nødvendige ER-konfigurasjonen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="54234-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="54234-138">Velg **OK**</span><span class="sxs-lookup"><span data-stu-id="54234-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="54234-139">Se gjennom den angitte ER-løsningen</span><span class="sxs-lookup"><span data-stu-id="54234-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="54234-140">Se gjennom modelltilordning</span><span class="sxs-lookup"><span data-stu-id="54234-140">Review model mapping</span></span>

1. <span data-ttu-id="54234-141">I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="54234-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="54234-142">Velg **Tilordning for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="54234-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="54234-143">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="54234-143">Select **Designer**.</span></span>
4. <span data-ttu-id="54234-144">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="54234-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="54234-145">Denne ER-modelltilordningen er utformet for å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="54234-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="54234-146">Hent listen over avgiftskoder (datakilden **Avgift**) som finnes i **TaxTable**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="54234-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="54234-147">Hent listen over avgiftstransaksjoner (datakilden **Trans**) som finnes i **TaxTrans**-tabellen:</span><span class="sxs-lookup"><span data-stu-id="54234-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="54234-148">Grupper listen over hentede transaksjoner (datakilden **Gr**) etter avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="54234-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="54234-149">Beregn for grupperte transaksjoner etter aggregerte verdier per avgiftskode:</span><span class="sxs-lookup"><span data-stu-id="54234-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="54234-150">Summen av basisverdier for avgift.</span><span class="sxs-lookup"><span data-stu-id="54234-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="54234-151">Summen av verdier for avgift.</span><span class="sxs-lookup"><span data-stu-id="54234-151">Sum of tax values.</span></span>
            - <span data-ttu-id="54234-152">Minimumsverdi for brukt avgiftssats.</span><span class="sxs-lookup"><span data-stu-id="54234-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="54234-153">Modelltilordningen i denne konfigurasjonen implementerer basisdatamodellen for alle ER-formatene som opprettes for denne modellen og som kjøres i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="54234-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="54234-154">Derfor vil inneholder i datakildene **Avgift** og **Gr** bli eksponert for ER-formater, for eksempel abstrakte datakilder.</span><span class="sxs-lookup"><span data-stu-id="54234-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Siden Modelltilordningsutforming viser datakildene Avgift og Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="54234-156">Lukk siden **Modelltilordningsutforming**.</span><span class="sxs-lookup"><span data-stu-id="54234-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="54234-157">Lukk siden **Modelltilordning**.</span><span class="sxs-lookup"><span data-stu-id="54234-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="54234-158">Gjennomgangsformat</span><span class="sxs-lookup"><span data-stu-id="54234-158">Review format</span></span>

1. <span data-ttu-id="54234-159">I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="54234-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="54234-160">Velg **Format for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="54234-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="54234-161">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="54234-161">Select **Designer**.</span></span> <span data-ttu-id="54234-162">Dette ER-formatet er utformet for å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="54234-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="54234-163">Generer en avgiftsoppgave i XML-format.</span><span class="sxs-lookup"><span data-stu-id="54234-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="54234-164">Presenter følgende nivåer for avgifter i avgiftsoppgaven: vanlig, redusert og ingen.</span><span class="sxs-lookup"><span data-stu-id="54234-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="54234-165">Presenter flere detaljer for hvert avgiftsnivå med ulikt antall detaljer på hvert nivå.</span><span class="sxs-lookup"><span data-stu-id="54234-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Formatutformingsside](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="54234-167">Velg **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="54234-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="54234-168">Vis elementene **Model**, **Data,** og **Summary**.</span><span class="sxs-lookup"><span data-stu-id="54234-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="54234-169">Det beregnede feltet **Model.Data.Summary.Level** inneholder uttrykket som returnerer koden for avgiftsnivået (**Vanlig**, **Redusert**, **Ingen** eller **Annet**) som en tekstverdi for avgiftskoder som kan hentes fra datamodellen **Model.Data.Summary** ved kjøretid.</span><span class="sxs-lookup"><span data-stu-id="54234-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Siden Formatutforming som viser detaljer for datamodellen Modell for å lære om parameterkall](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="54234-171">Vis elementet **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="54234-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="54234-172">Vis elementet **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="54234-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="54234-173">Datakilden **Model**.**Data2.Summary2** konfigureres til å gruppere transaksjonsdetaljene for datakilden **Model.Data.Summary** etter avgiftsnivå (returneres av det beregnede feltet **Model.Data.Summary.Level**) og beregne aggregeringene.</span><span class="sxs-lookup"><span data-stu-id="54234-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Siden Formatutforming som viser detaljer om datakilden Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="54234-175">Gå gjennom de beregnede feltene **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="54234-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="54234-176">Disse beregnede feltene brukes til å filtrere postlistene **Model**.**Data2. Summary2** og bare returnere poster som representerer et bestemt avgiftsnivå.</span><span class="sxs-lookup"><span data-stu-id="54234-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="54234-177">Lukk **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="54234-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="54234-178">Opprette et avledet format</span><span class="sxs-lookup"><span data-stu-id="54234-178">Create a derived format</span></span>
<span data-ttu-id="54234-179">Du kan forbedre det angitte formatet ved å legge til ett beregnet felt for å filtrere det nødvendige avgiftsnivået i stedet for å bruke de eksisterende tre feltene: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="54234-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="54234-180">Nødvendig avgiftsnivå kan angis der dette nye beregnede feltet vil bli kalt.</span><span class="sxs-lookup"><span data-stu-id="54234-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="54234-181">I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="54234-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="54234-182">Velg **Format for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="54234-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="54234-183">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="54234-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="54234-184">Velg **Avled fra navn: Format for å lære om parameterkall, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="54234-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="54234-185">I **Navn**-feltet angir du **Format for å lære om parameterkall (tilpasset)**.</span><span class="sxs-lookup"><span data-stu-id="54234-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="54234-186">Velg **Opprett konfigurasjon**</span><span class="sxs-lookup"><span data-stu-id="54234-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="54234-187">Konfigurere et parameterberegnet felt som returnerer en liste med poster</span><span class="sxs-lookup"><span data-stu-id="54234-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="54234-188">Begynne å legge til et nytt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="54234-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="54234-189">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="54234-189">Select **Designer**.</span></span>
2. <span data-ttu-id="54234-190">Velg **Vis/skjul** for å vise alle formatelementer.</span><span class="sxs-lookup"><span data-stu-id="54234-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="54234-191">Velg **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="54234-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="54234-192">Vis elementet **Model**.</span><span class="sxs-lookup"><span data-stu-id="54234-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="54234-193">Velg elementet **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="54234-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="54234-194">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="54234-194">Select **Add**.</span></span>
7. <span data-ttu-id="54234-195">Velg **Funksjoner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="54234-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="54234-196">Angi **Nivåer** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54234-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="54234-197">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="54234-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="54234-198">Definere en parameter for å legge til et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="54234-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="54234-199">Velg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="54234-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="54234-200">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="54234-200">Select **New**.</span></span>
3. <span data-ttu-id="54234-201">I **Navn**-feltet angir du **Avgiftsnivå**.</span><span class="sxs-lookup"><span data-stu-id="54234-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="54234-202">Velg **Streng** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54234-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="54234-203">Bare primitive datatyper kan brukes til å angi typen for parameterens argument.</span><span class="sxs-lookup"><span data-stu-id="54234-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="54234-204">Derfor kan ikke typene **Postliste**, **Post** og **Opplisting** brukes til dette formålet.</span><span class="sxs-lookup"><span data-stu-id="54234-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="54234-205">Det maksimale antallet parametere som kan angis for ett enkelt beregnet felt er 8.</span><span class="sxs-lookup"><span data-stu-id="54234-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Kildeliste for parameterdata](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="54234-207">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54234-207">Select **OK**.</span></span>

<span data-ttu-id="54234-208">Ved å legge til denne parameteren angir du betingelsen som må være tilstede for å kalle dette beregnede feltet.</span><span class="sxs-lookup"><span data-stu-id="54234-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="54234-209">Når du kaller dette beregnede feltet, må du sette argumentet for parameteren **Avgiftsnivå** til en verdi i **Streng**-format.</span><span class="sxs-lookup"><span data-stu-id="54234-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="54234-210">Pass på at du bare definerer parametere for de beregnede feltene som finnes seg i en container (enten **Postliste**, **Post** eller **Container**).</span><span class="sxs-lookup"><span data-stu-id="54234-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="54234-211">Den konfigurerte parameteren er tilgjengelig i listen over datakilder for dette beregnede feltet.</span><span class="sxs-lookup"><span data-stu-id="54234-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="54234-212">Du kan legge til parameteren i det konfigurerte uttrykket ved å velge **Legg til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="54234-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Datakildefelt](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="54234-214">Definere et uttrykk for å legge til et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="54234-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="54234-215">I **Formel**-feltet angir du:</span><span class="sxs-lookup"><span data-stu-id="54234-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="54234-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="54234-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="54234-217">Velg parameteren **Avgiftsnivå** i listen over datakilder.</span><span class="sxs-lookup"><span data-stu-id="54234-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="54234-218">Velg **Legg til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="54234-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="54234-219">I **Formel**-feltet fullfører du uttrykket slik:</span><span class="sxs-lookup"><span data-stu-id="54234-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="54234-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Avgiftsnivå')**</span><span class="sxs-lookup"><span data-stu-id="54234-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="54234-221">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="54234-221">Select **Save**.</span></span>

    ![Informasjon for datakildefelt](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="54234-223">Lukk siden **Formelutforming**.</span><span class="sxs-lookup"><span data-stu-id="54234-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="54234-224">Fullfør å legge til et nytt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="54234-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="54234-225">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54234-225">Select **OK**.</span></span>

<span data-ttu-id="54234-226">På siden **Formatutforming** krever det konfigurerte parameterberegnede feltet **Nivåer** et **Streng**-argument.</span><span class="sxs-lookup"><span data-stu-id="54234-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Vist liste over nivåer for beregnede felt](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements&quot;></a><span data-ttu-id=&quot;54234-228&quot;>Bruke det konfigurerte beregnede feltet til binding av formatelementer</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-228&quot;>Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id=&quot;54234-229&quot;>Velg **Model.Data2.Levels** for å velge det konfigurerte beregnede feltet.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-229&quot;>Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id=&quot;54234-230&quot;>Velg formatelementet **Statement.Taxation.Regular**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-230&quot;>Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id=&quot;54234-231&quot;>Velg **Bind**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-231&quot;>Select **Bind**.</span></span>
4. <span data-ttu-id=&quot;54234-232&quot;>Velg **Ja** for å bekrefte veksling av gjeldende brukerdatakilde, **Level1**, til den nye datakilden, **Levels**, i alle kjedede formatelementer i det valgte formatelementet.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-232&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id=&quot;54234-233&quot;>Brukt binding er bygget som et kall til det parameterberegnede feltet.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-233&quot;>Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id=&quot;54234-234&quot;>Som standard brukes navnet på det bundne formatelementet som et argument for parameterberegnede felt under følgende betingelser:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-234&quot;>By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id=&quot;54234-235&quot;>Det beregnede feltet er konfigurert til å bruke én enkelt parameter.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-235&quot;>The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id=&quot;54234-236&quot;>Datatypen for denne parameteren er definert som **Streng**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-236&quot;>The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id=&quot;54234-237&quot;>Når navnet på det bundne formatelementet er tomt, brukes datakildenavnet for dette elementet i den brukte bindingen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-237&quot;>When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id=&quot;54234-238&quot;>Velg formatelementet **Statement.Taxation.Reduced**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-238&quot;>Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id=&quot;54234-239&quot;>Velg **Bind**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-239&quot;>Select **Bind**.</span></span>
7. <span data-ttu-id=&quot;54234-240&quot;>Velg **Ja** for å bekrefte veksling av gjeldende brukerdatakilde, **Level2**, til den nye datakilden, **Levels**, i alle kjedede formatelementer under det valgte formatelementet.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-240&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id=&quot;54234-241&quot;>Velg formatelementet **Statement.Taxation.None**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-241&quot;>Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id=&quot;54234-242&quot;>Velg **Bind**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-242&quot;>Select **Bind**.</span></span>
10. <span data-ttu-id=&quot;54234-243&quot;>Velg **Ja** for å bekrefte veksling av gjeldende brukerdatakilde, **Level3**, til den nye datakilden, **Levels**, i alle kjedede formatelementer under det valgte formatelementet.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;54234-243&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id=&quot;54234-244&quot;>Når du angir argumentet for det parameterberegnede feltet for XML-elementet som representerer et avgiftsnivå (for eksempel **Model.Data2.Levels(&quot;Redusert")** som en tekstverdi), trenger du ikke gjøre det samme for kjedede XML-attributter. Bindingene deres arver automatisk verdien til argumentet som er definert på overordnet nivå (**Model.Data2.Levels.aggregated.Base**, ikke **Model.Data2.Levels("Redusert").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="54234-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="54234-245">Gjentakende kall til parameterberegnede felt støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="54234-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="54234-246">Du kan velge **Rediger formel** og endre argumentet som brukes om standard for det parameterberegnede feltet i den valgte bindingen.</span><span class="sxs-lookup"><span data-stu-id="54234-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="54234-247">Hvis dette argumentet mangler, kan det føre til feil ved kjøretid – brukerne får beskjed om en slik situasjon når gjeldende format blir validert.</span><span class="sxs-lookup"><span data-stu-id="54234-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Varsling om valideringsadvarsel](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="54234-249">Konfigurere et parameterberegnede felt til å returnere en post</span><span class="sxs-lookup"><span data-stu-id="54234-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="54234-250">Når et parameterberegnet felt returnerer en post, må du støtte binding av enkeltfelt til formatelementer i denne posten.</span><span class="sxs-lookup"><span data-stu-id="54234-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="54234-251">I slike tilfeller er det ingen overordnet binding som inneholder verdien til et argument for å kalle et parameterberegnet felt. Denne verdien må være definert i bindingen til feltet for en enkeltpost.</span><span class="sxs-lookup"><span data-stu-id="54234-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="54234-252">Begynne å legge til et nytt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="54234-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="54234-253">Velg elementet **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="54234-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="54234-254">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="54234-254">Select **Add**.</span></span>
3. <span data-ttu-id="54234-255">Velg **Funksjoner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="54234-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="54234-256">Angi **LevelRecord** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54234-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="54234-257">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="54234-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="54234-258">Definere en parameter for å legge til et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="54234-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="54234-259">Velg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="54234-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="54234-260">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="54234-260">Select **New**.</span></span>
3. <span data-ttu-id="54234-261">I **Navn**-feltet angir du **Avgiftsnivå**.</span><span class="sxs-lookup"><span data-stu-id="54234-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="54234-262">Velg **Streng** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54234-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="54234-263">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54234-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="54234-264">Definere et uttrykk for å legge til et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="54234-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="54234-265">I **Formel**-feltet angir du følgende:</span><span class="sxs-lookup"><span data-stu-id="54234-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="54234-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="54234-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="54234-267">Velg parameteren **Avgiftsnivå**.</span><span class="sxs-lookup"><span data-stu-id="54234-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="54234-268">Velg **Legg til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="54234-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="54234-269">I **Formel**-feltet legger du til **Avgiftsnivå))** i det du skrev inn i trinn 1, for å fullføre uttrykket slik:</span><span class="sxs-lookup"><span data-stu-id="54234-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="54234-270">**FIRSTORNULL(\@.Levels('Avgiftsnivå'))**</span><span class="sxs-lookup"><span data-stu-id="54234-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="54234-271">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="54234-271">Select **Save**.</span></span>
6. <span data-ttu-id="54234-272">Lukk siden **Formelutforming**.</span><span class="sxs-lookup"><span data-stu-id="54234-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="54234-273">Fullfør å legge til et nytt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="54234-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="54234-274">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54234-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="54234-275">Bruke det konfigurerte beregnede feltet til å binde formatelementer</span><span class="sxs-lookup"><span data-stu-id="54234-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="54234-276">Vis **Model.Data2.LevelRecord** for å velge det konfigurerte beregnede feltet.</span><span class="sxs-lookup"><span data-stu-id="54234-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="54234-277">Vid **Model.Data2.LevelRecord.aggregated**-container for det konfigurerte beregnede feltet.</span><span class="sxs-lookup"><span data-stu-id="54234-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="54234-278">Velg feltet **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="54234-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="54234-279">Velg formatelementet **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="54234-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="54234-280">Velg **Opphev binding**.</span><span class="sxs-lookup"><span data-stu-id="54234-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="54234-281">Velg formatelementet **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="54234-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="54234-282">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="54234-282">Select **Bind**.</span></span>
8. <span data-ttu-id="54234-283">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="54234-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="54234-284">Endre uttrykket til **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="54234-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Oppdatert uttrykk](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="54234-286">Fjerne beregnede felt som ikke brukes</span><span class="sxs-lookup"><span data-stu-id="54234-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="54234-287">Velg **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="54234-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="54234-288">Velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="54234-288">Select **Delete**.</span></span>
3. <span data-ttu-id="54234-289">Velg **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="54234-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="54234-290">Velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="54234-290">Select **Delete**.</span></span>
5. <span data-ttu-id="54234-291">Velg **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="54234-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="54234-292">Velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="54234-292">Select **Delete**.</span></span>
7. <span data-ttu-id="54234-293">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="54234-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="54234-294">Du brukte det samme beregnede feltet, **Model.Data2.Levels**, flere ganger i formatbindinger.</span><span class="sxs-lookup"><span data-stu-id="54234-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="54234-295">Det er mye enklere å bruke og vedlikeholde ett enkelt beregnet felt i stedet for å gjøre dette for flere lignende felt.</span><span class="sxs-lookup"><span data-stu-id="54234-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="54234-296">Lukk **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="54234-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="54234-297">Fullstendig justert versjon av et avledet format</span><span class="sxs-lookup"><span data-stu-id="54234-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="54234-298">I hurtigfanen **Versjoner** velger du **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="54234-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="54234-299">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="54234-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="54234-300">Eksporter fullført versjon av et avledet format</span><span class="sxs-lookup"><span data-stu-id="54234-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="54234-301">Velg formatet **Format for å lære om parameterkall (tilpasset)** i konfigurasjonstreet.</span><span class="sxs-lookup"><span data-stu-id="54234-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="54234-302">I hurtigfanen **Versjoner** velger du den fullførte versjon 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="54234-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="54234-303">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="54234-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="54234-304">Velg **Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="54234-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="54234-305">Lagre den nedlastede konfigurasjonen lokalt i XML-format.</span><span class="sxs-lookup"><span data-stu-id="54234-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="54234-306">Teste ER-formater</span><span class="sxs-lookup"><span data-stu-id="54234-306">Test ER formats</span></span> 
<span data-ttu-id="54234-307">Du kan kjøre de opprinnelige og forbedrede ER-formatene for å sikre at konfigurerte parameterberegnede felt fungerer slik de skal.</span><span class="sxs-lookup"><span data-stu-id="54234-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="54234-308">Importere ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="54234-308">Import ER configurations</span></span>
<span data-ttu-id="54234-309">Du kan importere gjennomgåtte konfigurasjoner fra RCS ved å bruke ER-repositoriet til **RCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="54234-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="54234-310">Hvis du allerede har gått gjennom trinnene gjort i emnet [Importere konfigurasjoner for elektronisk rapportering (ER) fra Regulatory Configuration Services](rcs-download-configurations.md), bruker du det konfigurerte ER-repositoriet til å importere konfigurasjoner som er beskrevet tidligere i dette emnet, til miljøet.</span><span class="sxs-lookup"><span data-stu-id="54234-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="54234-311">Hvis ikke følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="54234-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="54234-312">Velg firmaet **DEMF**, og velg **Elektronisk rapportering** på standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="54234-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="54234-313">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="54234-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="54234-314">Importer konfigurasjonene fra Microsoft Download Center i følgende rekkefølge: datamodell, modelltilordning, format.</span><span class="sxs-lookup"><span data-stu-id="54234-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="54234-315">Fullfør trinnene nedenfor for hver ER-konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="54234-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="54234-316">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="54234-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="54234-317">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="54234-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="54234-318">Velg **Bla gjennom** for å velge den nødvendige ER-konfigurasjonen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="54234-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="54234-319">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54234-319">Select **OK**.</span></span>

4. <span data-ttu-id="54234-320">Importer den eksporterte fra RCS-fullført versjon 1.1.1 i formatet **Format for å lære om parameterkall (tilpasset)**:</span><span class="sxs-lookup"><span data-stu-id="54234-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="54234-321">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="54234-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="54234-322">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="54234-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="54234-323">Velg **Bla gjennom** for å velge filen i **Format for å lære om parameterkall (tilpasset)** i XML-format.</span><span class="sxs-lookup"><span data-stu-id="54234-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="54234-324">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54234-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="54234-325">Kjøre ER-formater</span><span class="sxs-lookup"><span data-stu-id="54234-325">Run ER formats</span></span>

1. <span data-ttu-id="54234-326">I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="54234-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="54234-327">Velg **Format for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="54234-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="54234-328">Velg **Kjør** på det øverste båndet.</span><span class="sxs-lookup"><span data-stu-id="54234-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="54234-329">Lagre de lokalt genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="54234-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="54234-330">Velg elementet **Format for å lære om parameterkall (tilpasset)**.</span><span class="sxs-lookup"><span data-stu-id="54234-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="54234-331">Velg **Kjør** på det øverste båndet.</span><span class="sxs-lookup"><span data-stu-id="54234-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="54234-332">Lagre de genererte utdataene lokalt.</span><span class="sxs-lookup"><span data-stu-id="54234-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="54234-333">Sammenlign innholdet i de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="54234-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54234-334">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="54234-334">Additional resources</span></span>

- [<span data-ttu-id="54234-335">Formeldesigner i elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="54234-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="54234-336">Forbedre ytelse for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT</span><span class="sxs-lookup"><span data-stu-id="54234-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]