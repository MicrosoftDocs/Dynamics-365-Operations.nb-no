---
title: Angi egendefinerte lagerplasseringer for genererte dokumenter
description: Dette emnet forklarer hvordan du utvider listen over lagringssteder for dokumenter som genereres av Elektronisk rapportering (ER)-formater.
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 146e7fb5fefbecabc99c2978b52eb0e782da0322
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562220"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Angi egendefinerte lagerplasseringer for genererte dokumenter

[!include[banner](../includes/banner.md)]

API (Application programming interface) for Elektronisk rapportering-rammeverket (ER) lar deg utvide listen over lagringssteder for dokumenter som ER-formater genererer. Dette emnet forklarer hvordan du legger til en egendefinert lagringsplassering for genererte dokumenter ved å delegere oppgaven med å opprette ER-mål til standardmålfabrikk og deretter implementere en egendefinert klasse som har sin egen logikk.

## <a name="prerequisites"></a>Forutsetninger

Distribuer en topologi som støtter fortløpende bygging. Hvis du vil ha mer informasjon, kan du se [Distribuere topologier som støtter sammenhengende automatisering av bygging og testing](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Du må ha tilgang til denne topologien for én av følgende roller:

- Utvikler av elektronisk rapportering
- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

Du må også ha tilgang til utviklingsmiljøet for denne topologien.

Alle oppgavene i dette emnet kan fullføres i **USMF**-firmaet.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Importere ER-formatet Rull anleggsmidler forover

For å generere dokumentene du planlegger å legge til en egendefinert lagringsplassering for, kan du [importere](er-download-configurations-global-repo.md) ER-formatkonfigurasjonen **Rull anleggsmidler forover** til gjeldende topologi.

![Konfigurasjonsrepositorium-side](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Kjøre Rull anleggsmidler forover-rapporten

1. Gå til **Anleggsmidler** \> **Forespørsler og rapporter** \> **Transaksjonsrapporter** \> **Rull anleggsmidler forover**.
2. Angi **1/1/2017** (1. januar 2017) i **Fra dato**-feltet.
3. Angi **1/31/2017** (31. januar 2017) i **Til dato**-feltet.
4. I **Valuta-felt** velger du **Regnskapsvaluta**.
5. I feltet **Formattilordning** velger du **Rull anleggsmidler forover**.
6. Velg **OK**.

![Dialogboksen for kjøretid for Rull anleggsmidler forover-rapporten](./media/er-custom-storage-generated-files-runtime-dialog.png)

I Microsoft Excel kan du se gjennom det utgående dokumentet som er generert og tilgjengelig for nedlasting. Denne virkemåten er [standard virkemåte](electronic-reporting-destinations.md#default-behavior) for et ER-format som ingen [mål](electronic-reporting-destinations.md) er konfigurert for, og som kjører i interaktiv modus.

## <a name="review-the-source-code"></a>Gå gjennom kildekoden

Gå gjennom koden for `generateReportByGER()`-metoden for `AssetRollForwardService`-klasse. Legg merke til at `Run()`-metoden brukes til å kalle opp ER-rammeverket og generere rapporten **Rull anleggsmidler forover**.

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

## <a name="modify-the-source-code"></a>Endre kildekoden

1. I Visual Studio-prosjektet legger du til en ny klasse (`AssetRollForwardDestination` i dette eksemplet), og skriver kode for å implementere det egendefinerte målet for **Rull anleggsmidler forover**-rapporter som genereres.

    - `new()`-metoden er utformet for å hente det opprinnelige ER-målobjektet og den programlogikkbaserte parameteren som angir den egendefinerte lokasjonen der genererte rapporter skal lagres. I dette eksemplet er den egendefinerte plasseringen navnet på en mappe i det lokale filsystemet til serveren som kjører AOS-tjenesten.
    - `saveFile()`-metoden er utformet for å lagre et generert dokument i en mappe i det lokale filsystemet på serveren som kjører AOS-tjenesten.

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

2. I Visual Studio-prosjektet legger du til en ny klasse (`AssetRollForwardDestinationFactory` i dette eksemplet) og skriver kode for å definere en egendefinert målfabrikk som delegerer opprettelsen av et mål til standardmålfabrikken, og for å bryte en fildestinasjon med ditt eget mål.

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

3. Endre den eksisterende `AssetRollForwardService`-klassen, og skriv kode for å definere en egendefinert målfabrikk for rapportkjøringen. Legg merke til at når en egendefinert målfabrikk opprettes, blir den programdrevne parameteren som angir en målmappe, sendt. På denne måten brukes målmappen til å lagre genererte filer.

    > [!NOTE] 
    > Kontroller at den angitte mappen (**c:\\0** i dette eksemplet) finnes i det lokale filsystemet på serveren som kjører AOS-tjenesten. Hvis ikke vil unntaket [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) oppstå under kjøring.

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

4. Bygg prosjektet på nytt.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Kjøre Rull anleggsmidler forover-rapporten på nytt

1. Gå til **Anleggsmidler** \> **Forespørsler og rapporter** \> **Transaksjonsrapporter** \> **Rull anleggsmidler forover**.
2. Angi **1/1/2017** i feltet **Fra dato**.
3. Angi **1/31/2017** i feltet **Til dato**.
4. I **Valuta-felt** velger du **Regnskapsvaluta**.
5. I feltet **Formattilordning** velger du **Rull anleggsmidler forover**.
6. Velg **OK**.
7. Bla i den lokale mappen **C:\\0** for å finne den genererte filen.

> [!NOTE]
> Fordi `originDestination`-objektet ikke brukes i `AssetRollForwardDestination`-objektet i dette eksemplet, ignoreres konfigurasjonene for ER-format[målene](electronic-reporting-destinations.md) under kjøring.

## <a name="additional-resources"></a>Tilleggsressurser

- [Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Startside med utvidelsesmuligheter](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]