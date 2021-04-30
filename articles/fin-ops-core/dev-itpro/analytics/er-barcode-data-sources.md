---
title: Bruke strekkodedatakilder for å generere strekkodebilder
description: Dette emnet forklarer hvordan du bruker strekkodedatakilder for å generere strekkodebilder.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: cbc2b5870e855ff4d4a099a51cbb6887dd30bba7
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893558"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Bruke strekkodedatakilder for å generere strekkodebilder

[!include[banner](../includes/banner.md)]

Du kan bruke rammeverket [Elektronisk rapportering (ER)](general-electronic-reporting.md) til å utforme [ER-formatkomponenter](general-electronic-reporting.md#FormatComponentOutbound) som du kan kjøre for å generere elektroniske og utskrivbare utgående dokumenter som du trenger. Hvis du vil generere et utgående dokument i Microsoft Office-format, må du angi oppsettet for rapporten ved å bruke enten et Microsoft Excel-dokument eller et Microsoft Word-dokument som en rapportmal. Med [ER-operasjonsutforming](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) kan du legge ved et Excel- eller Word-dokument som en mal for et ER-format. Følgende navngitte elementer i den tilknyttede malen er knyttet til elementene i den konfigurerte formatkomponenten:

- Innholdskontroller i Word
- Navngitte ark, områder, celler, figurer og bilder i Excel

Disse navngitte elementene brukes som plassholdere for data som registreres i et generert dokument når et ER-format kjøres. ER-formatelementer er bundet til datakilder. Disse datakildene angir dataene som blir lagt inn i de genererte dokumentene under kjøring. Hvis du vil ha mer informasjon, se [Bygge inn bilder og figurer i dokumenter d.u genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md).

ER støtter nå **Strekkode**-datakildetypen. Derfor kan du nå generere en avbildning som representerer strekkoden for angitt tekst. Når du konfigurerer et ER-format, kan du angi datakilder for **Strekkode**-typen for å generere strekkodebilder. Du kan deretter legge til disse bildene i genererte forretningsdokumenter, for eksempel ordrer, fakturaer, følgesedler og kvitteringer. Du kan også legge dem til i ulike typer etiketter, for eksempel produkt- og hylleetiketter og etiketter for pakking og levering.

Følgende plassholdere kan brukes i rapportmaler til å angi strekkodebilder:

- [Bilde](/office/client-developer/word/content-controls-in-word)-innholdskontroll for Word
- [Bilde](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344)-objekt i Excel

Ved å bruke en datakilde av typen **Strekkode** kan du generere strekkoder i følgende formater:

- Endimensjonale strekkoder:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Intelligent Mail
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Todimensjonale strekkoder:

    - Aztec
    - Data Matrix
    - QR-kode

Når du konfigurerer en **Strekkode**-datakilde, kan du definere bestemte gjengivelsesparametere som brukes til å generere et bilde:

- **Bredde** – Angi strekkodeens bredde i piksler. En verdi på **0** (null) angir at standardbredden er brukt. Betydningen kan variere for ulike formater.
- **Høyde** – Angi strekkodeens høyde i piksler. En verdi på **0** (null) angir at standardhøyden er brukt. Betydningen kan variere for ulike formater.
- **Marg** – Angi størrelsen på strekkodens marg i piksler. Margen er området på hver side av en strekkode som må holdes tom (stillesone). En verdi på **0** (null) angir at standardmargen er brukt. Betydningen kan variere for ulike formater.
- **Utdatainnhold** – Sett verdien til **Ja** for å generere et strekkodebilde som inneholder den kodede informasjonen som tekst. Standardverdien er **Nei**.
- **Koding** – Angir tegntypen som er kodet i det genererte strekkodebildet. Som standard brukes **UTF-8**-koding.

> [!IMPORTANT]
> Når du legger til en **Strekkode**-datakilde, må du plassere den under et annet element (container) som et nestet element.
>
> Når du binder en **Strekkode**-datakilde til et celleelement i et format, og celleelementet representerer enten en Word-innholdskontroll eller et Excel-bilde, presenteres datakilden i denne bindingen som en funksjon som har en enkelt parameter av typen **Streng**. Du må bruke denne parameteren til å angi teksten som skal transformeres til et strekkodebilde og leses når en generert strekkode skannes.

Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplene i dette emnet.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Eksempel: Generer en betalingssjekk som inneholder en strekkode som koder det skyldige beløpet

Dette eksemplet viser hvordan en bruker i rollen **Systemansvarlig** eller **Funksjonell konsulent for elektronisk rapportering** kan konfigurere et ER-format som inneholder en mal som brukes til å generere et utgående dokument i Excel-format som inneholder en strekkode. Her er en oversikt over fremgangsmåten som er involvert.

1. [Fullfør forutsetningene](#ExamplePrerequisites).
2. [Aktivere en konfigurasjonsleverandør](#ExampleProvider).
3. [Importere den angitte ER-løsningen](#ExampleImportSolution).
4. [Generere en betalingssjekk](#ExampleGenerateCheque).
5. [Se gjennom den genererte betalingssjekken](#ExampleReviewGeneratedCheque).
6. [Endre formatet til den angitte ER-løsningen](#ExampleModifyFormat).

    1. [Bruke en ny sjekkmal](#ExampleModifyFormatApplyTemplate).
    2. [Legge til en ny strekkodedatakilde](#ExampleModifyFormatAddDataSource).
    3. [Binde et nytt formatelement](#ExampleModifyFormatBindFormatElement).
    4. [Gjøre den endrede versjonen tilgjengelig for testutførelser](#ExampleModifyFormatMakeVersionAvailable).

        1. [Fullføre den endrede formatversjonen](#CompleteToRun).
        2. [Gjøre utkastversjonen tilgjengelig for bruk](#MarkToRun).

7. [Generere en betalingssjekk](#ExampleGenerateCheque2).
8. [Konvertere den genererte sjekken til en PDF-fil](#ExampleConvertToPDF).

I dette eksemplet skal du bruke den angitte ER-løsningen som er konfigurert, til å generere betalingssjekker. Denne løsningen genererer betalingssjekker der beløpet for innkjøpet er skrevet både som et nummer og som tekst. Du skal endre denne ER-løsningen, slik at sjekken også inneholder en generert strekkode der beløpet som skal betales, er kodet og kan leses ved hjelp av en strekkodeskanner.

Trinnene kan fullføres i **USMF**-selskapet i Microsoft Dynamics 365 Finance.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Fullfør forutsetningene

For å fullføre dette eksempelet må du ha tilgang til USMF-selskapet i Finans for en av følgende roller:

- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

Hvis du enda ikke har utført eksempelet i emnet [Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md), laster du ned følgende konfigurasjoner av ER-eksempelløsningen.

| Innholdsbeskrivelse         | Filnavn                   |
|-----------------------------|-----------------------------|
| ER-datamodellkonfigurasjon | Modell for sjekker.xml       |
| ER-formatkonfigurasjon     | Utskriftsformat for sjekker.xml |

I tillegg laster du ned følgende Excel-fil som inneholder den endrede malen for den angitte ER-løsningen.

| Innholdsbeskrivelse | Filnavn                 |
|---------------------|---------------------------|
| Rapportmal     | Sjekkmal Excel.xlsx |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Aktivere en konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, må du sørge for at [konfigurasjonsleverandør](general-electronic-reporting.md#Provider) for eksempelselskapet **Litware, Inc.** er oppført, og at den er merket som aktiv. Hvis den ikke er oppført, eller hvis den ikke er merket som aktiv, følger du trinnene i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Angi eksempelselskapet som aktivt på Lokaliseringskonfigurasjoner-siden](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Importere den angitte ER-løsningen

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden, hvis **Modell for sjekker**-konfigurasjonen ikke er tilgjengelig i konfigurasjonstreet, følger du disse trinnene for å importere ER-datamodellkonfigurasjonen:

    1. I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.
    2. I dialogboksen velger du **Bla gjennom**, finner og velger **Modell for sjekker.xml**-filen og velger deretter **OK**.

4. Hvis **Utskriftsformat for sjekker**-konfigurasjonen ikke er tilgjengelig i konfigurasjonstreet, følger du disse trinnene for å importere ER-formatkonfigurasjonen:

    1. I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.
    2. I dialogboksen velger du **Bla gjennom**, finner og velger **Utskriftsformat for sjekker.xml**-filen og velger deretter **OK**.

5. Utvid **Modell for sjekker** i konfigurasjonstreet.
6. Gjennomgå listen over importerte ER-konfigurasjoner i konfigurasjonstreet.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Generere en betalingssjekk

1. Gå til **Kontant- og bankbehandling** \> **Bankkontoer** \> **Bankkontoer**.
2. Velg kontoen **USMF OPER** på siden **Bankkontoer**.
3. På siden for bankkontodetaljer, i handlingsruten i kategorien **Oppsett** i gruppen **Oppsett**, velger du **Sjekk**.
4. Velg **Rediger** på siden **Sjekkutforming**.
5. I hurtigfanen **Generelt** setter du alternativet **Generelt elektronisk eksportformat** til **Ja**.
6. I feltet **Eksportformatkonfigurasjon** velger du ER-formatet **Utskriftsformat for sjekker** som du importerte tidligere.
7. Velg **Skriv ut test** i handlingsruten.
8. I dialogboksen angir du **Sjekkformat som kan forhandles** til **Ja**, og deretter velger du **OK**.

    ![Dialogboksen Sjekkutforming – Skriv ut test](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Se gjennom den genererte betalingssjekken

- Åpne den genererte sjekken i Excel.
2. Se gjennom den genererte sjekken.

    ![Generert betalingsjekk i Excel](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Endre formatet til den angitte ER-løsningen

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Bruke en ny sjekkmal

Du kan bruke Excel-skrivebordsprogrammet til å åpne filen **Sjekkmal Excel.xlsx** du importerte tidligere. Legg merke til at denne malen er forskjellig fra malen som du brukte til å generere en betalingssjekk i den angitte ER-løsningen. I tillegg inneholder den et **AmountBarcode**-element for strekkodebildet.

![AmountBarcode-element i Excel-malen](./media/er-barcode-data-source-cheque2.png)

Du må nå endre ER-løsningen og deretter bruke den endrede malen [på nytt](modify-electronic-reporting-format-reapply-excel-template.md).

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du **Rapporteringskonfigurasjoner**.
3. På siden **Konfigurasjoner**, i konfigurasjonstreet, utvider du **Modell for sjekker** og velger **Utskriftsformat for sjekker**.
4. Velg **Utforming** i handlingsruten.
5. I ER-operasjonsutforming velger du kategorien **Tildeling** til høyre på siden, og deretter velger du **Vis/skjul** i formattreruten til venstre.
6. Legg merke til at alle celleformatelementene er bundet til de riktige datakildene.

    ![Binding av celleformatelementer til datakilder i ER-operasjonsutformingen](./media/er-barcode-data-source-cells-bound.png)

7. Velg kategorien **Format** til høyre på siden.
8. Velg ellipsen (**...**) i handlingsruten, og velg deretter **Importer**.
9. I gruppen **Importer** velger du **Oppdater fra Excel**, og deretter velger du **Oppdater mal**.
10. I dialogboksen blar du til filen **Sjekkmal Excel.xlsx** som er lagret på datamaskinen, merker den og velger **OK** for å bekrefte at den valgte malen skal brukes.
11. Velg kategorien **Tildeling** til høyre på siden, og deretter velger du **Vis/skjul** i formattreruten til venstre.
12. Merk at celleelementet **AmountBarcode** er lagt til i formatet. Dette elementet er knyttet til **AmountBarcode**-elementet som er lagt til i den endrede Excel-malen som en plassholder for et strekkodebilde.

    ![AmountBarcode-celleelement lagt til i formatet i ER-operasjonsutforming](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Legge til en ny strekkodedatakilde

Deretter må du legge til en ny datakilde av typen **Strekkode**.

1. I ER-operasjonsutforming, i kategorien **Tilordning** til høyre på siden, velger du datakilden for **utskrift**.
2. Velg **Legg til**, og deretter, i **Funksjoner**-gruppen, velger du datakildetypen **Strekkode**.

    ![Velge datakildetypen Strekkode](./media/er-barcode-data-source-add.png)

3. Skriv inn **strekkode** i **Navn**-feltet.
4. I **Strekkodeformat** velger du **Kode 128**.
5. I feltet **Bredde** angir du **500**.
6. Velg **OK**.

    ![Dialogboksen Egenskaper for datakilde](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Binde et nytt formatelement

Deretter må du binde det nye formatelementet til datakilden du nettopp la til.

1. I ER-operasjonsutforming, i kategorien **Tilordning** til høyre på siden, velger du datakilden **skriv ut\\strekkode**.
2. I formateringstreruten til venstre merker du celleelementet **AmountBarcode**, og deretter velger du **Bind**.
3. Velg **Vis detaljer** i handlingsruten.
4. Vær oppmerksom på at fordi **Strekkode**-datakilden er representert i bindingen som en funksjon som inneholder én enkelt parameter, blir navnet på det bundne formatelementet automatisk tatt opp som argument for den parameteren.

    ![Detaljer om strekkodedatakilden i ER-operasjonsutforming](./media/er-barcode-data-source-bind1.png)

5. Velg **Rediger formel** for å justere bindingen.

    Du vil ikke at navnet på celleelementet skal returneres. Derfor må du konfigurere et uttrykk som returnerer tekst som inneholder beløpet som skal betales på den gjeldende sjekken. Fordi det overordnede **ChequeLines**-området er bundet til **model.cheques**-datakilden, er beløpet på den gjeldende sjekken tilgjengelig i feltet **model.cheques.attributes.amount** for datatypen **Reell**.

6. I **Formel**-feltet angir du **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.
7. Velg **Lagre**, og lukk deretter [ER-formeldesigneren](general-electronic-reporting-formula-designer.md).
8. Legg merke til at bindingen er justert.

    ![Justert binding i ER-operasjonsutforming](./media/er-barcode-data-source-bind2.png)

9. Velg **Lagre**, og lukk deretter ER-operasjonsutforming.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Gjør den endrede versjonen tilgjengelig for testkjøringer

Som standard brukes de eneste versjonene som har statusen **Fullført** og **Delt** når du kjører et ER-format.

Hvis du har fullført endringene, kan du fullføre arbeidet med den gjeldende kladdeversjonen og gjøre endringene tilgjengelige for bruk. Hvis du vil ha instruksjoner, se delen [Fullføre den endrede formatversjonen](#CompleteToRun) nedenfor.

Hvis du vil fortsette å arbeide med den gjeldende kladdeversjonen, men du må bruke den til å generere sjekker, må du eksplisitt angi at du vil bruke kladdeversjonen av formatet for utførelsen. Hvis du vil ha instruksjoner, kan du se delen [Gjøre utkastversjonen tilgjengelig for bruk](#MarkToRun).

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Fullføre den endrede formatversjonen

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du **Rapporteringskonfigurasjoner**.
3. På siden **Konfigurasjoner**, i konfigurasjonstreet, utvider du **Modell for sjekker** og velger **Utskriftsformat for sjekker**.
4. I hurtigfanen **Versjoner** velger du posten med statusen **Utkast**.
5. Velg **Endre status**, og velg deretter **Fullfør**.
6. Klikk **OK** i dialogboksen.

Statusen for gjeldende versjon endres fra **Utkast** til **Fullført**, og det opprettes en ny versjon med statusen **Utkast**. Du kan bruke den nye kladdeversjonen til å legge til flere endringer.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Gjøre utkastversjonen tilgjengelig for bruk

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
4. I dialogboksen setter du **Kjøringsinnstillinger** til **Ja**, og deretter velger du **OK**.
5. I konfigurasjonstreet utvider du **Modell for sjekker** og velger **Utskriftsformat for sjekker**.
6. Sett **Kjør utkast**-alternativet til **Ja**.
7. Velg **Lagre**.

Utkastversjonen av det valgte formatet er merket som tilgjengelig for bruk når det valgte formatet er kjørt.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Generere en betalingssjekk

1. Gå til **Kontant- og bankbehandling** \> **Bankkontoer** \> **Bankkontoer**.
2. Velg kontoen **USMF OPER** på siden **Bankkontoer**.
3. På siden for bankkontodetaljer, i handlingsruten i kategorien **Oppsett** i gruppen **Oppsett**, velger du **Sjekk**.
4. På siden **Sjekkutforming** i handlingsruten velger du **Skriv ut test**.
5. I dialogboksen setter du alternativet **Sjekkformat som kan forhandles** til **Ja**.
6. Velg **OK**.
7. Se gjennom den genererte sjekken. Legg merke til at det er generert en strekkode for å kode beløpet på sjekken.

    ![Generert betalingssjekk strekkode i Excel](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Det oppstår et unntak hvis argumentet til en **Strekkode**-datakilde ikke samsvarer med de nødvendige kravene som er spesifikke for strekkodeformatet. Hvis for eksempel datakilden **Strekkode** kalles for å generere en [EAN-8](https://wikipedia.org/wiki/EAN-8)-strekkode for den angitte teksten, oppstår det et unntak hvis lengden på teksten overskrider sju tegn.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Konvertere den genererte sjekken til en PDF-fil

Som beskrevet i emnet [Generere FTI-skjemaer som kan skrives ut](er-generate-printable-fti-forms.md#finland), kan du bruke en spesiell skrift til å produsere strekkoder i et generert dokument. I dette tilfellet kan ytterligere transformasjoner av det genererte dokumentet være avhengig av tilgjengeligheten til skriften i transformasjonsmiljøet. Hvis du for eksempel prøver å konvertere et dokument til PDF-format eller forhåndsvise det i et miljø der skriften mangler, gjengis ikke strekkodene riktig.

Når du bruker datakilden **Strekkode** til å produsere strekkoder, er ikke gjengivelse av disse strekkodene avhengige av noen skrifttyper. Derfor er det enkelt å konvertere dokumenter som inneholder strekkodene, til PDF-format. Følgende illustrasjon viser forhåndsvisningen av en generert betalingskontroll som er [konvertert](electronic-reporting-destinations.md#OutputConversionToPDF) til en PDF-fil, basert på innstillingen for den konfigurerte ER-[destinasjonen](electronic-reporting-destinations.md).

![Forhåndsvise PDF-filen for en betalingssjekk](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Begrensninger

> [!NOTE]
> Noen typer strekkoder som genereres, har et fast størrelsesforhold. Denne virkemåten gir mening hvis du har aktivert funksjonen **Aktivere bruken av EPPlus-bibliotek i Rammeverk for elektronisk rapportering** for å arbeide med Excel-dokumenter i ER. I så fall angis det et bilde i en plassholder som har et låst størrelsesforhold. Når dimensjonene i en plassholder i en mal samsvarer med størrelsesforholdet til et bilde som legges inn, kan det derfor hende at størrelsen på et reelt bilde i et generert dokument endres for å opprettholde det nødvendige størrelsesforholdet. Du kan unngå å endre størrelsen på bildet ved å bruke en plassholder som har et forventet størrelsesforhold.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Mål for elektronisk rapportering](electronic-reporting-destinations.md)
- [Formelspråk i elektronisk rapportering](er-formula-language.md)
- [NUMBERFORMAT-funksjonen](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]