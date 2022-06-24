---
title: Utform et ER-format for å paginere genererte dokumenter i Excel
description: Denne artikkelen beskriver hvordan du utformer et ER-format (Electronic reporting) som paginerer et generert dokument i Microsoft Excel.
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.openlocfilehash: e8edc8bba62f74b4f81d423cf75b5fb87c01e43f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909285"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>Utform et ER-format for å paginere genererte dokumenter i Excel

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan en bruker i rollen som systemadministrator eller funksjonsrådgiver for elektronisk rapportering kan konfigurere et [ER-format](general-electronic-reporting.md) (elektronisk rapportering) til å generere utgående dokumenter i Microsoft Excel og administrere dokumentpaginering.

I dette eksemplet vil du endre ER-formatet som følger med Microsoft, som brukes til å skrive ut kontrollrapporten når Intrastat-deklareringen [genereres](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Med denne rapporten kan du observere rapporterte Intrastat-transaksjoner. Endringene dine gir deg tilgang til å administrere pagineringen av kontrollrapporter som genereres.

Prosedyrene i denne artikkelen kan fullføres i **DEMF**-firmaet. Ingen koding er nødvendig. Før du starter kan du laste ned og lagre følgende filer.

| beskrivelse       | Filnavn |
|-------------------|-----------| 
| Rapportmal 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Rapportmal 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>Konfigurere ER-rammeverket

Følg trinnene i [Konfigurere ER-rammeverket](er-quick-start2-customize-report.md#ConfigureFramework) for å konfigurere minimumssettet med ER-parametere. Du må fullføre dette oppsettet før du begynner å bruke ER-rammeverket til å utforme en egendefinert versjon av et standard ER-format.

## <a name="import-the-standard-er-format-configuration"></a>Importere standard ER-formatkonfigurasjon

Følg trinnene i [Importere standard ER-formatkonfigurasjon](er-quick-start2-customize-report.md#ImportERSolution1) for å legge til standard ER-konfigurasjoner i gjeldende forekomst av Dynamics 365 Finance. Importer versjon **1.9** av **Intrastat-rapport**-formatkonfigurasjonen. Basisversjon 1 av basiskonfigurasjonen for **Intrastat-modell** importeres automatisk fra repositoriet.

## <a name="customize-the-standard-er-format"></a>Tilpasse standard ER-format

### <a name="create-the-custom-er-format"></a>Opprette det egendefinerte ER-formatet

I dette scenariet er du representant for Litware, Inc, som for øyeblikket er valgt som aktiv ER-konfigurasjonsleverandør. Du må opprette en ny ER-formatkonfigurasjon ved å bruke **Intrastat-rapport**-konfigurasjonen som en basis.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. I konfigurasjonstreet i venstre rute utvider du **Intrastat-modell** og velger **Intrastat-rapport** på siden **Konfigurasjon**. Litware, Inc. bruker versjon 1.9 av denne ER-formatkonfigurasjonen som grunnlaget for den egendefinerte versjonen.
3. Velg **Opprett konfigurasjon** for å åpne nedtrekksdialogen. Du kan bruke denne dialogboksen til å opprette en ny konfigurasjon for et egendefinert betalingsformat.
4. I **Ny**-feltgruppen velger du **Avled fra navnet: Intrastat, Microsoft**.
5. I **Navn**-feltet skriver du inn **Intrastat-rapport Litware**.
6. Velg **Opprett konfigurasjon** for å opprette det nye formatet.

Versjon 1.9.1 av ER-formatkonfigurasjonen **Intrastat-rapport Litware** er opprettet. Denne versjonen har [statusen](general-electronic-reporting.md#component-versioning) **Utkast** og kan redigeres. Det gjeldende innholdet i egendefinert ER-format samsvarer med innholdet i formatet som leveres av Microsoft.

### <a name="make-the-custom-format-runnable"></a>Merke det egendefinerte formatet som kjørbart

Nå som den første versjonen av det egendefinerte formatet er opprettet og har statusen **Utkast**, kan du kjøre formatet for testformål. Når du skal kjøre rapporten, behandler du en leverandørbetaling ved å bruke betalingsmåten som refererer til det egendefinerte ER-formatet. Som standard [vurderes](general-electronic-reporting.md#component-versioning) bare versjonene som har statusen **Fullført** eller **Delt** når du kaller opp et ER-format fra programmet. Denne virkemåten hjelper til med å forhindre at ER-formater som har uferdige utforminger, brukes. Testingen kjøres imidlertid ved at du kan tvinge programmet til å bruke versjonen av ER-formatet som har statusen **Utkast**. På denne måten kan du justere gjeldende formatversjon hvis det kreves endringer. Hvis du vil ha mer informasjon, kan du se [Relevans](electronic-reporting-destinations.md#applicability).

Hvis du vil bruke utkastversjonen av et ER-format, må du eksplisitt markere ER-formatet.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. I dialogboksen **Brukerparametere** setter du **Kjøringsinnstillinger** til **Ja**, og deretter velger du **OK**.
4. Velg **Rediger** for å gjøre gjeldende side redigerbar, hvis nødvendig.
5. I konfigurasjonstreet i venstre rute velger du **Intrastat-rapport Litware**.
6. Sett alternativet **Kjør utkast** til **Ja**, og velg deretter **Lagre**.

    ![Alternativet Kjør utkast på Konfigurasjoner-siden.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Konfigurere utenrikshandelsparametere for å bruke det egendefinerte ER-formatet

Følg denne fremgangsmåten for å konfigurere utenrikshandelsparametere slik at du kan bruke det egendefinerte formatet.

1. Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **Utenrikshandelsparametere**.
2. På fanen **Utenrikshandelsparametere** i hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du Intrastat **Intrastat-rapport Litware**.
3. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport Litware**.
4. Velg **Lagre**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Konfigurere det egendefinerte formatet for å bruke den nedlastede rapportmalen

### <a name="review-the-first-downloaded-excel-template"></a>Gå gjennom den første nedlastede Excel-malen

1. Åpne malfilen **ERIntrastatReportDemo1.xlsx** du lastet ned tidligere, i skrivebordsversjonen av Excel.
2. Kontroller at malen inneholder navngitte områder for å opprette rapporthode, rapportdetaljer og bunntekstdeler i genererte dokumenter.

    ![Oppsettet i Excel-mal 1 i skrivebordsprogrammet.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Erstatte den gjeldende Excel-malen i det egendefinerte ER-formatet

Du må legge til en ny Excel-mal i det egendefinerte ER-formatet.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På siden **Konfigurasjoner** i konfigurasjonstreet i venstre ruten utvider du **Intrastat-modell** \> **Intrastat-rapport**, og velg konfigurasjonen **Intrastat-rapport Litware**.
3. Velg **Utforming**.
4. På siden **Formatutforming**, i handlingsruten, velger du **Vis detaljer**.
5. Kontroller at komponenten for **Intrastat: Excel**-rotformat er valgt, og deretter, i handlingsruten i fanen **Import** i gruppen **Import**, velger du **Oppdater fra Excel**.
6. I dialogboksen **Oppdater fra Excel** velger du **Oppdater mal**.
7. I dialogboksen **Åpne** blar du til og velger filen **ERIntrastatReportDemo1.xlsx** som du lastet ned tidligere, og deretter velger du **Åpne**.
8. Velg **OK**.
9. Velg **Lagre**.

![Formatstrukturen i ER-formatdesigneren etter at den nye Excel-malen er lagt til.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Endre databindingen slik at den viser varebeskrivelsen i en generert rapport

1. Velg kategorien **Tilordning** på **Formatutforming**-siden.
2. Utvid **Intrastat** \> **Rapportlinjer**, og velg **Artikkelkode**-komponent.
3. Velg **Rediger formel**.
4. Endre den bindende formelen fra `@.CommodityCode` til `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Velg **Lagre**.

![Konfigurert binding for å vise varebeskrivelsen i ER-formatutforming.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Generere en Intrastat-deklarasjonskontrollrapport

Først kontrollerer du at du har Intrastat-transaksjoner til rapportering på **Intrastat**-siden.

![Transaksjoner på Intrastat-siden.](./media/er-paginate-excel-reports-transactions1.gif)

Deretter bruker du det egendefinerte Er-formatet til å generere kontrollrapporten for Intrastat-deklareringen.

1. Gå til **Avgift** \> **Deklareringer** \> **Utenrikshandel** \> **Intrastat**.
2. På siden **Intrastat** på handlingsruten velger du **Utlevering** \> **Rapport**.
3. Følg denne fremgangsmåten for å kjøre rapporten i dialogboksen **Intrastat-rapport**:

    1. Angi **Fra dato**- og **Til dato**-feltene slik at de inneholder bestemte Intrastat-transaksjoner i rapporten.
    2. Sett alternativet **Generer fil** til **Nei**.
    3. Sett alternativet **Generer rapport** til **Ja**.
    4. Velg **OK**.

4. Last ned og lagre dokumentet som genereres.
5. Åpne dokumentet i Excel, og se gjennom det.

    ![Generert Excel-dokument i skrivebordprogrammet.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Konfigurer det egendefinerte formatet for å paginere genererte dokumenter

### <a name="review-the-second-downloaded-excel-template"></a>Gå gjennom den andre nedlastede Excel-malen

1. I Excel åpner du malfilen **ERIntrastatReportDemo2.xlsx** du lastet ned tidligere.
2. Sammenlign denne malen med malen **ERIntrastatReportDemo1.xlsx**, og kontroller at den inneholder flere nye Excel-navn for å opprette og fylle ut sidespesifikke deler i genererte dokumenter:

    - Området **ReportPageHeader** legges til for opprette sidehoder.
    - Området **ReportPageFooter** legges til for opprette sidebunntekster.
    - Cellen **ReportPageFooter\_PageLines** er konfigurert til å vise antall transaksjoner per side.
    - Cellen **ReportPageFooter\_PageAmount** er konfigurert til å vise totalt antall transaksjoner per side.
    - Cellen **ReportPageFooter\_PageWeight** er konfigurert til å vise total vekt av transaksjoner per side.
    - **ReportPageFooter\_RunningCounterLines**-cellen er konfigurert til å vise telleren for transaksjoner fra begynnelsen av rapporten via den gjeldende siden.
    - **ReportPageFooter\_RunningTotalAmount**-cellen er konfigurert til å vise beløp som løper totalt for alle transaksjoner fra begynnelsen av rapporten via den gjeldende siden.
    - **ReportPageFooter\_RunningTotalWeight**-cellen er konfigurert til å vise vekt som løper totalt for transaksjoner fra begynnelsen av rapporten via den gjeldende siden.

    ![Oppsettet i Excel-mal 2 i skrivebordsprogrammet.](./media/er-paginate-excel-reports-template2a.gif)

    **CommodityCode**-cellen i denne malen er konfigurert til å bryte celletekst. Fordi transaksjonsdetaljraden er konfigurert slik at den automatisk vil passe høyden på en rad, må høyden på hele raden automatisk endres når teksten i **CommodityCode**-cellen brytes.

    ![CommodityCode-cellen konfigurert til å bryte celletekst.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Gjenta erstatningen i den gjeldende Excel-malen i det egendefinerte ER-formatet

1. Følg trinnene i [Erstatte den gjeldende Excel-malen i det egendefinerte ER-formatet](#replace-template)-delen i denne artikkelen. I trinn 7 velger du imidlertid filen **ERIntrastatReportDemo2.xlsx**.
2. På siden **Formatutforming** utvider du **Intrastat**.
3. Gi navn til formatkomponentene [Område](er-fillable-excel.md#range-component) som er lagt til i ER-formatet for å synkronisere strukturen med strukturen i den brukte Excel-malen:

    1. Velg **Område**-komponenten som er knyttet til Excel-navnet **ReportPageHeader**.
    2. I fanen **Format** i feltet **Navn** angir du **Rapportsidetopptekst**.
    3. Velg **Område**-komponenten som er knyttet til Excel-navnet **ReportPageFooter**.
    4. I fanen **Format** i feltet **Navn** angir du **Rapportsidebunntekst**.

4. Velg **Lagre**.

![Formatstrukturen i ER-formatdesigneren etter at Excel-malen er erstattet.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Endre formatstrukturen for å implementere dokumentpaginering

1. På siden **Formatutforming** i formattreet i venstre rute velger du **Intrastat**-rotkomponenten.
2. Velg **Legg til**.
3. I dialogboksen **Legg til** velger du [Side](er-fillable-excel.md#page-component)-komponenten i **Excel**-gruppen av komponenter.
4. I dialogboksen **Komponentegenskaper** i feltet **Navn** angir du **Rapportside**. Velg deretter **OK**.
5. For å bruke komponenten **Rapportsidetopptekst** som en sidetopptekst på hver genererte side følger du disse trinnene:

    1. Velg komponenten **Rapportsidetopptekst**, og velg deretter **Klipp ut**.
    2. Velg komponenten **Rapportside**, og velg deretter **Lim inn**.
    3. Utvid **Rapportside**.
    4. Hvis du vil tvinge **Side**-komponenten til å [vurdere](er-fillable-excel.md#page-component-structure) dette området som en sidetopptekst, velger du **Rapportsidetopptekst**, og deretter, i fanen **Format** i feltet **Replikeringsretning** velger du **Ingen replikering**.

6. Følg denne fremgangsmåten for å paginere et generert dokument, slik at innholdet på rapportlinjer vurderes:

    1. Velg komponenten **Rapportlinjer**, og velg deretter **Klipp ut**.
    2. Velg komponenten **Rapportside**, og velg deretter **Lim inn**.

7. Følg denne fremgangsmåten for å inkludere bunnteksten i rapporten etter rapportlinjer, men før den siste bunnteksten på siden:

    1. Velg komponenten **Rapportbunntekst**, og velg deretter **Klipp ut**.
    2. Velg komponenten **Rapportside**, og velg deretter **Lim inn**.

8. For å bruke komponenten **Rapportbunntekst** som en sidebunntekst på hver genererte side følger du disse trinnene:

    1. Velg komponenten **Rapportsidebunntekst**, og velg deretter **Klipp ut**.
    2. Velg komponenten **Rapportside**, og velg deretter **Lim inn**.
    3. Hvis du vil tvinge **Side**-komponenten til å [vurdere](er-fillable-excel.md#page-component-structure) dette området som en sidebunntekst, velger du **Rapportsidebunntekst**, og deretter, i fanen **Format** i feltet **Replikeringsretning** velger du **Ingen replikering**.

![Formatstrukturen i ER-formatdesigneren etter at dokumentpaginering er implementert.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Legge til datakilder for å beregne bunnteksttotaler

Du må konfigurere nye datakilder til å beregne sidetotalen, telleren og totalverdiene for kjøring, og vise dem i bunntekstdelen på siden. Det anbefales at du bruker [Datainnsamling](er-data-collection-data-sources.md)-datakilder til dette formålet.

1. Velg kategorien **Tilordning** på **Formatutforming**-siden.
2. Velg **Legg til rot**, og følg deretter denne fremgangsmåten:

    1. I **Legg til datakilde**-dialogboksen i delen **Generelt** velger du **Tom beholder**.
    2. I dialogboksen **Tom beholder-datakildeegenskaper** i feltet **Navn** angir du **Total**.
    3. Velg **OK**.

3. Velg **Total**-datakilde, velg **Legg til**, og følg deretter denne fremgangsmåten:

    1. I **Legg til datakilde**-dialogboksen i delen **Generelt** velger du **Tom beholder**.
    2. I dialogboksen **Tom beholder-datakildeegenskaper** i feltet **Navn** angir du **Side**.
    3. Velg **OK**.

4. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Legg til datakilde**-dialogboksen i delen **Generelt** velger du **Tom beholder**.
    2. I dialogboksen **Tom beholder-datakildeegenskaper** i feltet **Navn** angir du **Kjører**.
    3. Velg **OK**.

5. Velg **Total.Page**-datakilde, velg **Legg til**, og følg deretter denne fremgangsmåten:

    1. I **Legg til datakilde**-dialogboksen i delen **Funksjoner** velger du **Datainnsamling**.
    2. I dialogboksen **Datakildeegenskaper for datainnsamling** i feltet **Navn** angir du **Beløp**.
    3. Velg **Faktisk** i **Varetype**-feltet.
    4. Sett **Samle inn alle verdier**-alternativet til **Ja**.
    5. Velg **OK**.

6. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Legg til datakilde**-dialogboksen i delen **Funksjoner** velger du **Datainnsamling**.
    2. I dialogboksen **Datakildeegenskaper for datainnsamling** i feltet **Navn** angir du **Vekt**.
    3. Velg **Faktisk** i **Varetype**-feltet.
    4. Sett **Samle inn alle verdier**-alternativet til **Ja**.
    5. Velg **OK**.

7. Velg **Total.Running**-datakilde, velg **Legg til**, og følg deretter denne fremgangsmåten:

    1. I **Legg til datakilde**-dialogboksen i delen **Funksjoner** velger du **Datainnsamling**.
    2. I dialogboksen **Datakildeegenskaper for datainnsamling** i feltet **Navn** angir du **Beløp**.
    3. Velg **Faktisk** i **Varetype**-feltet.
    4. Sett **Samle inn alle verdier**-feltet til **Ja**.
    5. Velg **OK**.

8. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Legg til datakilde**-dialogboksen i delen **Funksjoner** velger du **Datainnsamling**.
    2. I dialogboksen **Datakildeegenskaper for datainnsamling** i feltet **Navn** angir du **Vekt**.
    3. Velg **Faktisk** i **Varetype**-feltet.
    4. Sett **Samle inn alle verdier**-feltet til **Ja**.
    5. Velg **OK**.

9. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Legg til datakilde**-dialogboksen i delen **Funksjoner** velger du **Datainnsamling**.
    2. I dialogboksen **Datakildeegenskaper for datainnsamling** i feltet **Navn** angir du **Linjer**.
    3. Velg **Heltall** i feltet **Varetype**.
    4. Sett **Samle inn alle verdier**-feltet til **Ja**.
    5. Velg **OK**.

10. Velg **Lagre**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Legge til datakilder for å kontrollere sidebunntekstsynlighet

Hvis du planlegger å kontrollere bunnteksten på siden, og du ikke planlegger å inkludere bunnteksten på den siste siden hvis den inneholder transaksjoner, konfigurerer du en ny datakilde til å beregne den kjørende telleren.

1. Velg kategorien **Tilordning** på **Formatutforming**-siden.
2. Velg **Total.Running**-datakilden, og velg **Legg til**.
3. I **Legg til datakilde**-dialogboksen i delen **Funksjoner** velger du **Datainnsamling**.
4. I dialogboksen **Datakildeegenskaper for datainnsamling** i feltet **Navn** angir du **Lines2**.
5. Velg **Heltall** i feltet **Varetype**.
6. Sett **Samle inn alle verdier**-alternativet til **Ja**.
7. Velg **OK**.
8. Velg **Lagre**.

![Legge til datakilder i ER-formatutforming.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Konfigurere bindinger til å samle inn totalverdier

1. På siden **Formatutforming**, i formattreet, utvider du **Rapportlinjer**-komponenten, og velg komponenten **Fakturaverdi**.
2. Velg **Rediger formel**.
3. Endre den bindende formelen fra `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` til `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > I tillegg til å legge beløpsverdien i en Excel-celle for hver itererte transaksjon samler denne bindingen inn verdien i datasamlingen **Total.Page.Amount**.

4. Velg den nestede **Vekt**-komponenten.
5. Velg **Rediger formel**.
6. Endre den bindende formelen fra `@.'$RoundedWeight'` til `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > I tillegg til å legge vektverdien i en Excel-celle for hver itererte transaksjon samler denne bindingen inn verdien i datasamlingen **Total.Page.Weight**.

![Konfigurer bindinger for innsamling av totalverdier i ER-formatdesigneren.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Konfigurere bindinger til å fylle ut bunnteksttotaler

1. På siden **Formatutforming**, i formattreet, utvider du komponenten **Rapportsidebunntekst**, velger den nestede **Område**-komponenten som refererer til Excel-cellen **ReportPageFooter\_PageAmount**, og følg deretter disse trinnene:

    1. I datakildetreet, i høyre rute, velger du elementet **Total.Page.Amount.Sum()**.
    2. Velg **Bind**.
    3. Velg **Rediger formel**.
    4. Oppdater formelen til `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > Du må angi argumentet for denne funksjonen som **Usann** for å beholde innhentete data for den gjeldende siden, fordi disse dataene må beregne beløpet som løper totalt, totalt antall linjer per side og løpende teller for linjer.

2. I formattreet velger du den nestede **Område**-komponenten som refererer til Excel **ReportPageFooter\_PageWeight**-cellen, og deretter følger du disse trinnene:

    1. I datakildetreet, i høyre rute, velger du elementet **Total.Page.Weight.Sum()**.
    2. Velg **Bind**.
    3. Velg **Rediger formel**.
    4. Oppdater formelen til `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Konfigurere bindinger til å fylle ut løpende totalsummer

1. På siden **Formatutforming**, i formattreet, utvider du komponenten **Rapportsidebunntekst**, velger den nestede **Område**-komponenten som refererer til Excel-cellen **ReportPageFooter\_RunningTotalAmount**, og følg deretter disse trinnene:

    1. I datakildetreet, i høyre rute, velger du elementet **Total.Running.Amount.Collect()**.
    2. Velg **Bind**.
    3. Velg **Rediger formel**.
    4. Oppdater formelen til `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > `Total.Running.Amount.Sum(false)`-operanden returnerer det tidligere innsamlede beløpet som løper totalt. `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`-operanden returnerer totalbeløpet for den gjeldende siden. Du må angi argumentet for den nestede funksjonen til den andre operanden som **Sann** for å tilbakestille `Total.Page.Amount`-datainnsamlingen så snart denne verdien er plassert i den kjørende `Total.Running.Amount`-totalsamlingen. Det angitte argumentet må begynne å samle inn den neste sidetotal fra en 0-verdi (null).
    >
    > Funksjonen `Total.Running.Amount.Sum(false)` kalles for å angi det løpende totalbeløpet i Excel-cellen **ReportPageFooter\_RunningTotalAmount**-cellen på den gjeldende siden.

2. I formattreet velger du den nestede **Område**-komponenten som refererer til Excel **ReportPageFooter\_RunningTotalWeight**-cellen, og deretter følger du disse trinnene:

    1. I datakildetreet, i høyre rute, velger du elementet **Total.Running.Weight.Collect()**.
    2. Velg **Bind**.
    3. Velg **Rediger formel**.
    4. Oppdater formelen til `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Konfigurere bindinger til å fylle ut side med løpende teller

1. På siden **Formatutforming**, i formattreet, utvider du komponenten **Rapportsidebunntekst**, og velg den nestede **Område**-komponenten som refererer til Excel-cellen **ReportPageFooter\_RunningCounterLines**.
2. Velg **Rediger formel**.
3. Legg til formelen `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`.

    > [!NOTE]
    > Denne formelen returnerer antallet innsamlede beløpsverdier for hele rapporten. Dette antallet tilsvarer antall transaksjoner som har blitt iterert i det aktuelle øyeblikket. Samtidig samler formelen inn den returnerte verdien i **Total.Running.Lines**-samlingen.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Konfigurere bindinger til å fylle ut sidebunntekstteller

1. På siden **Formatutforming**, i formattreet, utvider du komponenten **Rapportsidebunntekst**, og velg den nestede **Område**-komponenten som refererer til Excel-cellen **ReportPageFooter\_PageLines**.
2. Velg **Rediger formel**.
3. Legg til formelen `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`.

    > [!NOTE]
    > Denne formelen beregner antall transaksjoner på den gjeldende siden som differansen mellom antall transaksjoner som ble samlet inn i **Total.Page.Amount.Result** for hele rapporten, og antall transaksjoner som er lagret på dette stadiet i **Total.Running.Lines.Sum**. Fordi antall transaksjoner for den gjeldende siden er lagret i **Total.Running.Lines** i bindingen til **Område**-komponenten som refererer til cellen **RapportPageFooter\_RunningCounterLines** er ikke antall transaksjoner på den gjeldende siden inkludert ennå. Derfor vil denne differansen være lik antall transaksjoner på den gjeldende siden.

![Konfigurerte bindinger for utfylling av bunnteksttelleren på siden i ER-formatutforming.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Konfigurere komponentsynlighet

Du kan endre synligheten til toppteksten og bunnteksten på en bestemt side i et generert dokument for å skjule følgende elementer:

- Sidehodet på den første siden, fordi rapporthodet allerede inneholder kolonnetitler
- Sidehodet på en side som ikke har transaksjoner som kan forekomme for den siste siden
- Sidebunntekst på en side som ikke har transaksjoner som kan forekomme for den siste siden

Hvis du vil endre synligheten, oppdaterer du egenskapen **Aktivert** i komponentene **Rapportsidetopptekst** og **Rapportsidebunntekst**.

1. På siden **Formatutforming**, i formattreet, utvider du **Rapportside**-komponenten, og velg den nestede komponenten **Rapportsidetopptekst**, og følg disse trinnene.

    1. Velg **Rediger** for **Aktivert**-feltet.
    2. På siden **Formeldesigner** i feltet **Formel** angir du følgende uttrykk:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. I formattreet velger du den nestede komponenten **Rapportsidebunntekst**, og deretter følger du denne fremgangsmåten:

    1. Velg **Rediger** for **Aktivert**-feltet.
    2. På siden **Formeldesigner** i feltet **Formel** angir du følgende uttrykk:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)`-oppbyggingen blir brukt til å beregne antall transaksjoner på den gjeldende siden. Konstruksjonen `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` brukes til å legge til antall transaksjoner på den gjeldende siden i samlingen for å håndtere den neste bunnteksten på en riktig måte.
    >
    > Samlingen `Total.Running.Lines` kan ikke brukes på nytt her, fordi **Aktivert**-egenskapen for en basiskomponent behandles **etter** at bindingene til nestede komponenter er behandlet. Når egenskapen **Aktivert** behandles, økes samlingen `Total.Running.Lines` allerede med antall transaksjoner på den gjeldende siden.

3. Velg **Lagre**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Generere en Intrastat-deklarasjonskontrollrapport (oppdatert)

1. Kontroller at du har 24 transaksjoner på **Intrastat**-siden. Gjenta trinnene i delen [Generere en Intrastat-deklareringskontrollrapport](#generate-intrastat-control-report) i denne artikkelen for å generere og gå gjennom kontrollrapporten.

    Alle transaksjoner presenteres på den første siden. Sidetotalene og tellerne er lik rapporttotalene og tellerne. Sidehodeområdet er skjult på den første siden, fordi rapporthodet allerede inneholder kolonnetitler. Toppteksten og bunnteksten er skjult på den andre siden, fordi siden ikke inneholder transaksjoner.

    ![Generert Excel-dokument i skrivebordprogrammet.](./media/er-paginate-excel-reports-document2.gif)

2. Oppdater to transaksjoner på **Intrastat**-siden ved å endre **Varenummer**-koden fra **D00006** til **L0010**. Legg merke til at produktnavnet på den nye varen, **Aktiv stereohøyttalerpar**, er lengre enn produktnavnet på den opprinnelige varen, **Standardhøyttaler**. Denne situasjonen tvinger tekstbryting i den tilsvarende cellen i det genererte dokumentet. Dokumentpaginering og siderelatert summering og opptelling må nå oppdateres. Gjenta trinnene i delen [Generere en Intrastat-deklareringskontrollrapport](#generate-intrastat-control-report) for å generere og gå gjennom kontrollrapporten.

    For øyeblikket presenteres transaksjoner på to sider, og sidetotaler og tellere beregnes riktig. Sideoverskriftsområdet er riktig skjult på den første siden og vises på den andre siden. Bunnteksten på siden er synlig på begge sider, fordi de inneholder transaksjoner.

    ![Oppdatert generert Excel-dokument i skrivebordprogrammet.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Er det mulig å gjenkjenne når den endelige siden behandles av sideformatkomponenten?

**Side**-komponenten [eksponerer ikke](er-fillable-excel.md#page-component-limitations)-informasjon om antall behandlede sider og totalt antall sider i et generert dokument. Likevel kan du konfigurere ER-[formler](er-formula-language.md) til å gjenkjenne den siste siden. Her er et eksempel:

- Beregn det totale antallet transaksjoner som allerede er behandlet, ved hjelp av **Rapportside**-komponenten. Du kan gjøre denne beregningen ved å bruke formelen `COUNT(Total.Page.Amount.Result)`. 
- Beregn det totale antallet transaksjoner som må behandles, basert på bindingen `model.CommodityRecord` som er konfigurert for komponenten **Rapportlinjer**. Du kan gjøre denne beregningen ved å bruke formelen `COUNT(model.CommodityRecord)`.
- Sammenligne to tall for å gjenkjenne den siste siden. Når begge verdiene er like, genereres den endelige siden.

> [!NOTE]
> Vi anbefaler at du bare bruker denne fremgangsmåten når **Aktivert**-egenskapen for **Rapportlinjer**-komponenten ikke inneholder noen formel som kan returnere [Usann](er-formula-supported-data-types-primitive.md#boolean) ved kjøretid for noen av de itererte [postene](er-formula-supported-data-types-composite.md#record) i den bundne [Postlisten](er-formula-supported-data-types-composite.md#record-list).

## <a name="additional-resources"></a>Tilleggsressurser

- [Utform en konfigurasjon til å generere dokumenter i Excel-format](er-fillable-excel.md)
- [Bruk datakilder for DATAINNSAMLING i formater for elektronisk rapportering (ER)](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
