---
title: Angi egendefinerte lagerplasseringer for genererte dokumenter
description: Dette emnet forklarer hvordan du utvider listen over lagringssteder for dokumenter som genereres av Elektronisk rapportering (ER)-formater.
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bd979bf5369b6878caaee82fc9c6a40d363cc165
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894154"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="b9c58-103">Angi egendefinerte lagerplasseringer for genererte dokumenter</span><span class="sxs-lookup"><span data-stu-id="b9c58-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b9c58-104">API (Application programming interface) for Elektronisk rapportering-rammeverket (ER) lar deg utvide listen over lagringssteder for dokumenter som ER-formater genererer.</span><span class="sxs-lookup"><span data-stu-id="b9c58-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="b9c58-105">Dette emnet forklarer hvordan du legger til en egendefinert lagringsplassering for genererte dokumenter ved å delegere oppgaven med å opprette ER-mål til standardmålfabrikk og deretter implementere en egendefinert klasse som har sin egen logikk.</span><span class="sxs-lookup"><span data-stu-id="b9c58-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b9c58-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="b9c58-106">Prerequisites</span></span>

<span data-ttu-id="b9c58-107">Distribuer en topologi som støtter fortløpende bygging.</span><span class="sxs-lookup"><span data-stu-id="b9c58-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="b9c58-108">Hvis du vil ha mer informasjon, kan du se [Distribuere topologier som støtter sammenhengende automatisering av bygging og testing](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="b9c58-108">For more information, see [Deploy topologies that support continuous build and test automation](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="b9c58-109">Du må ha tilgang til denne topologien for én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="b9c58-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="b9c58-110">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="b9c58-110">Electronic reporting developer</span></span>
- <span data-ttu-id="b9c58-111">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="b9c58-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="b9c58-112">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="b9c58-112">System administrator</span></span>

<span data-ttu-id="b9c58-113">Du må også ha tilgang til utviklingsmiljøet for denne topologien.</span><span class="sxs-lookup"><span data-stu-id="b9c58-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="b9c58-114">Alle oppgavene i dette emnet kan fullføres i **USMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="b9c58-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="b9c58-115">Importere ER-formatet Rull anleggsmidler forover</span><span class="sxs-lookup"><span data-stu-id="b9c58-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="b9c58-116">For å generere dokumentene du planlegger å legge til en egendefinert lagringsplassering for, kan du [importere](er-download-configurations-global-repo.md) ER-formatkonfigurasjonen **Rull anleggsmidler forover** til gjeldende topologi.</span><span class="sxs-lookup"><span data-stu-id="b9c58-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Konfigurasjonsrepositorium-side](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="b9c58-118">Kjøre Rull anleggsmidler forover-rapporten</span><span class="sxs-lookup"><span data-stu-id="b9c58-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="b9c58-119">Gå til **Anleggsmidler** \> **Forespørsler og rapporter** \> **Transaksjonsrapporter** \> **Rull anleggsmidler forover**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="b9c58-120">Angi **1/1/2017** (1. januar 2017) i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9c58-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="b9c58-121">Angi **1/31/2017** (31. januar 2017) i **Til dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9c58-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="b9c58-122">I **Valuta-felt** velger du **Regnskapsvaluta**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="b9c58-123">I feltet **Formattilordning** velger du **Rull anleggsmidler forover**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="b9c58-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-124">Select **OK**.</span></span>

![Dialogboksen for kjøretid for Rull anleggsmidler forover-rapporten](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="b9c58-126">I Microsoft Excel kan du se gjennom det utgående dokumentet som er generert og tilgjengelig for nedlasting.</span><span class="sxs-lookup"><span data-stu-id="b9c58-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="b9c58-127">Denne virkemåten er [standard virkemåte](electronic-reporting-destinations.md#default-behavior) for et ER-format som ingen [mål](electronic-reporting-destinations.md) er konfigurert for, og som kjører i interaktiv modus.</span><span class="sxs-lookup"><span data-stu-id="b9c58-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="b9c58-128">Gå gjennom kildekoden</span><span class="sxs-lookup"><span data-stu-id="b9c58-128">Review the source code</span></span>

<span data-ttu-id="b9c58-129">Gå gjennom koden for `generateReportByGER()`-metoden for `AssetRollForwardService`-klasse.</span><span class="sxs-lookup"><span data-stu-id="b9c58-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="b9c58-130">Legg merke til at `Run()`-metoden brukes til å kalle opp ER-rammeverket og generere rapporten **Rull anleggsmidler forover**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="b9c58-131">Endre kildekoden</span><span class="sxs-lookup"><span data-stu-id="b9c58-131">Modify the source code</span></span>

1. <span data-ttu-id="b9c58-132">I Visual Studio-prosjektet legger du til en ny klasse (`AssetRollForwardDestination` i dette eksemplet), og skriver kode for å implementere det egendefinerte målet for **Rull anleggsmidler forover**-rapporter som genereres.</span><span class="sxs-lookup"><span data-stu-id="b9c58-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="b9c58-133">`new()`-metoden er utformet for å hente det opprinnelige ER-målobjektet og den programlogikkbaserte parameteren som angir den egendefinerte lokasjonen der genererte rapporter skal lagres.</span><span class="sxs-lookup"><span data-stu-id="b9c58-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="b9c58-134">I dette eksemplet er den egendefinerte plasseringen navnet på en mappe i det lokale filsystemet til serveren som kjører AOS-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="b9c58-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="b9c58-135">`saveFile()`-metoden er utformet for å lagre et generert dokument i en mappe i det lokale filsystemet på serveren som kjører AOS-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="b9c58-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="b9c58-136">I Visual Studio-prosjektet legger du til en ny klasse (`AssetRollForwardDestinationFactory` i dette eksemplet) og skriver kode for å definere en egendefinert målfabrikk som delegerer opprettelsen av et mål til standardmålfabrikken, og for å bryte en fildestinasjon med ditt eget mål.</span><span class="sxs-lookup"><span data-stu-id="b9c58-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="b9c58-137">Endre den eksisterende `AssetRollForwardService`-klassen, og skriv kode for å definere en egendefinert målfabrikk for rapportkjøringen.</span><span class="sxs-lookup"><span data-stu-id="b9c58-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="b9c58-138">Legg merke til at når en egendefinert målfabrikk opprettes, blir den programdrevne parameteren som angir en målmappe, sendt.</span><span class="sxs-lookup"><span data-stu-id="b9c58-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="b9c58-139">På denne måten brukes målmappen til å lagre genererte filer.</span><span class="sxs-lookup"><span data-stu-id="b9c58-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="b9c58-140">Kontroller at den angitte mappen (**c:\\0** i dette eksemplet) finnes i det lokale filsystemet på serveren som kjører AOS-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="b9c58-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="b9c58-141">Hvis ikke vil unntaket [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) oppstå under kjøring.</span><span class="sxs-lookup"><span data-stu-id="b9c58-141">Otherwise, a [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="b9c58-142">Bygg prosjektet på nytt.</span><span class="sxs-lookup"><span data-stu-id="b9c58-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="b9c58-143">Kjøre Rull anleggsmidler forover-rapporten på nytt</span><span class="sxs-lookup"><span data-stu-id="b9c58-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="b9c58-144">Gå til **Anleggsmidler** \> **Forespørsler og rapporter** \> **Transaksjonsrapporter** \> **Rull anleggsmidler forover**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="b9c58-145">Angi **1/1/2017** i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="b9c58-146">Angi **1/31/2017** i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="b9c58-147">I **Valuta-felt** velger du **Regnskapsvaluta**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="b9c58-148">I feltet **Formattilordning** velger du **Rull anleggsmidler forover**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="b9c58-149">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9c58-149">Select **OK**.</span></span>
7. <span data-ttu-id="b9c58-150">Bla i den lokale mappen **C:\\0** for å finne den genererte filen.</span><span class="sxs-lookup"><span data-stu-id="b9c58-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="b9c58-151">Fordi `originDestination`-objektet ikke brukes i `AssetRollForwardDestination`-objektet i dette eksemplet, ignoreres konfigurasjonene for ER-format[målene](electronic-reporting-destinations.md) under kjøring.</span><span class="sxs-lookup"><span data-stu-id="b9c58-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9c58-152">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b9c58-152">Additional resources</span></span>

- [<span data-ttu-id="b9c58-153">Mål for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b9c58-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="b9c58-154">Startside med utvidelsesmuligheter</span><span class="sxs-lookup"><span data-stu-id="b9c58-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]