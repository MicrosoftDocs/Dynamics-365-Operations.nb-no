---
title: Konfigurere dataimport fra SharePoint
description: Dette emnet forklarer hvordan du importerer data fra Microsoft SharePoint.
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Konfigurere dataimport fra SharePoint

[!include[banner](../includes/banner.md)]

Hvis du vil importere data fra en innkommende fil ved hjelp av Elektronisk rapportering-rammeverket (ER), må du konfigurere et ER-format som støtter importen, og deretter kjøre en modelltilordning av typen **Til målet** som bruker dette formatet som datakilde. Hvis du vil importere data, må du navigere til filen som du vil importere. Den innkommende filen kan velges manuelt av brukeren. Med den nye ER-muligheten som støtter import av data fra Microsoft SharePoint, kan denne prosessen konfigureres som den uovervåkede. Du kan bruke ER-konfigurasjoner til å utføre dataimport fra filer som er lagret i Microsoft SharePoint-mappene. Dette emnet forklarer hvordan du fullfører import fra SharePoint til Microsoft Dynamics 365 for Finance and Operations. Eksemplene bruker leverandørtransaksjoner som forretningsdata.

## <a name="prerequisites"></a>Nødvendig programvare
Hvis du vil fullføre eksemplene i dette emnet, må du ha følgende tilgang:

- Tilgang til Finance and Operations for én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

- Tilgang til forekomsten av Microsoft SharePoint-serveren som er konfigurert for bruk med Finance and Operations
- ER-format- og modellkonfigurasjoner for 1099-betalinger

### <a name="create-required-er-configurations"></a>Opprette nødvendige ER-konfigurasjoner
Spill av **ER Importer data fra en Microsoft Excel-fil**-oppgaveveiledningene, som er en del av **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**-forretningsprosessen. Disse veiledningene forklarer prosessen med å utforme og bruke ER-konfigurasjoner til å interaktivt importere leverandørtransaksjoner fra eksterne Microsoft Excel-filer. Hvis du vil ha mer informasjon, se [Analysere innkommende dokumenter i Microsoft Excel](parse-incoming-documents-excel.md). Til slutt har du:

- ER-konfigurasjoner:

    - ER-modellkonfigurasjon, **1099-betalingsmodell**
    - ER-formatkonfigurasjon, **Format for import av leverandørenes transaksjoner fra Excel**

[![ER-konfigurasjoner for å importere data fra SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Eksempel på den innkommende filen for dataimport:

    - Excel-fil **1099import-data.xlsx**, med leverandørtransaksjonene som skal importeres til Finance and Operations

[![Eksempel på Microsoft Excel-fil for import fra SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Formatet for import av leverandørtransaksjoner velges som standard modelltilordning. Derfor, hvis du kjører en modelltilordning for **1099-betalingsmodell**, og modelltilordning er av typen **Til mål**, kjører modelltilordningen dette formatet for å importere data fra eksterne filer. Disse dataene brukes deretter til å oppdatere tabeller i programmet.

## <a name="configure-document-management-parameters"></a>Konfigurere parametere for dokumentstyring
1. På siden **Parametere for dokumentstyring** konfigurerer du tilgang til SharePoint-serverforekomsten som skal brukes av firmaet som du er logget på. I dette eksemplet er firmaet USMF.
2. Test tilkoblingen til SharePoint-serverforekomsten for å være sikker på at du har fått tilgang.

[![Innstilling for dokumentadministrasjon – SharePoint-server](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Åpne det konfigurerte SharePoint-området, og opprett de følgende mappene der de innkommende filene kan lagres:

    - Kilde for import av filer (hoved)
    - Kilde for import av filer (alternativ)

[![Innstilling for dokumentadministrasjon – SharePoint-server](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Innstilling for dokumentadministrasjon – SharePoint-server](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. På **Dokumenttyper**-siden i Finance and Operations kan du opprette følgende dokumenttyper som skal brukes for å få tilgang til SharePoint-mappene du nettopp opprettet.

    - SP hoved
    - SP alternativ

5. For opprettede dokumenttyper, i **Gruppe**-feltet angir du **Fil** og i **Plassering**-feltet angir du **SharePoint**. Skriv inn adressen til SharePoint-mappen:

    - For **SP hoved**-dokumenttype: Kilde for import av filer (hoved)
    - For **SP alternativ**-dokumenttype: Kilde for import av filer (alternativ)

[![SharePoint-innstilling – ny dokumenttype](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Konfigurere ER-kildene for ER-formatet
1. Klikk på **Organisasjonsstyring** > **Elektronisk rapportering** > **Kilde for elektronisk rapportering**.
2. På **Kilde for elektronisk rapportering**-siden konfigurer kildefilene for dataimport ved å bruke et konfigurert ER-format.
3. Definer en filnavnmaske, slik at bare XLSX-filer importeres. Filnavnmasken er valgfri og brukes bare når den er definert. Du kan bare definere én maske for hvert ER-format.
4. Velg begge SharePoint-mappene du opprettet tidligere.

[![Innstilling for ER-filkilde](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>*Kilden* for ER defineres for hvert programselskap individuelt. *Konfigurasjoner* for ER deles derimot på tvers av firmaer.

> [!NOTE]
> Når du sletter en ER-kildeinnstilling for et ER-format, slettes også alle tilkoblede filtilstandene (se nedenfor).

## <a name="review-the-files-states-for-the-er-format"></a>Gå gjennom filtilstandene for ER-formatene
1. På siden **Elektronisk rapporteringskilde** velger du **Filtilstander for kildene** for å se gjennom innholdet i de konfigurerte filkildene for gjeldende ER-format.
2. I **Filer**-delen kan du se gjennom listen over filer. Denne listen viser følgende:

    - Kildefiler som er nødvendige, basert på filnavnmasken (hvis en filnavnmaske er definert), og som er klar for dataimport. For disse filene er delen **Kildelogger for importformatet** tom.
    - Tidligere importerte filer. For hver av disse filene kan du se gjennom loggen for import av denne filen, i **Kildelogger for importformatet**-delen.

Du kan også åpne siden **Filtilstander for kildene** ved å velge **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Filtilstander for kildene**. I dette tilfellet gir siden informasjon om filkilder for alle ER-formater som filkilder er konfigurert for, i firmaet som du er logget på.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Importere data fra Excel-filer som er i en SharePoint-mappe
1. I SharePoint last opp Microsoft Excel-filen **1099import-data.xlsx** som inneholder leverandørtransaksjonene til **Kilde for import av filer (hoved)**-SharePoint-mappen som du opprettet tidligere.

[![SharePoint-innhold – Microsoft Excel-fil for import](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. I Finance and Operations, på siden **Filtilstander for kildene**, velger du **Oppdater** for å oppdatere siden. Legg merke til at Excel-filen som ble lastet opp til SharePoint, ble vist i dette skjemaet med statusen **Klar**. Følgende statuser støttes for øyeblikket:

    - **Klar** – Tilordnes automatisk for hver ny fil i en SharePoint-mappe. Denne statusen betyr at filen er klar for import.
    - **Importerer** – Tilordnet automatisk av en ER-rapport når filen blir låst av importprosessen for å forhindre at den brukes av andre prosesser (hvis mange kjøres samtidig).
    - **Importert** – Tilordnet automatisk av en ER-rapport når filimporten er fullført. Denne statusen betyr at den importerte filen er slettet fra den konfigurerte filkilden (SharePoint-mappe).
    - **Mislykket** – Tilordnet automatisk av en ER-rapport når filimporten er fullført med feil eller unntak.
    - **På vent** – Tilordnet manuelt av brukeren i dette skjemaet. Denne statusen betyr at filen ikke blir importert for øyeblikket. Denne statusen kan brukes til å utsette importen av noen filer.

[![Siden for ER-filtilstand for de valgte kildene](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Importer data fra SharePoint-filer
1. Åpne ER-konfigurasjonstreet, velg **1099-betalingsmodellen**, og utvid listen over ER-modellkomponenter.
2. Velg navnet på modelltilordningen for å åpne listen over modelltilordninger av den valgte ER-modellkonfigurasjonen.

[![Siden for ER-filtilstand for de valgte kildene](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Velg **Kjør** for å kjøre den valgte modelltilordningen. Fordi du har konfigurert filkilder for ER-formatet, kan du endre innstillingen for **Filkilde**-alternativet etter behov. Hvis du beholder innstillingen for dette alternativet, importeres XSLX-filene fra de konfigurerte kildene (SharePoint-mappene i dette eksemplet).

    I dette eksemplet skal du importere bare én fil. Hvis det finnes flere filer, velges de for import i rekkefølgen de ble lagt til i SharePoint-mappen. Hver kjøring av et ER-format importerer én enkelt valgt fil.

[![Kjør ER-modelltilordning](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Modelltilordningen kan kjøres uovervåket i satsvis modus. I dette tilfellet vil en enkelt fil importeres fra de konfigurerte filkildene hver gang et parti kjører dette ER-formatet. Bruk følgende kode for å implementere denne partikjøringen.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Når en fil er importert fra SharePoint-mappen, slettes den fra denne mappen.

5. Angi bilags-ID-en, for eksempel **V-00001**, og velg deretter **OK**.

[![Kjør ER-modelltilordning](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. På siden **Filtilstander for kildene** velger du **Oppdater** for å oppdatere siden.

[![Siden for ER-filtilstand for de valgte kildene](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. I **Filer**-delen kan du se gjennom listen over filer. Delen **Kildelogger for importformatet** inneholder loggen for Excel-filimporten. Fordi denne filen ble importert, er den merket som **Slettet** i SharePoint-mappen.
8. Gå gjennom SharePoint-mappen **Kilde for import av filer (hoved)**. Excel-filene som ble importert, er slettet fra denne mappen.
9. I Finance and Operations velger du **Leverandører** \> **Periodiske oppgaver** \> **Avgift 1099** \> **Leverandørutligning for 1099-skjema**.
10. I **Fra-dato** og **Til-dato** angir du riktige verdier. Velg deretter **Manuelle 1099-transaksjoner**.

    Leverandørtransaksjonene som ble importert fra Excel-filene i SharePoint for bilaget **V-00001**, vises på siden.

[![Siden for 1099-leverandørtransaksjoner](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Klargjøre en Excel-fil for import
1. Åpne Excel-filen som du har brukt tidligere. I rad 3 kolonne 1 kan du legge til en leverandørkode som ikke finnes i programmet. Legge til mer usann leverandørinformasjon i raden.

[![Eksempel på Microsoft Excel-fil for import fra SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Last opp den oppdaterte Excel-filen som inneholder leverandørtransaksjoner til SharePoint-mappen **Kilde for import av filer (hoved)** .
3. I Finance and Operations åpne ER-konfigurasjonstreet, velg **1099-betalingsmodellen**, og utvid listen over ER-modellkomponenter.
4. Velg navnet på modelltilordningen for å oppdatere modelltilordning, slik at leverandørkoden som er feil, regnes som en feil under import av data.
5. Velg **Utforming**.
6. I **Valideringer**-kategorien må du endre ettervalideringshandlingen for valideringsregelen som er konfigurert for å vurdere om leverandørkontoen som importeres, finnes i programmet. Oppdater verdien av feltet **Ettervalideringshandling** for å **Stoppe utførelse**, lagre endringene, og lukk siden.

[![Siden ER-utforming av modelltilordning](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Lagre endringene, og lukk ER-utformingen av modelltilordningen.
8. Velg **Kjør** for å kjøre den endrede ER-modelltilordningen.
9. Angi bilags-ID-en, for eksempel **V-00002**, og velg deretter **OK**.

    Legg merke til at infologgen inneholder varslingen som informerer om det som finnes i mappen for SharePoint-fil, inneholder ugyldig leverandørkonto og ikke kan importeres.

[![Kjør ER-modelltilordning](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. På siden **Filtilstander for kildene** velger du **Oppdater**, og deretter, i **Filer**-delen, ser du gjennom fillisten.

[![Siden for ER-filtilstand for de valgte kildene](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

**Kildelogger for importformatet**-delen angir at importprosessen mislyktes, og at filen fremdeles er i mappen SharePoint (**Er slettet**-boksen er ikke avmerket). Hvis du vil reparere denne filen i SharePoint ved å legge til den riktige leverandørkoden og deretter endre statusen for filen fra **Mislykket** til **Klar** i **Kildelogger for importformatet**-delen, kan du importere filen på nytt.

11. Gå gjennom SharePoint-mappen **Kilde for import av filer (hoved)**. Legg merke til at Excel-filen som ikke ble importert, fremdeles er i denne mappen.
12. I Finance and Operations velger du **Leverandører** \> **Periodiske oppgaver** \> **Avgift 1099** \> **Leverandørutligning for 1099-skjema**, skriv inn riktige verdier i **Fra dato**- og **Til dato**-feltene, og velg deretter **Manuelle 1099-transaksjoner**.

    Bare transaksjoner for bilaget V-00001 er tilgjengelige. Det finnes ingen transaksjoner for bilaget V-00002, selv om feilen for den sist importerte transaksjonen ble funnet i Excel-filen.

