---
title: Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer
description: Dette emnet inneholder informasjon om hvordan du bruker funksjonen ytelsessporing i elektronisk rapportering (ER) for å feilsøke ytelsesproblemer.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: a1a6b3711e58964ff266d84c75e79f741218ee23
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561154"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>Spore utførelse av ER-formater for å feilsøke ytelsesproblemer

[!include[banner](../includes/banner.md)]

Som en del av prosessen med å utforme konfigurasjoner for elektronisk rapportering (ER) for å generere elektroniske dokumenter, definerer du metoden som brukes til å hente data ut av programmet, og angir den i utdataene som genereres. Funksjonen ytelsessporing i ER bidrar til å redusere tiden og kostnadene betydelig ved innsamling av detaljer om ER-formatutførelsen og bruke dem til å feilsøke ytelsesproblemer. Denne opplæringen inneholder retningslinjer om hvordan du kan utføre ytelsessporinger for utførte ER-formater, og hvordan du bruker informasjonen fra disse sporingene for å forbedre ytelsen.

## <a name="prerequisites"></a>Forutsetninger

Hvis du vil fullføre eksemplene i denne opplæringen, må du ha følgende tilgang:

- Tilgang til én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

- Tilgang til forekomsten av Regulatory Configuration Service (RCS) som er klargjort for samme leietaker som programmet, for én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

Du må også laste ned og lagre følgende filer lokalt.

| Fil                                  | Innhold                               |
|---------------------------------------|---------------------------------------|
| Ytelsessporingsmodell.versjon.1     | [Eksempel ER-datamodellkonfigurasjon](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| Ytelsessporingsmetadata.versjon.1  | [Eksempel ER-metadatakonfigurasjon](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| Ytelsessporingstilordning.versjon.1.1 | [Eksempel ER-modelltilordningskonfigurasjon](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Ytelsessporingsformat.versjon.1.1  | [Eksempel ER-formatkonfigurasjon](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a>Konfigurere ER-parametere

Hver ER-ytelsessporing som genereres i programmet, lagres som et vedlegg til utførelsesloggposten. Dokumentbehandlingsrammeverket (DM) brukes til å administrere disse vedleggene. Du må konfigurere ER-parameterne på forhånd for å angi DM-dokumenttypen som skal brukes til å knytte ytelsesspor. I arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**. På siden **Parametere for elektronisk rapportering** i kategorien **Vedlegg** på siden **Andre** velger du deretter DM-dokumenttypen som skal brukes for ytelsessporinger.

![Siden Parametere for elektronisk rapportering](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

For å være tilgjengelig i **Andre**-oppslagsfeltet må en DM-dokumenttype konfigureres på følgende måte på siden **Dokumenttyper** (**Organisasjonsstyring \> Dokumentstyring \> Dokumenttyper**):

- **Klasse:** Tilknytt fil
- **Gruppe:** Fil

![Siden Dokumenttyper](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Den valgte dokumenttypen må være tilgjengelig i alle firmaer av gjeldende forekomst, fordi DM-vedlegg er firmaspesifikke.

### <a name="configure-rcs-parameters"></a>Konfigurere RCS-parametere

ER-ytelsessporinger som genereres, importeres til RCS for analyse ved hjelp av ER-formatdesigneren og ER-tilordningsdesigneren. Fordi ER-ytelsesspor lagres som vedlegg i utførelsesloggposten som er relatert til ER-formatet, må du konfigurere RCS-parametere på forhånd, for å angi DM-dokumenttypen som skal brukes for å knytte til ytelsessporinger. For RCS-forekomsten som er klargjort for ditt firma, går du til **Elektronisk rapportering** og velger **Parametere for elektronisk rapportering**. På siden **Parametere for elektronisk rapportering** i kategorien **Vedlegg** på siden **Andre** velger du deretter DM-dokumenttypen som skal brukes for ytelsessporinger.

![Siden Parametere for elektronisk rapportering i RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

For å være tilgjengelig i **Andre**-oppslagsfeltet må en DM-dokumenttype konfigureres på følgende måte på siden **Dokumenttyper** (**Organisasjonsstyring \> Dokumentstyring \> Dokumenttyper**):

- **Klasse:** Tilknytt fil
- **Gruppe:** Fil

## <a name="design-an-er-solution"></a>Utforme en ER-løsning

Anta at du har begynt å utforme en ny ER-løsning for å generere en ny rapport som presenterer leverandørtransaksjoner. For øyeblikket kan du finne transaksjonene for en valgt leverandør på siden **Leverandørtransaksjoner** (gå til **Leverandører \> Leverandører \> Alle leverandør**, velg en leverandør, og deretter, i handlingsruten i kategorien **Leverandør** i gruppen **Transaksjoner**, velger du **Transaksjoner**). Du vil imidlertid ha alle leverandørtransaksjoner samtidig i ett elektronisk dokument i XML-format. Denne løsningen vil bestå av flere ER-konfigurasjoner som inneholder den nødvendige datamodellen, metadataene, modelltilordningen og formatkomponentene.

1. Logg deg på forekomsten av RCS som er klargjort for firmaet ditt.
2. I denne opplæringen skal du opprette og endre konfigurasjoner for eksempelfirmaet **Litware, Inc.** Kontroller derfor at denne konfigurasjonsleverandøren er lagt til RCS og valgt som aktiv. Hvis du ha instruksjoner, se fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. I arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.
4. På siden **Konfigurasjoner** importerer du ER-konfigurasjoner som du lastet ned som en forutsetning til RCS, i denne rekkefølgen: datamodell, metadata, modelltilordning, format. For hver konfigurasjon følger du disse trinnene:

    1. På siden Handling velger du **Exchange \> Last fra XML-fil**.
    2. Velg **Bla gjennom** for å velge den riktige filen for den nødvendige ER-konfigurasjonen i XML-format.
    3. Velg **OK**.

    ![Siden Konfigurasjoner i RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>Kjør ER-løsningen for å spore kjøring

Anta at du er ferdig med å utforme den første versjonen av ER-løsningen. Nå skal du teste forekomsten og analysere kjøringsytelsen.

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a>Importere en ER-konfigurasjon fra RCS til Finance and Operations

1. Logg på programforekomsten.
2. I denne opplæringen skal du importere konfigurasjonene fra RCS-forekomsten (der du utformer ER-komponentene) i forekomsten (der du tester og til slutt bruker dem). Du må derfor kontrollere at alle de nødvendige artefaktene er forberedt. Hvis du vil ha instruksjoner, kan du se fremgangsmåten [Importere ER-konfigurasjoner (Electronic Reporting) fra Regulatory Configuration Service (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).
3. Følg disse trinnene for å importere konfigurasjonene fra RCS til programmet:

    1. I arbeidsområdet **Elektronisk rapportering**, på flisen for konfigurasjonsleverandøren **Litware, Inc.**, velger du **Repositorier**.
    2. På **Konfigurasjonsrepositorium**-siden velger du repositoriet for **RCS**-typen, og deretter velger du **Åpne**.
    3. I hurtigfanen **Konfigurasjoner** velger du **Ytelsessporingsformat**- konfigurasjonen.
    4. I **Versjoner**-hurtigkategorien velger du versjon **1.1** av den valgte konfigurasjonen, og deretter velger du **Importer**.

    ![Konfigurasjonsrepositorium-side](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

De tilsvarende versjonene av konfigurasjonene for datamodell og modelltilordning importeres automatisk som forutsetninger for den importerte ER-formatkonfigurasjonen.

### <a name="turn-on-the-er-performance-trace"></a>Aktivere ER-ytelsessporing

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. Følg disse trinnene i dialogboksen **Brukerparametere** i delen **Kjøringssporing**:

    1. I feltet **Sporingsformat for kjøring** velger du **Feilsøk sporingsformat** for å begynne å samle inn detaljer for kjøringen av ER-format. Når denne verdien er valgt, vil ytelsessporingen samle inn informasjon om tiden som brukes på følgende handlinger:

        - Kjøre hver datakilde i modelltilordningen som kalles for å hente data
        - Behandler hver formatvare for å angi data i utdataene som genereres

        Du bruker feltet **Sporingsformat for kjøring** til å angi formatet på den genererte ytelsessporingen som kjøringsdetaljene er lagret i for ER-format og tilordningselementer. Ved å velge **Feilsøk sporingsformat** som verdi kan du analysere innholdet i sporingen i ER-operasjonsutforming og se ER-formatet eller tilordningselementene som er nevnt i sporingen.

    2. Angi følgende alternativer til **Ja** for å samle inn bestemte detaljer for utførelsen av ER-modelltilordningen og ER-formatkomponentene:

        - **Samle inn spørringsstatistikk** – Når dette alternativet er aktivert, vil ytelsessporingen samle inn følgende informasjon:

            - Antall databasekall som er utført av datakilder
            - Antall dupliserte kall til databasen
            - Detaljer for SQL-setningene som ble brukt til å opprette databasekall

        - **SSpor tilgang for hurtigbufring** – Når dette alternativet er aktivert, samler ytelsessporingsinformasjon inn informasjon om ER-modelltilordningens hurtigbufferbruk.
        - **Spor datatilgang** – Når dette alternativet er aktivert, samler ytelsessporingeninformasjon inn informajson om antall kall til databasen for utførte datakilder av typen postliste.
        - **Sporingslisteopplisting** – Når dette alternativet er aktivert, samler ytelsessporingeninformasjon inn informajson om antall poster som forespørres fra datakilder av typen postliste.

    > [!NOTE]
    > Parameterne i dialogboksen **Brukerparametere** er spesifikke for brukeren og det gjeldende firmaet.

    ![Dialogboksen Brukerparametere](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a>Kjør ER-formatet

1. Velg **DEMF**-firmaet.
2. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
3. På siden **Konfigurasjoner** i konfigurasjonstreet, velger du elementet **Ytelsessporingsformat**.
4. Velg **Kjør** i handlingsruten.

Legg merke til at filen som genereres, presenterer informasjon om 265 transaksjoner for seks leverandører.

## <a name="review-the-execution-trace"></a>Se gjennom utførelsessporing

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a>Eksportere den genererte sporingen fra programmet

Ytelsessporinger kobles fra kilde-ER-formatet og kan serialiseres til en ekstern zip-fil.

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Feilsøkingslogger for konfigurasjon**.
2. På siden **Kjøringslogger for elektronisk rapportering**, i venstre rute i feltet **Konfigurasjonsnavn**, velger du **Ytelsessporingsformat** for å finne loggpostene som er generert ved å utføre **Ytelsessporingsformat**.
3. Velg **Vedlegg**-knappen (bindersikonet) i øvre høyre hjørne på siden, eller trykk på **Ctrl+Skift+A**.

    ![Vedlegg-knappen på siden Kjøringslogger for elektronisk rapportering](./media/GER-PerfTrace-GER-DebugLog.png)

4. På siden **Vedlegg for Kjøringslogger for elektronisk rapportering** velger du **Åpne** for å hente ytelsessporing som en zip-fil og lagre den lokalt.

    ![Vedlegg for Kjøringslogger for elektronisk rapportering](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Sporingen som genereres, har en referanse til kilde-ER-rapporten via en unik rapport-ID bare i **GUID**-format. Versjonsnummereringen for formatet vurderes ikke.

Legg merke til at tilknytningen mellom ytelsessporingen som er generert for det utførte ER-formatet og ER-modelltilordningen, er basert på rotbeskrivelsen som ble brukt og den felles datamodellen. Versjonsnummereringen for formatet og modelltilordningen vurderes ikke. Innstillingen til **Standard for modelltilordning**-flagget for modelltilordningen blir heller ikke vurdert.

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a>Importere den genererte sporingen til RCS

1. I RCS, i arbeidsområdet **Elektronisk rapportering**, velger du flisen **Rapporteringskonfigurasjoner**.
2. På siden **Konfigurasjoner**, i konfigurasjonstreet, utvider du elementet **Ytelsessporingsmodell**, og velg elementet **Ytelsessporingsformat**.
3. Velg **Utforming** i handlingsruten.
4. På siden **Formatutforming**, i handlingsruten, velger du **Ytelsessporing**.
5. I dialogboksen **Resultatinnstillinger for ytelsessporing** velg **Importer ytelsessporing**.
6. Velg **Bla gjennom** for å velge ZIP-filen du eksporterte tidligere.
7. Velg **OK**.

    ![Dialogboksen Resultatinnstillinger for ytelsessporing i RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Bruke ytelsessporing for analyse i RCS – Formatutførelse

1. Velg **Vis/Skjul** på **Formatutforming**-siden i RCS for å utvide innholdet for alle formatvarer.

    Legg merke til at tilleggsinformasjon vises for noen varer i gjeldende format:

    - Den faktiske tiden som ble brukt på å legge inn data i de genererte utdataene ved hjelp av formatvaren
    - Den samme tiden som prosent av den totale tiden som ble brukt til å generere hele utdataene

    ![Formatutformingsside i RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Lukk siden **Formatutforming**.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a>Bruke ytelsessporing for analyse i RCS – modelltilordning

1. I RCS, på siden **Konfigurasjoner** i konfigurasjonstreet, velger du elementet **Ytelsessporingstilordning**.
2. Velg **Utforming** i handlingsruten.
3. Velg **Utforming**.
4. På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.
5. Velg sporingen du importerte tidligere.
6. Velg **OK**.

Legg merke til at ny informasjon blir tilgjengelig for noen datakildeelementer av gjeldende modelltilordning:

- Den faktiske tiden som ble brukt til å hente data ved hjelp av datakilden
- Den samme tiden som prosent av den totale tiden som ble brukt til å kjøre hele modelltilordningen

Legg merke til at ER informerer deg om at gjeldende modelltilordning dupliserer databaseforespørsler når VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum-datakilden kjøres. Denne dupliseringen forekommer fordi listen over leverandørtransaksjoner kalles to ganger for hver leverandørpost som gjentas:

- Det blir laget ett kall for å angi detaljer for hver transaksjon i datamodellen, basert på konfigurerte bindinger.
- Det blir laget ett kall for å angi det beregnede antallet transaksjoner per leverandør i datamodellen.

![Melding om dupliserte databaseforespørsler på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Verdien **\[Q:530\]** angir at VendTrans-tabellen ble kalt 530 ganger for å returnere en post fra denne tabellen til VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum-datakilden. Verdien **\[530\]** angir at datakilden VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum ble kalt 530 ganger for å returnere en post fra den datakilden og angi detaljer fra den i datamodellen.

Vi anbefaler at du bruker hurtigbufring for datakilden VendTable/\<Relasjoner/VendTrans.VendTable\_AccountNum for å redusere antallet kall som gjøres for å hente detaljene for 265 transaksjoner og bidra til å forbedre ytelsen til modelltilordningen.

Det kan også være nyttig å redusere antall kall som gjøres til datakilden for LedgerTransTypeList-datakilden. Denne datakilden brukes til å knytte hver verdi for **LedgerTransType**-opplistingen til etiketten. Ved hjelp av denne datakilden kan du finne en passende etikett og angi den i datamodellen for hver leverandørtransaksjon. Gjeldende antall kall til denne datakilden (9027) er ganske høy for 265 transaksjoner.

![Siden Modelltilordningsutforming i RCS som viser 9027 kall til datakilden](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Forbedre modelltilordningen basert på informasjon fra kjøringssporingen

### <a name="modify-the-logic-of-the-model-mapping"></a>Endre logikken til modelltilordningen

1. Følg denne fremgangsmåten for å bruke bufring til å forhindre dupliserte kall til databasen:

    1. I RCS-ruten, på siden **Modelltilordningsutforming** i ruten **Datakilder**, velger du **VendTable**-elementet.
    2. Velg **Hurtigbuffer**.
    3. Utvid elementet **VendTable**, utvid listen med en-til-mange-relasjoner for datakilden VendTable (**\<Relasjoner**-elementet), og velg elementet **VendTrans.VendTable\_AccountNum**.
    4. Velg **Hurtigbuffer**.

    ![Hurtigbufre installasjonen for å hindre dupliserte kall](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Følg disse trinnene for å hente LedgerTransTypeList-datakilden til området for VendTable-datakilden:

    1. I ruten **Datakildetyper** utvider du **Funksjoner**-elementet og velger **Beregnet felt**-elementet.
    2. I **Datakilder**-ruten velger du **VendTable**-elementet.
    3. Velg **Legg til**.
    4. I feltet **Navn** angir du **\$TransType**.
    5. Velg **Rediger formel**.
    6. I feltet **Formel** angir du **LedgerTransTypeList**.
    7. Velg **Lagre**.
    8. Lukk siden **Formelredigering**.
    9. Klikk **OK**.

3. Følg disse trinnene for å utføre bufring av feltet **\$TransType**:

    1. Velg elementet **LedgerTransTypeList**.
    2. Velg **Hurtigbuffer**.
    3. Velg **VendTable.\$TransType**-elementet.
    4. Velg **Hurtigbuffer**.

    ![Bufre oppsett av $TransType-feltet](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Følg disse trinnene for å endre feltet **\$TransTypeRecord**, slik at det begynner å bruke det hurtigbufrede feltet **\$TransType**:

    1. I **Datakilder**-ruten utvider du **VendTable**-elementet, utvider **\<Relasjoner**-elementet, utvider elementet **VendTrans.VendTable\_AccountNum** og velger **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**-elementet.
    2. Velg **Rediger**.
    3. Velg **Rediger formel**.
    4. I **Formel**-feltet finner du følgende uttrykk:

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. I **Formel**-feltet angir du følgende uttrykk:

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Velg **Lagre**.
    7. Lukk siden **Formelredigering**.
    8. Velg **OK**.

5. Velg **Lagre**.
6. Lukk siden **Modelltilordningsutforming**.
7. Lukk siden **Modelltilordninger**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Fullføre den endrede versjonen av ER-modelltilordningen

1. I RCS, på siden **Konfigurasjoner** i hurtigfanen **Versjoner**, velger du versjon **1.2** av konfigurasjonen **Ytelsessporingstilordning**.
2. Velg **Endre status**.
3. Velg **Fullfør**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>Importere den endrede ER-modelltilordningskonfigurasjonen fra RCS til programmet

Gjenta trinnene i delen [Importere en ER-konfigurasjon fra RCS til Finance and Operations](#import-configuration) tidligere i dette emnet for å importere versjon 1.2 av konfigurasjonen **Ytelsessporingstilordning**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Kjøre den endrede ER-løsningen for å spore kjøring

### <a name="run-the-er-format"></a>Kjøre ER-formatet

Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.

## <a name="work-with-the-execution-trace"></a>Arbeide med utføringsporingen

### <a name="export-the-generated-trace-from-the-application"></a>Eksportere den genererte sporingen fra programmet

Gjenta trinnene i delen [Eksportere den genererte sporingen fra programmet](#export-trace) tidligere i dette emnet for å lagre en ny ytelsessporing lokalt.

### <a name="import-the-generated-trace-into-rcs"></a>Importere den genererte sporingen til RCS

Gjenta trinnene i delen [Importere den genererte sporingen til RCS](#import-trace) tidligere i dette emnet for å importere den nye ytelsessporingen til RCS.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Bruke ytelsessporing for analyse i RCS – modelltilordning

Gjenta trinnene i delen [Bruke ytelsessporing for analyse i RCS – modelltilordning](#use-trace) tidligere i dette emnet for å analysere den siste ytelsessporingen.

Legg merke til at justeringene du har gjort i modelltilordningen, har eliminert duplikate spørringer til databasen. Antall kall til databasetabeller og datakilder for denne modelltilordningen er også redusert. Derfor har ytelsen til hele ER-løsningen blitt forbedret.

![Sporingsinformasjon for VendTable-datakilden på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

I sporingsinformasjonen angir verdien **\[12\]** for VendTable-datakilden at denne datakilden ble kalt 12 ganger. Verdien **\[Q:6\]** angir at seks samtaler ble oversatt til databasekall til tabellen VendTable. Verdien **\[C:6\]** angir at postene som ble hentet fra databasen, ble bufret, og at seks andre kall ble behandlet ved hjelp av hurtigbufferen.

Legg merke til at antall kall til LedgerTransTypeList-datakilden er redusert fra 9027 til 240.

![Sporingsinformasjon for LedgerTransTypeList-datakilden på siden Modelltilordningsutforming i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>Se gjennom utførelsessporingen i programmet

I tillegg til RCS kan enkelte versjoner tilby funksjoner for en ER-rammeverkutformingsopplevelse. Disse versjonene har alternativet **Aktiver utformingsmodus** som kan aktiveres. Du finner dette alternativet i kategorien **Generelt** på siden **Parametere for elektronisk rapportering**, som du kan åpne fra arbeidsområdet **Elektronisk rapportering**.

![Alternativet Aktiver utformingsmodus på siden Parametere for elektronisk rapportering](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Hvis du bruker en av disse versjonene, kan du analysere detaljene for genererte ytelsessporinger direkte i programmet. Du trenger ikke å eksportere dem fra programmet og importere dem til RCS.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Se gjennom utførelsessporingen ved hjelp av eksterne verktøy

### <a name="configure-user-parameters"></a>Konfigurere brukerparametere

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. I dialogboksen **Brukerparametere** i delen **Kjøringssporing** i feltet **Sporingsformat for kjøring** velger du **PerfView XML**.

### <a name="run-the-er-format"></a>Kjøre ER-formatet

Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.

Legg merke til at nettleseren tilbyr en zip-fil for nedlasting. Denne filen inneholder ytelsessporingen i PerfView-format. Du kan deretter bruke verktøyet for PerfView-ytelsesanalyse til å analysere detaljene i ER-formatkjøringen.

![Informasjon om ytelsessporing i PerfView-format](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Bruke eksterne verktøy til å se gjennom en utførelsessporing som inneholder databasespørringer

På grunn av forbedringer i ER-rammeverket gir ytelsessporingen som genereres i PerfView-formatet, nå flere detaljer om ER-formatutførelsen. I Microsoft Dynamics 365 for Finance and Operations versjon 10.0.4 (juli 2019) kan denne sporingen også inneholde detaljer om utførte SQL-spørringer til programdatabasen.

### <a name="configure-user-parameters"></a>Konfigurere brukerparametere

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. I delen **Kjøringssporing** i dialogboksen **Brukerparametere** angir du følgende parametere:

    - I feltet **Sporingsformat for kjøring** velger du **PerfView XML**.
    - Sett alternativet **Samle inn spørringsstatistikk** til **Ja**.
    - Sett alternativet **Spor spørring** til **Ja**.

    ![Delen Utføringssporing, dialogboksen Brukerparametere](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>Kjøre ER-formatet

Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i dette emnet for å generere en ny ytelsessporing.

Legg merke til at nettleseren tilbyr en zip-fil for nedlasting. Denne filen inneholder ytelsessporingen i PerfView-format. Du kan deretter bruke verktøyet for PerfView-ytelsesanalyse til å analysere detaljene i ER-formatkjøringen. Denne sporingen inneholder nå detaljene for tilgang til SQL-database under utførelsen av ER-formatet.

![Sporingsinformasjon for det utførte ER-formatet i PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Forbedre ytelse for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]