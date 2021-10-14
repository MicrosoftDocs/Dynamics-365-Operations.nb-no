---
title: Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format
description: Dette emnet beskriver hvordan rapportformater som ble utformet for å generere rapporter som Excel-arbeidsbøker, kan konfigureres slik at de genererer rapporter som Word-dokumenter.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4eb4fd4ea32db5aa19e9d2b1300818b3aaf6fc
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594990"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format

[!include [banner](../../includes/banner.md)]

Hvis du vil generere rapporter som Microsoft Word-dokumenter, kan du [konfigurere](../er-design-configuration-word.md) et nytt [format](../general-electronic-reporting.md#FormatComponentOutbound) for [ER (Elektronisk rapportering)](../general-electronic-reporting.md). Du kan også bruke et ER-format på nytt som opprinnelig ble utformet for å generere rapporter som Excel-arbeidsbøker. I så fall må du erstatte Excel-malen med en Word-mal.

Fremgangsmåtene nedenfor viser hvordan en bruker med rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan konfigurere et ER-format slik at det genererer rapporter som Word-filer, ved å bruke et ER-format på nytt som ble utformet for å generere rapporter som Excel-filer.

Disse fremgangsmåtene kan fullføres i firmaet GBSI.

## <a name="prerequisites"></a>Forutsetninger

For å kunne fullføre disse fremgangsmåtene må du først følge trinnene i oppgaveveiledningen [Utforme en konfigurasjon for generering av rapporter i OPENXML-format](er-design-reports-openxml-2016-11.md).

Du må også laste ned og lagre følgende maler lokalt for eksempelrapporten:

- [Mal for betalingsrapport (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Bundet mal for betalingsrapport (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

Disse fremgangsmåtene er for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611 (november 2016).

## <a name="select-the-existing-er-report-configuration"></a>Velg den eksisterende ER-rapportkonfigurasjonen

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering** i Dynamics 365 Finance.
2. Kontroller at konfigurasjonsleverandøren **Litware, Inc.** er merket som **Aktiv**. Hvis den ikke er det, følger du trinnene i opprett oppgaveveiledningen [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).
3. Velg **Rapporteringskonfigurasjoner**. Du skal bruke den eksisterende ER-konfigurasjonen som opprinnelig ble utformet for å generere rapportutdataene i OPENXML-formatet, på nytt.
4. I konfigurasjonstreet i venstre rute på **Konfigurasjoner**-siden utvider du **Betalingsmodell** og velger **Regnearkeksempelrapport**.

    > [!NOTE]
    > Utkastversjonen av det valgte ER-formatet kan redigeres i hurtigfanen **Versjoner**.

5. Velg **Utforming**.
6. Merk at tittelen på rotformatelementet på **Formatutforming**-siden angir at en Excel-mal for øyeblikket er i bruk.

![Velge den eksisterende konfigurasjonen.](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Se gjennom den nedlastede Word-malen

1. Åpne malfilen **SampleVendPaymDocReport.docx** du lastet ned tidligere, i skrivebordsversjonen av Word.
2. Kontroller at malen bare inneholder oppsettet for dokumentet du vil generere som ER-utdata.

![Oppsettet i Word-malen i skrivebordsprogrammet.](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Erstatte Excel-malen med Word-malen og legge til en egendefinert XML-del

For øyeblikket brukes Excel-dokumentet som en mal til å generere utdataene i OPENXML-format. Du skal erstatte denne malen med Word-malfilen SampleVendPaymDocReport.docx du lastet ned tidligere. Du skal også utvide Word-malen ved å legge til en egendefinert XML-del.

1. Velg **Vedlegg** i **Format**-fanen på **Formatutforming**-siden i Finance.
2. Velg **Slett** på **Vedlegg**-siden for å fjerne den eksisterende Excel-malen. Velg **Ja** for å bekrefte endringen.
3. Velg **Ny** \> **Fil**.

    > [!NOTE]
    > Du må velge en dokumenttype som er [konfigurert](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parameterne, for å kunne lagre maler for ER-formater.

4. Velg **Bla gjennom**, og bla deretter til og velg filen **SampleVendPaymDocReport.docx** som du lastet ned tidligere.
5. Velg **OK**.
6. Lukk **Vedlegg**-siden.
7. Angi eller velg filen **SampleVendPaymDocReport.docx** i **Mal**-feltet på **Formatutforming**-siden for å bruke denne Word-malen i stedet for Excel-malen som ble brukt tidligere.
8. Velg **Lagre**.

    I tillegg til å lagre konfigurasjonsendringer, oppdaterer **Lagre**-handlingen den vedlagte Word-malen. Den hierarkiske strukturen til det utformede formatet føyes til det vedlagte Word-dokumentet som en ny, egendefinert XML-del med navnet **Rapport**. Den vedlagte Word-malen inneholder oppsettet for dokumentet som blir generert som ER-utdata, og strukturen til dataene som ER registrerer i denne malen under kjøring.

9. Merk at tittelen på rotformatelementet angir at en Word-mal for øyeblikket er i bruk.

    ![Erstatte Excel-malen med Word-malen og legge til en egendefinert XML-del.](../media/er-design-configuration-word-2016-11-image03.gif)

10. Velg **Vedlegg** i fanen **Format**.

Du kan nå tilordne elementene i den egendefinerte XML-delen **Rapport** til innholdskontrollene for Word-dokumentet.

Hvis du har erfaring med utforming av Word-dokumenter som skjemaer som inneholder [innholdskontroller](/office/client-developer/word/content-controls-in-word) som er tilordnet til elementer med [egendefinerte XML-deler](/visualstudio/vsto/custom-xml-parts-overview), fullfører du alle trinnene i den neste fremgangsmåten for å opprette dokumentet. Hvis du vil ha mer informasjon, kan du se [Opprette skjemaer som brukere fullfører eller skriver ut i Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Ellers hopper du over neste fremgangsmåte.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Hente et Word-dokument som har en egendefinert XML-del, og foreta datatilordning

1. Velg **Åpne** på **Vedlegg**-siden i Finance for å laste ned den valgte malen fra Finance og lagre den lokalt som et Word-dokument.
3. Åpne dokumentet du nettopp lastet ned, i skrivebordsversjonen av Word.
4. I **Utvikler**-fanen velger du ruten **XML-tilordning**.

    > [!NOTE]
    > Hvis **Utvikler**-fanen ikke vises på båndet, kan du tilpasse båndet for å legge den til.

5. Velg den egendefinerte XML-delen **Rapport** i feltet **Egendefinert XML-del** i ruten **XML-tilordning**.
6. Tilordne elementene i den valgte egendefinerte XML-delen **Rapport** og innholdskontrollene for Word-dokumentet.
7. Lagre det oppdaterte Word-dokumentet lokalt som **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Gå gjennom Word-malen der den egendefinerte XML-delen er tilordnet til innholdskontroller

1. Åpne malfilen **SampleVendPaymDocReportBounded.docx** i skrivebordsversjonen av Word.
2. Kontroller at malen inneholder oppsettet for dokumentet du vil generere som ER-utdata. Innholdskontrollene som brukes som plassholdere for data som ER skal registrere i denne malen ved kjøretid, er basert på tilordningene som er konfigurert mellom elementer i den egendefinerte XML-delen **Rapport** og innholdskontrollene i Word-dokumentet.

![Forhåndsvisning av Word-mal i skrivebordsprogrammet.](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Laste opp Word-malen der den egendefinerte XML-delen er tilordnet til innholdskontroller

1. Velg **Slett** på **Vedlegg**-siden i Finance for å fjerne Word-malen som ikke har noen tilordninger mellom elementer i den egendefinerte XML-delen **Rapport** og innholdskontrollene. Velg **Ja** for å bekrefte endringen.
2. Velg **Ny** \> **Fil** for å legge til en ny malfil som inneholder tilordninger mellom elementer i den egendefinerte XML-delen **Rapport** og innholdskontrollene.

    > [!NOTE]
    > Du må velge en dokumenttype som er [konfigurert](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parameterne, for å kunne lagre maler for ER-formater.

3. Velg **Bla gjennom**, og bla deretter til og velg filen **SampleVendPaymDocReportBounded.docx** du lastet ned eller klargjorde ved å fullføre fremgangsmåten i delen [Hente et Word-dokument som har en egendefinert XML-del, og foreta datatilordning](#get-word-doc).
4. Velg **OK**.
5. Lukk **Vedlegg**-siden.
6. Velg dokumentet du nettopp lastet ned, i **Mal**-feltet på **Formatutforming**-siden.
7. Velg **Lagre**.
8. Lukk **Formatutforming**-siden.

## <a name="mark-the-configured-format-as-runnable"></a>Merke det konfigurerte formatet som kjørbart

For å kunne kjøre utkastversjonen av det redigerbare formatet må du gjøre den [kjørbar](../er-quick-start2-customize-report.md#MarkFormatRunnable).

1. Velg **Brukerparametere** i gruppen **Avanserte innstillinger** i **Konfigurasjoner**-fanen i handlingsruten på **Konfigurasjoner**-siden i Finance.
2. I dialogboksen **Brukerparametere** setter du **Kjøringsinnstillinger** til **Ja**, og deretter velger du **OK**.
3. Velg **Rediger** for å gjøre gjeldende side redigerbar, hvis nødvendig.
4. Angi **Ja** for alternativet **Kjør utkast** for den valgte konfigurasjonen **Regnearkeksempelrapport**.
5. Velg **Lagre**.

## <a name="run-the-format-to-create-output-in-word-format"></a>Kjøre formatet for å opprette utdata i Word-format

1. Gå til **Leverandører** \> **Betalinger** \> **Betalingsjournal** i Finance.
2. Velg **Linjer** i en betalingsjournal du angav tidligere.
3. På **Leverandørbetalinger**-siden merker du alle radene i rutenettet.
4. Velg **Betalingsstatus** \> **Ingen**.

    ![Betalinger for behandling på Leverandørbetalinger-siden.](../media/er-design-configuration-word-2016-11-image05.png)

5. Velg **Generer betalinger** i handlingsruten.
6. Følg denne fremgangsmåten i dialogboksen som vises:

    1. Velg **Elektronisk** i feltet **Betalingsmåte**.
    2. Velg **GBSI OPER** i feltet **Bankkonto**.
    3. Velg **OK**.

7. I dialogboksen **Parametere for elektronisk rapport** velger du **OK**.
8. De genererte utdataene vises i Word-format og inneholder detaljene for de behandlede betalingene. Analyser de genererte utdataene.

    ![Genererte utdata i Word-format.](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Tilleggsressurser

- [Utforme en ny ER-konfigurasjon for å generere rapporter i Word-format](../er-design-configuration-word.md)
- [Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
