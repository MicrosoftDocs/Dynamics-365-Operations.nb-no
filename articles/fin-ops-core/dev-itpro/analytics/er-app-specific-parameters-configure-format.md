---
title: Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet
description: Dette emnet forklarer hvordan du kan konfigurere elektroniske rapporter (ER)-formater til å bruke parametere som angis per juridisk enhet.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: d32da76ee46ff5293ae8fefb16d251564b6be21a
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694252"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="195c3-103">Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="195c3-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="195c3-104">Oversikt</span><span class="sxs-lookup"><span data-stu-id="195c3-104">Overview</span></span>

<span data-ttu-id="195c3-105">I mange av formatene for elektronisk rapportering (ER) som du vil utforme, må du filtrere data ved hjelp av et verdisett som er spesifikke for hver juridiske enhet for forekomsten (for eksempel et sett med mva-koder for å filtrere mva-transaksjoner).</span><span class="sxs-lookup"><span data-stu-id="195c3-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="195c3-106">Når filtrering av denne typen er konfigurert i et ER-format, brukes verdier som er avhengige av den juridiske enheten (for eksempel skattekoder) i uttrykk med ER-formatet for å angi datafiltreringsregler.</span><span class="sxs-lookup"><span data-stu-id="195c3-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="195c3-107">Derfor er formatet opprettet juridisk enhet-spesifikt, og hvis du vil generere de nødvendige rapportene, må du opprette avledede kopier av det opprinnelige ER-formatet for hver juridiske enhet der du må kjøre ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="195c3-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="195c3-108">Hvert avledede ER-format må redigeres for å hente juridisk enhet-spesifikke verdier til den, basert på nytt når den opprinnelige versjonen (basis) er oppdatert, eksportert fra et testmiljø og importeres til et produksjonsmiljø når det må distribueres for produksjonsbruk, og så videre.</span><span class="sxs-lookup"><span data-stu-id="195c3-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="195c3-109">Derfor er vedlikehold av denne typen konfigurert ER-løsning ganske kompleks og tidkrevende av flere årsaker:</span><span class="sxs-lookup"><span data-stu-id="195c3-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="195c3-110">Jo flere juridiske enheter det er, jo flere ER-formatkonfigurasjoner må vedlikeholdes.</span><span class="sxs-lookup"><span data-stu-id="195c3-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="195c3-111">Vedlikehold av ER-konfigurasjoner krever at bedriftsbrukere har kjennskap til ER.</span><span class="sxs-lookup"><span data-stu-id="195c3-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="195c3-112">De ER-programspesifikke parameterne gjør det mulig for privilegerte brukere å konfigurere datafiltrering i et ER-format slik at det er basert på et sett med abstrakte regler.</span><span class="sxs-lookup"><span data-stu-id="195c3-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="195c3-113">Dette settet med regler kan konfigureres til å bruke datakildene som er tilgjengelige i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="195c3-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="195c3-114">Forretningsbrukere kan deretter angi reelle regler utenfor ER-rammeverket ved hjelp av brukergrensesnittet som automatisk genereres basert på innstillingene i det tilsvarende ER-formatet, og de gjeldende dataene for juridisk enhet blir åpnet av datakildene for ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="195c3-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="195c3-115">Regelsettet som er angitt for et ER-format, kan eksporteres fra den gjeldende juridiske enheten for Dynamics 365 Finance (Finance)-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="195c3-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="195c3-116">Det kan deretter importeres til en annen juridisk enhet av enten samme Finance-forekomst eller en annen forekomst som et sett med regler for samme ER-format.</span><span class="sxs-lookup"><span data-stu-id="195c3-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="195c3-117">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="195c3-117">Prerequisites</span></span>

<span data-ttu-id="195c3-118">For å fullføre eksemplene i dette emnet må du har tilgang til forekomsten av Regulatory Configuration Service (RCS) som er klargjort for samme leietaker som Finance and Operations, for én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="195c3-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="195c3-119">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="195c3-119">Electronic reporting developer</span></span>
- <span data-ttu-id="195c3-120">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="195c3-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="195c3-121">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="195c3-121">System administrator</span></span>

<span data-ttu-id="195c3-122">Vi anbefaler at du fullfører trinnene i emnet [Støtte for parametriserte kall av ER-datakilder av felttypen Beregnet](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="195c3-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="195c3-123">Hvis du allerede har fullført disse trinnene, kan du hoppe over trinnene i **Importere ER-konfigurasjoner til RCS**.</span><span class="sxs-lookup"><span data-stu-id="195c3-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="195c3-124">Importere ER-konfigurasjoner til RCS</span><span class="sxs-lookup"><span data-stu-id="195c3-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="195c3-125">Fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448) kan du laste ned den pakkede (komprimerte) filen **Støtte for parametriserte kall av ER-datakilder av felttypen Beregnet**.</span><span class="sxs-lookup"><span data-stu-id="195c3-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="195c3-126">Den inneholder følgende ER-konfigurasjoner som må pakkes ut og lagres lokalt.</span><span class="sxs-lookup"><span data-stu-id="195c3-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="195c3-127">**Innholdsbeskrivelse**</span><span class="sxs-lookup"><span data-stu-id="195c3-127">**Content description**</span></span>                        | <span data-ttu-id="195c3-128">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="195c3-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="195c3-129">Eksempel på konfigurasjonsfilen **ER-datamodell**</span><span class="sxs-lookup"><span data-stu-id="195c3-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="195c3-130">Modell for å lære om parameterkall.versjon.1.XML</span><span class="sxs-lookup"><span data-stu-id="195c3-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="195c3-131">Eksempel på konfigurasjonsfilen **ER-metadata**</span><span class="sxs-lookup"><span data-stu-id="195c3-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="195c3-132">Metadata for å lære om parameterkall.versjon.1.XML</span><span class="sxs-lookup"><span data-stu-id="195c3-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="195c3-133">Eksempel på konfigurasjonsfilen **ER-modelltilordning**</span><span class="sxs-lookup"><span data-stu-id="195c3-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="195c3-134">Tilordning for å lære om parameterkall.versjon.1.1.XML</span><span class="sxs-lookup"><span data-stu-id="195c3-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="195c3-135">Eksempel på **ER-format**-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="195c3-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="195c3-136">Format for å lære om parameterkall.versjon.1.1.XML</span><span class="sxs-lookup"><span data-stu-id="195c3-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="195c3-137">Logg deretter på RCS-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="195c3-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="195c3-138">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="195c3-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="195c3-139">Før du kan fullføre trinnene i denne prosedyren må du fullføre prosedyren i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS.</span><span class="sxs-lookup"><span data-stu-id="195c3-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="195c3-140">Velg **Elektronisk rapportering** på standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="195c3-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="195c3-141">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="195c3-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="195c3-142">Importer de nedlastede ER-konfigurasjonene til RCS i følgende rekkefølge: datamodell, metadata, modelltilordning, format.</span><span class="sxs-lookup"><span data-stu-id="195c3-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="195c3-143">For hver ER-konfigurasjon følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="195c3-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="195c3-144">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="195c3-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="195c3-145">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="195c3-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="195c3-146">Velg **Bla gjennom** for å velge den riktige filen for den nødvendige ER-konfigurasjonen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="195c3-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="195c3-147">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="195c3-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="195c3-148">Se gjennom den angitte ER-løsningen</span><span class="sxs-lookup"><span data-stu-id="195c3-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="195c3-149">I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="195c3-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="195c3-150">Velg elementet **Format for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="195c3-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="195c3-151">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="195c3-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="195c3-152">Velg **Vis/skjul**.</span><span class="sxs-lookup"><span data-stu-id="195c3-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="195c3-153">ER-formatet **Format for å lære om parameterkall** er utformet for å generere en skatteoppgave i XML-format som viser flere nivåer med avgifter (vanlig, redusert og ingen).</span><span class="sxs-lookup"><span data-stu-id="195c3-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="195c3-154">Hvert nivå har et ulikt antall detaljer.</span><span class="sxs-lookup"><span data-stu-id="195c3-154">Each level has a different number of details.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="195c3-156">Utvid elementene **Modell**, **Data** og **Sammendrag** i kategorien **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="195c3-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="195c3-157">Datakilden **Model.Data.Summary** returnerer listen over mva-transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="195c3-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="195c3-158">Disse transaksjonene er oppført etter mva-kode.</span><span class="sxs-lookup"><span data-stu-id="195c3-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="195c3-159">For denne datakilden er det beregnede **Model.Data.Summary.Level**-feltet konfigurert til å returnere koden for avgiftsnivået for hver summerte post.</span><span class="sxs-lookup"><span data-stu-id="195c3-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="195c3-160">For alle avgiftskoder som kan hentes fra **Model.Data.Summary**-datakilden ved kjøretid, returnerer det beregnede feltet avgiftsnivåkode (**Vanlig**, **Redusert**, **Ingen** eller **Annet**) som en tekstverdi.</span><span class="sxs-lookup"><span data-stu-id="195c3-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="195c3-161">Det beregnede **Model.Data.Summary.Level**-feltet brukes til å filtrere poster for **Model.Data.Summary**-datakilden og angi de filtrerte dataene i hvert XML-element som representerer et avgiftsnivå ved hjelp av feltene **Model.Data2.Level1**, **Model.Data2.Level2** og **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="195c3-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="195c3-163">Det beregnede **Model.Data.Summary.Level**-feltet er konfigurert slik at det inneholder et ER-uttrykk.</span><span class="sxs-lookup"><span data-stu-id="195c3-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="195c3-164">Legg merke til at avgiftskoder (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** og **InVAT0**) er hardkodet til denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="195c3-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="195c3-165">Derfor er dette ER-formatet avhengig av den juridiske enheten der disse avgiftskodene ble konfigurert.</span><span class="sxs-lookup"><span data-stu-id="195c3-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="195c3-167">Hvis du vil støtte et annet sett med mva-koder for hver juridiske enhet, må du følge denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="195c3-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="195c3-168">Opprett en avledet versjon av ER-formatet for hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="195c3-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="195c3-169">Oppdater avgiftskodene i det beregnede **Model.Data.Summary.Level**-feltet, basert på innstillingen for juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="195c3-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="195c3-170">Lukk **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="195c3-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="195c3-171">Opprette et avledet format</span><span class="sxs-lookup"><span data-stu-id="195c3-171">Create a derived format</span></span>

<span data-ttu-id="195c3-172">Deretter skal du bruke funksjonen for ER-programspesifikke parametere til å støtte et annet sett med mva-koder for hver juridiske enhet i ett enkelt ER-format.</span><span class="sxs-lookup"><span data-stu-id="195c3-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="195c3-173">I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="195c3-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="195c3-174">Velg elementet **Format for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="195c3-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="195c3-175">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="195c3-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="195c3-176">Velg alternativet **Avled fra navn: Format for å lære om parameterkall, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="195c3-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="195c3-177">I **Navn**-feltet angir du **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="195c3-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="195c3-178">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="195c3-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="195c3-179">Konfigurere et avledet format</span><span class="sxs-lookup"><span data-stu-id="195c3-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="195c3-180">Legge til en formatopplisting</span><span class="sxs-lookup"><span data-stu-id="195c3-180">Add a format enumeration</span></span>

<span data-ttu-id="195c3-181">Deretter legger du til en ny ER-formatopplisting.</span><span class="sxs-lookup"><span data-stu-id="195c3-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="195c3-182">Verdiene for denne formatopplistingen vil bli presentert for forretningsbrukere, som vil angi juridisk enhetsavhengige sett med mva-koder for de ulike avgiftsnivåene som brukes i ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="195c3-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="195c3-183">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="195c3-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="195c3-184">Velg **Formatopplistinger**.</span><span class="sxs-lookup"><span data-stu-id="195c3-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="195c3-185">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="195c3-185">Select **Add**.</span></span>
4.  <span data-ttu-id="195c3-186">I **Navn**-feltet angir du **Liste over avgiftsnivåer**.</span><span class="sxs-lookup"><span data-stu-id="195c3-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="195c3-187">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="195c3-187">Select **Save**.</span></span>
6.  <span data-ttu-id="195c3-188">Velg **Legg til** i kategorien **Verdier for formatopplisning**.</span><span class="sxs-lookup"><span data-stu-id="195c3-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="195c3-189">I **Navn**-feltet angir du **Vanlig avgift**.</span><span class="sxs-lookup"><span data-stu-id="195c3-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="195c3-190">Velg **Legg til** på nytt.</span><span class="sxs-lookup"><span data-stu-id="195c3-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="195c3-191">I **Navn**-feltet angir du **Redusert avgift**.</span><span class="sxs-lookup"><span data-stu-id="195c3-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="195c3-192">Velg **Legg til** på nytt.</span><span class="sxs-lookup"><span data-stu-id="195c3-192">Select **Add** again.</span></span>
11. <span data-ttu-id="195c3-193">I **Navn**-feltet angir du **Ingen avgift**.</span><span class="sxs-lookup"><span data-stu-id="195c3-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="195c3-194">Velg **Legg til** på nytt.</span><span class="sxs-lookup"><span data-stu-id="195c3-194">Select **Add** again.</span></span>
13. <span data-ttu-id="195c3-195">Angi **Annet** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="195c3-195">In the **Name** field, enter **Other**.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="195c3-197">Siden forretningsbrukerne kan bruke forskjellige språk til å angi juridisk enhetsavhengige sett med avgiftskoder, anbefaler vi at du oversetter verdiene for denne opplistingen til språkene som er konfigurert som foretrukne språk for disse brukerne i Økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="195c3-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="195c3-198">Velg posten **Ingen avgift**.</span><span class="sxs-lookup"><span data-stu-id="195c3-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="195c3-199">Klikk i **Etikett**-feltet.</span><span class="sxs-lookup"><span data-stu-id="195c3-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="195c3-200">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="195c3-200">Select **Translate**.</span></span>
17. <span data-ttu-id="195c3-201">Angi **LBL_LEVELENUM_NO** i **Tekstoversettelse**-ruten i **Etikett-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="195c3-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="195c3-202">I feltet **Tekst på standardspråk** angir du **Ingen avgift**.</span><span class="sxs-lookup"><span data-stu-id="195c3-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="195c3-203">I **Språk**-feltet velger du **DE**.</span><span class="sxs-lookup"><span data-stu-id="195c3-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="195c3-204">I **Oversatt tekst**-feltet angir du **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="195c3-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="195c3-205">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="195c3-205">Select **Translate**.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="195c3-207">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="195c3-207">Select **Save**.</span></span>
23. <span data-ttu-id="195c3-208">Lukk **Formatopplistinger**-siden.</span><span class="sxs-lookup"><span data-stu-id="195c3-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="195c3-209">Legg til en ny datakilde for oppslag</span><span class="sxs-lookup"><span data-stu-id="195c3-209">Add a new lookup data source</span></span>

<span data-ttu-id="195c3-210">Deretter legger du til en ny datakilde for å angi hvordan forretningsbrukere skal angi juridisk enhetsavhengige relger for å gjenkjenne det riktige avgiftsnivået for hver summerte transaksjonsoppføring.</span><span class="sxs-lookup"><span data-stu-id="195c3-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="195c3-211">Velg **Legg til** i **Tilordning**-fanen.</span><span class="sxs-lookup"><span data-stu-id="195c3-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="195c3-212">Velg **Formatopplisting\Oppslag**.</span><span class="sxs-lookup"><span data-stu-id="195c3-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="195c3-213">Du har nettopp identifisert at hver regel som forretningsbrukere angir for avgiftsnivågjenkjenning vil returnere en verdi for en ER-formatopplisting.</span><span class="sxs-lookup"><span data-stu-id="195c3-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="195c3-214">Legg merke til at du får tilgang til **Oppslag**-datakildetypen under **Datamodell** og **Dynamics 365 for Operations**-blokker i tillegg til **Formatopplisning**-blokken.</span><span class="sxs-lookup"><span data-stu-id="195c3-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="195c3-215">Derfor kan det brukes ER-datamodellopplistinger og programopplisninger til å angi typen verdier som returneres for datakilder av denne typen.</span><span class="sxs-lookup"><span data-stu-id="195c3-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="195c3-216">Angi **Velger** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="195c3-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="195c3-217">I **Formatopplisning**-feltet velger du **Liste over avgiftsnivåer**.</span><span class="sxs-lookup"><span data-stu-id="195c3-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="195c3-218">Du har akkurat angitt at en forretningsbruker må velge en av verdiene i formatopplisningen **Liste over avgiftsnivåer** som en retur verdi for hver regel som er angitt i denne datakilden.</span><span class="sxs-lookup"><span data-stu-id="195c3-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="195c3-219">Velg **Rediger oppslag**.</span><span class="sxs-lookup"><span data-stu-id="195c3-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="195c3-220">Velg **Kolonner**.</span><span class="sxs-lookup"><span data-stu-id="195c3-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="195c3-221">Vis elementet **Model**.</span><span class="sxs-lookup"><span data-stu-id="195c3-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="195c3-222">Vis elementet **Data**.</span><span class="sxs-lookup"><span data-stu-id="195c3-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="195c3-223">Vis elementet **Avgift**.</span><span class="sxs-lookup"><span data-stu-id="195c3-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="195c3-224">Velg elementet **Model.Data.Tax.Code**.</span><span class="sxs-lookup"><span data-stu-id="195c3-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="195c3-225">Velg **Legg til**-knappen (høyre pilen).</span><span class="sxs-lookup"><span data-stu-id="195c3-225">Select the **Add** button (the right arrow).</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="195c3-227">Du har akkurat angitt at en forretningsbruker må velge en av avgiftskodene som en betingelse for hver regel som er angitt i denne datakilden for avgiftsnivågjenkjenning.</span><span class="sxs-lookup"><span data-stu-id="195c3-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="195c3-228">Listen over avgiftskoder som firmabrukeren kan velge, vil bli returnert av **Model.Data.Tax**-datakilden.</span><span class="sxs-lookup"><span data-stu-id="195c3-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="195c3-229">Siden denne datakilden inneholder **Navn**-feltet, vises navnet på mva-koden for hver mva-kodeverdi i oppslaget som presenteres for forretningsbrukeren.</span><span class="sxs-lookup"><span data-stu-id="195c3-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="195c3-230">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="195c3-230">Select **OK**.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="195c3-232">Forretningsbrukere kan legge til flere regler som poster i denne datakilden.</span><span class="sxs-lookup"><span data-stu-id="195c3-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="195c3-233">Hver post vil bli nummerert med en linjekode.</span><span class="sxs-lookup"><span data-stu-id="195c3-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="195c3-234">Regler vil bli evaluert i stigende linjenummer.</span><span class="sxs-lookup"><span data-stu-id="195c3-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="195c3-235">Fordi du valgte **Mva-kode**-feltet som en betingelse for regler i denne oppslagsdatakilden, og fordi **Mva-kode** er definert som et felt av **Streng**-datatypen, evalueres hver regel ved kjøring ved å sammenligne avgiftskoden som sendes til datakilden med mva-koden som er definert i denne posten for datakilden.</span><span class="sxs-lookup"><span data-stu-id="195c3-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="195c3-236">Når en regel som er i samsvar med den konfigurerte betingelsen, blir funnet, returnerer denne datakilden oppslagsverdien for regelen som er definert i **Oppslagsresultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="195c3-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="195c3-237">Hvis ingen regel blir funnet, oppstår det et unntak for å varsle brukeren om at den gjeldende datakilden ikke kan returnere en riktig verdi.</span><span class="sxs-lookup"><span data-stu-id="195c3-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="195c3-238">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="195c3-238">Select **Save**.</span></span>
14. <span data-ttu-id="195c3-239">Lukk **Oppslagsutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="195c3-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="195c3-240">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="195c3-240">Select **OK**.</span></span>

    <span data-ttu-id="195c3-241">Legg merke til at du har lagt til en ny datakilde som returnerer avgiftsnivået som verdien for formatopplistingen **Liste over avgiftsnivåer** for en mva-kode som sendes til datakilden som argument for **kode**-parameteren til datatypen **streng**.</span><span class="sxs-lookup"><span data-stu-id="195c3-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="195c3-243">Legg merke til at evalueringen av konfigurerte regler avhenger av datatypen til feltene som er valgt for å definere betingelsene for disse reglene.</span><span class="sxs-lookup"><span data-stu-id="195c3-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="195c3-244">Når du velger et felt som er konfigurert som et felt enten for datatypen **numerisk** eller **dato**, vil vilkårene være forskjellige fra vilkårene som ble beskrevet tidligere for datatypen **streng**.</span><span class="sxs-lookup"><span data-stu-id="195c3-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="195c3-245">For **numerisk**- og **data**-felt må regelen angis som et verdiområde.</span><span class="sxs-lookup"><span data-stu-id="195c3-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="195c3-246">Betingelsen for regelen vil da anses som oppfylt når en verdi som sendes til datakilden, er i det konfigurerte området.</span><span class="sxs-lookup"><span data-stu-id="195c3-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="195c3-247">Illustrasjonen nedenfor viser et eksempel på denne typen oppsett.</span><span class="sxs-lookup"><span data-stu-id="195c3-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="195c3-248">I tillegg til **Model.Data.Tax.Code**-feltet i **streng**-datatypen brukes **Model.Tax.Summary.Base**-feltet for **Real**-datatypen til å angi betingelser for en oppslagsdatakilde.</span><span class="sxs-lookup"><span data-stu-id="195c3-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="195c3-250">Fordi feltene **Model.Data.Tax.Code** og **Model.Tax.Summary.Base** er valgt for denne oppslagsdatakilden, konfigureres hver regel for denne datakilden på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="195c3-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="195c3-251">I listen som vises, må verdien i formatopplistingen **Liste over avgiftsnivåer** velges som en returnert verdi.</span><span class="sxs-lookup"><span data-stu-id="195c3-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="195c3-252">Mva-koden må angis som en betingelse for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="195c3-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="195c3-253">Bare avgiftskoder som tilbys av modellen **Model.Data.Tax**-datakilden, er gjeldende.</span><span class="sxs-lookup"><span data-stu-id="195c3-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="195c3-254">Minimums- og maksimumsverdiene for avgiftsgrunnlagsbeløpet må angis som betingelser for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="195c3-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="195c3-255">Slik blir hver regel i denne datakilden evaluert ved kjøretid:</span><span class="sxs-lookup"><span data-stu-id="195c3-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="195c3-256">Er koden for **streng**-datatypen som ble sendt til denne datakilden, lik mva-koden for en regel?</span><span class="sxs-lookup"><span data-stu-id="195c3-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="195c3-257">Faller verdien av **Real**-datatypen som ble sendt til denne datakilden, mellom bestemte minimums- og maksimumsverdier?</span><span class="sxs-lookup"><span data-stu-id="195c3-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="195c3-258">En regel blir ansett som gjeldende når begge betingelser er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="195c3-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="195c3-259">Oversett etiketten til oppslagsdatakilden som ble lagt til</span><span class="sxs-lookup"><span data-stu-id="195c3-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="195c3-260">Siden forretningsbrukerne kan bruke forskjellige språk til å angi juridisk enhetsavhengige sett med avgiftskoder, anbefaler vi at du oversetter etiketten for alle oppslagsdatakilder du legger til, slik at den presenteres på hver brukes foretrukne språk på den tilsvarende siden.</span><span class="sxs-lookup"><span data-stu-id="195c3-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="195c3-261">Velg **Model.Data.Selector**-datakilden.</span><span class="sxs-lookup"><span data-stu-id="195c3-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="195c3-262">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="195c3-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="195c3-263">Klikk i **Etikett**-feltet.</span><span class="sxs-lookup"><span data-stu-id="195c3-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="195c3-264">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="195c3-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="195c3-265">Angi **LBL_SELECTOR_DS** i **Tekstoversettelse**-ruten i **Etikett-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="195c3-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="195c3-266">I feltet **Tekst på standardspråk** angir du **Velg skattenivå etter mva-kode**.</span><span class="sxs-lookup"><span data-stu-id="195c3-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="195c3-267">I **Språk**-feltet velger du **DE**.</span><span class="sxs-lookup"><span data-stu-id="195c3-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="195c3-268">I **Oversatt tekst**-feltet angir du **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="195c3-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="195c3-269">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="195c3-269">Select **Translate**.</span></span>
10. <span data-ttu-id="195c3-270">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="195c3-270">Select **OK**.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="195c3-272">Legg til et nytt felt for å bruke det konfigurerte oppslaget</span><span class="sxs-lookup"><span data-stu-id="195c3-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="195c3-273">Vis elementet **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="195c3-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="195c3-274">Velg elementet **Model.Data.Tax.Summary**.</span><span class="sxs-lookup"><span data-stu-id="195c3-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="195c3-275">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="195c3-275">Select **Add**.</span></span>
4.  <span data-ttu-id="195c3-276">Velg **Funksjoner/Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="195c3-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="195c3-277">I **Navn**-feltet angir du **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="195c3-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="195c3-278">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="195c3-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="195c3-279">I **Formel**-feltet angir du **Model.Selector(Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="195c3-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="195c3-280">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="195c3-280">Select **Save**.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="195c3-282">Lukk siden **Formelredigering**.</span><span class="sxs-lookup"><span data-stu-id="195c3-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="195c3-283">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="195c3-283">Select **OK**.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="195c3-285">Legg merke til at det beregnede **LevelByLookup**-feltet som du la til, returnerer avgiftsnivået som verdien for formatopplistingen **Liste over avgiftsnivåer** for hver summerte avgiftstransaksjonsoppføring.</span><span class="sxs-lookup"><span data-stu-id="195c3-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="195c3-286">Mva-koden for posten vil bli sendt til **Model.Selector**-oppslagsdatakilden, og settet med regler for denne datakilden blir brukt til å velge riktig avgiftsnivå.</span><span class="sxs-lookup"><span data-stu-id="195c3-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="195c3-287">Legg til en ny formatopplistingsbasert datakilde</span><span class="sxs-lookup"><span data-stu-id="195c3-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="195c3-288">Deretter legger du til en ny datakilde som refererer til formatopplistingen du la til tidligere.</span><span class="sxs-lookup"><span data-stu-id="195c3-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="195c3-289">Verdier i denne datakilden vil bli brukt i et ER-formatuttrykk senere.</span><span class="sxs-lookup"><span data-stu-id="195c3-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="195c3-290">Velg **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="195c3-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="195c3-291">Velg **Formatopplistinger\Opplisting**.</span><span class="sxs-lookup"><span data-stu-id="195c3-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="195c3-292">I **Navn**-feltet angir du **Avgiftsnivå**.</span><span class="sxs-lookup"><span data-stu-id="195c3-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="195c3-293">I **Formatopplisning**-feltet velger du **Liste over avgiftsnivåer**.</span><span class="sxs-lookup"><span data-stu-id="195c3-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="195c3-294">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="195c3-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="195c3-295">Endre et eksisterende felt for å begynne å bruke oppslaget</span><span class="sxs-lookup"><span data-stu-id="195c3-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="195c3-296">Deretter skal du endre det eksisterende beregnede feltet slik at det bruker den konfigurerte oppslagsdatakilden til å returnere den riktige avgiftsnivåverdien, avhengig av mva-koden.</span><span class="sxs-lookup"><span data-stu-id="195c3-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="195c3-297">Velg elementet **Model.Data.Summary.Level**.</span><span class="sxs-lookup"><span data-stu-id="195c3-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="195c3-298">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="195c3-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="195c3-299">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="195c3-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="195c3-300">Legg merke til at gjeldende uttrykk for **Model.Data.Summary.Level**-feltet inkluderer følgende hardkodede mva-koder:</span><span class="sxs-lookup"><span data-stu-id="195c3-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="195c3-301">CASE (@.Code, "VAT19", "Vanlig", "InVAT19", "Vanlig", "VAT7", "Reduced", "InVAT7", "Redusert", "THIRD", "Ingen", "InVAT0", "Ingen", "Annet")</span><span class="sxs-lookup"><span data-stu-id="195c3-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="195c3-302">I **Formel**-feltet angir du **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Vanlig", TaxationLevel.'Reduced taxation', "Redusert", TaxationLevel.'No taxation', "Ingen", "Annet")**.</span><span class="sxs-lookup"><span data-stu-id="195c3-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="195c3-304">Legg merke til at uttrykket for **Model.Data.Summary.Level**-feltet når returnerer avgiftsnivået, basert på mva-koden for den gjeldende posten og regelsettet som et firma bruker konfigurerer, i oppslagsdatakilden **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="195c3-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="195c3-305">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="195c3-305">Select **Save**.</span></span>
6.  <span data-ttu-id="195c3-306">Lukk siden **Formelutforming**.</span><span class="sxs-lookup"><span data-stu-id="195c3-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="195c3-307">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="195c3-307">Select **OK**.</span></span>
8.  <span data-ttu-id="195c3-308">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="195c3-308">Select **Save**.</span></span>
9.  <span data-ttu-id="195c3-309">Lukk siden **Formatutforming**.</span><span class="sxs-lookup"><span data-stu-id="195c3-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="195c3-310">Fullfør utkastversjonen av et avledet format</span><span class="sxs-lookup"><span data-stu-id="195c3-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="195c3-311">I hurtigfanen **Versjoner** velger du **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="195c3-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="195c3-312">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="195c3-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="195c3-313">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="195c3-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="195c3-314">Eksporter fullført versjon av et endret format</span><span class="sxs-lookup"><span data-stu-id="195c3-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="195c3-315">I konfigurasjonstreet velger du elementet \***Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="195c3-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="195c3-316">I hurtigfanen **Versjoner** velger du posten med statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="195c3-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="195c3-317">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="195c3-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="195c3-318">Velg **Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="195c3-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="195c3-319">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="195c3-319">Select **OK**.</span></span>
6.  <span data-ttu-id="195c3-320">Webleseren laster ned filen **Format for å lære hvordan du slår opp LE-data.xml**.</span><span class="sxs-lookup"><span data-stu-id="195c3-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="195c3-321">Lagre denne filen lokalt.</span><span class="sxs-lookup"><span data-stu-id="195c3-321">Store this file locally.</span></span>

<span data-ttu-id="195c3-322">Gjenta trinn i denne delen for overordnede elementer i formatet **Format for å lære hvordan du slår opp LE-data**, og lagre følgende filer lokalt:</span><span class="sxs-lookup"><span data-stu-id="195c3-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="195c3-323">Format for å lære om parameterkall.xml</span><span class="sxs-lookup"><span data-stu-id="195c3-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="195c3-324">Tilordning for å lære om parameterkall.xml</span><span class="sxs-lookup"><span data-stu-id="195c3-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="195c3-325">Modell for å lære om parameterkall.xml</span><span class="sxs-lookup"><span data-stu-id="195c3-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="195c3-326">Hvis du vil lære hvordan du bruker det konfigurerte ER-formatet **Format for å lære hvordan du slår opp LE-data** til å definere juridisk enhetsavhengige sett med mva-koder for å filtrere mva-transaksjoner etter ulike avgiftsnivåer, må du fullføre trinnene i emnet [Definere parameterne for et ER-format per juridisk enhetdataenhet](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="195c3-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="195c3-327">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="195c3-327">Additional resources</span></span>

[<span data-ttu-id="195c3-328">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="195c3-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="195c3-329">Definere parameterne for et ER-format per juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="195c3-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
