---
title: Bruke JOIN-datakilder i ER-modelltilordninger til å hente data fra flere programtabeller
description: Denne artikkelen forklarer hvordan du kan bruke datakilder av JOIN-typen i elektronisk rapportering (ER).
author: kfend
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 3f03e69dbce7c9039f22dbb8f3afa06f16d9c080
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285159"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Bruke JOIN-datakilder til å hente data fra flere programtabeller i modelltilordninger for elektronisk rapportering (ER)

[!include[banner](../includes/banner.md)]

Når du konfigurerer modelltilordninger eller formater for elektronisk rapportering (ER), kan du [legge til](#review) nødvendige datakilder av **Join**-typen. Under utformingen konfigureres en **Join**-datakilde som et sett med flere datakilder hver som returnerer en liste med poster. For hver datakilde unntatt den første må du definere nødvendige betingelser for å føye sammen poster for gjeldende og tidligere datakilder. Under kjøring [returnerer](#executeERformat) en konfigurert datatype av typen **Join** en enkelt sammenkoblet liste med poster som inneholder felt fra postene for nestede datakilder.

Følgende sammenkoblingstyper støttes for øyeblikket:

- Ytre (venstre) join:
    - Slå sammen alle poster i den første (helt til venstre) datakilden og deretter eventuelle samsvar i henhold til konfigurerte vilkårsposter i den andre (den høyre) datakilden.
- Indre (høyre) join:
    - Bare slå sammen poster i den første (helt til venstre) datakilden og bare poster i den andre (den høyre) datakilden som samsvarer med hverandre i henhold til konfigurerte vilkårsposter.

I den konfigurerte **Join**-datakilden, når alle datakilder er av typen **Tabellposter**, kan utførelse av Join-datakilden [utføres på databasenivå](#analyze) ved hjelp av én enkelt SQL-setning. Denne setningen reduserer antallet databasekall, noe som forbedrer modelltilordningsytelsen. Hvis ikke utføres **Join**-datakilden i minnet.

> [!NOTE]
> Bruk av **VALUEIN**-funksjonen i ER-uttrykk som angir betingelser for sammenkobling av poster i datakilder av Join-typen, støttes ikke ennå. Gå til siden [Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md) for mer informasjon om denne funksjonen.

Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet i denne artikkelen.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Eksempel: Bruk JOIN-datakilder i ER-modelltilordninger

De følgende trinnene forklarer hvordan den systemansvarlige eller utvikleren av elektronisk rapportering kan konfigurere modelltilordning for elektronisk rapportering (ER) for å hente data fra flere programtabeller samtidig ved å bruke datakilder av typen **Join** til å forbedre datatilgangsytelsen. Disse trinnene kan utføres for et hvilket som helst firma med Dynamics 365 Finance eller Regulatory Configuration Services (RCS).

### <a name="prerequisites"></a>Forutsetninger

Hvis du vil fullføre eksemplene i denne artikkelen, må du ha tilgang til ett av følgende, avhengig av hvilken tjeneste som brukes til å utføre disse trinnene:

**Tilgang til Finance for én av følgende roller:**

- Utvikler av elektronisk rapportering
- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

**Tilgang til RCS for én av følgende roller:**

- Utvikler av elektronisk rapportering
- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

Du må også først fullføre disse trinnene i fremgangsmåten [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

På forhånd må du også laste ned og lagre følgende eksempel-ER-konfigurasjonsfiler:

| **Innholdsbeskrivelse**  | **Filnavn**   |
|--------------------------|-----------------|
| Eksempel **ER-datamodell**-konfigurasjonsfil, som brukes som datakilde for eksemplene.| [Modell for å lære JOIN-datakilder.versjon.1.1.xml](https://download.microsoft.com/download/5/c/1/5c1d8a57-6ebd-425b-bc5d-c71dde92c6af/ModeltolearnJOINdatasources.version.1.xml) |
| Eksempelkonfigurasjonsfil for **ER-modelltilordning**, som implementerer ER-datamodellen for eksemplene. | [Tilordning for å lære JOIN-datakilder.versjon.1.1.xml](https://download.microsoft.com/download/9/2/f/92f339ca-41fc-4f5e-b458-6983c957d3dd/MappingtolearnJOINdatasources.version.1.1.xml)|
| Eksempelkonfigurasjonsfil for **ER-format**. Denne filen beskriver dataene for å fylle ut ER-formatkomponenten for eksemplene. | [Format for å lære JOIN-datakilder.versjon.1.1.xml](https://download.microsoft.com/download/f/f/8/ff8f1b48-14d0-4c73-9145-bcdf8b5265bc/FormattolearnJOINdatasources.version.1.1.xml) |

### <a name="activate-a-configurations-provider"></a>Aktivere en konfigurasjonsleverandør

1. Du får tilgang til Finance eller RCS i den første økten av webleseren.
2. Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.
3. På **Lokaliseringskonfigurasjoner**-siden i **Konfigurasjonsleverandører**-delen må du sørge for at konfigurasjonsleverandør for eksempelselskapet [Litware, Inc.](http://www.litware.com) er oppført, og at den er merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, følger du trinnene i prosedyren [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Arbeidsområdet Elektronisk rapportering.](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>Importere ER-eksempelkonfigurasjonsfiler

1. Velg **Rapporteringskonfigurasjoner**.
2. Importer ER-datamodellkonfigurasjonsfilen.
    1. Velg **Veksle**.
    2. Velg **Last fra XML-fil**.
    3. Velg **Bla gjennom** for å finne filen **Modell for å lære JOIN-datakilder.versjon.1.1.xml**.
    4. Velg **OK**.
3. Importer konfigurasjonsfilen for ER-modelltilordning.
    1. Velg **Veksle**.
    2. Velg **Last fra XML-fil**.
    3. Velg **Bla gjennom** for å finne filen **Tilordning for å lære JOIN-datakilder.versjon.1.1.xml**.
    4. Velg **OK**.
4. Importer ER-formatkonfigurasjonsfilen.
    1. Velg **Veksle**.
    2. Velg **Last fra XML-fil**.
    3. Velg **Bla gjennom** for å finne filen **Format for å lære JOIN-datakilder.versjon.1.1.xml**.
    4. Velg **OK**.
5. I konfigurasjonstreet utvider du elementet for **Modell for å lære JOIN-datakilder** samt andre modellelementer (når det er tilgjengelig).
6. Se på listen over ER-konfigurasjoner i treet i tillegg til versjonsdetaljer i hurtigfanen **Versjoner** – de brukes som datakilden for eksempelrapporten.

    ![Side for konfigurasjoner for elektronisk rapportering.](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Slå på alternativer for utførelsessporing

1. Velg **KONFIGURASJONER**.
2. Velg **Brukerparametere**.
3. Angi parametere for utførelsessporing som vist på skjermbildet nedenfor.

    ![Siden brukerparametere for elektronisk rapportering.](./media/GER-JoinDS-Parameters.PNG)

    Når disse parameterne er aktivert, genereres utførelsessporingen for hver utføring av den importerte ER-formatfilen. Ved hjelp av detaljer om generert utførelsessporing kan du analysere utførelsen av ER-format- og ER-modelltilordninger. Gå til siden [Spore utførelse av ER-format for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md) for flere detaljer om sporingsfunksjonen for ER-utførelse.

### <a name="review-er-model-mapping-part-1"></a>Gjennomgå ER-modelltilordning (del 1)

Se gjennom innstillingene for komponenten for ER-modelltilordning. Komponenten konfigureres for å få tilgang til informasjon om versjoner av ER-konfigurasjoner, detaljer om konfigurasjoner og konfigurasjonsleverandører uten bruk av datakilder av typen **Join**.

1. Velg konfigurasjonen **Tilordning for å lære JOIN-datakilder**.
2. Velg **Utforming** for å åpne listen over tilordninger.
3. Velg **Utforming** for å se gjennom tilordningensdetaljer.
4. Velg **Vis detaljer**.
5. I konfigurasjonstreet utvider du datamodellelementene **Set1** og **Set1.Details**:

    1. Bindingen **Details: Record list = Versions** angir at elementet **Set1.Details** er bundet til datakilden **Versions**, som returnerer poster i tabellen **ERSolutionVersionTable**. Hver post i denne tabellen representerer en enkelt versjon av en ER-konfigurasjon. Innholdet i denne tabellen vises i hurtigkategorien **Versjoner** på siden **Konfigurasjoner**.
    2. Bindingen **ConfigurationVersion: String = @.PublicVersionNumber** betyr at verdien av den offentlige versjonen av hver ER-konfigurasjonsversjon er tatt fra feltet **PublicVersionNumber** i tabellen **ERSolutionVersionTable** og plassert i elementet **ConfigurationVersion**.
    3. Bindingen **ConfigurationTitle: String = @.'>Relations'.Solution.Name** angir at navnet på en ER-konfigurasjon er tatt fra feltet **Name** i tabellen **ERSolutionTable** via mange-til-én-relasjonen (**>Relations**) mellom tabellene **ERSolutionVersionTable** og **ERSolutionTable**. Navn på ER-konfigurasjoner av gjeldende programforekomst vises i konfigurasjonstreet på siden **Konfigurasjoner**.
    4. Bindingen **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** betyr at navnet på konfigurasjonsleverandøren som eier gjeldende konfigurasjon, hentes fra feltet **Name** i tabellen **ERVendorTable**, via mange-til-én-realsjonen mellom tabellene **ERSolutionTable** og **ERVendorTable**. Navnene på ER-konfigurasjonsleverandørene vises i konfigurasjonstreet på siden **Konfigurasjoner** på sidehodet for hver konfigurasjon. Du finner hele listen med ER-konfigurasjonsleverandører på tabellsiden **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjonsleverandør**.

    ![Siden ER-utforming av modelltilordning, liste over datamodellelementer som er bundet.](./media/GER-JoinDS-Set1Review.PNG)

6. I konfigurasjonstreet utvider du datamodellelementet **Set1.Summary**:

    1. Bindingene **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** angir at elementet **Set1.Summary.VersionsNumber** er bundet til **VersionsNumber**-aggregasjonfeltet i **VersionsSummary**-datakilden av **GroupBy**-typen som ble konfigurert til å returnere antallet poster i tabellen **ERSolutionVersionTable** via datakilden **Versions**.

    ![Rediger parametersiden Grupper etter.](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. Lukk siden.

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a> Gjennomgå ER-modelltilordning (del 2)

Se gjennom innstillingene for komponenten for ER-modelltilordning. Komponenten konfigureres for å få tilgang til informasjon om versjoner av ER-konfigurasjoner, detaljer om konfigurasjoner og konfigurasjonsleverandører ved å bruke en datakilde av typen **Join**.

1. I konfigurasjonstreet utvider du datamodellelementene **Set2** og **Set2.Details**. Bindingen **Details: Record list = Details** angir at elementet **Set2.Details** er bundet til **Details**-datakilden som er konfigurert som datakilde av typen **Join**.

    ![Er-modelltilordningsutformingssiden som viser utvidede Set2:Record-datamodellelementer.](./media/GER-JoinDS-Set2Review.PNG)

    Datakilden for **Join** kan legges til ved å velge datakilden **Functions\Join**:

    ![Siden ER-utforming av modelltilordning, JOIN-datakildetype.](./media/GER-JoinDS-AddJoinDS.PNG)

2. Velg datakilden **Details**.
3. Velg **Rediger** i ruten **Datakilder**.
4. Velg **Rediger join**.
5. Velg **Vis detaljer**.

    ![Siden med JOIN-parametre for datakilde.](./media/GER-JoinDS-JoinDSEditor.PNG)

    Denne siden brukes til å utforme den påkrevde datakilden for **Join-type**. Under kjøring vil denne datakilden opprette én enkelt sammenføyet liste med poster fra datakildene i rutenettet **Sammenkoblet liste**. Sammenføyning av poster starter fra datakilden **ConfigurationProviders** som er i rutenettet som første (**Type**-kolonnen er tom for den). Poster med alle andre datakilder vil bli føyd sammen til poster av den overordnede datakilden basert på rekkefølgen i dette rutenettet. Alle Join-datakilder må konfigureres som en datakilde nestet under en måldatakilde (`1Versions`-datakilden er nestet under én `1Configurations`, datakilden `1Configurations` som er nestet under én **ConfigurationProviders**). Hver konfigurerte datakilde må inneholde betingelsene for Join-sammenkoblingen. I datakilden for denne bestemte **Join** er følgende Join-sammenkoblinger definert:

    - Hver post i datakilden **ConfigurationProviders** (henvises til i **ERVendorTable**-tabellen) er bare koblet sammen med poster av én **1Configurations** (henvises til i **ERSolutionTable**-tabell) som har samme verdi i feltene **SolutionVendor** og **RecId**. Den **indre join**-typen brukes for denne sammenføyningen samt følgende betingelser for samsvarende poster:

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Hver post i datakilden **1Configurations** (henvises til i **ERSolutionTable**-tabellen) er bare koblet til poster av én **1Configurations** (henvises til i **ERSolutionVersionTable**-tabellen) som har samme verdi i feltene **Solution** og **RecId**. Den **Indre join**-typen brukes for denne sammenføyningen samt følgende betingelser for samsvarende poster:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - **Utfør**-alternativet er konfigurert som **Spørring**, som betyr at denne join-datakilden utføres under kjøring på databasenivå som et direkte SQL-kall.

    Ved sammenkobling av poster i datakilder som representerer programtabeller, kan du angi join-vilkår ved å bruke andre felt enn de som beskriver eksisterende i AOT-relasjoner mellom disse tabellene. Denne sammenkoblingstypen kan også konfigureres til å utføres på databasenivå.

6. Lukk siden.
7. Velg **Avbryt**.
8. I konfigurasjonstreet utvider du datamodellelementet **Set2.Summary**:

    - Bindingen **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** angir at elementet **Set2.Summary.VersionsNumber** er bundet til **VersionsNumber**-aggregasjonfeltet i **DetailsSummary**-datakilden av **GroupBy**-typen som ble konfigurert til å returnere antallet sammenkoblede poster i **Details**-datakilden av typen **Join**.
    - Stedsalternativet **Utfør** er konfigurert som **Spørring**, som betyr at denne **GroupBy**-datakilden utføres under kjøring som et direkte SQL-kall på databasenivå. Denne virkemåten er mulig fordi basisdatakilden **Details** for typen **Join** er konfigurert som utført på databasenivå.

    ![Siden for GROUPBY-datakildeparametere.](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. Lukk siden.
10. Velg **Avbryt**.

### <a name="execute-er-format"></a><a name="executeERformat"></a> Utføre ER-format

1. Få tilgang til Finance eller RCS i den andre økten av webleseren med samme legitimasjon og firma som i den første økten.
2. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
3. Utvid konfigurasjonen **Modell for å lære JOIN-datakilder**.
4. Velg konfigurasjonen **Format for å lære JOIN-datakilder**.
5. Velg **Utforming**.
6. Velg **Vis detaljer**.
7. Velg **Tilordning**.
8. Velg **Vis/skjul**.

    Dette formatet er utformet for å fylle ut en generert tekstfil med en ny linje for hver versjon av en ER-konfigurasjon (**Versjon**-sekvens). Hver genererte linje inneholder navnet på en konfigurasjonsleverandør som eier den gjeldende konfigurasjonen, konfigurasjonsnavnet og konfigurasjonsversjonen atskilt med semikolon. Den siste linjen i den genererte filen vil inneholde antall oppdagede versjoner av ER-konfigurasjoner (**Sammendrag**-sekvens).

    ![Side med ER-formatutforming, kategorien Format.](./media/GER-JoinDS-FormatReview.PNG)

    Datakildene **Data** og **Sammendrag** brukes til å fylle ut konfigurasjonsversjonsdetaljer for den genererte filen:

    - Informasjon fra datamodellen **Set1** brukes når du velger **Nei** for datakilden **Velger** under kjøring på siden med brukerdialogboks når ER-format kjøres.
    - Informasjon fra datamodellen **Set2** brukes når du velger **Ja** for datakilden **Velger** under kjøring på siden med brukerdialogboks.

    ![Side med ER-formatutforming, kategorien Tilordning.](./media/GER-JoinDS-FormatMappingReview.PNG)

9. Velg **Kjør**.
10. Velg **Nei** på dialogbokssiden i feltet **Bruk JOIN-datakilder**.
11. Velg **OK**.
12. Se gjennom den genererte filen.

    ![Fil generert av elektronisk rapportparametere som ikke bruker JOIN-datakilde.](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>Analysere utførelsessporing i ER-format

1. I den første Finance- eller RCS-økten velger du **Utforming**.
2. Velg **Ytelsessporing**.
3. I rutenettet **Ytelsessporing** velger du den øverste oppføringen i den siste utførelsessporingen i et ER-format som brukte den gjeldende modelltilordningskomponenten.
4. Velg **OK**.

    Utførelsesstatistikken informerer deg om dupliserte kall til programtabeller:

    - **ERSolutionTable** er kalt så mange ganger som du har konfigurasjonsversjonsposter i **ERSolutionVersionTable** -tabellen, men antallet slike kall kan til tider bli redusert for å forbedre ytelsen.
    - **ERVendorTable** er kalt to ganger for hver konfigurasjonsversjonspost som ble oppdaget i tabellen **ERSolutionVersionTable**, men antallet slike kall kan imidlertid blir redusert.

    ![Utførelsesstatistikk på siden ER-utforming av modelltilordning.](./media/GER-JoinDS-Set1Run2.PNG)

5. Lukk siden.

### <a name="execute-er-format"></a>Utføre ER-format

1. Bytt til webleserkategorien med den andre økten av Finance eller RCS.
2. Velg **Kjør**.
3. Velg **Ja** på dialogbokssiden i feltet **Bruk JOIN-datakilder**.
4. Velg **OK**.
5. Se gjennom den genererte filen.

    ![Fil generert av elektronisk rapportparametere som bruker JOIN-datakilde.](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a> Analysere utførelsessporing i ER-format

1. I den første Finance- eller RCS-økten velger du **Utforming**.
2. Velg **Ytelsessporing**.
3. I rutenettet **Ytelsessporing** velger du den øverste oppføringen som representerer den siste utførelsessporingen i et ER-format som brukte den gjeldende modelltilordningskomponenten.
4. Velg **OK**.

    Statistikker informerer deg om følgende:

    - Programdatabasen har blitt kalt én gang for å hente poster fra tabellene **ERVendorTable**, **ERSolutionTable** og **ERSolutionVersionTable** for å få tilgang til de obligatoriske feltene.

    ![Utførelsesstatistikkdetaljer på siden ER-utforming av modelltilordning.](./media/GER-JoinDS-Set2Run2.PNG)

    - Programdatabasen har blitt kalt én gang for å beregne antallet konfigurasjonsversjoner ved hjelp av sammenføyninger som ble konfigurert i datakilden **Detaljer**.

    ![Siden ER-utforming av modelltilordning som viser programdatabaseanrop.](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a>Begrensninger

Som du kan se fra eksemplet i denne artikkelen, kan **JOIN**-datakilden bygges fra flere datakilder som beskriver de individuelle datasettene for postene som til slutt må sammenføyes. Du kan konfigurere disse datakildene ved å bruke den innebygde ER-funksjonen [FILTER](er-functions-list-filter.md). Når du konfigurerer datakilden slik at den kalles utenfor **JOIN**-datakilden, kan du bruke firmaområder som en del av betingelsen for datavalg. Den første implementeringen av **JOIN**-datakilden støtter ikke datakilder av denne typen. Når du for eksempel kaller en [FILTER](er-functions-list-filter.md)-basert datakilde innenfor omfanget av utføringen av en **JOIN**-datakilde, oppstår det et unntak hvis den kalte datakilden inneholder firmaområder som en del av betingelsen for datavalg.

I Microsoft Dynamics 365 Finance versjon 10.0.12 (august 2020) kan du bruke firmaområder som en del av vilkåret for datavalget i [FILTER](er-functions-list-filter.md)-baserte datakilder som kalles i omfanget av utføringen for en **JOIN**-datakilde. På grunn av begrensningene i programmets [spørrings](../dev-ref/xpp-library-objects.md#query-object-model)-verktøy støttes bare firmaområdene bare for den første datakilden for en **JOIN**-datakilde.

### <a name="example"></a>Eksempel

Du må for eksempel opprette ett enkelt kall til programdatabasen for å hente listen over utenlandske handelstransaksjoner for flere firmaer, og detaljene for lagervaren som det refereres til i disse transaksjonene.

I dette tilfellet konfigurerer du følgende artefakter i ER-modelltilordningen din:

- **Intrastat**-rotdatakilden som representerer **Intrastat**-tabellen.
- **Elementer**-rotdatakilden som representerer **InventTable**-tabellen.
- **Firmaer**-rotdatakilden som returnerer listen over firmaer (**DEMF** og **GBSI** i dette eksemplet) der transaksjoner må gis tilgang. Firmakoden er tilgjengelig fra feltet **Companies.Code**.
- **X1**-rotdatakilde som har uttrykket `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))`. Som en del av betingelsen for datautvalg inneholder dette uttrykket definisjonen for firmaområder `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)`.
- **X2**-datakilde som et nestet element i **X1**-datakilden. Den inneholder uttrykket `FILTER (Items, Items.ItemId = X1.ItemId)`.

Til slutt kan du konfigurere en **JOIN**-datakilde, der **X1** er den første datakilden og **X2** er den andre datakilden. Du kan angi **Spørring** som **Utfør**-alternativet for å tvinge ER til å kjøre denne datakilden på databasenivået som et direkte SQL-kall.

Når den konfigurerte datakilden kjøres mens ER-kjøringen [spores](trace-execution-er-troubleshoot-perf.md), vises følgende setning i ER-modelltilordningsutformingen som en del av ER-sporingsytelsen.

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> Det oppstår en feil hvis en **JOIN**-datakilde som er konfigurert slik at den inneholder datautvalgsbetingelser som har firmaområder for flere datakilder i den utførte **JOIN**-datakilden.

## <a name="additional-resources"></a>Tilleggsressurser

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Spore utførelse av ER-format for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
