---
title: Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet
description: Dette emnet forklarer hvordan du kan konfigurere elektroniske rapporter (ER)-formater til å bruke parametere som angis per juridisk enhet.
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 0af3e1d589fd99cc722d8aedeb9596388a9e2e8c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018292"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="3c65f-103">Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="3c65f-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="3c65f-104">Oversikt</span><span class="sxs-lookup"><span data-stu-id="3c65f-104">Overview</span></span>

<span data-ttu-id="3c65f-105">I mange av formatene for elektronisk rapportering (ER) som du vil utforme, må du filtrere data ved hjelp av et verdisett som er spesifikke for hver juridiske enhet for forekomsten (for eksempel et sett med mva-koder for å filtrere mva-transaksjoner).</span><span class="sxs-lookup"><span data-stu-id="3c65f-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="3c65f-106">Når filtrering av denne typen er konfigurert i et ER-format, brukes verdier som er avhengige av den juridiske enheten (for eksempel skattekoder) i uttrykk med ER-formatet for å angi datafiltreringsregler.</span><span class="sxs-lookup"><span data-stu-id="3c65f-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="3c65f-107">Derfor er formatet opprettet juridisk enhet-spesifikt, og hvis du vil generere de nødvendige rapportene, må du opprette avledede kopier av det opprinnelige ER-formatet for hver juridiske enhet der du må kjøre ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="3c65f-108">Hvert avledede ER-format må redigeres for å hente juridisk enhet-spesifikke verdier til den, basert på nytt når den opprinnelige versjonen (basis) er oppdatert, eksportert fra et testmiljø og importeres til et produksjonsmiljø når det må distribueres for produksjonsbruk, og så videre.</span><span class="sxs-lookup"><span data-stu-id="3c65f-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment, and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="3c65f-109">Derfor er vedlikehold av denne typen konfigurert ER-løsning kompleks og tidkrevende av flere årsaker:</span><span class="sxs-lookup"><span data-stu-id="3c65f-109">Therefore, maintenance of this type of configured ER solution is complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="3c65f-110">Jo flere juridiske enheter det er, jo flere ER-formatkonfigurasjoner må vedlikeholdes.</span><span class="sxs-lookup"><span data-stu-id="3c65f-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="3c65f-111">Vedlikehold av ER-konfigurasjoner krever at bedriftsbrukere har kjennskap til ER.</span><span class="sxs-lookup"><span data-stu-id="3c65f-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="3c65f-112">De ER-programspesifikke parameterne gjør det mulig for privilegerte brukere å konfigurere datafiltrering i et ER-format slik at det er basert på et sett med abstrakte regler.</span><span class="sxs-lookup"><span data-stu-id="3c65f-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="3c65f-113">Dette settet med regler kan konfigureres til å bruke datakildene som er tilgjengelige i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="3c65f-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="3c65f-114">Forretningsbrukere kan deretter angi reelle regler utenfor ER-rammeverket ved hjelp av brukergrensesnittet som automatisk genereres basert på innstillingene i det tilsvarende ER-formatet, og de gjeldende dataene for juridisk enhet blir åpnet av datakildene for ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="3c65f-115">Regelsettet som er angitt for et ER-format, kan eksporteres fra den gjeldende juridiske enheten for Dynamics 365 Finance (Finance)-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="3c65f-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="3c65f-116">Det kan deretter importeres til en annen juridisk enhet av enten samme Finance-forekomst eller en annen forekomst som et sett med regler for samme ER-format.</span><span class="sxs-lookup"><span data-stu-id="3c65f-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3c65f-117">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="3c65f-117">Prerequisites</span></span>

<span data-ttu-id="3c65f-118">For å fullføre eksemplene i dette emnet må du har tilgang til forekomsten av Regulatory Configuration Service (RCS) som er klargjort for samme leietaker som Finance and Operations, for én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="3c65f-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="3c65f-119">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3c65f-119">Electronic reporting developer</span></span>
- <span data-ttu-id="3c65f-120">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3c65f-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="3c65f-121">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="3c65f-121">System administrator</span></span>

<span data-ttu-id="3c65f-122">Vi anbefaler at du fullfører trinnene i emnet [Støtte for parametriserte kall av ER-datakilder av felttypen Beregnet](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="3c65f-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="3c65f-123">Hvis du allerede har fullført disse trinnene, kan du hoppe over trinnene i **Importere ER-konfigurasjoner til RCS**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="3c65f-124">Importere ER-konfigurasjoner til RCS</span><span class="sxs-lookup"><span data-stu-id="3c65f-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="3c65f-125">Last ned og lagre følgende ER-konfigurasjoner lokalt:</span><span class="sxs-lookup"><span data-stu-id="3c65f-125">Download and locally store the following ER configurations.</span></span>

| <span data-ttu-id="3c65f-126">**Innholdsbeskrivelse**</span><span class="sxs-lookup"><span data-stu-id="3c65f-126">**Content description**</span></span>                        | <span data-ttu-id="3c65f-127">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="3c65f-127">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c65f-128">Eksempel på konfigurasjonsfilen **ER-datamodell**</span><span class="sxs-lookup"><span data-stu-id="3c65f-128">Sample **ER data model** configuration file</span></span>    | [<span data-ttu-id="3c65f-129">Modell for å lære om parameterkall.versjon.1.XML</span><span class="sxs-lookup"><span data-stu-id="3c65f-129">Model to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| <span data-ttu-id="3c65f-130">Eksempel på konfigurasjonsfilen **ER-metadata**</span><span class="sxs-lookup"><span data-stu-id="3c65f-130">Sample **ER metadata** configuration file</span></span>      | [<span data-ttu-id="3c65f-131">Metadata for å lære om parameterkall.versjon.1.XML</span><span class="sxs-lookup"><span data-stu-id="3c65f-131">Metadata to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| <span data-ttu-id="3c65f-132">Eksempel på konfigurasjonsfilen **ER-modelltilordning**</span><span class="sxs-lookup"><span data-stu-id="3c65f-132">Sample **ER model mapping** configuration file</span></span> | [<span data-ttu-id="3c65f-133">Tilordning for å lære om parameterkall.versjon.1.1.XML</span><span class="sxs-lookup"><span data-stu-id="3c65f-133">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| <span data-ttu-id="3c65f-134">Eksempel på **ER-format**-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3c65f-134">Sample **ER format** configuration</span></span>             | [<span data-ttu-id="3c65f-135">Format for å lære om parameterkall.versjon.1.1.XML</span><span class="sxs-lookup"><span data-stu-id="3c65f-135">Format to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

<span data-ttu-id="3c65f-136">Logg deretter på RCS-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="3c65f-136">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="3c65f-137">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3c65f-137">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="3c65f-138">Før du kan fullføre trinnene i denne prosedyren må du fullføre prosedyren i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS.</span><span class="sxs-lookup"><span data-stu-id="3c65f-138">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="3c65f-139">Velg **Elektronisk rapportering** på standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="3c65f-139">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="3c65f-140">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-140">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="3c65f-141">Importer de nedlastede ER-konfigurasjonene til RCS i følgende rekkefølge: datamodell, metadata, modelltilordning, format.</span><span class="sxs-lookup"><span data-stu-id="3c65f-141">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="3c65f-142">For hver ER-konfigurasjon følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="3c65f-142">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="3c65f-143">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-143">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="3c65f-144">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-144">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="3c65f-145">Velg **Bla gjennom** for å velge den riktige filen for den nødvendige ER-konfigurasjonen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="3c65f-145">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="3c65f-146">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-146">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="3c65f-147">Se gjennom den angitte ER-løsningen</span><span class="sxs-lookup"><span data-stu-id="3c65f-147">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="3c65f-148">I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-148">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="3c65f-149">Velg elementet **Format for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-149">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="3c65f-150">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-150">Select **Designer**.</span></span>
4.  <span data-ttu-id="3c65f-151">Velg **Vis/skjul**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-151">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="3c65f-152">ER-formatet **Format for å lære om parameterkall** er utformet for å generere en skatteoppgave i XML-format som viser flere nivåer med avgifter (vanlig, redusert og ingen).</span><span class="sxs-lookup"><span data-stu-id="3c65f-152">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="3c65f-153">Hvert nivå har et ulikt antall detaljer.</span><span class="sxs-lookup"><span data-stu-id="3c65f-153">Each level has a different number of details.</span></span>

    ![Flere nivåer av ER-format. Format for å lære parameteriserte samtaler](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="3c65f-155">Utvid elementene **Modell**, **Data** og **Sammendrag** i kategorien **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-155">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="3c65f-156">Datakilden **Model.Data.Summary** returnerer listen over mva-transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="3c65f-156">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="3c65f-157">Disse transaksjonene er oppført etter mva-kode.</span><span class="sxs-lookup"><span data-stu-id="3c65f-157">These transactions are summarized by tax code.</span></span> <span data-ttu-id="3c65f-158">For denne datakilden er det beregnede **Model.Data.Summary.Level**-feltet konfigurert til å returnere koden for avgiftsnivået for hver summerte post.</span><span class="sxs-lookup"><span data-stu-id="3c65f-158">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="3c65f-159">For alle avgiftskoder som kan hentes fra **Model.Data.Summary**-datakilden ved kjøretid, returnerer det beregnede feltet avgiftsnivåkode (**Vanlig**, **Redusert**, **Ingen** eller **Annet**) som en tekstverdi.</span><span class="sxs-lookup"><span data-stu-id="3c65f-159">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="3c65f-160">Det beregnede **Model.Data.Summary.Level**-feltet brukes til å filtrere poster for **Model.Data.Summary**-datakilden og angi de filtrerte dataene i hvert XML-element som representerer et avgiftsnivå ved hjelp av feltene **Model.Data2.Level1**, **Model.Data2.Level2** og **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-160">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![Datakildelisten Model.Data.Summary over mva-transaksjoner](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="3c65f-162">Det beregnede **Model.Data.Summary.Level**-feltet er konfigurert slik at det inneholder et ER-uttrykk.</span><span class="sxs-lookup"><span data-stu-id="3c65f-162">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="3c65f-163">Avgiftskoder (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** og **InVAT0**) er hardkodet til denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3c65f-163">Tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="3c65f-164">Derfor er dette ER-formatet avhengig av den juridiske enheten der disse avgiftskodene ble konfigurert.</span><span class="sxs-lookup"><span data-stu-id="3c65f-164">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![Det beregnede feltet Model.Data.Summary.Level med hardkodede avgiftskoder](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="3c65f-166">Hvis du vil støtte et annet sett med mva-koder for hver juridiske enhet, må du følge denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="3c65f-166">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="3c65f-167">Opprett en avledet versjon av ER-formatet for hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-167">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="3c65f-168">Oppdater avgiftskodene i det beregnede **Model.Data.Summary.Level**-feltet, basert på innstillingen for juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-168">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="3c65f-169">Lukk **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-169">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="3c65f-170">Opprette et avledet format</span><span class="sxs-lookup"><span data-stu-id="3c65f-170">Create a derived format</span></span>

<span data-ttu-id="3c65f-171">Deretter skal du bruke funksjonen for ER-programspesifikke parametere til å støtte et annet sett med mva-koder for hver juridiske enhet i ett enkelt ER-format.</span><span class="sxs-lookup"><span data-stu-id="3c65f-171">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="3c65f-172">I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-172">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="3c65f-173">Velg elementet **Format for å lære om parameterkall**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-173">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="3c65f-174">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-174">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="3c65f-175">Velg alternativet **Avled fra navn: Format for å lære om parameterkall, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-175">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="3c65f-176">I **Navn**-feltet angir du **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-176">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="3c65f-177">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-177">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="3c65f-178">Konfigurere et avledet format</span><span class="sxs-lookup"><span data-stu-id="3c65f-178">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="3c65f-179">Legge til en formatopplisting</span><span class="sxs-lookup"><span data-stu-id="3c65f-179">Add a format enumeration</span></span>

<span data-ttu-id="3c65f-180">Deretter legger du til en ny ER-formatopplisting.</span><span class="sxs-lookup"><span data-stu-id="3c65f-180">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="3c65f-181">Verdiene for denne formatopplistingen vil bli presentert for forretningsbrukere, som vil angi juridisk enhetsavhengige sett med mva-koder for de ulike avgiftsnivåene som brukes i ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-181">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="3c65f-182">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-182">Select **Designer**.</span></span>
2.  <span data-ttu-id="3c65f-183">Velg **Formatopplistinger**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-183">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="3c65f-184">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-184">Select **Add**.</span></span>
4.  <span data-ttu-id="3c65f-185">I **Navn**-feltet angir du **Liste over avgiftsnivåer**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-185">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="3c65f-186">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-186">Select **Save**.</span></span>
6.  <span data-ttu-id="3c65f-187">Velg **Legg til** i kategorien **Verdier for formatopplisning**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-187">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="3c65f-188">I **Navn**-feltet angir du **Vanlig avgift**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-188">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="3c65f-189">Velg **Legg til** på nytt.</span><span class="sxs-lookup"><span data-stu-id="3c65f-189">Select **Add** again.</span></span>
9.  <span data-ttu-id="3c65f-190">I **Navn**-feltet angir du **Redusert avgift**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-190">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="3c65f-191">Velg **Legg til** på nytt.</span><span class="sxs-lookup"><span data-stu-id="3c65f-191">Select **Add** again.</span></span>
11. <span data-ttu-id="3c65f-192">I **Navn**-feltet angir du **Ingen avgift**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-192">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="3c65f-193">Velg **Legg til** på nytt.</span><span class="sxs-lookup"><span data-stu-id="3c65f-193">Select **Add** again.</span></span>
13. <span data-ttu-id="3c65f-194">Angi **Annet** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-194">In the **Name** field, enter **Other**.</span></span>

    ![Ny post på Format-opplistingssiden](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="3c65f-196">Siden forretningsbrukerne kan bruke forskjellige språk til å angi juridisk enhetsavhengige sett med avgiftskoder, anbefaler vi at du oversetter verdiene for denne opplistingen til språkene som er konfigurert som foretrukne språk for disse brukerne i Økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="3c65f-196">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="3c65f-197">Velg posten **Ingen avgift**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-197">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="3c65f-198">Klikk i **Etikett**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-198">Click in the **Label** field.</span></span>
16. <span data-ttu-id="3c65f-199">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-199">Select **Translate**.</span></span>
17. <span data-ttu-id="3c65f-200">Angi **LBL_LEVELENUM_NO** i **Tekstoversettelse**-ruten i **Etikett-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-200">In the **Text translation** pane, in the **Label ID** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="3c65f-201">I feltet **Tekst på standardspråk** angir du **Ingen avgift**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-201">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="3c65f-202">I **Språk**-feltet velger du **DE**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-202">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="3c65f-203">I **Oversatt tekst**-feltet angir du **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-203">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="3c65f-204">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-204">Select **Translate**.</span></span>

    ![Lysbilde ut for tekstoversetting](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="3c65f-206">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-206">Select **Save**.</span></span>
23. <span data-ttu-id="3c65f-207">Lukk **Formatopplistinger**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-207">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="3c65f-208">Legg til en ny datakilde for oppslag</span><span class="sxs-lookup"><span data-stu-id="3c65f-208">Add a new lookup data source</span></span>

<span data-ttu-id="3c65f-209">Deretter legger du til en ny datakilde for å angi hvordan forretningsbrukere skal angi juridisk enhetsavhengige relger for å gjenkjenne det riktige avgiftsnivået for hver summerte transaksjonsoppføring.</span><span class="sxs-lookup"><span data-stu-id="3c65f-209">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="3c65f-210">Velg **Legg til** i **Tilordning**-fanen.</span><span class="sxs-lookup"><span data-stu-id="3c65f-210">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="3c65f-211">Velg **Formatopplisting\Oppslag**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-211">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="3c65f-212">Du har nettopp identifisert at hver regel som forretningsbrukere angir for avgiftsnivågjenkjenning vil returnere en verdi for en ER-formatopplisting.</span><span class="sxs-lookup"><span data-stu-id="3c65f-212">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="3c65f-213">Legg merke til at du får tilgang til **Oppslag**-datakildetypen under **Datamodell** og **Dynamics 365 for Operations**-blokker i tillegg til **Formatopplisning**-blokken.</span><span class="sxs-lookup"><span data-stu-id="3c65f-213">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="3c65f-214">Derfor kan det brukes ER-datamodellopplistinger og programopplisninger til å angi typen verdier som returneres for datakilder av denne typen.</span><span class="sxs-lookup"><span data-stu-id="3c65f-214">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that are returned for data sources of that type.</span></span> <span data-ttu-id="3c65f-215">Hvis du vil lære mer om **Oppslag**-datakildene, kan du se [Konfigurer Oppslag-datakilder for å bruke funksjonen for ER-programspesifikke parametere](er-lookup-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="3c65f-215">To learn more about the **Lookup** data sources, see [Configure Lookup data sources to use the ER application-specific parameters feature](er-lookup-data-sources.md).</span></span>
    
3.  <span data-ttu-id="3c65f-216">Angi **Velger** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="3c65f-217">I **Formatopplisning**-feltet velger du **Liste over avgiftsnivåer**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="3c65f-218">Du har angitt at en forretningsbruker må velge en av verdiene i formatopplisningen **Liste over avgiftsnivåer** som en retur verdi for hver regel som er angitt i denne datakilden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-218">You specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="3c65f-219">Velg **Rediger oppslag**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="3c65f-220">Velg **Kolonner**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="3c65f-221">Vis elementet **Model**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="3c65f-222">Vis elementet **Data**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="3c65f-223">Vis elementet **Avgift**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="3c65f-224">Velg elementet **Model.Data.Tax.Code**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="3c65f-225">Velg **Legg til**-knappen (høyre pilen).</span><span class="sxs-lookup"><span data-stu-id="3c65f-225">Select the **Add** button (the right arrow).</span></span>

    ![Kolonner lysbilde ut](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="3c65f-227">Du har akkurat angitt at en forretningsbruker må velge en av avgiftskodene som en betingelse for hver regel som er angitt i denne datakilden for avgiftsnivågjenkjenning.</span><span class="sxs-lookup"><span data-stu-id="3c65f-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="3c65f-228">Listen over avgiftskoder som firmabrukeren kan velge, vil bli returnert av **Model.Data.Tax**-datakilden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="3c65f-229">Siden denne datakilden inneholder **Navn**-feltet, vises navnet på mva-koden for hver mva-kodeverdi i oppslaget som presenteres for forretningsbrukeren.</span><span class="sxs-lookup"><span data-stu-id="3c65f-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="3c65f-230">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-230">Select **OK**.</span></span>

    ![Oppslagsutformingsside](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="3c65f-232">Forretningsbrukere kan legge til flere regler som poster i denne datakilden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="3c65f-233">Hver post vil bli nummerert med en linjekode.</span><span class="sxs-lookup"><span data-stu-id="3c65f-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="3c65f-234">Regler vil bli evaluert i stigende linjenummer.</span><span class="sxs-lookup"><span data-stu-id="3c65f-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="3c65f-235">Fordi du valgte **Mva-kode**-feltet som en betingelse for regler i denne oppslagsdatakilden, og fordi **Mva-kode** er definert som et felt av **Streng**-datatypen, evalueres hver regel ved kjøring ved å sammenligne avgiftskoden som sendes til datakilden med mva-koden som er definert i denne posten for datakilden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="3c65f-236">Når en regel som er i samsvar med den konfigurerte betingelsen, blir funnet, returnerer denne datakilden oppslagsverdien for regelen som er definert i **Oppslagsresultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="3c65f-237">Hvis ingen regel blir funnet, oppstår det et unntak for å varsle brukeren om at den gjeldende datakilden ikke kan returnere en riktig verdi.</span><span class="sxs-lookup"><span data-stu-id="3c65f-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="3c65f-238">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-238">Select **Save**.</span></span>
14. <span data-ttu-id="3c65f-239">Lukk **Oppslagsutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="3c65f-240">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-240">Select **OK**.</span></span>

    <span data-ttu-id="3c65f-241">Legg merke til at du har lagt til en ny datakilde som returnerer avgiftsnivået som verdien for formatopplistingen **Liste over avgiftsnivåer** for en mva-kode som sendes til datakilden som argument for **kode**-parameteren til datatypen **streng**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![Formatutformingsside med en ny datakilde](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="3c65f-243">Evalueringen av konfigurerte regler avhenger av datatypen til feltene som er valgt for å definere betingelsene for disse reglene.</span><span class="sxs-lookup"><span data-stu-id="3c65f-243">The evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="3c65f-244">Når du velger et felt som er konfigurert som et felt enten for datatypen **numerisk** eller **dato**, vil vilkårene være forskjellige fra vilkårene som ble beskrevet tidligere for datatypen **streng**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="3c65f-245">For **numerisk**- og **data**-felt må regelen angis som et verdiområde.</span><span class="sxs-lookup"><span data-stu-id="3c65f-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="3c65f-246">Betingelsen for regelen vil da anses som oppfylt når en verdi som sendes til datakilden, er i det konfigurerte området.</span><span class="sxs-lookup"><span data-stu-id="3c65f-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="3c65f-247">Illustrasjonen nedenfor viser et eksempel på denne typen oppsett.</span><span class="sxs-lookup"><span data-stu-id="3c65f-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="3c65f-248">I tillegg til **Model.Data.Tax.Code**-feltet i **streng**-datatypen brukes **Model.Tax.Summary.Base**-feltet for **Real**-datatypen til å angi betingelser for en oppslagsdatakilde.</span><span class="sxs-lookup"><span data-stu-id="3c65f-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![Oppslagsutformingsside med tilleggskolonner](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="3c65f-250">Fordi feltene **Model.Data.Tax.Code** og **Model.Tax.Summary.Base** er valgt for denne oppslagsdatakilden, konfigureres hver regel for denne datakilden på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="3c65f-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="3c65f-251">I listen som vises, må verdien i formatopplistingen **Liste over avgiftsnivåer** velges som en returnert verdi.</span><span class="sxs-lookup"><span data-stu-id="3c65f-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="3c65f-252">Mva-koden må angis som en betingelse for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="3c65f-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="3c65f-253">Bare avgiftskoder som tilbys av modellen **Model.Data.Tax**-datakilden, er gjeldende.</span><span class="sxs-lookup"><span data-stu-id="3c65f-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="3c65f-254">Minimums- og maksimumsverdiene for avgiftsgrunnlagsbeløpet må angis som betingelser for denne regelen.</span><span class="sxs-lookup"><span data-stu-id="3c65f-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="3c65f-255">Slik blir hver regel i denne datakilden evaluert ved kjøretid:</span><span class="sxs-lookup"><span data-stu-id="3c65f-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="3c65f-256">Er koden for **streng**-datatypen som ble sendt til denne datakilden, lik mva-koden for en regel?</span><span class="sxs-lookup"><span data-stu-id="3c65f-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="3c65f-257">Faller verdien av **Real**-datatypen som ble sendt til denne datakilden, mellom bestemte minimums- og maksimumsverdier?</span><span class="sxs-lookup"><span data-stu-id="3c65f-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="3c65f-258">En regel blir ansett som gjeldende når begge betingelser er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="3c65f-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="3c65f-259">Oversett etiketten til oppslagsdatakilden som ble lagt til</span><span class="sxs-lookup"><span data-stu-id="3c65f-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="3c65f-260">Siden forretningsbrukerne kan bruke forskjellige språk til å angi juridisk enhetsavhengige sett med avgiftskoder, anbefaler vi at du oversetter etiketten for alle oppslagsdatakilder du legger til, slik at den presenteres på hver brukes foretrukne språk på den tilsvarende siden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="3c65f-261">Velg **Model.Data.Selector**-datakilden.</span><span class="sxs-lookup"><span data-stu-id="3c65f-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="3c65f-262">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="3c65f-263">Klikk i **Etikett**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="3c65f-264">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="3c65f-265">Angi **LBL_SELECTOR_DS** i **Tekstoversettelse**-ruten i **Etikett-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c65f-265">In the **Text translation** pane, in the **Label ID** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="3c65f-266">I feltet **Tekst på standardspråk** angir du **Velg skattenivå etter mva-kode**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="3c65f-267">I **Språk**-feltet velger du **DE**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="3c65f-268">I **Oversatt tekst**-feltet angir du **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="3c65f-269">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-269">Select **Translate**.</span></span>
10. <span data-ttu-id="3c65f-270">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-270">Select **OK**.</span></span>

    ![Datakildeegenskaper dras ut](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="3c65f-272">Legg til et nytt felt for å bruke det konfigurerte oppslaget</span><span class="sxs-lookup"><span data-stu-id="3c65f-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="3c65f-273">Vis elementet **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="3c65f-274">Velg elementet **Model.Data.Tax.Summary**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="3c65f-275">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-275">Select **Add**.</span></span>
4.  <span data-ttu-id="3c65f-276">Velg **Funksjoner/Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="3c65f-277">I **Navn**-feltet angir du **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="3c65f-278">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="3c65f-279">I **Formel**-feltet angir du **Model.Selector(Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="3c65f-280">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-280">Select **Save**.</span></span>

    ![Legg til Model.Selector(Model.Data.Summary.Code) på Formeldesigner-siden](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="3c65f-282">Lukk siden **Formelredigering**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="3c65f-283">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-283">Select **OK**.</span></span>

    ![Formatutformingsside med ny formel lagt til](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="3c65f-285&quot;>Legg merke til at det beregnede **LevelByLookup**-feltet som du la til, returnerer avgiftsnivået som verdien for formatopplistingen **Liste over avgiftsnivåer** for hver summerte avgiftstransaksjonsoppføring.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-285&quot;>Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id=&quot;3c65f-286&quot;>Mva-koden for posten vil bli sendt til **Model.Selector**-oppslagsdatakilden, og settet med regler for denne datakilden blir brukt til å velge riktig avgiftsnivå.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-286&quot;>The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name=&quot;add-a-new-format-enumeration-based-data-source&quot;></a><span data-ttu-id=&quot;3c65f-287&quot;>Legg til en ny formatopplistingsbasert datakilde</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-287&quot;>Add a new format enumeration-based data source</span></span>

<span data-ttu-id=&quot;3c65f-288&quot;>Deretter legger du til en ny datakilde som refererer til formatopplistingen du la til tidligere.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-288&quot;>Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id=&quot;3c65f-289&quot;>Verdier i denne datakilden vil bli brukt i et ER-formatuttrykk senere.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-289&quot;>Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id=&quot;3c65f-290&quot;>Velg **Legg til rot**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-290&quot;>Select **Add root**.</span></span>
2.  <span data-ttu-id=&quot;3c65f-291&quot;>Velg **Formatopplistinger\Opplisting**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-291&quot;>Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id=&quot;3c65f-292&quot;>I **Navn**-feltet angir du **Avgiftsnivå**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-292&quot;>In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id=&quot;3c65f-293&quot;>I **Formatopplisning**-feltet velger du **Liste over avgiftsnivåer**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-293&quot;>In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id=&quot;3c65f-294&quot;>Velg **Lagre**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-294&quot;>Select **Save**.</span></span>

### <a name=&quot;modify-an-existing-field-to-start-to-use-the-lookup&quot;></a><span data-ttu-id=&quot;3c65f-295&quot;>Endre et eksisterende felt for å begynne å bruke oppslaget</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-295&quot;>Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id=&quot;3c65f-296&quot;>Deretter skal du endre det eksisterende beregnede feltet slik at det bruker den konfigurerte oppslagsdatakilden til å returnere den riktige avgiftsnivåverdien, avhengig av mva-koden.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-296&quot;>Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id=&quot;3c65f-297&quot;>Velg elementet **Model.Data.Summary.Level**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-297&quot;>Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id=&quot;3c65f-298&quot;>Velg **Rediger**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-298&quot;>Select **Edit**.</span></span>
3.  <span data-ttu-id=&quot;3c65f-299&quot;>Velg **Rediger formel**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-299&quot;>Select **Edit formula**.</span></span>

    <span data-ttu-id=&quot;3c65f-300&quot;>Legg merke til at gjeldende uttrykk for **Model.Data.Summary.Level**-feltet inkluderer følgende hardkodede mva-koder:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c65f-300&quot;>Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id=&quot;3c65f-301&quot;>CASE (@.Code, &quot;VAT19&quot;, &quot;Vanlig&quot;, &quot;InVAT19&quot;, &quot;Vanlig&quot;, &quot;VAT7&quot;, &quot;Reduced&quot;, &quot;InVAT7&quot;, &quot;Redusert&quot;, &quot;THIRD&quot;, &quot;Ingen&quot;, &quot;InVAT0&quot;, &quot;Ingen&quot;, &quot;Annet")</span><span class="sxs-lookup"><span data-stu-id="3c65f-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="3c65f-302">I **Formel**-feltet angir du **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Vanlig", TaxationLevel.'Reduced taxation', "Redusert", TaxationLevel.'No taxation', "Ingen", "Annet")**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![Side med ER-operasjonsutforming](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="3c65f-304">Legg merke til at uttrykket for **Model.Data.Summary.Level**-feltet nå returnerer avgiftsnivået, basert på mva-koden for den gjeldende posten og regelsettet som en forretningsbruker konfigurerer, i oppslagsdatakilden **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="3c65f-305">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-305">Select **Save**.</span></span>
6.  <span data-ttu-id="3c65f-306">Lukk siden **Formelutforming**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="3c65f-307">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-307">Select **OK**.</span></span>
8.  <span data-ttu-id="3c65f-308">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-308">Select **Save**.</span></span>
9.  <span data-ttu-id="3c65f-309">Lukk siden **Formatutforming**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="3c65f-310">Fullfør utkastversjonen av et avledet format</span><span class="sxs-lookup"><span data-stu-id="3c65f-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="3c65f-311">På hurtigfanen **Versjoner** velger du **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-311">On the **Versions** FastTab, select **Change status**.</span></span>
2.  <span data-ttu-id="3c65f-312">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="3c65f-313">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="3c65f-314">Eksporter fullført versjon av et endret format</span><span class="sxs-lookup"><span data-stu-id="3c65f-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="3c65f-315">I konfigurasjonstreet velger du elementet **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-315">In the configuration tree, select the **Format to learn how to look up LE data** item.</span></span>
2.  <span data-ttu-id="3c65f-316">På hurtigfanen **Versjoner** velger du posten med statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-316">On the **Versions** FastTab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="3c65f-317">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="3c65f-318">Velg **Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="3c65f-319">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-319">Select **OK**.</span></span>
6.  <span data-ttu-id="3c65f-320">Nettleseren laster ned filen **Format for å lære hvordan du slår opp LE-data.xml**.</span><span class="sxs-lookup"><span data-stu-id="3c65f-320">The web browser downloads a **Format to learn how to look up LE data.xml** file.</span></span> <span data-ttu-id="3c65f-321">Lagre denne filen lokalt.</span><span class="sxs-lookup"><span data-stu-id="3c65f-321">Store this file locally.</span></span>

<span data-ttu-id="3c65f-322">Gjenta trinn i denne delen for overordnede elementer i formatet **Format for å lære hvordan du slår opp LE-data**, og lagre følgende filer lokalt:</span><span class="sxs-lookup"><span data-stu-id="3c65f-322">Repeat steps in this section for parent items of the **Format to learn how to look up LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="3c65f-323">Format for å lære om parameterkall.xml</span><span class="sxs-lookup"><span data-stu-id="3c65f-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="3c65f-324">Tilordning for å lære om parameterkall.xml</span><span class="sxs-lookup"><span data-stu-id="3c65f-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="3c65f-325">Modell for å lære om parameterkall.xml</span><span class="sxs-lookup"><span data-stu-id="3c65f-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="3c65f-326">Hvis du vil lære hvordan du bruker det konfigurerte ER-formatet **Format for å lære hvordan du slår opp LE-data** til å definere juridisk enhetsavhengige sett med mva-koder for å filtrere mva-transaksjoner etter ulike avgiftsnivåer, må du fullføre trinnene i emnet [Definere parameterne for et ER-format per juridisk enhetdataenhet](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="3c65f-326">To learn how to use the configured **Format to learn how to look up LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c65f-327">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3c65f-327">Additional resources</span></span>

[<span data-ttu-id="3c65f-328">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3c65f-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="3c65f-329">Definere parameterne for et ER-format per juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="3c65f-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)

[<span data-ttu-id="3c65f-330">Konfigurer Oppslag-datakilder for å bruke funksjonen for ER-programspesifikke parametere</span><span class="sxs-lookup"><span data-stu-id="3c65f-330">Configure Lookup data sources to use the ER application-specific parameters feature</span></span>](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
