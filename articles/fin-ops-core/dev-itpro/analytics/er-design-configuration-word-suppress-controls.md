---
title: Skjule Word-innholdskontroller i genererte rapporter
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Electronic reporting) til å generere rapporter som Microsoft Word-filer der innholdskontroller skjules.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 2c2d79c9ea36c42cfc0f6ba0d3c81d063d8d9446
ms.sourcegitcommit: 6c1bf233748c4bc70fc5a1a9711758cdfd9e07dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782184"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Skjule Word-innholdskontroller i genererte rapporter

[!include [banner](../includes/banner.md)]

Hvis du vil generere rapporter som Microsoft Word-dokumenter, må du utforme en mal for rapportene som et Word-dokument. Denne malen må inneholde Word-innholdskontroller som plassholdere for data som fylles ut ved kjøretid. Hvis du vil bruke Word-dokumentet som opprettes som en mal for rapportene dine, kan du [konfigurere](er-design-configuration-word.md) en ny løsning for [Elektronisk rapportering (ER)](general-electronic-reporting.md)[løsning](er-quick-start1-new-solution.md). Løsningen må inneholde en ER-[konfigurasjon](general-electronic-reporting.md#Configuration) som inneholder en komponent for ER-format. Dette ER-formatet må konfigureres til å bruke den utformede malen for rapportgenerering.

I versjon 10.0.6 og senere av Dynamics 365 Finance kan du konfigurere formler i ER-formatet for å vise informasjon om enkelte Word-innholdskontroller i genererte dokumenter.

Trinnene nedenfor forklarer hvordan en bruker som er tilordnet til systemadministratoren eller den elektroniske rapporteringsfunksjonelle konsulentrollen, kan konfigurere et ER-format som genererer rapporter som Word-filer og viser noen av innholdskontrollene i de genererte rapportene som er konfigurert ved hjelp av en Word-mal.

Denne fremgangsmåten kan gjennomføres i firmaet GBSI.

## <a name="prerequisites"></a>Forutsetninger

For å fullføre disse trinnene, må du først fullføre trinnene i fløgende oppgaveveiledninger:

- [Utforme en konfigurasjon for generering av rapporter i OPENXML-format](./tasks/er-design-reports-openxml-2016-11.md)
- [Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format](./tasks/er-design-configuration-word-2016-11.md)

Når du fullfører trinnene i disse oppgavehåndbokene, klargjøres følgende elementer:

- Et ER-format kalt **Regnearkeksempelrapport** som konfigureres til å generere et dokument i Word-format
- Et [utkast](general-electronic-reporting.md#component-versioning) til ER-formatet for **Regnearkeksempelrapport** som er merket som **Kjørbar**
- En **elektronisk** betalingsmåte som er konfigurert til å bruke ER-formatet for **Regnearkeksempelrapport** for leverandørbetalingsbehandling

Du må også laste ned og lagre følgende mal for eksempelrapporten:

- [Bundet mal 2 for betalingsrapport (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/1/9/b/19b36e39-861a-414e-9150-9880d9d2487c/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Se gjennom den nedlastede Word-malen

1. Åpne malfilen **SampleVendPaymDocReportBounded2.docx** du lastet ned tidligere, i skrivebordsversjonen av Word.
2. Kontroller at malfilen inneholder et sammendragsseksjon som viser totalt betalingsbeløp for hver valutakode som er oppfylt i de behandlede betalingene.

    - Sammendragsdelen ligger i en separat tabell i Word-dokumentet.
    - Den første raden i denne tabellen inneholder tabellkolonneoverskriftene som seksjonshode.
    - Den andre raden i denne tabellen inneholder den gjentagende innholdskontrollen som deldetaljene.
    - Denne innholdskontrollen er tilordnet til feltet **SummaryLines** i delen om tilpasset XML i **rapporten**.
    - Basert på denne tilordningen er innholdskontrollen knyttet til elementet **SummaryLines** i det redigerbare ER-formatet.

    > [!NOTE]
    > Den gjentagende innholdskontrollen merkes av nøkkelen **SummaryLines** som samsvarer med feltet for den egendefinerte XML-delen den er tilordnet.

    ![Oppsett for Word-mal.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Velg den eksisterende ER-rapportkonfigurasjonen

I disse trinnene bruker du den eksisterende ER-konfigurasjonen du konfigurerte på nytt da du fullførte trinnene i de tidligere nevnte oppgaveveiledningene.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. Velg **Rapporteringskonfigurasjoner**.
3. På siden **Konfigurasjoner** utvider du **Betalingsmodell** i konfigurasjonstreet og velger **Regnearkeksempelrapport**.
4. Velg **Utforming** for å redigere utkastversjonen av det valgte ER-formatet.

## <a name="replace-the-current-template-with-the-new-template"></a>Erstatt den gjeldende malen med den nye malen

For øyeblikket brukes filen SampleVendPaymDocReportBounded.docx som en mal for å generere utdataene i Word-format. I fremgangsmåten nedenfor skal du erstatte denne Word-malen med den nye Word-malfilen, SampleVendPaymDocReportBounded2.docx, du lastet ned tidligere.

1. På siden **Formatutforming** velger du **Vedlegg**.
2. Velg **Slett** på siden **Vedlegg** for å fjerne den eksisterende malen.
3. Velg **Ja** for å bekrefte slettingen.
4. Velg **Ny** \> **Fil**.
5. Velg **Bla gjennom**, og bla til og velg filen **SampleVendPaymDocReportBounded2.docx** som du lastet ned tidligere.
6. Velg **OK**.
7. Lukk **Vedlegg**-siden.
8. Angi eller velg filen **SampleVendPaymDocReportBounded2.docx** i feltet **Mal** på siden **Formatutforming**.

## <a name="run-the-format-to-create-word-output"></a>Kjøre formatet for å opprette Word-utdata

1. Gå til **Leverandører** \> **Betalinger** \> **Betalingsjournal**.
2. Velg alle betalingene på i fanen **Liste** på siden **Leverandørbetalinger**.
3. Velg **Betalingsstatus** \> **Ingen**.
4. Velg **Generer betalinger**.
5. Velg **Elektronisk** i feltet **Betalingsmåte**.
6. Velg **GBSI OPER** i feltet **Bankkonto**.
7. Velg **OK**.
8. I dialogboksen **Parametere for elektronisk rapport** velger du **OK** og analyserer de genererte utdataene.

    ![Betalinger for behandling på Leverandørbetalinger-siden.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Resultatet vises i Word-format, og inneholder sammendragsdelen.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Konfigurere det redigerbare formatet til å skrive ned sammendragsdelen

Hvis du vil skrive inn sammendragsdelen i et generert dokument basert på forespørselen til en bruker som kjører dette ER-formatet, må du endre ER-formatet.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering** og åpne utkastversjonen av ER-formatet for redigering.
2. Velg **Rapporteringskonfigurasjoner**. 
3. Vis **Betalingsmodell** \> **Regnearkeksempelrapport** i konfigurasjonstreet på siden **Konfigurasjoner**.
4. Velg **Utforming**.
5. Vis **Word** og velg **SummaryLines** på siden **Formatutforming**.
6. I fanen **Tilordning** legger du til en ny datakilde for å spørre brukeren i kjøretid om sammendragsdelen skal undersøkes:

    1. Velg **Legg til rot**.
    2. I dialogboksen **Legg til datakilde** velger du **Generelt\Inndataparameter for bruker** for å åpne dialogboksen **Datakildeegenskaper for Inndataparameter for bruker** .
    3. Angi **uipSuppress** i feltet **Navn**.
    4. Angi **Skjul sammendragsdel** i feltet **Etikett**.
    5. I feltet **Navn på operasjonsdatatype** velger eller angir du **NoYes**.
    6. Velg **OK**.

7. Legg til en ny datakilde av programopplistingstypen **NoYes**:

    1. Velg **Legg til rot**.
    2. I dialogboksen **Legg til datakilde** velger du **Dynamics 365 for Operations\Opplisting** for å åpne dialogboksen **Datakildeegenskaper for Opplisting**.
    3. Angi **enumNoYes** i feltet **Navn**.
    4. Angi **Skjul alternativer** i feltet **Etikett**.
    5. I feltet **Navn på operasjonsdatatype** velger eller angir du **NoYes**.
    6. Velg **OK**.

8. For det valgte elementet for **SummaryLines**-format konfigurerer du formelen til å angi når Word-innholdskontrollen som er knyttet til det valgte formatelementet, skal skjules:

    1. Velg **Rediger** for å åpne siden **[Formelutforming](general-electronic-reporting-formula-designer.md)** i delen **Fjernet** i fanen **Tilordning**.
    2. I feltet **Formel** angir du formelen `uipSuppress = enumNoYes.Yes`.
    3. Velg **Lagre**, og lukk siden **Formeldesigner**.

        > [!NOTE]
        > Denne formelen brukes på et generert dokument **etter at alle andre formatelementer er kjørt**. Hvis du vil bruke denne formelen, finnes det en Word-innholdskontroll som er merket som et formatelement som formelen er konfigurert for (**SummaryLines** i dette tilfellet), i et generert dokument. Denne innholdskontrollen fjernes deretter fullstendig, sammen med raden i Word-tabellen som inneholder den. Detaljraden i sammendragsdelen fjernes fra det genererte dokumentet.
        >
        > På utformingstidsprogrammet kan du konfigurere formelen **Fjernet** for et formatelement, selv om ingen innholdskontroll i Word-malen du bruker, har en kode som samsvarer med navnet på et formatelement som egenskapen **Fjernet** er konfigurert for. Når du validerer formatet på utformingstidsprogrammet, får du en [advarsel](er-components-inspections.md#i14) om denne inkonsekvensen.
        >
        > Ved kjøretid skjer det unntak hvis ingen innholdskontroll i Word-malen du bruker, har en kode som samsvarer med navnet på et formatelement som egenskapen **Fjernet** er konfigurert for.

    4. Sett alternativet **Med overordnet** til **Ja** i delen **Fjernet** i fanen **Tilordning**.

        > [!NOTE]
        > Du må velge **Yes** for å fjerne hele Word-tabellen som det overordnede objektet i raden som inneholder detaljene for sammendragsdelen. Hvis du setter dette alternativet til **Nei**, blir overskriftsraden for delen stående i det genererte dokumentet.

9. Velg **Lagre** for å lagre endringene i det redigerbare formatet.

    ![De genererte utdataene i Word-format.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Kjøre det endreded formatet for å opprette Word-utdata

1. Gå til **Leverandører** \> **Betalinger** \> **Betalingsjournal**.
2. Velg betalingsjournalen du opprettet, og velg deretter **Linjer**.
3. På sien **Leverandørbetalinger** merker du alle radene, og deretter velger du **Betalingsstatus** \> **Ingen**.
4. Velg **Generer betalinger**.
5. Velg **Elektronisk** i feltet **Betalingsmåte**.
6. Velg **GBSI OPER** i feltet **Bankkonto**.
7. Velg **OK**.
8. Velg **Ja** feltet **Skjul sammendragsdel** i dialogboksen **Parametere for elektronisk rapport**.
9. Velg **OK** og analyser de genererte utdataene.

    ![Genererte utdata i Word-format.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Legg merke til at utdataene ikke inneholder sammendragsdelen fordi det er skjedd en feil.

## <a name="additional-resources"></a>Tilleggsressurser

- [Utforme en konfigurasjon for generering av rapporter i OPENXML-format](./tasks/er-design-reports-openxml-2016-11.md)
- [Utforme en ny ER-konfigurasjon for å generere rapporter i Word-format](er-design-configuration-word.md)
- [Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format](./tasks/er-design-configuration-word-2016-11.md)
- [Kontrollere den konfigurerte ER-komponenten for å forhindre kjøretidsproblemer](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
