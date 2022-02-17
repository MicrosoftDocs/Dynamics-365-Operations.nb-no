---
title: Importer data fra manuelt valgte filer i satsvis modus
description: Dette emnet beskriver hvordan du importerer data fra filer som er valgt manuelt i satsvis modus.
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 8615b5a0623fd696c64f4ec03e481a2bcb16c0ac
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075625"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Importer data fra manuelt valgte filer i satsvis modus

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Hvis du vil bruke [ER-rammeverket (Electronic Reporting)](general-electronic-reporting.md) til å importere data fra manuelt valgte innkommende filer i satsvis modus, konfigurerer du et [ER-format](er-overview-components.md#format-component) som støtter importen. Deretter kjører du en [modelltilordning](er-overview-components.md#model-mapping-component) av **Til mål**-typen som bruker dette formatet som en datakilde. Hvis du vil importere data, må du navigere til filen som du vil importere, og velge den manuelt. 

Med den nye ER-muligheten som støtter dataimport i satsvis modus, kan denne prosessen konfigureres som uovervåket. Du kan bruke ER-konfigurasjoner til å utføre dataimport ved å planlegge en ny satsvis jobb fra ER-brukergrensesnittet.

Dette emnet beskriver hvordan du fullføre dataimport filer en manuelt valgt fil i satsvis modus. Eksemplene bruker leverandørtransaksjoner som forretningsdata. Trinnene i disse eksemplene kan fullføres i **USMF**-selskapet. Ingen koding er nødvendig.

## <a name="prerequisites"></a>Forutsetninger

Hvis du vil fullføre eksemplene i dette emnet, må du ha følgende tilgang:

- Én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

- ER-format- og modellkonfigurasjoner for 1099-betalinger

### <a name="create-the-required-er-configurations"></a>Opprett de nødvendige ER-konfigurasjonene

Følg ett av disse trinnene for å opprette de nødvendige ER-konfigurasjonene og hente andre forutsetninger:

- Spill av **ER Importer data fra en Microsoft Excel-fil**-oppgaveveiledningene, som er en del av **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**-forretningsprosessen. Disse oppgaveveiledningene forklarer prosessen med å utforme og bruke ER-konfigurasjoner som interaktivt importerer leverandørtransaksjoner fra Microsoft Excel-filer. Hvis du vil ha mer informasjon, se [Analysere innkommende dokumenter i Excel-format](parse-incoming-documents-excel.md).
- Fullfør eksemplene under [Konfigurer dataimport fra SharePoint](er-configure-data-import-sharepoint.md). Disse eksemplene forklarer prosessen med å utforme og bruke ER-konfigurasjoner til å interaktivt importere leverandørtransaksjoner fra Excel-filer som er lagret i en SharePoint-mappe.

### <a name="download-the-required-er-configurations"></a>Last ned de nødvendige ER-konfigurasjonene

1. Last ned følgende ER-konfigurasjoner, og lagre dem lokalt.

    | Innholdsbeskrivelse | Fil |
    |---------------------|------|
    | ER-datamodellkonfigurasjon **1099-betalingsmodell** | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | ER-formatkonfigurasjon **For import av leverandørenes transaksjoner (Excel)** | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Bruk ER-alternativet [Last fra XML-fil](er-defer-sequence-element.md#import-the-sample-er-configurations) til å importere de nedlastede ER-konfigurasjonene til din forekomst av Dynamics 365 Finance i følgende rekkefølge:

    1. ER-datamodellkonfigurasjon
    2. ER-formatkonfigurasjon

### <a name="download-the-required-excel-files"></a>Laste ned de nødvendige Excel-filene

- Last ned eksempeldatasettet nedenfor, og lagre det lokalt.

    | Innholdsbeskrivelse | Fil |
    |---------------------|------|
    | Innkommende **1099import-data.xlsx**-fil som inneholder eksempeldata for import | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Gå gjennom forutsetningene

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden går du gjennom den forberedte ER-løsningen for dataimport i satsvis modus.
3. Gå gjennom formatkonfigurasjonen av **For import av leverandørers transaksjoner (Excel)**.

    - Formatkomponenten for denne konfigurasjonen er utformet for å analysere en innkommende Excel-fil.
    - Modelltilordningskomponenten for denne konfigurasjonen brukes til å fylle ut basisdatamodellen ved hjelp av data fra den analyserte Excel-filen.

    ![ER-formatkonfigurasjon for import av data i satsvis modus fra ER-grensesnittet.](./media/er-configure-data-import-batch-configurations-1.png)

4. Gå gjennom datamodellkonfigurasjonen **1099-betalingsmodell**.

    - Modellkomponenten for denne konfigurasjonen representerer strukturen til datamodellen som brukes til å sende data mellom kjøring av ER-komponenter.
    - Modelltilordningskomponenten for denne konfigurasjonen brukes til å hente data fra den utførte formatkomponenten og deretter oppdatere programtabeller.

    ![ER-datamodellkonfigurasjon for import av data i satsvis modus fra ER-grensesnittet.](./media/er-configure-data-import-batch-configurations-2.png)

5. Åpne filen **1099import-data.xlsx** i Excel.

    ![Eksempel på Excel-fil med data for import i satsvis modus.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Aktiver satsvis dataimport for ER fra grensesnittet

1. Gå til **Systemadministrasjon** \> **Arbeidsområder** \> **Funksjonsbehandling**.
2. I arbeidsområdet **Funksjonsbehandling** velger du funksjonen **Kjør ER-import av manuelt opplastede dokumenter i parti** og velger deretter **Aktiver nå**.

## <a name="import-data-from-manually-selected-excel-files"></a>Importer data fra manuelt valgte Excel-filer

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden velger du datamodellkonfigurasjonen **1099-betalingsmodell**.
3. På hurtigfanen **Konfigurasjonskomponenter** velger du koblingen **For import for manuelle 1099-transaksjoner**.
4. På siden **Tilordning av modell til datakilde** er modelltilordningen **For import for manuelle 1099-transaksjoner** forhåndsvalgt. Velg **Kjør**.
5. Velg **Bla gjennom** på fanen **Parametere**. Finn og velg filen **1099import-data.xlsx**, og velg deretter **OK**.
6. I feltet **Angi bilags-ID** angir du **V-00001**.
7. På fanen **Kjør i bakgrunnen** setter du **Satsvis behandling** til **Ja**.

    Legg merke til feltet **Oppgavebeskrivelse** er angitt til **Kjøring av modelltilordning "For import for manuelle 1099-transaksjoner", konfigurasjon "1099-betalingsmodell"**. Denne verdien angir at kjøringen av den valgte modelltilordningen vil bli planlagt som en ny satsvis jobb.

    ![Angi detaljer for dataimport i satsvis modus i dialogboksen Parametere for elektronisk rapport.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Velg **OK**. En melding gir deg beskjed om at en ny satsvis jobb er planlagt.

    ![Melding om en ny planlagt satsvis jobb på siden Tilordning av modell til datakilde.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Gå gjennom resultatene av dataimporten på siden for satsvis jobb

1. Gå til **Felles** \> **Forespørsler** \> **Satsvise jobber** \> **Mine satsvise jobber**.
2. På siden **Satsvis jobb** filtrerer du listen med satsvise jobber for å finne den planlagte bunken, og deretter velger du den.
3. Velg koblingen **Jobb-ID** for å se gjennom jobbdetaljer.
4. Velg **Logg** i hurtigfanen **Satsvise oppgaver**.

    ![Logg-knappen på siden Satsvis jobb.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Se gjennom kjøringsdetaljene.

    ![Kjøringslogg for den planlagte satsvise jobben på siden Satsvis jobb.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Endre dataimportparameterne

Når den satsvise jobben er planlagt og mens den ennå ikke er kjørt, kan du endre parameterne for den planlagte dataimporten.

1. Gå til **Felles** \> **Forespørsler** \> **Satsvise jobber** \> **Mine satsvise jobber**.
2. På siden **Satsvis jobb** filtrerer du listen med satsvise jobber for å finne den planlagte bunken, og deretter velger du den.
3. Velg **Endre status**.
4. I dialogboksen **Velg ny status** velger du **Trekk tilbake** og deretter **OK**.
5. Velg koblingen **Jobb-ID** for å få tilgang til jobbdetaljene.
6. Velg **Parametere** i hurtigfanen **Satsvise oppgaver**.
7. I dialogboksen **Parametere for elektronisk rapport** følger du disse trinnene:

    1. Velg **Bla gjennom** for å velge den alternative filen for dataimport.
    2. Velg **Angi bilags-ID** for å endre bilagsnummeret for import av leverandørtransaksjoner.

        ![Endring av parameterne for dataimporten for den planlagte satsvise jobben i dialogboksen Parametere for elektronisk rapport.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Velg **OK**.

8. Kontroller at partiet fremdeles er valgt, og velg deretter **Endre status** på nytt.
9. I dialogboksen **Velg ny status** velger du **Venter** og deretter **OK**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Gå gjennom resultatene av dataimporten på siden for ER-kilden

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Kilde for elektronisk rapportering**.
2. Velg posten **For import av leverandørens transaksjoner (Excel)** som ble opprettet automatisk under dataimporten.

    ![Posten for konfigurasjonen av For import av leverandørenes transaksjoner (Excel) på siden Kilde for elektronisk rapportering.](./media/er-configure-data-import-batch-files-source-1.png)

3. Velg **Filtilstander for kildene**.
4. På hurtigfanene **Filer** og **Kildelogger for importformatet** går du gjennom importdetaljene.
5. Velg posten på hurtigfanen **Filer**. Legg merke til at den importerte filen er knyttet til denne posten.

    ![Importert fil som er knyttet til posten på siden Filtilstander for kildene.](./media/er-configure-data-import-batch-files-source-2.png)

6. Velg **Vedlegg** for å gå gjennom den importerte filen.

    ![Importert fil på dokumentvisningssiden.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > For å beholde disse vedleggene bruker ER-rammeverket en dokumenttype som er [angitt](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) for det gjeldende firmaet i **Annet**-feltet for ER-parameterne.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Gå gjennom dataimportresultatene på siden Leverandørutligning for 1099-skjema

1. Gå til **Leverandører** \> **Periodiske oppgaver** \> **1099-avgift** \> **Leverandørutligning for 1099-skjema**.
2. Angi **12/31/2017** (31. desember 2017) i **Fra dato**-feltet.
3. Velg **Manuelle 1099-transaksjoner**.

    ![Importerte leverandørtransaksjoner på siden 1099-avgiftstransaksjoner.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
