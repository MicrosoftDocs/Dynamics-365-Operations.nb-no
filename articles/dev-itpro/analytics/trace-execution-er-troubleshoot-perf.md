---
title: Spore utførelse av ER-format for å feilsøke ytelsesproblemer
description: Dette emnet inneholder informasjon om hvordan du bruker funksjonen ytelsessporing i elektronisk rapportering (ER) for å feilsøke ytelsesproblemer.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ec16bea1e4f7685f95178f848ba7348a06c31f3
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741509"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="38536-103">Spore utførelse av ER-formater for å feilsøke ytelsesproblemer</span><span class="sxs-lookup"><span data-stu-id="38536-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="38536-104">Som en del av prosessen med å utforme konfigurasjoner for elektronisk rapportering (ER) for å generere elektroniske dokumenter, definerer du metoden som brukes til å hente data ut av Microsoft Dynamics 365 for Finance and Operations, og angir den i utdataene som genereres.</span><span class="sxs-lookup"><span data-stu-id="38536-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="38536-105">Funksjonen ytelsessporing i ER bidrar til å redusere tiden og kostnadene betydelig ved innsamling av detaljer om ER-formatutførelsen og bruke dem til å feilsøke ytelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="38536-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="38536-106">Denne opplæringen inneholder retningslinjer om hvordan du kan utføre ytelsessporinger for utførte ER-formater i Finance and Operations, og hvordan du bruker informasjonen fra disse sporingene for å forbedre ytelsen.</span><span class="sxs-lookup"><span data-stu-id="38536-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="38536-107">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="38536-107">Prerequisites</span></span>

<span data-ttu-id="38536-108">Hvis du vil fullføre eksemplene i denne opplæringen, må du ha følgende tilgang:</span><span class="sxs-lookup"><span data-stu-id="38536-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="38536-109">Tilgang til Finance and Operations for én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="38536-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="38536-110">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="38536-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="38536-111">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="38536-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="38536-112">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="38536-112">System administrator</span></span>

- <span data-ttu-id="38536-113">Tilgang til forekomsten av Regulatory Configuration Service (RCS) som er klargjort for samme leietaker som Finance and Operations, for én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="38536-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="38536-114">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="38536-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="38536-115">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="38536-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="38536-116">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="38536-116">System administrator</span></span>

<span data-ttu-id="38536-117">Du må også laste ned og lagre følgende filer lokalt.</span><span class="sxs-lookup"><span data-stu-id="38536-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="38536-118">Fil</span><span class="sxs-lookup"><span data-stu-id="38536-118">File</span></span>                                  | <span data-ttu-id="38536-119">Innhold</span><span class="sxs-lookup"><span data-stu-id="38536-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="38536-120">Ytelsessporingsmodell.versjon.1</span><span class="sxs-lookup"><span data-stu-id="38536-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="38536-121">Eksempel ER-datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="38536-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="38536-122">Ytelsessporingsmetadata.versjon.1</span><span class="sxs-lookup"><span data-stu-id="38536-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="38536-123">Eksempel ER-metadatakonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="38536-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="38536-124">Ytelsessporingstilordning.versjon.1.1</span><span class="sxs-lookup"><span data-stu-id="38536-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="38536-125">Eksempel ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="38536-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="38536-126">Ytelsessporingsformat.versjon.1.1</span><span class="sxs-lookup"><span data-stu-id="38536-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="38536-127">Eksempel ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="38536-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="38536-128">Konfigurere ER-parametere</span><span class="sxs-lookup"><span data-stu-id="38536-128">Configure ER parameters</span></span>

<span data-ttu-id="38536-129">Hver ER-ytelsessporing som genereres i Finance and Operations, lagres som et vedlegg til utførelsesloggposten.</span><span class="sxs-lookup"><span data-stu-id="38536-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="38536-130">Dokumentbehandlingsrammeverket (DM) for Finance and Operations brukes til å administrere disse vedleggene.</span><span class="sxs-lookup"><span data-stu-id="38536-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="38536-131">Du må konfigurere ER-parameterne på forhånd for å angi DM-dokumenttypen som skal brukes til å knytte ytelsesspor.</span><span class="sxs-lookup"><span data-stu-id="38536-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="38536-132">I Finance and Operations i **Elektronisk rapportering**-arbeidsområdet velger du **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="38536-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="38536-133">På siden **Parametere for elektronisk rapportering** i kategorien **Vedlegg** på siden **Andre** velger du deretter DM-dokumenttypen som skal brukes for ytelsessporinger.</span><span class="sxs-lookup"><span data-stu-id="38536-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Siden for elektroniske rapporteringsparametere i Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="38536-135">For å være tilgjengelig i **Andre**-oppslagsfeltet må en DM-dokumenttype konfigureres på følgende måte på siden **Dokumenttyper** (**Organisasjonsstyring \> Dokumentstyring \> Dokumenttyper**):</span><span class="sxs-lookup"><span data-stu-id="38536-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="38536-136">**Klasse:** Tilknytt fil</span><span class="sxs-lookup"><span data-stu-id="38536-136">**Class:** Attach file</span></span>
- <span data-ttu-id="38536-137">**Gruppe:** Fil</span><span class="sxs-lookup"><span data-stu-id="38536-137">**Group:** File</span></span>

![Dokumenttypeside i Finance and Operations](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="38536-139">Den valgte dokumenttypen må være tilgjengelig i alle firmaer av gjeldende Finance and Operations-forekomst, fordi DM-vedlegg er firmaspesifikke.</span><span class="sxs-lookup"><span data-stu-id="38536-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="38536-140">Konfigurere RCS-parametere</span><span class="sxs-lookup"><span data-stu-id="38536-140">Configure RCS parameters</span></span>

<span data-ttu-id="38536-141">ER-ytelsessporinger som genereres i Finance and Operations, importeres til RCS for analyse ved hjelp av ER-formatdesigneren og ER-tilordningsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="38536-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="38536-142">Fordi ER-ytelsesspor lagres som vedlegg i utførelsesloggposten som er relatert til ER-formatet, må du konfigurere RCS-parametere på forhånd, for å angi DM-dokumenttypen som skal brukes for å knytte til ytelsessporinger.</span><span class="sxs-lookup"><span data-stu-id="38536-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="38536-143">For RCS-forekomsten som er klargjort for ditt firma, går du til **Elektronisk rapportering** og velger **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="38536-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="38536-144">På siden **Parametere for elektronisk rapportering** i kategorien **Vedlegg** på siden **Andre** velger du deretter DM-dokumenttypen som skal brukes for ytelsessporinger.</span><span class="sxs-lookup"><span data-stu-id="38536-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Siden Parametere for elektronisk rapportering i RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="38536-146">For å være tilgjengelig i **Andre**-oppslagsfeltet må en DM-dokumenttype konfigureres på følgende måte på siden **Dokumenttyper** (**Organisasjonsstyring \> Dokumentstyring \> Dokumenttyper**):</span><span class="sxs-lookup"><span data-stu-id="38536-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="38536-147">**Klasse:** Tilknytt fil</span><span class="sxs-lookup"><span data-stu-id="38536-147">**Class:** Attach file</span></span>
- <span data-ttu-id="38536-148">**Gruppe:** Fil</span><span class="sxs-lookup"><span data-stu-id="38536-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="38536-149">Utforme en ER-løsning</span><span class="sxs-lookup"><span data-stu-id="38536-149">Design an ER solution</span></span>

<span data-ttu-id="38536-150">Anta at du har begynt å utforme en ny ER-løsning for å generere en ny rapport som presenterer leverandørtransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="38536-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="38536-151">For øyeblikket kan du finne transaksjonene for en valgt leverandør på siden **Leverandørtransaksjoner** (gå til **Leverandører \> Leverandører \> Alle leverandør**, velg en leverandør, og deretter, i handlingsruten i kategorien **Leverandør** i gruppen **Transaksjoner**, velger du **Transaksjoner**).</span><span class="sxs-lookup"><span data-stu-id="38536-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="38536-152">Du vil imidlertid ha alle leverandørtransaksjoner samtidig i ett elektronisk dokument i XML-format.</span><span class="sxs-lookup"><span data-stu-id="38536-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="38536-153">Denne løsningen vil bestå av flere ER-konfigurasjoner som inneholder den nødvendige datamodellen, metadataene, modelltilordningen og formatkomponentene.</span><span class="sxs-lookup"><span data-stu-id="38536-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="38536-154">Logg deg på forekomsten av RCS som er klargjort for firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="38536-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="38536-155">I denne opplæringen skal du opprette og endre konfigurasjoner for eksempelfirmaet **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="38536-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="38536-156">Kontroller derfor at denne konfigurasjonsleverandøren er lagt til RCS og valgt som aktiv.</span><span class="sxs-lookup"><span data-stu-id="38536-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="38536-157">Hvis du ha instruksjoner, se fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="38536-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="38536-158">I arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="38536-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="38536-159">På siden **Konfigurasjoner** importerer du ER-konfigurasjoner som du lastet ned som en forutsetning til RCS, i denne rekkefølgen: datamodell, metadata, modelltilordning, format.</span><span class="sxs-lookup"><span data-stu-id="38536-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="38536-160">For hver konfigurasjon følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="38536-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="38536-161">På siden Handling velger du **Exchange \> Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="38536-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="38536-162">Velg **Bla gjennom** for å velge den riktige filen for den nødvendige ER-konfigurasjonen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="38536-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="38536-163">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="38536-163">Select **OK**.</span></span>

    ![Siden Konfigurasjoner i RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="38536-165">Kjør ER-løsningen for å spore kjøring</span><span class="sxs-lookup"><span data-stu-id="38536-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="38536-166">Anta at du er ferdig med å utforme den første versjonen av ER-løsningen.</span><span class="sxs-lookup"><span data-stu-id="38536-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="38536-167">Nå skal du teste den i Finance and Operations-forekomsten og analysere kjøringsytelsen.</span><span class="sxs-lookup"><span data-stu-id="38536-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="38536-168">Importere en ER-konfigurasjon fra RCS til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="38536-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="38536-169">Logg på forekomsten av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="38536-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="38536-170">I denne opplæringen skal du importere konfigurasjonene fra RCS-forekomsten (der du utformer ER-komponentene) i forekomsten av Finance and Operations (der du tester og til slutt bruker dem).</span><span class="sxs-lookup"><span data-stu-id="38536-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="38536-171">Du må derfor kontrollere at alle de nødvendige artefaktene er forberedt.</span><span class="sxs-lookup"><span data-stu-id="38536-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="38536-172">Hvis du vil ha instruksjoner, kan du se fremgangsmåten [Importere ER-konfigurasjoner (Electronic Reporting) fra Regulatory Configuration Service (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="38536-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="38536-173">Følg disse trinnene for å importere konfigurasjonene fra RCS til Finance and Operations::</span><span class="sxs-lookup"><span data-stu-id="38536-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="38536-174">I arbeidsområdet **Elektronisk rapportering**, på flisen for konfigurasjonsleverandøren **Litware, Inc.**, velger du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="38536-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="38536-175">På **Konfigurasjonsrepositorium**-siden velger du repositoriet for **RCS**-typen, og deretter velger du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="38536-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="38536-176">I hurtigfanen **Konfigurasjoner** velger du **Ytelsessporingsformat**- konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="38536-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="38536-177">I **Versjoner**-hurtigkategorien velger du versjon **1.1** av den valgte konfigurasjonen, og deretter velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="38536-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfigurasjonsrepositorium-siden i Finance and Operations](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="38536-179">De tilsvarende versjonene av konfigurasjonene for datamodell og modelltilordning importeres automatisk som forutsetninger for den importerte ER-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="38536-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="38536-180">Aktivere ER-ytelsessporing</span><span class="sxs-lookup"><span data-stu-id="38536-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="38536-181">I Finance and Operations går du til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="38536-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="38536-182">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="38536-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="38536-183">Følg disse trinnene i dialogboksen **Brukerparametere** i delen **Kjøringssporing**:</span><span class="sxs-lookup"><span data-stu-id="38536-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="38536-184">I feltet **Sporingsformat for kjøring** velger du **Feilsøk sporingsformat** for å begynne å samle inn detaljer for kjøringen av ER-format.</span><span class="sxs-lookup"><span data-stu-id="38536-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="38536-185">Når denne verdien er valgt, vil ytelsessporingen samle inn informasjon om tiden som brukes på følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="38536-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="38536-186">Kjøre hver datakilde i modelltilordningen som kalles for å hente data</span><span class="sxs-lookup"><span data-stu-id="38536-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="38536-187">Behandler hver formatvare for å angi data i utdataene som genereres</span><span class="sxs-lookup"><span data-stu-id="38536-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="38536-188">Du bruker feltet **Sporingsformat for kjøring** til å angi formatet på den genererte ytelsessporingen som kjøringsdetaljene er lagret i for ER-format og tilordningselementer.</span><span class="sxs-lookup"><span data-stu-id="38536-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="38536-189">Ved å velge **Feilsøk sporingsformat** som verdi kan du analysere innholdet i sporingen i ER-operasjonsutforming og se ER-formatet eller tilordningselementene som er nevnt i sporingen.</span><span class="sxs-lookup"><span data-stu-id="38536-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="38536-190">Angi følgende alternativer til **Ja** for å samle inn bestemte detaljer for utførelsen av ER-modelltilordningen og ER-formatkomponentene:</span><span class="sxs-lookup"><span data-stu-id="38536-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="38536-191">**Samle inn spørringsstatistikk** – Når dette alternativet er aktivert, vil ytelsessporingen samle inn følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="38536-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="38536-192">Antall databasekall som er utført av datakilder</span><span class="sxs-lookup"><span data-stu-id="38536-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="38536-193">Antall dupliserte kall til databasen</span><span class="sxs-lookup"><span data-stu-id="38536-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="38536-194">Detaljer for SQL-setningene som ble brukt til å opprette databasekall</span><span class="sxs-lookup"><span data-stu-id="38536-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="38536-195">**SSpor tilgang for hurtigbufring** – Når dette alternativet er aktivert, samler ytelsessporingsinformasjon inn informasjon om ER-modelltilordningens hurtigbufferbruk.</span><span class="sxs-lookup"><span data-stu-id="38536-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="38536-196">**Spor datatilgang** – Når dette alternativet er aktivert, samler ytelsessporingeninformasjon inn informajson om antall kall til databasen for utførte datakilder av typen postliste.</span><span class="sxs-lookup"><span data-stu-id="38536-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="38536-197">**Sporingslisteopplisting** – Når dette alternativet er aktivert, samler ytelsessporingeninformasjon inn informajson om antall poster som forespørres fra datakilder av typen postliste.</span><span class="sxs-lookup"><span data-stu-id="38536-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="38536-198">Parameterne i dialogboksen **Brukerparametere** er spesifikke for brukeren og det gjeldende firmaet.</span><span class="sxs-lookup"><span data-stu-id="38536-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Dialogboksen Brukerparametere i Finance and Operations](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="38536-200">Kjør ER-formatet</span><span class="sxs-lookup"><span data-stu-id="38536-200">Run the ER format</span></span>

1. <span data-ttu-id="38536-201">I Finance and Operations velger du **DEMF**-selskapet.</span><span class="sxs-lookup"><span data-stu-id="38536-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="38536-202">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="38536-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="38536-203">På siden **Konfigurasjoner** i konfigurasjonstreet, velger du elementet **Ytelsessporingsformat**.</span><span class="sxs-lookup"><span data-stu-id="38536-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="38536-204">Velg **Kjør** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="38536-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="38536-205">Legg merke til at filen som genereres, presenterer informasjon om 265 transaksjoner for seks leverandører.</span><span class="sxs-lookup"><span data-stu-id="38536-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="38536-206">Se gjennom utførelsessporing</span><span class="sxs-lookup"><span data-stu-id="38536-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="38536-207">Eksportere den genererte sporingen fra Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="38536-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="38536-208">Ytelsessporinger kobles fra kilde-ER-formatet og kan serialiseres til en ekstern zip-fil.</span><span class="sxs-lookup"><span data-stu-id="38536-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="38536-209">I Finance and Operations går du til **Organisasjonsstyring \> Elektronisk rapportering \> Feilsøkingslogger for konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="38536-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="38536-210">På siden **Kjøringslogger for elektronisk rapportering**, i venstre rute i feltet **Konfigurasjonsnavn**, velger du **Ytelsessporingsformat** for å finne loggpostene som er generert ved å utføre **Ytelsessporingsformat**.</span><span class="sxs-lookup"><span data-stu-id="38536-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="38536-211">Velg **Vedlegg**-knappen (bindersikonet) i øvre høyre hjørne på siden, eller trykk på **Ctrl+Skift+A**.</span><span class="sxs-lookup"><span data-stu-id="38536-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Vedlegg-knappen på siden Kjøringslogger for elektronisk rapportering i Finance and Operations](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="38536-213">På siden **Vedlegg for Kjøringslogger for elektronisk rapportering** velger du **Åpne** for å hente ytelsessporing som en zip-fil og lagre den lokalt.</span><span class="sxs-lookup"><span data-stu-id="38536-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Siden Vedlegg for Kjøringslogger for elektronisk rapportering i Finance and Operations](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="38536-215">Sporingen som genereres, har en referanse til kilde-ER-rapporten via en unik rapport-ID bare i **GUID**-format.</span><span class="sxs-lookup"><span data-stu-id="38536-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="38536-216">Versjonsnummereringen for formatet vurderes ikke.</span><span class="sxs-lookup"><span data-stu-id="38536-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="38536-217">Legg merke til at tilknytningen mellom ytelsessporingen som er generert for det utførte ER-formatet og ER-modelltilordningen, er basert på rotbeskrivelsen som ble brukt og den felles datamodellen.</span><span class="sxs-lookup"><span data-stu-id="38536-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="38536-218">Versjonsnummereringen for formatet og modelltilordningen vurderes ikke.</span><span class="sxs-lookup"><span data-stu-id="38536-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="38536-219">Innstillingen til **Standard for modelltilordning**-flagget for modelltilordningen blir heller ikke vurdert.</span><span class="sxs-lookup"><span data-stu-id="38536-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="38536-220">Importere den genererte sporingen til RCS</span><span class="sxs-lookup"><span data-stu-id="38536-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="38536-221">I RCS, i arbeidsområdet **Elektronisk rapportering**, velger du flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="38536-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="38536-222">På siden **Konfigurasjoner**, i konfigurasjonstreet, utvider du elementet **Ytelsessporingsmodell**, og velg elementet **Ytelsessporingsformat**.</span><span class="sxs-lookup"><span data-stu-id="38536-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="38536-223">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="38536-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="38536-224">På siden **Formatutforming**, i handlingsruten, velger du **Ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="38536-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="38536-225">I dialogboksen **Resultatinnstillinger for ytelsessporing** velg **Importer ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="38536-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="38536-226">Velg **Bla gjennom** for å velge zip-filen du eksporterte fra Finance and Operations earlier. tidligere.</span><span class="sxs-lookup"><span data-stu-id="38536-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="38536-227">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="38536-227">Select **OK**.</span></span>

    ![Dialogboksen Resultatinnstillinger for ytelsessporing i RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="38536-229">Bruke ytelsessporing for analyse i RCS – Formatutførelse</span><span class="sxs-lookup"><span data-stu-id="38536-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="38536-230">Velg **Vis/Skjul** på **Formatutforming**-siden i RCS for å utvide innholdet for alle formatvarer.</span><span class="sxs-lookup"><span data-stu-id="38536-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="38536-231">Legg merke til at tilleggsinformasjon vises for noen varer i gjeldende format:</span><span class="sxs-lookup"><span data-stu-id="38536-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="38536-232">Den faktiske tiden som ble brukt på å legge inn data i de genererte utdataene ved hjelp av formatvaren</span><span class="sxs-lookup"><span data-stu-id="38536-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="38536-233">Den samme tiden som prosent av den totale tiden som ble brukt til å generere hele utdataene</span><span class="sxs-lookup"><span data-stu-id="38536-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Formatutformingsside i RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="38536-235">Lukk siden **Formatutforming**.</span><span class="sxs-lookup"><span data-stu-id="38536-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="38536-236">Bruke ytelsessporing for analyse i RCS – modelltilordning</span><span class="sxs-lookup"><span data-stu-id="38536-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="38536-237">I RCS, på siden **Konfigurasjoner** i konfigurasjonstreet, velger du elementet **Ytelsessporingstilordning**.</span><span class="sxs-lookup"><span data-stu-id="38536-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="38536-238">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="38536-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="38536-239">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="38536-239">Select **Designer**.</span></span>
4. <span data-ttu-id="38536-240">På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="38536-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="38536-241">Velg sporingen du importerte tidligere.</span><span class="sxs-lookup"><span data-stu-id="38536-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="38536-242">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="38536-242">Select **OK**.</span></span>

<span data-ttu-id="38536-243">Legg merke til at ny informasjon blir tilgjengelig for noen datakildeelementer av gjeldende modelltilordning:</span><span class="sxs-lookup"><span data-stu-id="38536-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="38536-244">Den faktiske tiden som ble brukt til å hente data ved hjelp av datakilden</span><span class="sxs-lookup"><span data-stu-id="38536-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="38536-245">Den samme tiden som prosent av den totale tiden som ble brukt til å kjøre hele modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="38536-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="38536-246">Legg merke til at ER informerer deg om at gjeldende modelltilordning dupliserer databaseforespørsler når VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum-datakilden kjøres.</span><span class="sxs-lookup"><span data-stu-id="38536-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="38536-247">Denne dupliseringen forekommer fordi listen over leverandørtransaksjoner kalles to ganger for hver leverandørpost som gjentas:</span><span class="sxs-lookup"><span data-stu-id="38536-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="38536-248">Det blir laget ett kall for å angi detaljer for hver transaksjon i datamodellen, basert på konfigurerte bindinger.</span><span class="sxs-lookup"><span data-stu-id="38536-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="38536-249">Det blir laget ett kall for å angi det beregnede antallet transaksjoner per leverandør i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="38536-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Melding om dupliserte databaseforespørsler på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="38536-251">Verdien **\[Q:530\]** angir at VendTrans-tabellen ble kalt 530 ganger for å returnere en post fra denne tabellen til VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum-datakilden.</span><span class="sxs-lookup"><span data-stu-id="38536-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="38536-252">Verdien **\[530\]** angir at datakilden VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum ble kalt 530 ganger for å returnere en post fra den datakilden og angi detaljer fra den i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="38536-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="38536-253">Vi anbefaler at du bruker hurtigbufring for datakilden VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum for å redusere antallet kall som gjøres for å hente detaljene for 265 transaksjoner og bidra til å forbedre ytelsen til modelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="38536-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="38536-254">Det kan også være nyttig å redusere antall kall som gjøres til datakilden for LedgerTransTypeList-datakilden.</span><span class="sxs-lookup"><span data-stu-id="38536-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="38536-255">Denne datakilden brukes til å knytte hver verdi for **LedgerTransType**-opplistingen til etiketten.</span><span class="sxs-lookup"><span data-stu-id="38536-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="38536-256">Ved hjelp av denne datakilden kan du finne en passende etikett og angi den i datamodellen for hver leverandørtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="38536-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="38536-257">Gjeldende antall kall til denne datakilden (9027) er ganske høy for 265 transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="38536-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Siden Modelltilordningsutforming i RCS som viser 9027 kall til datakilden](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="38536-259">Forbedre modelltilordningen basert på informasjon fra kjøringssporingen</span><span class="sxs-lookup"><span data-stu-id="38536-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="38536-260">Endre logikken til modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="38536-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="38536-261">Følg denne fremgangsmåten for å bruke bufring til å forhindre dupliserte kall til databasen:</span><span class="sxs-lookup"><span data-stu-id="38536-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="38536-262">I RCS-ruten, på siden **Modelltilordningsutforming** i ruten **Datakilder**, velger du **VendTable**-elementet.</span><span class="sxs-lookup"><span data-stu-id="38536-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="38536-263">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="38536-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="38536-264">Utvid elementet **VendTable**, utvid listen med en-til-mange-relasjoner for datakilden VendTable (**\<Relasjoner**-elementet), og velg elementet **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="38536-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="38536-265">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="38536-265">Select **Cache**.</span></span>

    ![Hurtigbufre installasjonen for å hindre dupliserte kall](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="38536-267">Følg disse trinnene for å hente LedgerTransTypeList-datakilden til området for VendTable-datakilden:</span><span class="sxs-lookup"><span data-stu-id="38536-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="38536-268">I ruten **Datakildetyper** utvider du **Funksjoner**-elementet og velger **Beregnet felt**-elementet.</span><span class="sxs-lookup"><span data-stu-id="38536-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="38536-269">I **Datakilder**-ruten velger du **VendTable**-elementet.</span><span class="sxs-lookup"><span data-stu-id="38536-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="38536-270">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="38536-270">Select **Add**.</span></span>
    4. <span data-ttu-id="38536-271">I feltet **Navn** angir du **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="38536-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="38536-272">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="38536-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="38536-273">I feltet **Formel** angir du **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="38536-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="38536-274">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="38536-274">Select **Save**.</span></span>
    8. <span data-ttu-id="38536-275">Lukk siden **Formelredigering**.</span><span class="sxs-lookup"><span data-stu-id="38536-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="38536-276">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="38536-276">Click **OK**.</span></span>

3. <span data-ttu-id="38536-277">Følg disse trinnene for å utføre bufring av feltet **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="38536-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="38536-278">Velg elementet **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="38536-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="38536-279">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="38536-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="38536-280">Velg **VendTable.\$TransType**-elementet.</span><span class="sxs-lookup"><span data-stu-id="38536-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="38536-281">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="38536-281">Select **Cache**.</span></span>

    ![Bufre oppsett av $TransType-feltet](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="38536-283">Følg disse trinnene for å endre feltet **\$TransTypeRecord**, slik at det begynner å bruke det hurtigbufrede feltet **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="38536-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="38536-284">I **Datakilder**-ruten utvider du **VendTable**-elementet, utvider **\<Relasjoner**-elementet, utvider elementet **VendTrans.VendTable\_AccountNum** og velger **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**-elementet.</span><span class="sxs-lookup"><span data-stu-id="38536-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="38536-285">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="38536-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="38536-286">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="38536-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="38536-287">I **Formel**-feltet finner du følgende uttrykk:</span><span class="sxs-lookup"><span data-stu-id="38536-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="38536-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="38536-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="38536-289">I **Formel**-feltet angir du følgende uttrykk:</span><span class="sxs-lookup"><span data-stu-id="38536-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="38536-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="38536-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="38536-291">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="38536-291">Select **Save**.</span></span>
    7. <span data-ttu-id="38536-292">Lukk siden **Formelredigering**.</span><span class="sxs-lookup"><span data-stu-id="38536-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="38536-293">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="38536-293">Select **OK**.</span></span>

5. <span data-ttu-id="38536-294">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="38536-294">Select **Save**.</span></span>
6. <span data-ttu-id="38536-295">Lukk siden **Modelltilordningsutforming**.</span><span class="sxs-lookup"><span data-stu-id="38536-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="38536-296">Lukk siden **Modelltilordninger**.</span><span class="sxs-lookup"><span data-stu-id="38536-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="38536-297">Fullføre den endrede versjonen av ER-modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="38536-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="38536-298">I RCS, på siden **Konfigurasjoner** i hurtigfanen **Versjoner**, velger du versjon **1.2** av konfigurasjonen **Ytelsessporingstilordning**.</span><span class="sxs-lookup"><span data-stu-id="38536-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="38536-299">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="38536-299">Select **Change status**.</span></span>
3. <span data-ttu-id="38536-300">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="38536-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="38536-301">Importere den endrede ER-modelltilordningskonfigurasjonen fra RCS til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="38536-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="38536-302">Gjenta trinnene i delen [Importere en ER-konfigurasjon fra RCS til Finance and Operations](#import-configuration) tidligere i dette emnet for å importere versjon 1.2 av konfigurasjonen **Ytelsessporingstilordning** til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="38536-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="38536-303">Kjøre den endrede ER-løsningen for å spore kjøring</span><span class="sxs-lookup"><span data-stu-id="38536-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="38536-304">Kjøre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="38536-304">Run the ER format</span></span>

<span data-ttu-id="38536-305">Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.</span><span class="sxs-lookup"><span data-stu-id="38536-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="38536-306">Se gjennom utførelsessporing</span><span class="sxs-lookup"><span data-stu-id="38536-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="38536-307">Eksportere den genererte sporingen fra Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="38536-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="38536-308">Gjenta trinnene i delen [Eksportere den genererte sporingen fra Finance and Operations](#export-trace) tidligere i dette emnet for å lagre en ny ytelsessporing lokalt.</span><span class="sxs-lookup"><span data-stu-id="38536-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="38536-309">Importere den genererte sporingen til RCS</span><span class="sxs-lookup"><span data-stu-id="38536-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="38536-310">Gjenta trinnene i delen [Importere den genererte sporingen til RCS](#import-trace) tidligere i dette emnet for å importere den nye ytelsessporingen til RCS.</span><span class="sxs-lookup"><span data-stu-id="38536-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="38536-311">Bruke ytelsessporing for analyse i RCS – modelltilordning</span><span class="sxs-lookup"><span data-stu-id="38536-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="38536-312">Gjenta trinnene i delen [Bruke ytelsessporing for analyse i RCS – modelltilordning](#use-trace) tidligere i dette emnet for å analysere den siste ytelsessporingen.</span><span class="sxs-lookup"><span data-stu-id="38536-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="38536-313">Legg merke til at justeringene du har gjort i modelltilordningen, har eliminert duplikate spørringer til databasen.</span><span class="sxs-lookup"><span data-stu-id="38536-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="38536-314">Antall kall til databasetabeller og datakilder for denne modelltilordningen er også redusert.</span><span class="sxs-lookup"><span data-stu-id="38536-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="38536-315">Derfor har ytelsen til hele ER-løsningen blitt forbedret.</span><span class="sxs-lookup"><span data-stu-id="38536-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Sporingsinformasjon for VendTable-datakilden på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="38536-317">I sporingsinformasjonen angir verdien **\[12\]** for VendTable-datakilden at denne datakilden ble kalt 12 ganger.</span><span class="sxs-lookup"><span data-stu-id="38536-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="38536-318">Verdien **\[Q:6\]** angir at seks samtaler ble oversatt til databasekall til tabellen VendTable.</span><span class="sxs-lookup"><span data-stu-id="38536-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="38536-319">Verdien **\[C:6\]** angir at postene som ble hentet fra databasen, ble bufret, og at seks andre kall ble behandlet ved hjelp av hurtigbufferen.</span><span class="sxs-lookup"><span data-stu-id="38536-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="38536-320">Legg merke til at antall kall til LedgerTransTypeList-datakilden er redusert fra 9027 til 240.</span><span class="sxs-lookup"><span data-stu-id="38536-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Sporingsinformasjon for LedgerTransTypeList-datakilden på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="38536-322">Se gjennom utførelsessporing i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="38536-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="38536-323">I tillegg til RCS kan enkelte versjoner av Finance and Operations tilby funksjoner for en ER-rammeverkutformingsopplevelse.</span><span class="sxs-lookup"><span data-stu-id="38536-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="38536-324">Disse versjonene av Finance and Operations har alternativet **Aktiver utformingsmodus** som kan aktiveres.</span><span class="sxs-lookup"><span data-stu-id="38536-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="38536-325">Du finner dette alternativet i kategorien **Generelt** på siden **Parametere for elektronisk rapportering**, som du kan åpne fra arbeidsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="38536-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Aktivere utformingsmodusalternativ på siden Parametere for elektronisk rapportering i Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="38536-327">Hvis du bruker en av disse versjonene av Finance and Operations, kan du analysere detaljene for genererte ytelsessporinger direkte i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="38536-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="38536-328">Du trenger ikke å eksportere dem fra Finance and Operation og importere dem til RCS.</span><span class="sxs-lookup"><span data-stu-id="38536-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="38536-329">Se gjennom utførelsessporingen ved hjelp av eksterne verktøy</span><span class="sxs-lookup"><span data-stu-id="38536-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="38536-330">Konfigurere brukerparametere</span><span class="sxs-lookup"><span data-stu-id="38536-330">Configure user parameters</span></span>

1. <span data-ttu-id="38536-331">I Finance and Operations går du til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="38536-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="38536-332">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="38536-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="38536-333">I dialogboksen **Brukerparametere** i delen **Kjøringssporing** i feltet **Sporingsformat for kjøring** velger du **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="38536-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="38536-334">Kjøre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="38536-334">Run the ER format</span></span>

<span data-ttu-id="38536-335">Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.</span><span class="sxs-lookup"><span data-stu-id="38536-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="38536-336">Legg merke til at nettleseren tilbyr en zip-fil for nedlasting.</span><span class="sxs-lookup"><span data-stu-id="38536-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="38536-337">Denne filen inneholder ytelsessporingen i PerfView-format.</span><span class="sxs-lookup"><span data-stu-id="38536-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="38536-338">Du kan deretter bruke verktøyet for PerfView-ytelsesanalyse til å analysere detaljene i ER-formatkjøringen.</span><span class="sxs-lookup"><span data-stu-id="38536-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Sporingsinformasjon for det utførte ER-formatet i PerfView](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="38536-340">Bruke eksterne verktøy til å se gjennom en utførelsessporing som inneholder databasespørringer</span><span class="sxs-lookup"><span data-stu-id="38536-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="38536-341">På grunn av forbedringer i ER-rammeverket gir ytelsessporingen som genereres i PerfView-formatet, nå flere detaljer om ER-formatutførelsen.</span><span class="sxs-lookup"><span data-stu-id="38536-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="38536-342">I Microsoft Dynamics 365 for Finance and Operations versjon 10.0.4 (juli 2019) kan denne sporingen også inneholde detaljer om utførte SQL-spørringer til programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="38536-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="38536-343">Konfigurere brukerparametere</span><span class="sxs-lookup"><span data-stu-id="38536-343">Configure user parameters</span></span>

1. <span data-ttu-id="38536-344">I Finance and Operations går du til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="38536-344">In Finance and Operations, go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="38536-345">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="38536-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="38536-346">I delen **Kjøringssporing** i dialogboksen **Brukerparametere** angir du følgende parametere:</span><span class="sxs-lookup"><span data-stu-id="38536-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="38536-347">I feltet **Sporingsformat for kjøring** velger du **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="38536-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="38536-348">Sett alternativet **Samle inn spørringsstatistikk** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="38536-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="38536-349">Sett alternativet **Spor spørring** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="38536-349">Set the **Trace query** option to **Yes**.</span></span>

    ![Dialogboksen Brukerparametere i Finance and Operations](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="38536-351">Kjøre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="38536-351">Run the ER format</span></span>

<span data-ttu-id="38536-352">Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.</span><span class="sxs-lookup"><span data-stu-id="38536-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="38536-353">Legg merke til at nettleseren tilbyr en zip-fil for nedlasting.</span><span class="sxs-lookup"><span data-stu-id="38536-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="38536-354">Denne filen inneholder ytelsessporingen i PerfView-format.</span><span class="sxs-lookup"><span data-stu-id="38536-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="38536-355">Du kan deretter bruke verktøyet for PerfView-ytelsesanalyse til å analysere detaljene i ER-formatkjøringen.</span><span class="sxs-lookup"><span data-stu-id="38536-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="38536-356">Denne sporingen inneholder nå detaljene for tilgang til SQL-database under utførelsen av ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="38536-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Sporingsinformasjon for det utførte ER-formatet i PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)
