---
title: Forbedre ytelsen til ER-løsninger ved å redusere antall tabellfelt som hentes ved kjøretid
description: Denne artikkelen forklarer hvordan du kan bidra til å forbedre ytelsen ved å redusere antall tabellfelt som hentes ved kjøretid.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: eb76c415da87d421b8135a93b84f4e905f01e70d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847458"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Forbedre ytelsen til ER-løsninger ved å redusere antall tabellfelt som hentes ved kjøretid

[!include[banner](../includes/banner.md)]

Du kan utforme [Elektronisk rapportering](general-electronic-reporting.md) (ER) [formater](er-overview-components.md#format-components-for-outgoing-electronic-documents) for å generere utgående dokumenter i forskjellige formater. Når et dokument genereres, kaller et ER-format datakilder som ble konfigurert i en tilsvarende ER-[modelltilordning](er-overview-components.md#model-mapping-component). Hvis du vil konfigurere tilgang til programtabeller, spørringer eller enheter for henting av poster, kan du bruke ER-datakilder av typen *Tabellposter*. Som standard henter en datakilde for *Tabellpost*-typen verdiene til alle felt i de ønskede postene. Du kan imidlertid konfigurere denne typen datakilde, slik at den bare henter feltverdiene som kreves for å kjøre ER-formatet. Denne konfigurasjonen bidrar til å redusere minneforbruket til applikasjonsserveren som utfører datahenting og ytterligere postbufring.

Hvis du vil lære mer om hvordan du begrenser listen over hentede felt for datakilder av *Tabellposter*-typen, kan du fullføre eksemplet i denne artikkelen.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Eksempel: Reduser antall tabellfelt som hentes ved kjøretid

Følgende fremgangsmåter viser hvordan en bruker i rollen som Systemansvarlig eller Utvikler av elektronisk rapportering kan konfigurere en ER-modelltilordning slik at den bare henter feltene som kreves for å kjøre ER-formatet, for å redusere forbruket av programserverminne.

Disse prosedyrene kan gjennomføres i firmaet **USMF** i Microsoft Dynamics 365 Finance. Ingen koding er nødvendig.

For å fullføre dette eksempelet må du ha tilgang til **USMF**-selskapet for en av følgende roller:

- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

I dette eksemplet skal du bruke ER-[konfigurasjonene](general-electronic-reporting.md#Configuration) som finnes for eksempelfirmaet **Litware, Inc**. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet **Litware, Inc.** (`http://www.litware.com`) er oppført for ER-rammeverket og at det er merket som **Aktiv**. Hvis denne konfigurasjonsleverandøren ikke er oppført, eller hvis den ikke er merket som **Aktiv**, følger du trinnene i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>Konfigurere ER-rammeverket

Følg trinnene i [Konfigurere ER-rammeverket](er-quick-start2-customize-report.md#ConfigureFramework) for å konfigurere minimumssettet med ER-parametere. Du må fullføre denne konfigurasjonen før du begynner å bruke ER-rammeverket til å endre datakiler for den angitte ER-løsning.

### <a name="import-the-sample-er-configurations"></a>Importere ER-eksempelkonfigurasjonene

Hvis du ikke har fullført eksemplet i artikkelen [Utforme en ny ER-løsning for å skrive ut et egendefinert rapport](er-quick-start1-new-solution.md), kan du laste ned og lagre XML-filene lokalt for følgende konfigurasjoner av ER-løsningen som tilbys.

| Innholdsbeskrivelse            | Filnavn |
|--------------------------------|-----------|
| ER-datamodellkonfigurasjon    | [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| Konfigurasjon for ER-modellkartlegging | [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER-formatkonfigurasjon        | [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Følg deretter denne fremgangsmåten for å laste opp konfigurasjonene av angitt ER-løsning i Finance-forekomsten.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. Velg **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden importerer du ER-datamodellkonfigurasjonen.

    1. Velg **Veksle**, og velg deretter **Last inn fra XML-fil**.
    2. Velg **Bla gjennom**, og finn og velg filen **Questionnaires model.version.1.xml** og velg **OK**.

4. Importer konfigurasjonen for ER-modelltilordning.

    1. Velg **Veksle**, og velg deretter **Last inn fra XML-fil**.
    2. Velg **Bla gjennom**, og finn og velg filen **Questionnaires mapping.version.1.1.xml**, og velg deretter **OK**.

5. Importer ER-formatkonfigurasjonen.

    1. Velg **Veksle**, og velg deretter **Last inn fra XML-fil**.
    2. Velg **Bla gjennom**, og finn og velg filen **Questionnaires format.1.1.xml**, og velg deretter **OK**.

6. Utvid **Spørreskjemamodell** i konfigurasjonstreet.
7. Gjennomgå listen over importerte ER-konfigurasjoner i konfigurasjonstreet.

    ![Se gjennom listen over importerte ER-konfigurasjoner på Konfigurasjoner-siden.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Gjennomgå den angitte ER-modelltilordningen

1. Velg **Spørreskjematilordning** på siden **Konfigurasjoner**.
2. Velg **Utforming** i handlingsruten.
3. Velg **Utforming** på siden **Tilordning av modell til datakilde**.
4. På siden **Utforming av modelltilordning**, i handlingsruten, velger du **Gruppevisning** for å aktivere **Gruppe**-visningen.
5. I **Datamodell**-ruten utvider du **Spørreskjema**.

    Legg merke til at **Spørreskjema**-datakilden er konfigurert til å få tilgang til programtabellen `KMCollection`.

6. I ruten **Datakilder** utvider du **Tabellposter** \> **Spørreskjema** \> **Felter**.

    Legg merke til hvor mange felt fra programtabellen `KMCollection` som vises av **Spørreskjema**-datakilden for *Tabellposter*-typen.

    ![Gå gjennom den angitte modelltilordningen på utformingssiden for Modelltilordning når Gruppevisning er aktivert.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Velg **Gruppevisning** på nytt i handlingsruten for å slå av **Gruppe**-visning, og velg deretter **Vis alle** \> **Vis bare tilordnet**.

    Legg merke til at noen få felt i søknadstabellen `KMCollection` brukes til å fylle ut **Spørreskjema**-postlisten i ER-datamodellen:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Gå gjennom den angitte modelltilordningen på utformingssiden for Modelltilordning når Gruppevisning er deaktivert.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>Aktivere ER-ytelsessporing

Følg trinnene i [Aktivere ER-ytelsessporing](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) for å angi ER-brukerparameterne som aktiverer utføring av ER-komponenter som skal spores.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Kjør det angitte ER-formatet ved å bruke den angitte modelltilordningen

Følg trinnene i [Kjør et designet format fra ER](er-quick-start1-new-solution.md#RunFormatFromER) for å kjøre det angitte ER-formatet for et enkelt spørreskjema fra **Konfigurasjoner**-siden.

### <a name="review-the-execution-trace-of-the-first-run"></a>Se gjennom utførelsessporingen for den første kjøringen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering \> Konfigurasjoner**.
2. På siden **Konfigurasjoner** utvider du **Spørreskjemamodell** og velger **Spørreskjematilordning**.

    > [!NOTE]
    > Detaljene i hurtigkategorien **Versjoner** angir at du har valgt utkastversjonen for konfigurasjonen **Spørreskjematilordning**. Derfor kan du endre innholdet i denne modelltilordningen.

3. Velg **Utforming** i handlingsruten.
4. Velg **Utforming** på siden **Tilordning av modell til datakilde**.
5. På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.
6. I dialogboksen **Innstillinger for ytelsessporingsresultat** velger du sporingen som ble generert under den siste formatkjøringen.

    ![Velge sporet i dialogboksen Innstillinger for ytelsessporingsresultat.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Velg **OK**. 
8. I hurtigkategorien **Detaljer** filtrerer du **Spørreskjema**-banen som peker til datakilden **Spørreskjema**.
9. Gå gjennom detaljene i databasespørringen som ble generert da **Spørreskjema**-datakilden ble kalt.

    Legg merke til at alle feltene i programtabellen `KMCollection` ble hentet ved kjøretid da **Spørreskjema**-datakilden ble kalt.

    ![Ser gjennom detaljene i databasespørringen på utformingssiden for modelltilordning.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Endre den angitte ER-modelltilordningen

1. På siden **Modelltilordningsutforming** i ruten **Datakilder**, velger du **Spørreskjema**-datakilden.
2. I **Datakilder**-ruten velger du **Rediger**.
3. I dialogboksen **Datakildeegenskaper** velger du **Velg felt** for å angi listen over felt for den refererte `KMCollection` -programtabellen som hentes ved kjøretid når den redigerbare **Spørreskjema**-datakilden kalles.

    ![Valg av Velg felt i dialogboksen Datakildeegenskaper for å starte konfigurasjon av listen over felt som må hentes fra programtabellen ved å bruke den redigerbare datakilden.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Velg **Autofyll** på siden **Velg felt**.

    Listen **Velg felt** fylles automatisk ut, basert på forhåndskonfigurerte artefakter av modelltilordningen. Alle felt og relasjoner til den refererte tabellen som er nevnt i en hvilken som helst binding, formel eller datakilde for modelltilordningen, blir lagt til i listen.

    ![Konfigurer listen over felt som skal hentes fra programtabellen på siden Velg felt.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Velg **Lagre**, og lukk deretter siden **Velg felt**.
6. Velg **OK** for å lagre endringene du har gjort i innstillingene for datakilden.
7. Velg **Vis alle** i handlingsruten.

    Legg merke til at datakilden for **Spørreskjema** nå viser teksten **\<Fields are filtered\>**. Denne teksten angir at datakilden er konfigurert til å hente et begrenset antall felt fra den refererte programtabellen.

    ![Se gjennom den oppdaterte modelltilordningen på siden Utforming av modelltilordning.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Velg **Lagre** for å lagre endringene du har gjort i innstillingene for redigerbar modelltilordning.

    > [!NOTE]
    > Ved kjøretid analyserer ER de tilføyde relasjonene og legger til alle felt som brukes i dem i databasespørringen, selv om disse feltene ikke er uttrykkelig lagt til i listen over hentede felt på utformingstidsprogrammet.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Kjør det angitte ER-formatet ved å bruke den oppdaterte modelltilordningen.

Følg trinnene i [Kjør et designet format fra ER](er-quick-start1-new-solution.md#RunFormatFromER) for å kjøre det angitte ER-formatet for et enkelt spørreskjema fra **Konfigurasjoner**-siden.

### <a name="review-the-execution-trace-of-the-second-run"></a>Se gjennom utførelsessporingen for den andre kjøringen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På siden **Konfigurasjoner** utvider du **Spørreskjemamodell** og velger **Spørreskjematilordning**.
3. Velg **Utforming** i handlingsruten.
4. Velg **Utforming** på siden **Tilordning av modell til datakilde**.
5. På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.
6. I dialogboksen **Innstillinger for ytelsessporingsresultat** velger du sporingen som ble generert under den siste formatkjøringen.
7. Velg **OK**.
8. I hurtigkategorien **Detaljer** filtrerer du **Spørreskjema**-banen som peker til datakilden **Spørreskjema**.
9. Gå gjennom detaljene i databasespørringen som ble generert da **Spørreskjema**-datakilden ble kalt.

    Legg merke til at bare feltene som kreves for å fylle ut datakilden, ble hentet ved kjøretid fra `KMCollection`-programtabellen da **Spørreskjema**-datakilden ble kalt.

    > [!NOTE]
    > Enkelte felt, for eksempel feltene for partisjons-IDen, dataområde-IDen og post-IDen, legges automatisk til av Datastyring-rammeverket i Finance-appen.

    ![Ser gjennom detaljene i databasespørringen for den oppdaterte modelltilordningen på utformingssiden for modelltilordning.](./media/er-reduce-fetched-fields-number-query2.png)

Du kan bruke denne teknikken til å redusere antall hentede poster når du må redusere minneforbruket ved å kjøre ER-modelltilordning og ER-format.

## <a name="limitations"></a>Begrensninger

Når du begrenser antallet hentede felt for en datakilde for *Tabellposter*-typen, kan du ikke bruke metodene for en programtabell som datakilden refererer til, fordi programmetadata ikke gir informasjon om tabellfelt som kreves for å kalle disse metodene.

## <a name="usage-notes"></a>Bruksnotater

Selv om kommandoen **Autofill** legger til felt automatisk, sletter den ikke automatisk felt som er lagt til tidligere, selv om de ikke lenger brukes i bindinger, formler og datakilder til den redigerbare modelltilordningen.

Når du velger **Autofyll**, analyserer ER bindinger, formler og datakildene som den redigerbare modelltilordningen hadde da du åpnet den for redigering. Hvis du endrer bindinger, formler og datakilder til den redigerbare modelltilordningen, og du vil bruke kommandoen **Autofyll**, lukker du utforming av modelltilordning og åpner den deretter for å redigere modelltilordningen. 

## <a name="additional-resources"></a>Tilleggsressurser

- [Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md)
- [Feilsøke ytelsesproblemer i ER-konfigurasjoner](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
