---
title: Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer
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
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 9a5f943a507483bb4c1bd7fe87c0d65353194a6e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687433"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="dff19-103">Spore utførelse av ER-formater for å feilsøke ytelsesproblemer</span><span class="sxs-lookup"><span data-stu-id="dff19-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dff19-104">Som en del av prosessen med å utforme konfigurasjoner for elektronisk rapportering (ER) for å generere elektroniske dokumenter, definerer du metoden som brukes til å hente data ut av programmet, og angir den i utdataene som genereres.</span><span class="sxs-lookup"><span data-stu-id="dff19-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="dff19-105">Funksjonen ytelsessporing i ER bidrar til å redusere tiden og kostnadene betydelig ved innsamling av detaljer om ER-formatutførelsen og bruke dem til å feilsøke ytelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="dff19-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="dff19-106">Denne opplæringen inneholder retningslinjer om hvordan du kan utføre ytelsessporinger for utførte ER-formater, og hvordan du bruker informasjonen fra disse sporingene for å forbedre ytelsen.</span><span class="sxs-lookup"><span data-stu-id="dff19-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dff19-107">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="dff19-107">Prerequisites</span></span>

<span data-ttu-id="dff19-108">Hvis du vil fullføre eksemplene i denne opplæringen, må du ha følgende tilgang:</span><span class="sxs-lookup"><span data-stu-id="dff19-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="dff19-109">Tilgang til én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="dff19-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="dff19-110">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dff19-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="dff19-111">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dff19-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="dff19-112">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="dff19-112">System administrator</span></span>

- <span data-ttu-id="dff19-113">Tilgang til forekomsten av Regulatory Configuration Service (RCS) som er klargjort for samme leietaker som programmet, for én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="dff19-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="dff19-114">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dff19-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="dff19-115">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dff19-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="dff19-116">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="dff19-116">System administrator</span></span>

<span data-ttu-id="dff19-117">Du må også laste ned og lagre følgende filer lokalt.</span><span class="sxs-lookup"><span data-stu-id="dff19-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="dff19-118">Fil</span><span class="sxs-lookup"><span data-stu-id="dff19-118">File</span></span>                                  | <span data-ttu-id="dff19-119">Innhold</span><span class="sxs-lookup"><span data-stu-id="dff19-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="dff19-120">Ytelsessporingsmodell.versjon.1</span><span class="sxs-lookup"><span data-stu-id="dff19-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="dff19-121">Eksempel ER-datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="dff19-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="dff19-122">Ytelsessporingsmetadata.versjon.1</span><span class="sxs-lookup"><span data-stu-id="dff19-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="dff19-123">Eksempel ER-metadatakonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="dff19-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="dff19-124">Ytelsessporingstilordning.versjon.1.1</span><span class="sxs-lookup"><span data-stu-id="dff19-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="dff19-125">Eksempel ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="dff19-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="dff19-126">Ytelsessporingsformat.versjon.1.1</span><span class="sxs-lookup"><span data-stu-id="dff19-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="dff19-127">Eksempel ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="dff19-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="dff19-128">Konfigurere ER-parametere</span><span class="sxs-lookup"><span data-stu-id="dff19-128">Configure ER parameters</span></span>

<span data-ttu-id="dff19-129">Hver ER-ytelsessporing som genereres i programmet, lagres som et vedlegg til utførelsesloggposten.</span><span class="sxs-lookup"><span data-stu-id="dff19-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="dff19-130">Dokumentbehandlingsrammeverket (DM) brukes til å administrere disse vedleggene.</span><span class="sxs-lookup"><span data-stu-id="dff19-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="dff19-131">Du må konfigurere ER-parameterne på forhånd for å angi DM-dokumenttypen som skal brukes til å knytte ytelsesspor.</span><span class="sxs-lookup"><span data-stu-id="dff19-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="dff19-132">I arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="dff19-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="dff19-133">På siden **Parametere for elektronisk rapportering** i kategorien **Vedlegg** på siden **Andre** velger du deretter DM-dokumenttypen som skal brukes for ytelsessporinger.</span><span class="sxs-lookup"><span data-stu-id="dff19-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Siden Parametere for elektronisk rapportering](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="dff19-135">For å være tilgjengelig i **Andre**-oppslagsfeltet må en DM-dokumenttype konfigureres på følgende måte på siden **Dokumenttyper** (**Organisasjonsstyring \> Dokumentstyring \> Dokumenttyper**):</span><span class="sxs-lookup"><span data-stu-id="dff19-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="dff19-136">**Klasse:** Tilknytt fil</span><span class="sxs-lookup"><span data-stu-id="dff19-136">**Class:** Attach file</span></span>
- <span data-ttu-id="dff19-137">**Gruppe:** Fil</span><span class="sxs-lookup"><span data-stu-id="dff19-137">**Group:** File</span></span>

![Siden Dokumenttyper](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="dff19-139">Den valgte dokumenttypen må være tilgjengelig i alle firmaer av gjeldende forekomst, fordi DM-vedlegg er firmaspesifikke.</span><span class="sxs-lookup"><span data-stu-id="dff19-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="dff19-140">Konfigurere RCS-parametere</span><span class="sxs-lookup"><span data-stu-id="dff19-140">Configure RCS parameters</span></span>

<span data-ttu-id="dff19-141">ER-ytelsessporinger som genereres, importeres til RCS for analyse ved hjelp av ER-formatdesigneren og ER-tilordningsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="dff19-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="dff19-142">Fordi ER-ytelsesspor lagres som vedlegg i utførelsesloggposten som er relatert til ER-formatet, må du konfigurere RCS-parametere på forhånd, for å angi DM-dokumenttypen som skal brukes for å knytte til ytelsessporinger.</span><span class="sxs-lookup"><span data-stu-id="dff19-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="dff19-143">For RCS-forekomsten som er klargjort for ditt firma, går du til **Elektronisk rapportering** og velger **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="dff19-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="dff19-144">På siden **Parametere for elektronisk rapportering** i kategorien **Vedlegg** på siden **Andre** velger du deretter DM-dokumenttypen som skal brukes for ytelsessporinger.</span><span class="sxs-lookup"><span data-stu-id="dff19-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Siden Parametere for elektronisk rapportering i RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="dff19-146">For å være tilgjengelig i **Andre**-oppslagsfeltet må en DM-dokumenttype konfigureres på følgende måte på siden **Dokumenttyper** (**Organisasjonsstyring \> Dokumentstyring \> Dokumenttyper**):</span><span class="sxs-lookup"><span data-stu-id="dff19-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="dff19-147">**Klasse:** Tilknytt fil</span><span class="sxs-lookup"><span data-stu-id="dff19-147">**Class:** Attach file</span></span>
- <span data-ttu-id="dff19-148">**Gruppe:** Fil</span><span class="sxs-lookup"><span data-stu-id="dff19-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="dff19-149">Utforme en ER-løsning</span><span class="sxs-lookup"><span data-stu-id="dff19-149">Design an ER solution</span></span>

<span data-ttu-id="dff19-150">Anta at du har begynt å utforme en ny ER-løsning for å generere en ny rapport som presenterer leverandørtransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="dff19-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="dff19-151">For øyeblikket kan du finne transaksjonene for en valgt leverandør på siden **Leverandørtransaksjoner** (gå til **Leverandører \> Leverandører \> Alle leverandør**, velg en leverandør, og deretter, i handlingsruten i kategorien **Leverandør** i gruppen **Transaksjoner**, velger du **Transaksjoner**).</span><span class="sxs-lookup"><span data-stu-id="dff19-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="dff19-152">Du vil imidlertid ha alle leverandørtransaksjoner samtidig i ett elektronisk dokument i XML-format.</span><span class="sxs-lookup"><span data-stu-id="dff19-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="dff19-153">Denne løsningen vil bestå av flere ER-konfigurasjoner som inneholder den nødvendige datamodellen, metadataene, modelltilordningen og formatkomponentene.</span><span class="sxs-lookup"><span data-stu-id="dff19-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="dff19-154">Logg deg på forekomsten av RCS som er klargjort for firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="dff19-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="dff19-155">I denne opplæringen skal du opprette og endre konfigurasjoner for eksempelfirmaet **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="dff19-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="dff19-156">Kontroller derfor at denne konfigurasjonsleverandøren er lagt til RCS og valgt som aktiv.</span><span class="sxs-lookup"><span data-stu-id="dff19-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="dff19-157">Hvis du ha instruksjoner, se fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="dff19-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="dff19-158">I arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="dff19-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="dff19-159">På siden **Konfigurasjoner** importerer du ER-konfigurasjoner som du lastet ned som en forutsetning til RCS, i denne rekkefølgen: datamodell, metadata, modelltilordning, format.</span><span class="sxs-lookup"><span data-stu-id="dff19-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="dff19-160">For hver konfigurasjon følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="dff19-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="dff19-161">På siden Handling velger du **Exchange \> Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="dff19-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="dff19-162">Velg **Bla gjennom** for å velge den riktige filen for den nødvendige ER-konfigurasjonen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="dff19-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="dff19-163">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dff19-163">Select **OK**.</span></span>

    ![Siden Konfigurasjoner i RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="dff19-165">Kjør ER-løsningen for å spore kjøring</span><span class="sxs-lookup"><span data-stu-id="dff19-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="dff19-166">Anta at du er ferdig med å utforme den første versjonen av ER-løsningen.</span><span class="sxs-lookup"><span data-stu-id="dff19-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="dff19-167">Nå skal du teste forekomsten og analysere kjøringsytelsen.</span><span class="sxs-lookup"><span data-stu-id="dff19-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="dff19-168">Importere en ER-konfigurasjon fra RCS til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dff19-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="dff19-169">Logg på programforekomsten.</span><span class="sxs-lookup"><span data-stu-id="dff19-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="dff19-170">I denne opplæringen skal du importere konfigurasjonene fra RCS-forekomsten (der du utformer ER-komponentene) i forekomsten (der du tester og til slutt bruker dem).</span><span class="sxs-lookup"><span data-stu-id="dff19-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="dff19-171">Du må derfor kontrollere at alle de nødvendige artefaktene er forberedt.</span><span class="sxs-lookup"><span data-stu-id="dff19-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="dff19-172">Hvis du vil ha instruksjoner, kan du se fremgangsmåten [Importere ER-konfigurasjoner (Electronic Reporting) fra Regulatory Configuration Service (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="dff19-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="dff19-173">Følg disse trinnene for å importere konfigurasjonene fra RCS til programmet:</span><span class="sxs-lookup"><span data-stu-id="dff19-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="dff19-174">I arbeidsområdet **Elektronisk rapportering**, på flisen for konfigurasjonsleverandøren **Litware, Inc.**, velger du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="dff19-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="dff19-175">På **Konfigurasjonsrepositorium**-siden velger du repositoriet for **RCS**-typen, og deretter velger du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="dff19-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="dff19-176">I hurtigfanen **Konfigurasjoner** velger du **Ytelsessporingsformat**- konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="dff19-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="dff19-177">I **Versjoner**-hurtigkategorien velger du versjon **1.1** av den valgte konfigurasjonen, og deretter velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="dff19-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfigurasjonsrepositorium-side](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="dff19-179">De tilsvarende versjonene av konfigurasjonene for datamodell og modelltilordning importeres automatisk som forutsetninger for den importerte ER-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="dff19-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="dff19-180">Aktivere ER-ytelsessporing</span><span class="sxs-lookup"><span data-stu-id="dff19-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="dff19-181">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="dff19-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="dff19-182">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="dff19-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="dff19-183">Følg disse trinnene i dialogboksen **Brukerparametere** i delen **Kjøringssporing**:</span><span class="sxs-lookup"><span data-stu-id="dff19-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="dff19-184">I feltet **Sporingsformat for kjøring** velger du **Feilsøk sporingsformat** for å begynne å samle inn detaljer for kjøringen av ER-format.</span><span class="sxs-lookup"><span data-stu-id="dff19-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="dff19-185">Når denne verdien er valgt, vil ytelsessporingen samle inn informasjon om tiden som brukes på følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="dff19-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="dff19-186">Kjøre hver datakilde i modelltilordningen som kalles for å hente data</span><span class="sxs-lookup"><span data-stu-id="dff19-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="dff19-187">Behandler hver formatvare for å angi data i utdataene som genereres</span><span class="sxs-lookup"><span data-stu-id="dff19-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="dff19-188">Du bruker feltet **Sporingsformat for kjøring** til å angi formatet på den genererte ytelsessporingen som kjøringsdetaljene er lagret i for ER-format og tilordningselementer.</span><span class="sxs-lookup"><span data-stu-id="dff19-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="dff19-189">Ved å velge **Feilsøk sporingsformat** som verdi kan du analysere innholdet i sporingen i ER-operasjonsutforming og se ER-formatet eller tilordningselementene som er nevnt i sporingen.</span><span class="sxs-lookup"><span data-stu-id="dff19-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="dff19-190">Angi følgende alternativer til **Ja** for å samle inn bestemte detaljer for utførelsen av ER-modelltilordningen og ER-formatkomponentene:</span><span class="sxs-lookup"><span data-stu-id="dff19-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="dff19-191">**Samle inn spørringsstatistikk** – Når dette alternativet er aktivert, vil ytelsessporingen samle inn følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="dff19-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="dff19-192">Antall databasekall som er utført av datakilder</span><span class="sxs-lookup"><span data-stu-id="dff19-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="dff19-193">Antall dupliserte kall til databasen</span><span class="sxs-lookup"><span data-stu-id="dff19-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="dff19-194">Detaljer for SQL-setningene som ble brukt til å opprette databasekall</span><span class="sxs-lookup"><span data-stu-id="dff19-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="dff19-195">**SSpor tilgang for hurtigbufring** – Når dette alternativet er aktivert, samler ytelsessporingsinformasjon inn informasjon om ER-modelltilordningens hurtigbufferbruk.</span><span class="sxs-lookup"><span data-stu-id="dff19-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="dff19-196">**Spor datatilgang** – Når dette alternativet er aktivert, samler ytelsessporingeninformasjon inn informajson om antall kall til databasen for utførte datakilder av typen postliste.</span><span class="sxs-lookup"><span data-stu-id="dff19-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="dff19-197">**Sporingslisteopplisting** – Når dette alternativet er aktivert, samler ytelsessporingeninformasjon inn informajson om antall poster som forespørres fra datakilder av typen postliste.</span><span class="sxs-lookup"><span data-stu-id="dff19-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dff19-198">Parameterne i dialogboksen **Brukerparametere** er spesifikke for brukeren og det gjeldende firmaet.</span><span class="sxs-lookup"><span data-stu-id="dff19-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Dialogboksen Brukerparametere](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="dff19-200">Kjør ER-formatet</span><span class="sxs-lookup"><span data-stu-id="dff19-200">Run the ER format</span></span>

1. <span data-ttu-id="dff19-201">Velg **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="dff19-201">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="dff19-202">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="dff19-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="dff19-203">På siden **Konfigurasjoner** i konfigurasjonstreet, velger du elementet **Ytelsessporingsformat**.</span><span class="sxs-lookup"><span data-stu-id="dff19-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="dff19-204">Velg **Kjør** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dff19-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="dff19-205">Legg merke til at filen som genereres, presenterer informasjon om 265 transaksjoner for seks leverandører.</span><span class="sxs-lookup"><span data-stu-id="dff19-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="dff19-206">Se gjennom utførelsessporing</span><span class="sxs-lookup"><span data-stu-id="dff19-206">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="dff19-207">Eksportere den genererte sporingen fra programmet</span><span class="sxs-lookup"><span data-stu-id="dff19-207">Export the generated trace from the application</span></span>

<span data-ttu-id="dff19-208">Ytelsessporinger kobles fra kilde-ER-formatet og kan serialiseres til en ekstern zip-fil.</span><span class="sxs-lookup"><span data-stu-id="dff19-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="dff19-209">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Feilsøkingslogger for konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="dff19-209">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="dff19-210">På siden **Kjøringslogger for elektronisk rapportering**, i venstre rute i feltet **Konfigurasjonsnavn**, velger du **Ytelsessporingsformat** for å finne loggpostene som er generert ved å utføre **Ytelsessporingsformat**.</span><span class="sxs-lookup"><span data-stu-id="dff19-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="dff19-211">Velg **Vedlegg**-knappen (bindersikonet) i øvre høyre hjørne på siden, eller trykk på **Ctrl+Skift+A**.</span><span class="sxs-lookup"><span data-stu-id="dff19-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Vedlegg-knappen på siden Kjøringslogger for elektronisk rapportering](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="dff19-213">På siden **Vedlegg for Kjøringslogger for elektronisk rapportering** velger du **Åpne** for å hente ytelsessporing som en zip-fil og lagre den lokalt.</span><span class="sxs-lookup"><span data-stu-id="dff19-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Vedlegg for Kjøringslogger for elektronisk rapportering](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="dff19-215">Sporingen som genereres, har en referanse til kilde-ER-rapporten via en unik rapport-ID bare i **GUID**-format.</span><span class="sxs-lookup"><span data-stu-id="dff19-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="dff19-216">Versjonsnummereringen for formatet vurderes ikke.</span><span class="sxs-lookup"><span data-stu-id="dff19-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="dff19-217">Legg merke til at tilknytningen mellom ytelsessporingen som er generert for det utførte ER-formatet og ER-modelltilordningen, er basert på rotbeskrivelsen som ble brukt og den felles datamodellen.</span><span class="sxs-lookup"><span data-stu-id="dff19-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="dff19-218">Versjonsnummereringen for formatet og modelltilordningen vurderes ikke.</span><span class="sxs-lookup"><span data-stu-id="dff19-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="dff19-219">Innstillingen til **Standard for modelltilordning**-flagget for modelltilordningen blir heller ikke vurdert.</span><span class="sxs-lookup"><span data-stu-id="dff19-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="dff19-220">Importere den genererte sporingen til RCS</span><span class="sxs-lookup"><span data-stu-id="dff19-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="dff19-221">I RCS, i arbeidsområdet **Elektronisk rapportering**, velger du flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="dff19-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="dff19-222">På siden **Konfigurasjoner**, i konfigurasjonstreet, utvider du elementet **Ytelsessporingsmodell**, og velg elementet **Ytelsessporingsformat**.</span><span class="sxs-lookup"><span data-stu-id="dff19-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="dff19-223">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dff19-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="dff19-224">På siden **Formatutforming**, i handlingsruten, velger du **Ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="dff19-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="dff19-225">I dialogboksen **Resultatinnstillinger for ytelsessporing** velg **Importer ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="dff19-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="dff19-226">Velg **Bla gjennom** for å velge ZIP-filen du eksporterte tidligere.</span><span class="sxs-lookup"><span data-stu-id="dff19-226">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="dff19-227">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dff19-227">Select **OK**.</span></span>

    ![Dialogboksen Resultatinnstillinger for ytelsessporing i RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="dff19-229">Bruke ytelsessporing for analyse i RCS – Formatutførelse</span><span class="sxs-lookup"><span data-stu-id="dff19-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="dff19-230">Velg **Vis/Skjul** på **Formatutforming**-siden i RCS for å utvide innholdet for alle formatvarer.</span><span class="sxs-lookup"><span data-stu-id="dff19-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="dff19-231">Legg merke til at tilleggsinformasjon vises for noen varer i gjeldende format:</span><span class="sxs-lookup"><span data-stu-id="dff19-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="dff19-232">Den faktiske tiden som ble brukt på å legge inn data i de genererte utdataene ved hjelp av formatvaren</span><span class="sxs-lookup"><span data-stu-id="dff19-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="dff19-233">Den samme tiden som prosent av den totale tiden som ble brukt til å generere hele utdataene</span><span class="sxs-lookup"><span data-stu-id="dff19-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Formatutformingsside i RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="dff19-235">Lukk siden **Formatutforming**.</span><span class="sxs-lookup"><span data-stu-id="dff19-235">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="dff19-236">Bruke ytelsessporing for analyse i RCS – modelltilordning</span><span class="sxs-lookup"><span data-stu-id="dff19-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="dff19-237">I RCS, på siden **Konfigurasjoner** i konfigurasjonstreet, velger du elementet **Ytelsessporingstilordning**.</span><span class="sxs-lookup"><span data-stu-id="dff19-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="dff19-238">Velg **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dff19-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="dff19-239">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="dff19-239">Select **Designer**.</span></span>
4. <span data-ttu-id="dff19-240">På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.</span><span class="sxs-lookup"><span data-stu-id="dff19-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="dff19-241">Velg sporingen du importerte tidligere.</span><span class="sxs-lookup"><span data-stu-id="dff19-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="dff19-242">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dff19-242">Select **OK**.</span></span>

<span data-ttu-id="dff19-243">Legg merke til at ny informasjon blir tilgjengelig for noen datakildeelementer av gjeldende modelltilordning:</span><span class="sxs-lookup"><span data-stu-id="dff19-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="dff19-244">Den faktiske tiden som ble brukt til å hente data ved hjelp av datakilden</span><span class="sxs-lookup"><span data-stu-id="dff19-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="dff19-245">Den samme tiden som prosent av den totale tiden som ble brukt til å kjøre hele modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="dff19-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="dff19-246">Legg merke til at ER informerer deg om at gjeldende modelltilordning dupliserer databaseforespørsler når VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum-datakilden kjøres.</span><span class="sxs-lookup"><span data-stu-id="dff19-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="dff19-247">Denne dupliseringen forekommer fordi listen over leverandørtransaksjoner kalles to ganger for hver leverandørpost som gjentas:</span><span class="sxs-lookup"><span data-stu-id="dff19-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="dff19-248">Det blir laget ett kall for å angi detaljer for hver transaksjon i datamodellen, basert på konfigurerte bindinger.</span><span class="sxs-lookup"><span data-stu-id="dff19-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="dff19-249">Det blir laget ett kall for å angi det beregnede antallet transaksjoner per leverandør i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="dff19-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Melding om dupliserte databaseforespørsler på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="dff19-251">Verdien **\[Q:530\]** angir at VendTrans-tabellen ble kalt 530 ganger for å returnere en post fra denne tabellen til VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum-datakilden.</span><span class="sxs-lookup"><span data-stu-id="dff19-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="dff19-252">Verdien **\[530\]** angir at datakilden VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum ble kalt 530 ganger for å returnere en post fra den datakilden og angi detaljer fra den i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="dff19-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="dff19-253">Vi anbefaler at du bruker hurtigbufring for datakilden VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum for å redusere antallet kall som gjøres for å hente detaljene for 265 transaksjoner og bidra til å forbedre ytelsen til modelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="dff19-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="dff19-254">Det kan også være nyttig å redusere antall kall som gjøres til datakilden for LedgerTransTypeList-datakilden.</span><span class="sxs-lookup"><span data-stu-id="dff19-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="dff19-255">Denne datakilden brukes til å knytte hver verdi for **LedgerTransType**-opplistingen til etiketten.</span><span class="sxs-lookup"><span data-stu-id="dff19-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="dff19-256">Ved hjelp av denne datakilden kan du finne en passende etikett og angi den i datamodellen for hver leverandørtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="dff19-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="dff19-257">Gjeldende antall kall til denne datakilden (9027) er ganske høy for 265 transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="dff19-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Siden Modelltilordningsutforming i RCS som viser 9027 kall til datakilden](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="dff19-259">Forbedre modelltilordningen basert på informasjon fra kjøringssporingen</span><span class="sxs-lookup"><span data-stu-id="dff19-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="dff19-260">Endre logikken til modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="dff19-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="dff19-261">Følg denne fremgangsmåten for å bruke bufring til å forhindre dupliserte kall til databasen:</span><span class="sxs-lookup"><span data-stu-id="dff19-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="dff19-262">I RCS-ruten, på siden **Modelltilordningsutforming** i ruten **Datakilder**, velger du **VendTable**-elementet.</span><span class="sxs-lookup"><span data-stu-id="dff19-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="dff19-263">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="dff19-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="dff19-264">Utvid elementet **VendTable**, utvid listen med en-til-mange-relasjoner for datakilden VendTable (**\<Relasjoner**-elementet), og velg elementet **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="dff19-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="dff19-265">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="dff19-265">Select **Cache**.</span></span>

    ![Hurtigbufre installasjonen for å hindre dupliserte kall](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="dff19-267">Følg disse trinnene for å hente LedgerTransTypeList-datakilden til området for VendTable-datakilden:</span><span class="sxs-lookup"><span data-stu-id="dff19-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="dff19-268">I ruten **Datakildetyper** utvider du **Funksjoner**-elementet og velger **Beregnet felt**-elementet.</span><span class="sxs-lookup"><span data-stu-id="dff19-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="dff19-269">I **Datakilder**-ruten velger du **VendTable**-elementet.</span><span class="sxs-lookup"><span data-stu-id="dff19-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="dff19-270">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="dff19-270">Select **Add**.</span></span>
    4. <span data-ttu-id="dff19-271">I feltet **Navn** angir du **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="dff19-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="dff19-272">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="dff19-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="dff19-273">I feltet **Formel** angir du **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="dff19-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="dff19-274">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dff19-274">Select **Save**.</span></span>
    8. <span data-ttu-id="dff19-275">Lukk siden **Formelredigering**.</span><span class="sxs-lookup"><span data-stu-id="dff19-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="dff19-276">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="dff19-276">Click **OK**.</span></span>

3. <span data-ttu-id="dff19-277">Følg disse trinnene for å utføre bufring av feltet **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="dff19-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="dff19-278">Velg elementet **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="dff19-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="dff19-279">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="dff19-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="dff19-280">Velg **VendTable.\$TransType**-elementet.</span><span class="sxs-lookup"><span data-stu-id="dff19-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="dff19-281">Velg **Hurtigbuffer**.</span><span class="sxs-lookup"><span data-stu-id="dff19-281">Select **Cache**.</span></span>

    ![Bufre oppsett av $TransType-feltet](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="dff19-283">Følg disse trinnene for å endre feltet **\$TransTypeRecord**, slik at det begynner å bruke det hurtigbufrede feltet **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="dff19-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="dff19-284">I **Datakilder**-ruten utvider du **VendTable**-elementet, utvider **\<Relasjoner**-elementet, utvider elementet **VendTrans.VendTable\_AccountNum** og velger **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**-elementet.</span><span class="sxs-lookup"><span data-stu-id="dff19-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="dff19-285">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="dff19-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="dff19-286">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="dff19-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="dff19-287">I **Formel**-feltet finner du følgende uttrykk:</span><span class="sxs-lookup"><span data-stu-id="dff19-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="dff19-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="dff19-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="dff19-289">I **Formel**-feltet angir du følgende uttrykk:</span><span class="sxs-lookup"><span data-stu-id="dff19-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="dff19-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="dff19-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="dff19-291">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dff19-291">Select **Save**.</span></span>
    7. <span data-ttu-id="dff19-292">Lukk siden **Formelredigering**.</span><span class="sxs-lookup"><span data-stu-id="dff19-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="dff19-293">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dff19-293">Select **OK**.</span></span>

5. <span data-ttu-id="dff19-294">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dff19-294">Select **Save**.</span></span>
6. <span data-ttu-id="dff19-295">Lukk siden **Modelltilordningsutforming**.</span><span class="sxs-lookup"><span data-stu-id="dff19-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="dff19-296">Lukk siden **Modelltilordninger**.</span><span class="sxs-lookup"><span data-stu-id="dff19-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="dff19-297">Fullføre den endrede versjonen av ER-modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="dff19-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="dff19-298">I RCS, på siden **Konfigurasjoner** i hurtigfanen **Versjoner**, velger du versjon **1.2** av konfigurasjonen **Ytelsessporingstilordning**.</span><span class="sxs-lookup"><span data-stu-id="dff19-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="dff19-299">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="dff19-299">Select **Change status**.</span></span>
3. <span data-ttu-id="dff19-300">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="dff19-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="dff19-301">Importere den endrede ER-modelltilordningskonfigurasjonen fra RCS til programmet</span><span class="sxs-lookup"><span data-stu-id="dff19-301">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="dff19-302">Gjenta trinnene i delen [Importere en ER-konfigurasjon fra RCS til Finance and Operations](#import-configuration) tidligere i dette emnet for å importere versjon 1.2 av konfigurasjonen **Ytelsessporingstilordning**.</span><span class="sxs-lookup"><span data-stu-id="dff19-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="dff19-303">Kjøre den endrede ER-løsningen for å spore kjøring</span><span class="sxs-lookup"><span data-stu-id="dff19-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="dff19-304">Kjøre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="dff19-304">Run the ER format</span></span>

<span data-ttu-id="dff19-305">Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.</span><span class="sxs-lookup"><span data-stu-id="dff19-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="dff19-306">Arbeide med utføringsporingen</span><span class="sxs-lookup"><span data-stu-id="dff19-306">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="dff19-307">Eksportere den genererte sporingen fra programmet</span><span class="sxs-lookup"><span data-stu-id="dff19-307">Export the generated trace from the application</span></span>

<span data-ttu-id="dff19-308">Gjenta trinnene i delen [Eksportere den genererte sporingen fra programmet](#export-trace) tidligere i dette emnet for å lagre en ny ytelsessporing lokalt.</span><span class="sxs-lookup"><span data-stu-id="dff19-308">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="dff19-309">Importere den genererte sporingen til RCS</span><span class="sxs-lookup"><span data-stu-id="dff19-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="dff19-310">Gjenta trinnene i delen [Importere den genererte sporingen til RCS](#import-trace) tidligere i dette emnet for å importere den nye ytelsessporingen til RCS.</span><span class="sxs-lookup"><span data-stu-id="dff19-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="dff19-311">Bruke ytelsessporing for analyse i RCS – modelltilordning</span><span class="sxs-lookup"><span data-stu-id="dff19-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="dff19-312">Gjenta trinnene i delen [Bruke ytelsessporing for analyse i RCS – modelltilordning](#use-trace) tidligere i dette emnet for å analysere den siste ytelsessporingen.</span><span class="sxs-lookup"><span data-stu-id="dff19-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="dff19-313">Legg merke til at justeringene du har gjort i modelltilordningen, har eliminert duplikate spørringer til databasen.</span><span class="sxs-lookup"><span data-stu-id="dff19-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="dff19-314">Antall kall til databasetabeller og datakilder for denne modelltilordningen er også redusert.</span><span class="sxs-lookup"><span data-stu-id="dff19-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="dff19-315">Derfor har ytelsen til hele ER-løsningen blitt forbedret.</span><span class="sxs-lookup"><span data-stu-id="dff19-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Sporingsinformasjon for VendTable-datakilden på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="dff19-317">I sporingsinformasjonen angir verdien **\[12\]** for VendTable-datakilden at denne datakilden ble kalt 12 ganger.</span><span class="sxs-lookup"><span data-stu-id="dff19-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="dff19-318">Verdien **\[Q:6\]** angir at seks samtaler ble oversatt til databasekall til tabellen VendTable.</span><span class="sxs-lookup"><span data-stu-id="dff19-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="dff19-319">Verdien **\[C:6\]** angir at postene som ble hentet fra databasen, ble bufret, og at seks andre kall ble behandlet ved hjelp av hurtigbufferen.</span><span class="sxs-lookup"><span data-stu-id="dff19-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="dff19-320">Legg merke til at antall kall til LedgerTransTypeList-datakilden er redusert fra 9027 til 240.</span><span class="sxs-lookup"><span data-stu-id="dff19-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Sporingsinformasjon for LedgerTransTypeList-datakilden på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="dff19-322">Se gjennom utførelsessporingen i programmet</span><span class="sxs-lookup"><span data-stu-id="dff19-322">Review the execution trace in the application</span></span>

<span data-ttu-id="dff19-323">I tillegg til RCS kan enkelte versjoner tilby funksjoner for en ER-rammeverkutformingsopplevelse.</span><span class="sxs-lookup"><span data-stu-id="dff19-323">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="dff19-324">Disse versjonene har alternativet **Aktiver utformingsmodus** som kan aktiveres.</span><span class="sxs-lookup"><span data-stu-id="dff19-324">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="dff19-325">Du finner dette alternativet i kategorien **Generelt** på siden **Parametere for elektronisk rapportering**, som du kan åpne fra arbeidsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="dff19-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Alternativet Aktiver utformingsmodus på siden Parametere for elektronisk rapportering](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="dff19-327">Hvis du bruker en av disse versjonene, kan du analysere detaljene for genererte ytelsessporinger direkte i programmet.</span><span class="sxs-lookup"><span data-stu-id="dff19-327">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="dff19-328">Du trenger ikke å eksportere dem fra programmet og importere dem til RCS.</span><span class="sxs-lookup"><span data-stu-id="dff19-328">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="dff19-329">Se gjennom utførelsessporingen ved hjelp av eksterne verktøy</span><span class="sxs-lookup"><span data-stu-id="dff19-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="dff19-330">Konfigurere brukerparametere</span><span class="sxs-lookup"><span data-stu-id="dff19-330">Configure user parameters</span></span>

1. <span data-ttu-id="dff19-331">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="dff19-331">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="dff19-332">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="dff19-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="dff19-333">I dialogboksen **Brukerparametere** i delen **Kjøringssporing** i feltet **Sporingsformat for kjøring** velger du **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="dff19-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="dff19-334">Kjøre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="dff19-334">Run the ER format</span></span>

<span data-ttu-id="dff19-335">Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.</span><span class="sxs-lookup"><span data-stu-id="dff19-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="dff19-336">Legg merke til at nettleseren tilbyr en zip-fil for nedlasting.</span><span class="sxs-lookup"><span data-stu-id="dff19-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="dff19-337">Denne filen inneholder ytelsessporingen i PerfView-format.</span><span class="sxs-lookup"><span data-stu-id="dff19-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="dff19-338">Du kan deretter bruke verktøyet for PerfView-ytelsesanalyse til å analysere detaljene i ER-formatkjøringen.</span><span class="sxs-lookup"><span data-stu-id="dff19-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Informasjon om ytelsessporing i PerfView-format](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="dff19-340">Bruke eksterne verktøy til å se gjennom en utførelsessporing som inneholder databasespørringer</span><span class="sxs-lookup"><span data-stu-id="dff19-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="dff19-341">På grunn av forbedringer i ER-rammeverket gir ytelsessporingen som genereres i PerfView-formatet, nå flere detaljer om ER-formatutførelsen.</span><span class="sxs-lookup"><span data-stu-id="dff19-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="dff19-342">I Microsoft Dynamics 365 for Finance and Operations versjon 10.0.4 (juli 2019) kan denne sporingen også inneholde detaljer om utførte SQL-spørringer til programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="dff19-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="dff19-343">Konfigurere brukerparametere</span><span class="sxs-lookup"><span data-stu-id="dff19-343">Configure user parameters</span></span>

1. <span data-ttu-id="dff19-344">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="dff19-344">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="dff19-345">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="dff19-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="dff19-346">I delen **Kjøringssporing** i dialogboksen **Brukerparametere** angir du følgende parametere:</span><span class="sxs-lookup"><span data-stu-id="dff19-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="dff19-347">I feltet **Sporingsformat for kjøring** velger du **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="dff19-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="dff19-348">Sett alternativet **Samle inn spørringsstatistikk** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dff19-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="dff19-349">Sett alternativet **Spor spørring** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dff19-349">Set the **Trace query** option to **Yes**.</span></span>

    ![Delen Utføringssporing, dialogboksen Brukerparametere](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="dff19-351">Kjøre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="dff19-351">Run the ER format</span></span>

<span data-ttu-id="dff19-352">Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.</span><span class="sxs-lookup"><span data-stu-id="dff19-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="dff19-353">Legg merke til at nettleseren tilbyr en zip-fil for nedlasting.</span><span class="sxs-lookup"><span data-stu-id="dff19-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="dff19-354">Denne filen inneholder ytelsessporingen i PerfView-format.</span><span class="sxs-lookup"><span data-stu-id="dff19-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="dff19-355">Du kan deretter bruke verktøyet for PerfView-ytelsesanalyse til å analysere detaljene i ER-formatkjøringen.</span><span class="sxs-lookup"><span data-stu-id="dff19-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="dff19-356">Denne sporingen inneholder nå detaljene for tilgang til SQL-database under utførelsen av ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dff19-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Sporingsinformasjon for det utførte ER-formatet i PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="dff19-358">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="dff19-358">Additional resources</span></span>

- [<span data-ttu-id="dff19-359">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dff19-359">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="dff19-360">Forbedre ytelse for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT</span><span class="sxs-lookup"><span data-stu-id="dff19-360">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)
