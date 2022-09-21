---
title: Definere en alternativ dataflyt for anbefalinger
description: Denne artikkelen beskriver hvordan du konfigurerer et miljø ved hjelp av en alternativ dataflyt for å angi data til anbefalingstjenesten.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460166"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Definere en alternativ dataflyt for anbefalinger

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer et miljø ved hjelp av en alternativ dataflyt for å angi data til anbefalingstjenesten.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Sammenligning av medfølgende dataflyt med alternativ dataflyt

Illustrasjonen nedenfor viser den medfølgende dataflyten i et miljø.

![Medfølgende dataflyt i et miljø](media/reco-out-of-the-box-dataflow-2.png)

Illustrasjonen nedenfor viser en alternativ dataflyt der den satsvise jobben for enhetslagersynkronisering er erstattet med alternative dataflyttrinn.

![Alternativ dataflyt i et miljø](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Antagelser

- Denne artikkelen antar at du allerede har aktivert anbefalingstjenesten for miljøet ditt. Hvis du vil ha mer informasjon, kan du se [Aktivere produktanbefalinger](enable-product-recommendations.md).
- Når du arbeider med filer og mapper i Microsoft Azure Data Lake-lagringskontoen:

    - Du kan bruke grensesnittet for Azure-webportalen eller Azure Storage Explorer-appen.
    - Startpunktene for arbeid med filer og mapper finnes i beholderen **dynamics365-financeandoperations**, som er plassert under mappen som er navngitt i henhold til URL-adressen til miljøet ditt.
    - Hvis navnet på sandkassemiljøet ditt er **MyUAT**, blir URL-basisadressen til miljøet `myuat.sandbox.operations.dynamics.com`.
    - Hvis flere miljøer er koblet til samme lagringskonto, vil hvert miljø ha sin egen rotmappe.

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger må være på plass før du kan implementere den alternative tilnærmingen til dataflyt.

### <a name="set-up-microsoft-power-platform"></a>Definer Microsoft Power Platform

Hvis du vil konfigurere Microsoft Power Platform, følger du instruksjonene i [Aktiver Microsoft Power Platform-integreringen](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>Installer tilleggsprogrammet Eksporter til Data Lake

Hvis du vil installere tilleggsprogrammet Eksporter til Data Lake, følger du instruksjonene i [Installer tilleggsprogrammet Eksporter til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Legg merke til konfigurasjonsverdiene fordi du trenger dem i noen av trinnene som følger.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Konfigurere tabeller som skal eksporteres i Dynamics 365

Tabellsynkronisering fra Dynamics 365 til Azure Data Lake Storage håndteres på siden **Eksporter til Data Lake**. Siden denne siden ikke har et menyelement for øyeblikket, kan bare brukere med sikkerhetsrollen **Systemansvarlig** åpne den.

Følg denne fremgangsmåten for å konfigurere tabeller som skal eksporteres i Dynamics 365.

1. For å åpne siden **Eksporter til Data Lake** må du legge til strengen `?mi=DataFeedsDefinitionWorkspace` i miljøets basis-URL, som vist i følgende eksempel:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. Gå til siden **Eksporter til Data Lake**, og kopier tabellene som vises i delen [Liste over RetailSales-kubetabeller](#list-of-retailsales-cube-tables) i denne artikkelen.
1. I **Systemnavn**-kolonnen utvider du listen med filteralternativer.
1. For filtertypen velger du **er en av**. Plasser deretter markøren i tekstboksen, og lim inn listen over tabeller du kopierte fra siden **Eksporter til Data Lake**.
1. Velg **Bruk** nederst i listen over filteralternativer.
1. Velg alle radene i rutenettet, og velg deretter **Aktiver**.

> [!NOTE]
> Før du går videre til neste trinn, må alle rader oppdateres til statusen **Kjører**. Feilsøk og løs eventuelle feil etter behov.

### <a name="create-a-synapse-workspace"></a>Opprett et Synapse-arbeidsområde

For å opprette et Synapse-arbeidsområde hvis du ikke allerede har et, følger du instruksjonene i [Hurtigstart: Opprett et Synapse-arbeidsområde](/azure/synapse-analytics/quickstart-create-workspace).

For å holde Azure-ressursene organisert anbefaler vi at du plasserer Data Lake Storage-kontoen og Synapse-arbeidsområdet sammen i en ressursgruppe i Azure. Du kan gjenbruke lagringskontoen du opprettet da du installerte tilleggsprogrammet Eksporter til Data Lake.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Opprett en database i Synapse for behandling av anbefalingsdata

Bruk Common Data Model-verktøykonsollappen (CDMUtil_ConsoleApp) til å opprette en database i Synapse-arbeidsområdet, og fyll den ut fra Common Data Model-tabellene i Data Lake Storage. Vi anbefaler at du bruker Common Data Model-verktøyet med databasen i et utviklingsmiljø, i tilfelle det finnes utvidelser.

> [!NOTE]
> Trinnene nedenfor forutsetter at det ikke blir lagt til noen utvidelsesdata i RetailSales-kuben.

Følg disse trinnene for å opprette en database i Synapse.

1. Gå til [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app), og følg trinnene for å laste ned **CDMUtilConsoleApp.zip**-filen.
1. Pakk ut zip-filen i en lokal mappe.
1. Åpne filen **CDMUtil_ConsoleApp.dll.config** i et tekstredigeringsprogram, og oppdater følgende verdier:

    1. Angi verdien for **Leier-ID** (Azure-leier-ID).
    1. Angi verdien for **Tilgangsnøkkel** (tilgangsnøkkelen for Data Lake Storage-kontoen).

        1. Åpne lagringskontoen din i Azure-portalen.
        1. Velg **Tilgangsnøkler** på menyen til venstre på siden.
        1. Velg **Vis nøkler** øverst på siden.
        1. Velg kopieringsknappen for ett av de to nøkkelfeltene, og lim deretter inn verdien mellom de doble anførselstegnene i konfigurasjonsfilen.

    1. Angi verdien for **ManifestURL** til URL-adressen til **Tables.manifest.cdm.json**-filen i Azure Data Lake Storage. Du kan hente URL-adressen ved å bla til filen i Azure-portalen, merke ellipsen (**...**) til høyre for visningen og deretter velge **Egenskaper**. URL-adressen er den første egenskapen som vises på **Oversikt**-fanen.
    1. Angi **TargetDbConnectionString**-verdien til tilkoblingsstrengen for den innebygde serverløse SQL-gruppen uten server i Synapse-arbeidsområdet.

        1. Velg **Administrer**-fanen i Synapse-arbeidsområdet.
        1. Velg **SQL-grupper** på undermenyen.
        1. Velg navnet **Innebygd** for å vise gruppens egenskaper.
        1. Velg ADO.NET-tilkoblingstypen du vil bruke, i dialogboksen Egenskaper. Deretter kopierer du tilkoblingsstrengverdien og limer den inn mellom de doble anførselstegnene i konfigurasjonsfilen.

        > [!NOTE]
        > Du må ha tillatelse til å opprette databaser. For å gjøre det enklere kan du bruke den innebygde **sqladminuser**-administratorkontoen.

    1. Fjern kommentaren på **ProcessEntities**-noden, og angi verdien til **true** (for eksempel `<add key="ProcessEntities" value ="true"/>`).

1. Lagre og lukk **CDMUtil_ConsoleApp.dll.config**-filen.
1. Kopier **EntityList.json**-filen til **/Manifest**-katalogen.
1. I et ledetekstvindu kjører du **cdmutil_consoleapp.exe**.

> [!NOTE]
> Når du går gjennom utdataene, skal det være 35 enheter/visninger, minst 75 tabeller og ingen feil.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Klargjør katalogen Aggregerte målinger under RetailSales i Data Lake

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Sikkerhetskopier nåværende RetailSales-kubedata fra Data Lake Storage

Den enkleste måten å sikkerhetskopiere gjeldende RetailSales-kubedata på er å endre navnet på **RetailSales**-katalogen i Data Lake Storage til **RetailSales-sikkerhetskopi** eller noe lignende. Denne metoden bevarer de eksisterende dataene hvis feilsøking er nødvendig senere.

Kubemappen **/RetailSales** finnes på følgende plassering:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Opprett en ny RetailSales-mappe og last opp modellfilen

Følg denne fremgangsmåten for å opprette en ny **RetailSales**-katalog og laste opp **model.json**-filen til Data Lake Storage.

1. Opprett en ny tom katalog på samme nivå som den forrige katalogen, og gi den navnet **RetailSales**.
1. Last opp **model.json**-filen til den nye katalogen.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Opprett et datasamlebånd for å kopiere RetailSales-kubedataene

Datasamlebåndet vil lese RetailSales-kubevisningene og eksportere dataene til .csv-filer i Data Lake Storage.

Gjør følgende for å opprette et datasamlebånd for å kopiere RetailSales-kubedataene.

1. Velg **Integrer**-fanen i Synapse-arbeidsområdet.
1. Velg plusstegnet (**+**), og velg deretter **Importer fra datasamlebåndmal**.
1. Last ned og velg deretter [ExportRetailSalesCubeViews.zip-filen](https://aka.ms/reco-alternate-dataflow-files).
1. Velg den tilknyttede SQL-databasen.
1. Velg den tilknyttede tjenesten for lagringskontoen.
1. Åpne verktøyet **Kopier data**, og endre egenskapen **Mappebane** til **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Test kjøringen av datasamlebåndet

Vi anbefaler at du tester datasamlebåndet bare ved hjelp av én visning. Visningen **RetailSales_RetailMediaTemplateView** fungerer bra, fordi den vanligvis inneholder færre enn ti rader.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Planlegg at datasamlebåndet skal kjøres etter en regelmessig plan

Hver gang et datasamlebånd kjøres, forekommer Azure-forbruk. Vi anbefaler at du planlegger kjøringer i intervaller på minst 48 timer. Du kan alltid kjøre datasamlebåndet manuelt hvis du må synkronisere data umiddelbart. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Tabellliste for synkronisering fra Dynamics 365 til Data Lake Storage

Følgende liste over tabeller er et delsett av alle tabellene som er nødvendige for hele RetailSales-kuben. Bare 15 av visningene i RetailSales-kuben brukes av anbefalingstjenesten, og listen over nødvendige tabeller ble filtrert i henhold til dette.

### <a name="list-of-retailsales-cube-tables"></a>Liste over RetailSales-kubetabeller

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Katalog
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Vis liste for parameteren som skal gå til Synapse-datasamlebåndet

Følgende kommadelte liste inneholder RetailSales-kubevisningene som datasamlebåndet utfører en "velg"-operasjon på. Resultatene kopieres deretter til Data Lake Storage.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Datasamlebåndparameteren må være en liste over visningsnavn som er atskilt med enkle komma. Det må ikke være mellomrom eller linjemating.

## <a name="environment-specific-fixes"></a>Miljøspesifikke reparasjoner

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW-reparasjon

**RETAILCHANNELVIEW**-visningen inneholder et hardkodet heltall som representerer en organisasjon av typen "detaljhandelskanal". Den faktiske verdien av typen kan endres fra miljø til miljø, eller fra leier til leier.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Gjør følgende for å oppdatere det hardkodede heltallet:

1. I Dynamics 365 slår du opp **ChannelID**-verdien for den nettbaserte kanalen.
1. I en forekomst av SQL Server Management Studio (SSMS) som er knyttet til Synapse-databasen, kjører du følgende spørring.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Kopier verdien fra første kolonne (**INSTANCERELATIONTYPE**), og lim den inn i visningsdefinisjonen.

## <a name="troubleshooting"></a>Feilsøking

### <a name="pipeline-task-fails"></a>Datasamlebåndoppgave mislykkes

Det skal finnes 15 kjøringer av datasamlebåndoppgaver for **CopyData**-oppgaven. Hvis en kjøring mislykkes, må du validere at alle de avhengige SQL-objektene finnes, og at spørringene kjører. Den enkleste måten å komme til alle avhengighetene på, er å bruke SSMS til å koble til databasen. Deretter kan du velge og holde (eller høyreklikke) en visning og velge **Generer OPPRETT som til et nytt vindu**.

Feilmeldingen kan inkludere følgende tekst:

- Feil: Det oppstod en feil på "Kilde"-siden
- Feil under behandlng av ekstern fil: "Maksimalt antall feil."
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Eksempelscenario

I dette eksemplet mislyktes oppgaven **RetailSales_RetailProductCategory**, og du får en feil av typen "Maksimalt antall feil".

Gjør følgende for å feilsøke feilen.

1. Åpne filen **EntityList.json** i et tekstredigeringsprogram (for eksempel Visual Studio Code).
1. Finn visningsdefinisjonen for **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Denne visningen avhenger bare av én annen visning: **RetailProductCategoryView** _. Finn visningsdefinisjonen for _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Denne visningen avhenger av tre andre visninger: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** og **RETAILCATEGORYEXPANDED**. Finn definisjonen for hver av disse visningene, og vis avhengighetene i den. Fortsett til du finner alle de avhengige visningene.

    Her er hele listen i avhengighetstrerekkefølge. Tretten visninger må valideres.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. I Excel oppretter du følgende 13 **select count(\*) fra \<view_name\>**-setninger. Kjør disse setningene i SSMS, og send resultatene til tekst. Bla deretter gjennom resultatene for å se om noen av visningene mislyktes. Den innledende feilen antyder at minst én av visningene vil mislykkes.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Én måte å validere det du ser på, er å opprette en rotavhengig visning for å generere visningsdefinisjonen i SSMS. Deretter kontrollerer du at det finnes en Azure Data Lake-filkolonne med navnet **r.filepath**. Hvis denne kolonnen finnes, betyr det at visningen du undersøker, leser data fra Data Lake Storage.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger på transaksjonsskjermen](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
