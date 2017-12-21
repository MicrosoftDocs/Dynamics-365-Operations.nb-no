---
title: Tilbakestille data mart for finansrapportering
description: Dette emnet beskriver hvordan du tilbakestiller data mart for finansrapportering.
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: nb-no
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Tilbakestille data mart for finansrapportering

[!include[banner](../includes/banner.md)]

Dette emnet forklarer hvordan du tilbakestiller data mart for finansrapportering for følgende versjoner:

- Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.2.6.0 og nyere
- Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.0.10000.4 og nyere
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (lokal)

Hvis du vil ha Finance and Operations Financial reporting versjon 7.2.6.0, kan du laste ned KB 4052514 fra <https://support.microsoft.com/en-us/help/4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Tilbakestille data mart for finansrapportering for Finance and Operations Financial reporting versjon 7.2.6.0 og nyere

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Tilbakestille datamart for finansrapportering fra Rapportutforming

> [!NOTE]
> Trinnene i denne prosessen støttes for Finance and Operations Financial reporting versjon 7.2.6.0 og senere. Hvis du har en eldre versjon, kan du kontakte kundestøtteteamet for å få hjelp.

I bestemte situasjoner må du kanskje tilbakestille data mart for finansrapportering. Du kan fullføre denne oppgaven i Rapportutforming-klienten. Her er noen scenarier der du kanskje må tilbakestille data mart:

- Finance and Operations-databasen ble gjenopprettet, men data mart-databasen ble ikke gjenopprettet.
- Du kan se uriktige data for en periode.
- Kundestøtte ber deg om å tilbakestille data mart-databasen som en del av et trinn i feilsøkingsprosessen.

Data mart-tilbakestillingen bør bare utføres når det foregår lite behandling i databasen. Finansrapportering blir ikke tilgjengelig under tilbakestillingen.

#### <a name="reset-the-data-mart"></a>Tilbakestill data mart

Hvis du vil tilbakestille data mart, går du til rapportutforming og velger **Tilbakestill data mart** på **Verktøy**-menyen. Dialogboksen som vises, har to deler: **Statistikk** og **Tilbakestill**.

[![Dialogboksen Tilbakestill data mart](./media/Statistics.png)](./media/Statistics.png)

##### <a name="integration-attempts"></a>Integreringsforsøk

**Integreringsforsøk**-rutenettet viser hvor mange ganger systemet har forsøkt å integrere transaksjoner. Systemet fortsetter å prøve å integrere data i en periode med dager hvis de første få forsøkene ikke lykkes. Du vil vite at data mart må tilbakestilles hvis antall forsøk er 8 eller mer, og hvis det er mange dimensjonskombinasjoner eller transaksjonsposter. I så fall vil ikke dataene rapporteres.

##### <a name="data-status"></a>Datastatus

**Datastatus**-rutenettet gir en oversikt over transaksjoner, valutakurser og dimensjonsverdier i data mart. Mange foreldede oppføringer angir at det har oppstått mange oppdateringer av postene. Dette kan føre til at rapportgenereringstidene kan gå saktere.

##### <a name="misaligned-main-account-categories"></a>Feiljusterte hovedkontokategorier

Hvis du bruker en versjon som er eldre enn Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.2.1, må du kanskje tilbakestille data mart hvis du gir kontoer nytt navn og flytter kontoer mellom kontokategorier. Disse handlingene kan føre til at hovedkontokategorier blir feiljustert. **Feiljusterte hovedkontokategorier**-feltet viser om du opplever dette problemet.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Tilbakestille data mart i Finance and Operations Financial reporting versjon 7.2.6.0

Hvis du vil tilbakestille data mart i Finance and Operations Financial reporting versjon 7.2.6.0 og tidligere, går du til **Tilbakestill data mart**-dialogboksen, merker av for **Tilbakestill data mart** og velger **OK**. Du bør bare tilbakestille data mart under planlagt nedetid.

[![Avmerkingsboksen Tilbakestill data mart](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Tilbakestille data mart og velge en årsak i Microsoft Dynamics 365 for Finance and Operations Financial reporting versjon 7.3.0

Hvis du finner ut at det kreves en tilbakestilling av data mart, merker du av for **Tilbakestill data mart**, og velger deretter en årsak i **Årsak**-feltet. Følgende alternativer er tilgjengelige:

- **Manglende eller ugyldige data** – Basert på statistikken har du fastslått at data kan mangle. Før du fortsetter, anbefaler vi at du arbeider med støtte for å fastslå årsaken.
- **Gjenopprett database** – Finance and Operations-databasen ble gjenopprettet, men databasen for data-mart for finansrapportering ble ikke gjenopprettet.
- **Andre** – Du tilbakestiller data mart av en annen grunn. Hvis du er redd for at det er et problem, kan du kontakte kundestøtte for å identifisere det.

> [!NOTE]
> Kontroller at alle eksisterende oppgaver har fullført integreringen før du fullfører trinnene. Du kan vise statusen for integreringen ved å velge **Verktøy** &gt; **Integreringsstatus**.

#### <a name="clear-users-and-companies"></a>Fjern brukere og firmaer

Merk av for **Fjern brukere og firmaer** hvis du har gjenopprettet databasen, men deretter har gjort endringer i brukere eller selskaper. Du bør sjeldent få behov for å merke av i denne boksen.

Når du er klar til å starte tilbakestillingen, velger du **OK**. Du blir bedt om å bekrefte at du er klar til å starte prosessen. Legg merke til at finansrapportering ikke er tilgjengelig under tilbakestillingen og den første dataintegreringen som skjer etterpå.

Hvis du vil vise statusen for integreringen, velger du **Verktøy** &gt; **Integreringsstatus** for å se sist gang integreringen ble kjørt og statusen.

[![Vise statusen for integreringen](./media/Integration.png)](./media/Integration.png)

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Tilbakestille data mart for finansrapportering for Finance and Operations Financial reporting versjon 7.0.10000.4 og nyere

Hvis du gjenoppretter Finance and Operations-databasen fra en sikkerhetskopi eller kopierer databasen fra et annet miljø, må du følge trinnene i denne delen for å sikre at data mart for finansrapportering bruker den gjenopprettede Finance and Operations-databasen på riktig måte.

> [!NOTE]
> Fremgangsmåten i denne prosessen støttes for Microsoft Dynamics AX-programmet versjon 7.0.1 (mai 2016) (programbygg 7.0.1265.23014 og Financial reporting bygg 7.0.10000.4) og nyere. Hvis du har en tidligere versjon av Finance and Operations, kan du kontakte kundestøtte for å få hjelp.

### <a name="export-report-definitions"></a>Eksportere rapportdefinisjoner

Først gjør du følgende for å eksportere rapportutformingene fra Rapportutforming.

1. I Rapportutforming velger du **Firma** &gt; **Byggeblokkgrupper**.
2. Velg byggeblokkgruppen du vil eksportere, og velg deretter **Eksporter**.

    > [!NOTE]
    > For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.

3. Velg rapportdefinisjonene som skal eksporteres:

    - Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, velger du **Merk alle**.
    - Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du den aktuelle kategorien og velger deretter elementene som skal eksporteres. Trykk og hold inne Ctrl-tasten for å velge flere varer i en kategori. Når du velger rapporter som skal eksporteres, velges de tilhørende radene, kolonnene, trærne og dimensjonssettene.

4. Velg **Eksporter**.
5. Skriv inn et filnavn, og velger en sikkert plassering der du vil lagre de eksporterte rapportdefinisjonene.
6. Velg **Lagre**.

Du kan kopiere eller laste opp filen til en sikker plassering. På denne måten kan filen importeres til et annet miljø senere. Du finner informasjon om hvordan du bruker en Microsoft Azure-lagringskonto i [Overføre data med kommandolinjeverktøyet AzCopy](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft tilbyr ingen lagringskonto som en del av Finance and Operations-avtalen. Du må kjøpe en lagringskonto eller bruke en lagringskonto fra et eget Azure-abonnement.

> [!WARNING]
> Vær oppmerksom på virkemåten til stasjon D på virtuelle Azure-maskiner (VM-er). Ikke lagre de eksporterte byggeblokkgruppene permanent på stasjon D. Hvis du vil ha mer informasjon om midlertidige stasjoner, kan du se [Forstå den midlertidige stasjonen på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Stoppe tjenester

Følgende Microsoft Windows-tjenester vil ha åpne tilkoblinger til Finance and Operations-databasen. Derfor må du bruke Microsoft Eksternt skrivebord til å koble til alle datamaskinene i miljøet, og deretter bruke services.msc til å stoppe disse tjenestene.

- Webpubliseringstjenesten (for alle AOS-datamaskiner (Application Object-servere))
- Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)
- Prosesstjenesten for Management Reporter 2012 (bare på Business intelligence [BI]-datamaskiner)

### <a name="reset"></a>Tilbakestill

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Last ned den siste MinorVersionDataUpgrade.zip-pakken

Last ned den siste MinorVersionDataUpgrade.zip-pakken. For instruksjoner om hvordan du finner og laster ned riktig versjon av dataoppgraderingspakken, kan du se [Last ned den nyeste distribuerbare dataoppgraderingspakken](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). En oppgradering er ikke nødvendig for å laste ned MinorVersionDataUpgrade.zip-pakken. Du må derfor bare følge trinnene i delen "Last ned den nyeste distribuerbare dataoppgraderingspakken" i dette emnet. Du kan hoppe over alle de andre trinnene i emnet.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Kjøre skript på Finance and Operations-databasen

Kjør skriptene nedenfor på Finance and Operations-databasen (ikke mot finansrapporteringsdatabasen):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Disse skriptene bidrar til å sikre at innstillinger for brukere, roller og endringssporing er riktige.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Kjøre en Windows PowerShell-kommando for å tilbakestille databasen

På AOS-datamaskinen starter du Microsoft Windows PowerShell som administrator, og kjører følgende kommandoer for å tilbakestille integreringen mellom Finance and Operations og finansrapportering.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Her finner du en forklaring på parameterne i **Reset-DatamartIntegration**-kommandoen:

- Gyldige verdier for **-Reason** er **SERVICING**, **BADDATA** og **OTHER**.
- Parameteren **-ReasonDetail** er fritekst.
- Reason og reason detail blir registrert i telemetri / miljøovervåking.

> [!NOTE]
> Når du har kjørt kommandoene, får du spørsmål om å angi **Y** for å bekrefte at du vil tilbakestille databasen.

#### <a name="restart-services"></a>Starte tjenester på nytt

Bruk Services.msc til å starte tjenestene du stoppet tidligere:

- Webpubliseringstjenesten (for alle AOS-datamaskiner)
- Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)
- Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)

#### <a name="import-report-definitions"></a>Importere rapportdefinisjoner

Importer rapportutformingene fra Rapportutforming ved hjelp av filen som ble opprettet under eksporten.

1. I Rapportutforming velger du **Firma** &gt; **Byggeblokkgrupper**.
2. Velg byggeblokkgruppen du vil eksportere, og velg deretter **Eksporter**.

    > [!NOTE]
    > For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.

3. Velg **Standard**-byggeblokken, og velg deretter **Importer**.
4. Velg filen som inneholder de eksporterte rapportdefinisjonene, og velg deretter **Åpne**.
5. Velg rapportdefinisjonene som skal importeres, i dialogboksen **Importer**:

    - Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, velger du **Merk alle**.
    - Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, merker du rapportene, radene, kolonnene, trærne eller dimensjonssettene som skal importeres.

6. Velg **Import**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Tilbakestille data mart for finansrapportering for Finance and Operations (lokal)

1. Be alle brukerne om å avslutte Rapportutforming og Finansrapportering-området i Finance and Operations.
2. Kjør følgende skript på Finansrapportering-databasen (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Avkort eller slett alle postene fra tabellen FINANCIALREPORTS i Finance and Operations-databasen (AXDB).
4. Avkort eller slett alle postene fra tabellen FINANCIALREPORTVERSION hvis denne tabellen finnes i Finance and Operations-databasen. Hvis tabellen ikke finnes i Finance and Operations-databasen, hopper du over dette trinnet.
5. Kjør **ResetDatamart**-skriptet på Finansrapportering-databasen. Dette skriptet deaktiverer data mart-integreringen, sletter alle data mart-dataene og aktiverer deretter data mart-integreringen på nytt.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Etter tilbakestillingen, kan du bekrefte den nye datainnlastingen manuelt ved å kjøre følgende spørring mot Finansrapportering-databasen.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Kontroller at alle rader har verdien **LastRunTime**, og at **StateType** er satt til **5**. En **StateType**-verdi på **5** angir at dataene ble lastet inn på nytt. En verdi på **7** angir en feilstatus. Noen ganger har organisasjonshierarkikartet denne tilstanden første gang den kjøres. Feilstatusen må imidlertid løses automatisk.

