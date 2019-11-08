---
title: Bruke JOIN-datakilder i ER-modelltilordninger til å hente data fra flere programtabeller
description: Dette emnet forklarer hvordan du kan bruke datakilder av JOIN-typen i elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667960"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a><span data-ttu-id="a7b7b-103">Bruke JOIN-datakilder til å hente data fra flere programtabeller i modelltilordninger for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="a7b7b-103">Use JOIN data sources to get data from multiple application tables in Electronic reporting (ER) model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a7b7b-104">Når du konfigurerer modelltilordninger eller formater for elektronisk rapportering (ER), kan du [legge til](#review) nødvendige datakilder av **Join**-typen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-104">While configuring Electronic reporting (ER) model mappings or formats, you can [add](#review) required data sources of the **Join** type.</span></span> <span data-ttu-id="a7b7b-105">Under utformingen konfigureres en **Join**-datakilde som et sett med flere datakilder hver som returnerer en liste med poster.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-105">At design time, a **Join** data source is configured as a set of several data sources each of which returns a list of records.</span></span> <span data-ttu-id="a7b7b-106">For hver datakilde unntatt den første må du definere nødvendige betingelser for å føye sammen poster for gjeldende og tidligere datakilder.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-106">For every data source except the first one, you need to define necessary conditions to join records of the current and previous data sources.</span></span> <span data-ttu-id="a7b7b-107">Under kjøring [returnerer](#executeERformat) en konfigurert datatype av typen **Join** en enkelt sammenkoblet liste med poster som inneholder felt fra postene for nestede datakilder.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-107">At runtime, a configured data source of **Join** type [returns](#executeERformat) a single joined list of records containing fields from the records of nested data sources.</span></span>

<span data-ttu-id="a7b7b-108">Følgende sammenkoblingstyper støttes for øyeblikket:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-108">The following type of joins are currently supported:</span></span>

- <span data-ttu-id="a7b7b-109">Ytre (venstre) join:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-109">Outer (left) join:</span></span>
    - <span data-ttu-id="a7b7b-110">Slå sammen alle poster i den første (helt til venstre) datakilden og deretter eventuelle samsvar i henhold til konfigurerte vilkårsposter i den andre (den høyre) datakilden.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-110">Join all records of the first (left-most) data source and then any matching in accordance to configured conditions records of the second (right-most) data source.</span></span>
- <span data-ttu-id="a7b7b-111">Indre (høyre) join:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-111">Inner (right) join:</span></span>
    - <span data-ttu-id="a7b7b-112">Bare slå sammen poster i den første (helt til venstre) datakilden og bare poster i den andre (den høyre) datakilden som samsvarer med hverandre i henhold til konfigurerte vilkårsposter.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-112">Join only records of the first (left-most) data source and only records of the second (right-most) data source matching to each other in accordance to configured conditions.</span></span>

<span data-ttu-id="a7b7b-113">I den konfigurerte **Join**-datakilden, når alle datakilder er av typen **Tabellposter**, kan utførelse av Join-datakilden [utføres på databasenivå](#analyze) ved hjelp av én enkelt SQL-setning.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-113">In the configured **Join** data source, when all data sources are the **Table records** type, execution of the Join data source can be [performed at the database level](#analyze) using a single SQL statement.</span></span> <span data-ttu-id="a7b7b-114">Dette reduserer antallet databasekall, noe som forbedrer modelltilordningsytelsen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-114">This reduces the number of database calls, which improves model mapping performance.</span></span> <span data-ttu-id="a7b7b-115">Hvis ikke utføres **Join**-datakilden i minnet.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-115">Otherwise, execution of **Join data** source is performed in memory.</span></span>

> [!NOTE]
> <span data-ttu-id="a7b7b-116">Bruk av **VALUEIN**-funksjonen i ER-uttrykk som angir betingelser for sammenkobling av poster i datakilder av Join-typen, støttes ikke ennå.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-116">Using the **VALUEIN** function in ER expressions that specify conditions for joining records in data sources of Join type is not supported yet.</span></span> <span data-ttu-id="a7b7b-117">Gå til siden [Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md) for mer informasjon om denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-117">Visit the [Formula designer in Electronic reporting](general-electronic-reporting-formula-designer.md) page for more details about this function.</span></span>

<span data-ttu-id="a7b7b-118">Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-118">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="example-use-join-data-sources-in-er-model-mappings"></a><span data-ttu-id="a7b7b-119">Eksempel: Bruk JOIN-datakilder i ER-modelltilordninger</span><span class="sxs-lookup"><span data-stu-id="a7b7b-119">Example: Use JOIN data sources in ER model mappings</span></span>

<span data-ttu-id="a7b7b-120">De følgende trinnene forklarer hvordan den systemansvarlige eller utvikleren av elektronisk rapportering kan konfigurere modelltilordning for elektronisk rapportering (ER) for å hente data fra flere programtabeller samtidig ved å bruke datakilder av typen **Join** til å forbedre datatilgangsytelsen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-120">The following steps explain how the System administrator or Electronic reporting developer can configure an Electronic reporting (ER) model mapping to get data from multiple application tables at once by using data sources of the **Join** type to improve data access performance.</span></span> <span data-ttu-id="a7b7b-121">Disse trinnene kan utføres for et hvilket som helst firma med Dynamics 365 Finance eller Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="a7b7b-121">These steps can be performed for any company of Dynamics 365 Finance or Regulatory Configuration Services (RCS).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a7b7b-122">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="a7b7b-122">Prerequisites</span></span>

<span data-ttu-id="a7b7b-123">Hvis du vil fullføre eksemplene i dette emnet, må du ha tilgang til ett av følgende, avhengig av hvilken tjeneste som brukes til å utføre disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-123">To complete the examples in this topic, you must have access to one of the following depending on what service is used to compete these steps:</span></span>

<span data-ttu-id="a7b7b-124">**Tilgang til Finance for én av følgende roller:**</span><span class="sxs-lookup"><span data-stu-id="a7b7b-124">**Access to Finance for one of the following roles:**</span></span>

- <span data-ttu-id="a7b7b-125">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a7b7b-125">Electronic reporting developer</span></span>
- <span data-ttu-id="a7b7b-126">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a7b7b-126">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="a7b7b-127">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="a7b7b-127">System administrator</span></span>

<span data-ttu-id="a7b7b-128">**Tilgang til RCS for én av følgende roller:**</span><span class="sxs-lookup"><span data-stu-id="a7b7b-128">**Access to RCS for one of the following roles:**</span></span>

- <span data-ttu-id="a7b7b-129">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a7b7b-129">Electronic reporting developer</span></span>
- <span data-ttu-id="a7b7b-130">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a7b7b-130">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="a7b7b-131">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="a7b7b-131">System administrator</span></span>

<span data-ttu-id="a7b7b-132">Du må også først fullføre disse trinnene i fremgangsmåten [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a7b7b-132">You also must first complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

<span data-ttu-id="a7b7b-133">På forhånd må du også laste ned fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) og lagre følgende eksempel-ER-konfigurasjonsfiler lokalt:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-133">In advance, you must also download from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) and save locally the following sample ER configuration files:</span></span>

| <span data-ttu-id="a7b7b-134">**Innholdsbeskrivelse**</span><span class="sxs-lookup"><span data-stu-id="a7b7b-134">**Content description**</span></span>  | <span data-ttu-id="a7b7b-135">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="a7b7b-135">**File name**</span></span>   |
|--------------------------|-----------------|
| <span data-ttu-id="a7b7b-136">Eksempel **ER-datamodell**-konfigurasjonsfil, som brukes som datakilde for eksemplene.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-136">Sample **ER data model** configuration file, which is used as the data source for the examples.</span></span>| [<span data-ttu-id="a7b7b-137">Modell for å lære JOIN-datakilder.versjon.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="a7b7b-137">Model to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="a7b7b-138">Eksempelkonfigurasjonsfil for **ER-modelltilordning**, som implementerer ER-datamodellen for eksemplene.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-138">Sample **ER model mapping** configuration file, which implements the ER data model for the examples.</span></span> | [<span data-ttu-id="a7b7b-139">Tilordning for å lære JOIN-datakilder.versjon.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="a7b7b-139">Mapping to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="a7b7b-140">Eksempelkonfigurasjonsfil for **ER-format**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-140">Sample **ER format** configuration file.</span></span> <span data-ttu-id="a7b7b-141">Denne filen beskriver dataene for å fylle ut ER-formatkomponenten for eksemplene.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-141">This file describes the data to populate the ER format component for the examples.</span></span> | [<span data-ttu-id="a7b7b-142">Format for å lære JOIN-datakilder.versjon.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="a7b7b-142">Format to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="a7b7b-143">Aktivere en konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="a7b7b-143">Activate a configurations provider</span></span>

1. <span data-ttu-id="a7b7b-144">Du får tilgang til Finance eller RCS i den første økten av webleseren.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-144">Access either Finance or RCS in the first session of your web browser.</span></span>
2. <span data-ttu-id="a7b7b-145">Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-145">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
3. <span data-ttu-id="a7b7b-146">På siden for **Lokaliseringskonfigurasjoner** i delen **Konfigurasjonsleverandører** må du kontrollere at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. (http://www.litware.com) er oppført og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-146">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the configuration provider for the Litware, Inc. (http://www.litware.com) sample company is listed, and that it's marked as **Active**.</span></span> <span data-ttu-id="a7b7b-147">Hvis du ikke ser denne konfigurasjonsleverandøren, følger du trinnene i prosedyren [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a7b7b-147">If you don't see this configuration provider, follow the steps in [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

    ![Arbeidsområdet Elektronisk rapportering](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a><span data-ttu-id="a7b7b-149">Importere ER-eksempelkonfigurasjonsfiler</span><span class="sxs-lookup"><span data-stu-id="a7b7b-149">Import sample ER configuration files</span></span>

1. <span data-ttu-id="a7b7b-150">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-150">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="a7b7b-151">Importer ER-datamodellkonfigurasjonsfilen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-151">Import the ER data model configuration file.</span></span>
    1. <span data-ttu-id="a7b7b-152">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-152">Select **Exchange**.</span></span>
    2. <span data-ttu-id="a7b7b-153">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-153">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="a7b7b-154">Velg **Bla gjennom** for å finne filen **Modell for å lære JOIN-datakilder.versjon.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-154">Select **Browse** to find the **Model to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="a7b7b-155">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-155">Select **OK**.</span></span>
3. <span data-ttu-id="a7b7b-156">Importer konfigurasjonsfilen for ER-modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-156">Import the ER model mapping configuration file.</span></span>
    1. <span data-ttu-id="a7b7b-157">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-157">Select **Exchange**.</span></span>
    2. <span data-ttu-id="a7b7b-158">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-158">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="a7b7b-159">Velg **Bla gjennom** for å finne filen **Tilordning for å lære JOIN-datakilder.versjon.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-159">Select **Browse** to find the **Mapping to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="a7b7b-160">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-160">Select **OK**.</span></span>
4.  <span data-ttu-id="a7b7b-161">Importer ER-formatkonfigurasjonsfilen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-161">Import the ER format configuration file.</span></span>
    1. <span data-ttu-id="a7b7b-162">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-162">Select **Exchange**.</span></span>
    2. <span data-ttu-id="a7b7b-163">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-163">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="a7b7b-164">Velg **Bla gjennom** for å finne filen **Format for å lære JOIN-datakilder.versjon.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-164">Select **Browse** to find the **Format to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="a7b7b-165">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-165">Select **OK**.</span></span>
5.  <span data-ttu-id="a7b7b-166">I konfigurasjonstreet utvider du elementet for **Modell for å lære JOIN-datakilder** samt andre modellelementer (når det er tilgjengelig).</span><span class="sxs-lookup"><span data-stu-id="a7b7b-166">In the configurations tree, expand the **Model to learn JOIN data sources** item as well as other model items (when available).</span></span>
6.  <span data-ttu-id="a7b7b-167">Se på listen over ER-konfigurasjoner i treet i tillegg til versjonsdetaljer i hurtigfanen **Versjoner** – de brukes som datakilden for eksempelrapporten.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-167">Observe the list of ER configurations in the tree as well as version details on the **Versions** fast tab – they will be used as the source of data for your sample report.</span></span>

    ![Side for konfigurasjoner for elektronisk rapportering](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a><span data-ttu-id="a7b7b-169">Slå på alternativer for utførelsessporing</span><span class="sxs-lookup"><span data-stu-id="a7b7b-169">Turn on execution trace options</span></span>
1.  <span data-ttu-id="a7b7b-170">Velg **KONFIGURASJONER**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-170">Select **CONFIGURATIONS**.</span></span>
2.  <span data-ttu-id="a7b7b-171">Velg **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-171">Select **User parameters**.</span></span>
3.  <span data-ttu-id="a7b7b-172">Angi parametere for utførelsessporing som vist på skjermbildet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-172">Set execution trace parameters as shown on the screenshot below.</span></span>

    ![Siden brukerparametere for elektronisk rapportering](./media/GER-JoinDS-Parameters.PNG)

    <span data-ttu-id="a7b7b-174">Når disse parameterne er aktivert, genereres utførelsessporingen for hver utføring av den importerte ER-formatfilen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-174">With these parameters turned on, for every execution of the imported ER format file, the execution trace will be generated.</span></span> <span data-ttu-id="a7b7b-175">Ved hjelp av detaljer om generert utførelsessporing kan du analysere utførelsen av ER-format- og ER-modelltilordninger.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-175">Using details of generated execution trace, you can analyze the execution of ER format and ER model mapping components.</span></span> <span data-ttu-id="a7b7b-176">Gå til siden [Spore utførelse av ER-format for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md) for flere detaljer om sporingsfunksjonen for ER-utførelse.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-176">Visit the [Trace execution of ER format to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md) page for more details about ER execution trace feature.</span></span>

### <a name="review-er-model-mapping-part-1"></a><span data-ttu-id="a7b7b-177">Gjennomgå ER-modelltilordning (del 1)</span><span class="sxs-lookup"><span data-stu-id="a7b7b-177">Review ER model mapping (part 1)</span></span>

<span data-ttu-id="a7b7b-178">Se gjennom innstillingene for komponenten for ER-modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-178">Review settings of the ER model mapping component.</span></span> <span data-ttu-id="a7b7b-179">Komponenten konfigureres for å få tilgang til informasjon om versjoner av ER-konfigurasjoner, detaljer om konfigurasjoner og konfigurasjonsleverandører uten bruk av datakilder av typen **Join**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-179">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers without using data sources of the **Join** type.</span></span>

1.  <span data-ttu-id="a7b7b-180">Velg konfigurasjonen **Tilordning for å lære JOIN-datakilder**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-180">Select **Mapping to learn JOIN data sources** configuration.</span></span>
2.  <span data-ttu-id="a7b7b-181">Velg **Utforming** for å åpne listen over tilordninger.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-181">Select **Designer** to open the list of mappings.</span></span>
3.  <span data-ttu-id="a7b7b-182">Velg **Utforming** for å se gjennom tilordningensdetaljer.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-182">Select **Designer** to review the mapping details.</span></span> 
4.  <span data-ttu-id="a7b7b-183">Velg **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-183">Select **Show details**.</span></span>
5.  <span data-ttu-id="a7b7b-184">I konfigurasjonstreet utvider du datamodellelementene **Set1** og **Set1.Details**:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-184">In the configurations tree, expand the **Set1** and **Set1.Details** data model items:</span></span>

    1. <span data-ttu-id="a7b7b-185">Bindingen **Details: Record list = Versions** angir at elementet **Set1.Details** er bundet til datakilden **Versions**, som returnerer poster i tabellen **ERSolutionVersionTable**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-185">Binding **Details: Record list = Versions** indicates that the **Set1.Details** item is bound to the **Versions** data source returning records of the **ERSolutionVersionTable** table.</span></span> <span data-ttu-id="a7b7b-186">Hver post i denne tabellen representerer en enkelt versjon av en ER-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-186">Each record of this table represents a single version of an ER configuration.</span></span> <span data-ttu-id="a7b7b-187">Innholdet i denne tabellen vises i hurtigkategorien **Versjoner** på siden **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-187">The content of this table is presented in the **Versions** fast tab on the **Configurations** page.</span></span>
    2. <span data-ttu-id="a7b7b-188">Bindingen **ConfigurationVersion: String = @.PublicVersionNumber** betyr at verdien av den offentlige versjonen av hver ER-konfigurasjonsversjon er tatt fra feltet **PublicVersionNumber** i tabellen **ERSolutionVersionTable** og plassert i elementet **ConfigurationVersion**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-188">Binding **ConfigurationVersion: String = @.PublicVersionNumber** means that the value of the public version of each ER configuration’s version is taken from the **PublicVersionNumber** field of the **ERSolutionVersionTable** table and placed to the **ConfigurationVersion** item.</span></span>
    3. <span data-ttu-id="a7b7b-189">Bindingen **ConfigurationTitle: String = @.'>Relations'.Solution.Name** angir at navnet på en ER-konfigurasjon er tatt fra feltet **Name** i tabellen **ERSolutionTable** via mange-til-én-relasjonen (**>Relations**) mellom tabellene **ERSolutionVersionTable** og **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-189">Binding **ConfigurationTitle: String = @.'>Relations'.Solution.Name** indicates that the name of an ER configuration is taken from the **Name** field of the **ERSolutionTable** table assessing by using the many-to-one relation (**'>Relations'**) between the **ERSolutionVersionTable** and **ERSolutionTable** tables.</span></span> <span data-ttu-id="a7b7b-190">Navn på ER-konfigurasjoner av gjeldende programforekomst vises i konfigurasjonstreet på siden **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-190">Names of ER configurations of the current application instance are presented in the configurations tree on the **Configurations** page.</span></span>
    4. <span data-ttu-id="a7b7b-191">Bindingen **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** betyr at navnet på konfigurasjonsleverandøren som eier gjeldende konfigurasjon, hentes fra feltet **Name** i tabellen **ERVendorTable**, via mange-til-én-realsjonen mellom tabellene **ERSolutionTable** og **ERVendorTable**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-191">Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** means that the name of the configuration provider that owns the current configuration is taken from the **Name** field of the **ERVendorTable** table assessing by using the many-to-one relation between **ERSolutionTable** and **ERVendorTable** tables.</span></span> <span data-ttu-id="a7b7b-192">Navnene på ER-konfigurasjonsleverandørene vises i konfigurasjonstreet på siden **Konfigurasjoner** på sidehodet for hver konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-192">Names of ER configuration providers are presented in the configurations tree on the **Configurations** page on the page header for each configuration.</span></span> <span data-ttu-id="a7b7b-193">Du finner hele listen med ER-konfigurasjonsleverandører på tabellsiden **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjonsleverandør**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-193">The entire list of ER configuration providers can be found on the **Organization administration \> Electronic reporting \> Configuration provider** table page.</span></span>

    ![Siden ER-utforming av modelltilordning](./media/GER-JoinDS-Set1Review.PNG)

6.  <span data-ttu-id="a7b7b-195">I konfigurasjonstreet utvider du datamodellelementet **Set1.Summary**:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-195">In the configurations tree, expand the **Set1.Summary** data model item:</span></span>

    1. <span data-ttu-id="a7b7b-196">Bindingene **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** angir at elementet **Set1.Summary.VersionsNumber** er bundet til **VersionsNumber**-aggregasjonfeltet i **VersionsSummary**-datakilden av **GroupBy**-typen som ble konfigurert til å returnere antallet poster i tabellen **ERSolutionVersionTable** via datakilden **Versions**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-196">Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** indicates that the **Set1.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **VersionsSummary** data source of the **GroupBy** type that was configured to return the number of records of the **ERSolutionVersionTable** table via the **Versions** data source.</span></span>

    ![Siden for GROUPBY-datakildeparametere](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  <span data-ttu-id="a7b7b-198">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-198">Close the page.</span></span>

### <a name="review"></a> <span data-ttu-id="a7b7b-199">Gjennomgå ER-modelltilordning (del 2)</span><span class="sxs-lookup"><span data-stu-id="a7b7b-199">Review ER model mapping (part 2)</span></span>

<span data-ttu-id="a7b7b-200">Se gjennom innstillingene for komponenten for ER-modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-200">Review settings of the ER model mapping component.</span></span> <span data-ttu-id="a7b7b-201">Komponenten konfigureres for å få tilgang til informasjon om versjoner av ER-konfigurasjoner, detaljer om konfigurasjoner og konfigurasjonsleverandører ved å bruke en datakilde av typen **Join**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-201">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers with using a data source of the **Join** type.</span></span>

1.  <span data-ttu-id="a7b7b-202">I konfigurasjonstreet utvider du datamodellelementene **Set2** og **Set2.Details**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-202">In the configurations tree, expand the **Set2** and **Set2.Details** data model items.</span></span> <span data-ttu-id="a7b7b-203">Legg merke til at **Details: Record list = Details** angir at elementet **Set2.Details** er bundet til **Details**-datakilden som er konfigurert som datakilde av typen **Join**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-203">Note that the binding **Details: Record list = Details** indicates that the **Set2.Details** item is bound to the **Details** data source configured as the data source of the **Join** type.</span></span>

    ![Siden ER-utforming av modelltilordning](./media/GER-JoinDS-Set2Review.PNG)

    <span data-ttu-id="a7b7b-205">Datakilden for **Join** kan legges til ved å velge datakilden **Functions\Join**:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-205">The **Join** data source can be added by selecting the **Functions\Join** data source:</span></span>

    ![Siden ER-utforming av modelltilordning](./media/GER-JoinDS-AddJoinDS.PNG)

2.  <span data-ttu-id="a7b7b-207">Velg datakilden **Details**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-207">Select **Detail**s data source.</span></span>
3.  <span data-ttu-id="a7b7b-208">Velg **Rediger** i ruten **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-208">Select **Edit** in the **Data sources** pane.</span></span>
4.  <span data-ttu-id="a7b7b-209">Velg **Rediger join**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-209">Select **Edit join**.</span></span>
5.  <span data-ttu-id="a7b7b-210">Velg **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-210">Select **Show details**.</span></span>

    ![Siden med JOIN-parametre for datakilde](./media/GER-JoinDS-JoinDSEditor.PNG)

    <span data-ttu-id="a7b7b-212">Denne siden brukes til å utforme den påkrevde datakilden for **Join-type**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-212">This page is used to design the required data source of the **Join type**.</span></span> <span data-ttu-id="a7b7b-213">Under kjøring vil denne datakilden opprette én enkelt sammenføyet liste med poster fra datakildene i rutenettet **Sammenkoblet liste**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-213">At runtime, this data source will create a single joined list of records from the data sources in the **Joined list** grid.</span></span> <span data-ttu-id="a7b7b-214">Sammenføyning av poster starter fra datakilden **ConfigurationProviders** som er i rutenettet som første (**Type**-kolonnen er tom for den).</span><span class="sxs-lookup"><span data-stu-id="a7b7b-214">Join of records will start from the **ConfigurationProviders** data source that is in the grid as a first one (the **Type** column is blank for it).</span></span> <span data-ttu-id="a7b7b-215">Poster med alle andre datakilder vil bli føyd sammen til poster av den overordnede datakilden basert på rekkefølgen i dette rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-215">Records of every other data source will be joined consequently to records of the parent data source based on its order in this grid.</span></span> <span data-ttu-id="a7b7b-216">Alle Join-datakilder må konfigureres som en datakilde nestet under en måldatakilde (**1Versions**-datakilden er nestet under én **1Configurations**, **1Configurations**-datakilden som er nestet under én **ConfigurationProviders**).</span><span class="sxs-lookup"><span data-stu-id="a7b7b-216">Every joining data source must be configured as a data source nested under a target data source (**1Versions** data source is nested under **1Configurations** one; **1Configurations** data source is nested under **ConfigurationProviders** one).</span></span> <span data-ttu-id="a7b7b-217">Hver konfigurerte datakilde må inneholde betingelsene for Join-sammenkoblingen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-217">Each configured data source must contain the conditions for the join.</span></span> <span data-ttu-id="a7b7b-218">I datakilden for denne bestemte **Join** er følgende Join-sammenkoblinger definert:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-218">In the data source for this particular **Join**, the following joins are defined:</span></span>

    - <span data-ttu-id="a7b7b-219">Hver post i datakilden **ConfigurationProviders** (henvises til i **ERVendorTable**-tabellen) er bare koblet sammen med poster av én **1Configurations** (henvises til i **ERSolutionTable**-tabell) som har samme verdi i feltene **SolutionVendor** og **RecId**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-219">Each record of the **ConfigurationProviders** data source (referred to the **ERVendorTable** table) is joined with only records of the **1Configurations** one (referred to in the **ERSolutionTable** table) having the same value in the **SolutionVendor** and **RecId** fields.</span></span> <span data-ttu-id="a7b7b-220">Den **indre join**-typen brukes for denne sammenføyningen samt følgende betingelser for samsvarende poster:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-220">The **Inner join** type is used for this join as well as the following conditions for matching records:</span></span> 

    <span data-ttu-id="a7b7b-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span><span class="sxs-lookup"><span data-stu-id="a7b7b-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span></span>

    - <span data-ttu-id="a7b7b-222">Hver post i datakilden **1Configurations** (henvises til i **ERSolutionTable**-tabellen) er bare koblet til poster av én **1Configurations** (henvises til i **ERSolutionVersionTable**-tabellen) som har samme verdi i feltene **Solution** og **RecId**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-222">Each record of the **1Configurations** data source (referred to the **ERSolutionTable** table) is joined with the only records of the **1Versions** one (referred to the **ERSolutionVersionTable** table) having the same value in the **Solution** and **RecId** fields.</span></span> <span data-ttu-id="a7b7b-223">Den **Indre join**-typen brukes for denne sammenføyningen samt følgende betingelser for samsvarende poster:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-223">**Inner join** type is used for this join as well as the following conditions for matching records:</span></span>

    <span data-ttu-id="a7b7b-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span><span class="sxs-lookup"><span data-stu-id="a7b7b-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span></span>

    - <span data-ttu-id="a7b7b-225">**Utfør**-alternativet er konfigurert som **Spørring**, som betyr at denne join-datakilden utføres under kjøring på databasenivå som et direkte SQL-kall.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-225">**Execute** option is configured as **Query** meaning that this join data source will be executed at runtime on database level as a direct SQL call.</span></span>

    <span data-ttu-id="a7b7b-226">Legg merke til at ved sammekobling av poster i datakilder som representerer programtabeller, kan du angi join-vilkår ved å bruke andre felt enn de som beskriver eksisterende i AOT-relasjoner mellom disse tabellene.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-226">Note that for joining records of data sources representing application tables, you can specify join conditions by using pairs of fields other than ones that describe existing in AOT relations between these tables.</span></span> <span data-ttu-id="a7b7b-227">Denne sammenkoblingstypen kan også konfigureres til å utføres på databasenivå.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-227">This type of join can be configured to execute at the database level as well.</span></span>

6.  <span data-ttu-id="a7b7b-228">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-228">Close the page.</span></span>
7.  <span data-ttu-id="a7b7b-229">Velg **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-229">Select **Cancel**.</span></span>
8.  <span data-ttu-id="a7b7b-230">I konfigurasjonstreet utvider du datamodellelementet **Set2.Summary**:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-230">In the configurations tree, expand the **Set2.Summary** data model item:</span></span>

    - <span data-ttu-id="a7b7b-231">Bindingen **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** angir at elementet **Set2.Summary.VersionsNumber** er bundet til **VersionsNumber**-aggregasjonfeltet i **DetailsSummary**-datakilden av **GroupBy**-typen som ble konfigurert til å returnere antallet sammenkoblede poster i **Details**-datakilden av typen **Join**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-231">Binding **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** indicates that the **Set2.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **DetailsSummary** data source of the **GroupBy** type that was configured to return the number of joined records of the **Details** data source of the **Join** type.</span></span>
    - <span data-ttu-id="a7b7b-232">Legg merke til at stedsalternativet **Utfør** er konfigurert som **Spørring**, som betyr at denne **GroupBy**-datakilden utføres under kjøring som et direkte SQL-kall på databasenivå.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-232">Note that the **Execution** location option is configured as **Query** meaning that this **GroupBy** data source will be executed at runtime as a direct SQL call at the database level.</span></span> <span data-ttu-id="a7b7b-233">Dette er mulig fordi basisdatakilden **Details** for typen **Join** er konfigurert som utført på databasenivå.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-233">This is possible because the base data source **Details** of the **Join** type is configured as executed at the database level.</span></span>

    ![Siden for GROUPBY-datakildeparametere](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  <span data-ttu-id="a7b7b-235">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-235">Close the page.</span></span>
10. <span data-ttu-id="a7b7b-236">Velg **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-236">Select **Cancel**.</span></span>

### <a name="executeERformat"></a> <span data-ttu-id="a7b7b-237">Utføre ER-format</span><span class="sxs-lookup"><span data-stu-id="a7b7b-237">Execute ER format</span></span>

1.  <span data-ttu-id="a7b7b-238">Få tilgang til Finance eller RCS i den andre økten av webleseren med samme legitimasjon og firma som i den første økten.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-238">Access Finance or RCS in the second session of your web browser using same credentials and company as in the first session.</span></span>
2.  <span data-ttu-id="a7b7b-239">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-239">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="a7b7b-240">Utvid konfigurasjonen **Modell for å lære JOIN-datakilder**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-240">Expand **Model to learn JOIN data sources** configuration.</span></span>
4.  <span data-ttu-id="a7b7b-241">Velg konfigurasjonen **Format for å lære JOIN-datakilder**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-241">Select **Format to learn JOIN data sources** configuration.</span></span>
5.  <span data-ttu-id="a7b7b-242">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-242">Select **Designer**.</span></span>
6.  <span data-ttu-id="a7b7b-243">Velg **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-243">Select **Show details**.</span></span>
7.  <span data-ttu-id="a7b7b-244">Velg **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-244">Select **Mapping**.</span></span>
8.  <span data-ttu-id="a7b7b-245">Velg **Vis/skjul**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-245">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="a7b7b-246">Legg merke til at dette formatet er utformet for å fylle ut en generert tekstfil med en ny linje for hver versjon av en ER-konfigurasjon (**Versjon**-sekvens).</span><span class="sxs-lookup"><span data-stu-id="a7b7b-246">Note that this format is designed to populate a generated text file with a new line for every version of an ER configuration (**Version** sequence).</span></span> <span data-ttu-id="a7b7b-247">Hver genererte linje inneholder navnet på en konfigurasjonsleverandør som eier den gjeldende konfigurasjonen, konfigurasjonsnavnet og konfigurasjonsversjonen atskilt med semikolon.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-247">Each generated line will contain the name of a configuration provider owning the current configuration, the configuration name and the configuration version separated by semicolon mark.</span></span> <span data-ttu-id="a7b7b-248">Den siste linjen i den genererte filen vil inneholde antall oppdagede versjoner av ER-konfigurasjoner (**Sammendrag**-sekvens).</span><span class="sxs-lookup"><span data-stu-id="a7b7b-248">The final line of generated file will contain the number of discovered versions of ER configurations (**Summary** sequence).</span></span>

    ![Side med ER-formatutforming](./media/GER-JoinDS-FormatReview.PNG)

    <span data-ttu-id="a7b7b-250">Datakildene **Data** og **Sammendrag** brukes til å fylle ut konfigurasjonsversjonsdetaljer for den genererte filen:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-250">The **Data** and **Summary** data sources are used to populate configuration version details to the generated file:</span></span>

    - <span data-ttu-id="a7b7b-251">Informasjon fra datamodellen **Set1** brukes når du velger **Nei** for datakilden **Velger** under kjøring på siden med brukerdialogboks når ER-format kjøres.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-251">Information from the **Set1** data model is used when you choose **No** for the **Selector** data source at runtime on the user dialog page when running ER format.</span></span>
    - <span data-ttu-id="a7b7b-252">Informasjon fra datamodellen **Set2** brukes når du velger **Ja** for datakilden **Velger** under kjøring på siden med brukerdialogboks.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-252">Information from the **Set2** data model is used when you choose **Yes** for the **Selector** data source at runtime on the user dialog page.</span></span>

    ![Side med ER-formatutforming](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  <span data-ttu-id="a7b7b-254">Velg **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-254">Select **Run**.</span></span>
10. <span data-ttu-id="a7b7b-255">Velg **Nei** på dialogbokssiden i feltet **Bruk JOIN-datakilder**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-255">On the dialog page, select **No** in the **Use JOIN data source** field.</span></span>
11. <span data-ttu-id="a7b7b-256">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-256">Select **OK**.</span></span>
12. <span data-ttu-id="a7b7b-257">Se gjennom den genererte filen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-257">Review generated file.</span></span>

    ![Siden med ER-brukerdialogboks](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><span data-ttu-id="a7b7b-259">Analysere utførelsessporing i ER-format</span><span class="sxs-lookup"><span data-stu-id="a7b7b-259">Analyze ER format execution trace</span></span>

1.  <span data-ttu-id="a7b7b-260">I den første Finance- eller RCS-økten velger du **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-260">In the first session of Finance or RCS, select **Designer**.</span></span>
2.  <span data-ttu-id="a7b7b-261">Velg **Ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-261">Select **Performance trac**e.</span></span>
3.  <span data-ttu-id="a7b7b-262">I rutenettet **Ytelsessporing** velger du den øverste oppføringen i den siste utførelsessporingen i et ER-format som brukte den gjeldende modelltilordningskomponenten.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-262">In the **Performance trace** grid, select the top-most record of the latest execution trace of an ER format that used the current model mapping component.</span></span>
4.  <span data-ttu-id="a7b7b-263">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-263">Select **OK**.</span></span>

    <span data-ttu-id="a7b7b-264">Legg merke til at ttførelsesstatistikken informerer deg om dupliserte kall til programtabeller:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-264">Note that execution statistics informs you about duplicated calls to application tables:</span></span>

    - <span data-ttu-id="a7b7b-265">**ERSolutionTable** er kalt så mange ganger som du har konfigurasjonsversjonsposter i **ERSolutionVersionTable** -tabellen, men antallet slike kall kan til tider bli redusert for å forbedre ytelsen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-265">**ERSolutionTable** has been called as many times as you have configuration version records in the **ERSolutionVersionTable** table, while the number of such calls could be reduced in times for performance improvement.</span></span>
    - <span data-ttu-id="a7b7b-266">**ERVendorTable** er kalt to ganger for hver konfigurasjonsversjonspost som ble oppdaget i tabellen **ERSolutionVersionTable**, men antallet slike kall kan imidlertid blir redusert.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-266">**ERVendorTable** has been called twice for every configuration version record that was discovered in the **ERSolutionVersionTable** table, while the number of such calls could be reduced as well.</span></span>

    ![Siden ER-utforming av modelltilordning](./media/GER-JoinDS-Set1Run2.PNG)

5.  <span data-ttu-id="a7b7b-268">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-268">Close the page.</span></span>

### <a name="execute-er-format"></a><span data-ttu-id="a7b7b-269">Utføre ER-format</span><span class="sxs-lookup"><span data-stu-id="a7b7b-269">Execute ER format</span></span>

1.  <span data-ttu-id="a7b7b-270">Bytt til webleserkategorien med den andre økten av Finance eller RCS.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-270">Switch to your web browser tab with the second session of Finance or RCS.</span></span>
2.  <span data-ttu-id="a7b7b-271">Velg **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-271">Select **Run**.</span></span>
3.  <span data-ttu-id="a7b7b-272">Velg **Ja** på dialogbokssiden i feltet **Bruk JOIN-datakilder**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-272">On the dialog page, select **Yes** in the **Use JOIN data source** field.</span></span>
4.  <span data-ttu-id="a7b7b-273">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-273">Select **OK**.</span></span>
5.  <span data-ttu-id="a7b7b-274">Se gjennom den genererte filen.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-274">Review generated file.</span></span>

    ![Siden med ER-brukerdialogboks](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> <span data-ttu-id="a7b7b-276">Analysere utførelsessporing i ER-format</span><span class="sxs-lookup"><span data-stu-id="a7b7b-276">Analyze ER format execution trace</span></span>

1.  <span data-ttu-id="a7b7b-277">I den første Finance- eller RCS-økten velger du **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-277">In the first session of Finance or RCS, select **Designer**.</span></span>
2.  <span data-ttu-id="a7b7b-278">Velg **Ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-278">Select **Performance trace**.</span></span>
3.  <span data-ttu-id="a7b7b-279">I rutenettet **Ytelsessporing** velger du den øverste oppføringen som representerer den siste utførelsessporingen i et ER-format som brukte den gjeldende modelltilordningskomponenten.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-279">In the **Performance trace** grid, select top-most record representing the latest execution trace of an ER format that used the current model mapping component.</span></span>
4.  <span data-ttu-id="a7b7b-280">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-280">Select **OK**.</span></span>

    <span data-ttu-id="a7b7b-281">Legg merke til at utførelsesstatistikken informerer deg om følgende:</span><span class="sxs-lookup"><span data-stu-id="a7b7b-281">Note that execution statistics informs you about the following:</span></span>

    - <span data-ttu-id="a7b7b-282">Programdatabasen har blitt kalt én gang for å hente poster fra tabellene **ERVendorTable**, **ERSolutionTable** og **ERSolutionVersionTable** for å få tilgang til de obligatoriske feltene.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-282">Application database has been called once to get records from **ERVendorTable**, **ERSolutionTable**, and **ERSolutionVersionTable** tables to access required fields.</span></span>

    ![Siden ER-utforming av modelltilordning](./media/GER-JoinDS-Set2Run2.PNG)

    - <span data-ttu-id="a7b7b-284">Programdatabasen har blitt kalt én gang for å beregne antallet konfigurasjonsversjoner ved hjelp av sammenføyninger som ble konfigurert i datakilden **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="a7b7b-284">Application database has been called once to calculate the number of configuration versions by using joins that were configured in the **Details** data source.</span></span>

    ![Siden ER-utforming av modelltilordning](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a><span data-ttu-id="a7b7b-286">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a7b7b-286">Additional resources</span></span>

[<span data-ttu-id="a7b7b-287">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a7b7b-287">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="a7b7b-288">Spore utførelse av ER-format for å feilsøke ytelsesproblemer</span><span class="sxs-lookup"><span data-stu-id="a7b7b-288">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

