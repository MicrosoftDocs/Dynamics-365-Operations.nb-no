---
title: Utforme et ER-format for å generere en rapport i Excel-format med innebygde bilder i topptekster og bunntekster
description: Dette emnet beskriver hvordan du bruker verktøyet for elektronisk rapportering (ER) til å generere forretningsdokumenter som har innebygde bilder og figurer i topptekster og bunntekster.
author: NickSelin
ms.date: 06/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1115be8c33eeaf16c1a533e63b31d87b0fc5f68d6469ff075428f72ac146b2f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746641"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>Utforme et ER-format for å generere en rapport i Excel-format med innebygde bilder i topptekster og bunntekster

[!include[banner](../includes/banner.md)]

Dette emnet forklarer hvordan en bruker i rollen systemansvarlig eller funksjonsrådgiver for elektronisk rapportering kan utføre disse oppgavene:

- Konfigurere parametere for rammeverket for [elektronisk rapportering (ER)](general-electronic-reporting.md).
- Importer ER [-konfigurasjoner](general-electronic-reporting.md#Configuration) som [leveres](general-electronic-reporting.md#Provider) av Microsoft og brukes til å generere [fritekstfakturaer](../../../finance/accounts-receivable/create-free-text-invoice-new.md), basert på en [mal](er-fillable-excel.md#excel-file-component) i Microsoft Excel-format.
- Opprett en [egendefinert (avledet)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) versjon av en standard ER-formatkonfigurasjon som leveres av Microsoft.
- Endre den egendefinerte ER-formatkonfigurasjonen slik at den genererer en fritekstfakturarapport som har et firmalogobilde i bunnteksten.

Prosedyrene i dette emnet kan fullføres i **USMF**-firmaet. Ingen koding er nødvendig. Før du starter kan du laste ned og lagre følgende fil.

| beskrivelse        | Filnavn |
|--------------------|-----------|
| Firmalogobilde | [Firmalogo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Innhold

- [Konfigurere den juridiske enheten](#ConfigureLegalEntity)
- [Konfigurere ER-rammeverket](#ConfigureFramework)

    - [Konfigurere ER-parametere](#ConfigureParameters)
    - [Aktivere en ER-konfigurasjonsleverandør](#ActivateProvider)

        - [Se gjennom listen over ER-konfigurasjonsleverandører](#ReviewProvidersList)
        - [Legg til en ny ER-konfigurasjonsleverandør](#AddProvider)
        - [Aktivere den nye ER-konfigurasjonsleverandøren](#ActivateAddedProvider)

- [Importer standard ER-formatkonfigurasjoner](#ImportERSolution1)

    - [Importer standard ER-konfigurasjoner](#ImportERFormat)
    - [Se gjennom importerte ER-konfigurasjoner](#ReviewImportedERSolution)

- [Skrive ut en fritekstfaktura ved hjelp av standard ER-format](#PrintInvoice1)

    - [Definere utskriftsbehandling](#ConfigurePrintManagement1)
    - [Skriv ut en fritekstfaktura](#ProcessInvoice1)

- [Tilpasse standard ER-format](#CustomizeProvidedFormat)

    - [Opprette et egendefinert format](#DeriveProvidedFormat)
    - [Redigere det tilpassede formatet](#ConfigureDerivedFormat)
    - [Merke det egendefinerte formatet som kjørbart](#MarkFormatRunnable)

- [Skrive ut en fritekstfaktura ved hjelp av det egendefinerte ER-formatet](#PrintInvoice2)

    - [Definere utskriftsbehandling](#ConfigurePrintManagement2)
    - [Skriv ut en fritekstfaktura](#ProcessInvoice2)

- [Tilleggsressurser](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Konfigurere den juridiske enheten

1. Gå til **Organisasjonsstyring** \> **Organisasjoner** \> **Juridiske enheter**.
2. På siden **Juridiske enheter** i hurtigfanen **Rapporter for firmalogo** velger du **Endre**.
3. I dialogboksen **Velg bilde som skal lastes opp** velger du **Bla gjennom**, og velger **Firmalogo.png**-filen du lastet ned tidligere.
4. Velg **Lagre**, og lukk deretter siden **Juridiske enheter**.

![Firmalogobilde valgt på Juridiske enheter-siden.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Konfigurere ER-rammeverket

Som en bruker i rollen funksjonsrådgiver for elektroniske rapportering, må du konfigurere minimumsparameterne for ER-parametere før du kan begynne å bruke ER-rammeverket til å utforme en egendefinert versjon av et standardformat.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurere ER-parametere

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Parametere for elektronisk rapportering**.
3. På **Parametere for elektronisk rapportering**-siden, i **Generelt**-fanen angi **Aktiver utformingsmodus** til **Ja**.
4. Angi følgende parametere i fanen **Vedlegg**:

    - I **Konfigurasjoner**-feltet velger du **Fil**-typen for **USMF**-firmaet.
    - I feltene **Jobbarkiv**, **Midlertidig**, **Grunnlinje** og **Annet** velger du **Fil**-typen.

Hvis du vil ha mer informasjon om ER-parametere, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivere en ER-konfigurasjonsleverandør

Hver ER-konfigurasjon som legges til, er merket som eid av en ER-konfigurasjonsleverandør. ER-konfigurasjonsleverandøren som aktiveres i **Elektronisk rapportering**-arbeidsområdet, brukes til dette formålet. Derfor må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet før du begynner å legge til eller redigere ER-konfigurasjoner.

> [!NOTE]
> Bare eieren av en ER-konfigurasjon kan redigere den. Før en ER-konfigurasjon kan redigeres, må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Se gjennom listen over ER-konfigurasjonsleverandører

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.
3. På **Konfigurasjonsleverandørtabell**-siden har hver leverandørpost et unikt navn og en unik URL-adresse. Se gjennom innholdet på denne siden. Hvis det allerede finnes en post for **Litware, Inc.** (`https://www.litware.com`), hopper du over den neste fremgangsmåten og [legger til en ny ER-konfigurasjonsleverandør](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Legg til en ny ER-konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.
3. Velg **Ny** på siden **Konfigurasjonsleverandører**.
4. I **Navn**-feltet angir du **Litware, Inc.**
5. I **Internett-adresse**-feltet angir du `https://www.litware.com`.
6. Velg **Lagre**.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivere den nye ER-konfigurasjonsleverandøren

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Litware, Inc.**-flisen og deretter **Angi aktiv**.

Hvis du ha mer informasjon om ER-konfigurasjonsleverandører, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Importer standard ER-formatkonfigurasjoner

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Importer standard ER-konfigurasjoner

Hvis du vil legge til standard ER-konfigurasjoner i den gjeldende forekomsten av Dynamics 365 Finance, må du importere dem fra ER-[repositoriet](general-electronic-reporting.md#Repository) som ble konfigurert for den forekomsten.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Microsoft**-flisen og deretter **Repositorier** for å vise listen over repositorier for **Microsoft**-leverandøren.
3. På **Konfigurasjonsrepositorier**-siden velger du repositoriet for **Global**-typen, og deretter velger du **Åpne**. Hvis du blir spurt om godkjenning for å koble til [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md), følger du godkjenningsinstruksjonene.
4. På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet i venstre rute og velger **Fritekstfaktura (Excel)**-formatkonfigurasjonen.
5. I **Versjoner**-hurtigkategorien velger du siste versjon (for eksempel **240.112**) av den valgte ER-formatkonfigurasjonen.
6. Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet til den gjeldende forekomsten av Finance.

![Importere standard ER-konfigurasjoner på Konfigurasjonsrepositorium-siden.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Hvis du har problemer med å få tilgang til det [globale repositoriet](er-download-configurations-global-repo.md), kan du [laste ned konfigurasjoner](download-electronic-reporting-configuration-lcs.md) fra Microsoft Dynamics Lifecycle Services (LCS) i stedet.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Se gjennom importerte ER-konfigurasjoner

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.
3. I konfigurasjonstreet i venstre rute på **Konfigurasjoner**-siden utvider du **Fakturamodell**.
4. I tillegg til det valgte ER-formatet for **Fritekstfaktura (Excel)**, ble andre ER-konfigurasjoner importert. Kontroller at følgende ER-konfigurasjoner er tilgjengelige i konfigurasjonstreet:

    - **Fakturamodell** – denne konfigurasjonen inneholder ER-komponenten for [datamodell](general-electronic-reporting.md#data-model-and-model-mapping-components) som representerer datastrukturen til faktureringsforretningsdomenet.
    - **Fakturamodelltilordning** – denne konfigurasjonen inneholder ER-komponenten for [modelltilordning](general-electronic-reporting.md#data-model-and-model-mapping-components) som beskriver hvordan datamodellen fylles ut med programdata ved kjøring.
    - **Fritekstfaktura (Excel)** – Denne konfigurasjonen inneholder [formatet](general-electronic-reporting.md#FormatComponentOutbound) og formatet som tilordner ER-komponenter. Formatkomponenten angir rapportoppsettet, basert på en mal i Excel-format. Formattilordningskomponenten inneholder modelldatakilden og angir hvordan denne datakilden brukes til å rapportoppsettet fylles ut under kjøring.

![Importerte ER-konfigurasjoner på konfigurasjonssiden.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Skrive ut en fritekstfaktura ved hjelp av standard ER-format

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Definer utskriftsbehandling

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På **Fritekstfaktura**-siden velger du **FTI-00000002**-fakturaen, og deretter, i handlingsruten på **Faktura**-fanen i **Utskriftsbehandling**-gruppen, velger du **Utskriftsbehandling**.
3. På siden **Oppsett for utskriftsbehandling**, i treet til venstre, utvider du **Modul - kunder \> Dokumenter \> Fritekstfaktura**, og velger deretter elementet **Original \<Default\>**.
4. I **Rapportformat**-feltet velger du **Fritekstfaktura (Excel)**.
5. Velg **Esc**-tasten for å gå ut av siden **Oppsett for utskriftsbehandling** og gå tilbake til **Fritekstfaktura**-siden.

![Innstillinger for utskriftsbehandling for en fritekstfaktura i standard ER-format på oppsettsiden for utskriftsbehandling.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Skriv ut en fritekstfaktura

1. På **Fritekstfaktura**-siden kontrollerer du at **FTI-00000002**-fakturaen fremdeles er valgt, og deretter, i handlingsruten på **Faktura**-fanen i **Dokument**-gruppen, velger du **Skriv ut** \> **Valgt**.
2. Last ned den genererte fakturaen i Excel-format, og åpne den for forhåndsvisning.
3. Legg merke til at i henhold til strukturen i Excel-malen for det angitte ER-formatet, inneholder bunnteksten til den genererte fakturaen informasjon om det gjeldende sidenummeret og det totale antall sider i rapporten.

![Generert fritekstfaktura.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Tilpasse standard ER-format

For eksemplet i denne delen kan du bruke ER-konfigurasjonene som leveres av Microsoft, til å generere en fritekstfaktura i Excel-format. Du må imidlertid legge til en tilpasning for å plassere et firmalogobilde i bunnteksten til genererte fakturaer.

I dette tilfellet må du som representanten for Litware, Inc., opprette (avlede) en ny ER-formatkonfigurasjon som er basert på **Fritekstfaktura (Excel)**-konfigurasjonen fra Microsoft.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Opprette et egendefinert format

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Fakturamodell** og velger **Fritekstfaktura (Excel)**. Litware, Inc. bruker den importerte versjonen (for eksempel **240.112**) av denne ER-formatkonfigurasjonen som grunnlaget for den egendefinerte versjonen.
3. Velg **Opprett konfigurasjon** for å åpne nedtrekksdialogen. Bruk denne dialogboksen til å opprette en ny konfigurasjon for et egendefinert betalingsformat.
4. I **Ny**-feltgruppen velger du alternativet **Avled fra navn: Fritekstfaktura (Excel), Microsoft**.
5. I **Navn**-feltet angir du **Tilpasset fritekstfaktura (Excel)**.
6. Velg **Opprett konfigurasjon**.

![Opprette en konfigurasjon for et egendefinert betalingsformat i dialogboksen Opprett konfigurasjon.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Versjon 240.112.1 av ER-formatkonfigurasjonen **Tilpasset fritekstfaktura (Excel)** opprettes. Denne versjonen har [statusen](general-electronic-reporting.md#component-versioning) **Utkast** og kan redigeres. Det gjeldende innholdet i egendefinert ER-format samsvarer med innholdet i formatet som leveres av Microsoft.

![Ny versjon av ER-formatkonfigurasjonen opprettet på Konfigurasjoner-siden.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Redigere det tilpassede formatet

Konfigurer det egendefinerte formatet, slik at et firmalogobilde legges i bunnteksten på hver side i rapporten.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **Tilpasset fritekstfaktura (Excel)**.
3. I **Versjoner**-hurtigkategorien velger du versjon **240.112.1** for den valgte konfigurasjonen.
4. Velg **Utforming**.
5. På **Formatutforming**-siden velger du **Vis detaljer** for å vise mer informasjon om formatelementene.
6. Vis og gå gjennom følgende elementer:

    - Elementet **Fritekstfaktura** av **Excel**-typen. Dette elementet brukes til å generere en faktura i Excel-arbeidsbokformat.
    - Elementet **Fritekstfaktura \\ Faktura** av **Ark**-typen. Dette elementet brukes til å generere et regneark for den genererte Excel-arbeidsboken.
    - Elementet **Fritekstfaktura \\ Faktura \\ Bunntekst** av **Bunntekst**-typen. Dette elementet brukes til å fylle ut en fakturabunntekst.

7. Velg elementet **Fritekstfaktura \\ Faktura \\ Bunntekst**.

    ![Bunntekstselement i ER-operasjonsutforming.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Hver bunntekst på siden på en generert faktura inneholder informasjon om det gjeldende sidenummeret og totalt antall sider i rapporten. Som du kan se, inneholder elementet **Fritekstfaktura \\ Faktura \\ Bunntekst** ingen underordnede elementer. Derfor konfigureres Excel-malen som brukes til å vise sidevekslingsdetaljer i midten av bunnteksten i hver rapport.

8. Velg **Legg til**, og velg deretter **Excel \\-bilde**-typen for formatelementet du legger til:

    1. I **Justering**-feltet velger du **Høyre**.
    2. Velg **Relativ** i feltet **Skaler høyden**.
    3. I feltet **Skala i prosent** skriver du inn **70**.
    4. Velg **OK**.

        > [!NOTE]
        > Elementet **Excel \\-bilde** brukes til å legge til et firmalogobilde og justere det på høyre side av bunnteksten på siden.

    ![Egenskaper for bildeelementet i dialogboksen Komponentegenskaper.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Velg **bilde**-elementet du nettopp la til, i formatstrukturtreet til venstre, og utvid deretter **modell**-datakilden på fanen **Tilordning**.
10. Utvid **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo**, og velg deretter datakildefeltet **model.InvoiceBase.CompanyInfo.Logo**. Datakildefeltet av [Container](er-formula-supported-data-types-composite.md#container)-typen viser firmalogobildet som medieinnhold.
11. Velg **Bind**. Elementet **Bilde**-format er nå knyttet til datakildefeltet **model.InvoiceBase.CompanyInfo.Logo**. Derfor blir det lagt inn et firmalogobilde i bunnteksten til genererte fakturaer ved kjøretid.

    ![Bildeformatelementet er nå knyttet til datakildefeltet model.InvoiceBase.CompanyInfo.Logo i ER-operasjonsutforming.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Velg **Lagre**, og lukk deretter siden **Utforming**.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Merke det egendefinerte formatet som kjørbart

Nå som den første versjonen av det egendefinerte formatet er opprettet og har statusen **Utkast**, kan du kjøre formatet for testformål. Når du skal kjøre rapporten, behandler du en leverandørbetaling ved å bruke betalingsmåten som refererer til det egendefinerte ER-formatet. Som standard [vurderes](general-electronic-reporting.md#component-versioning) bare versjonene som har statusen **Fullført** eller **Delt** når du kaller opp et ER-format fra programmet. Denne virkemåten hjelper til med å forhindre at ER-formater som har uferdige utforminger, brukes. Testingen kjøres imidlertid ved at du kan tvinge programmet til å bruke versjonen av ER-formatet som har statusen **Utkast**. På denne måten kan du justere gjeldende formatversjon hvis det kreves endringer. Hvis du vil ha mer informasjon, kan du se [Relevans](electronic-reporting-destinations.md#applicability).

Hvis du vil bruke utkastversjonen av et ER-format, må du eksplisitt markere ER-formatet.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. I dialogboksen **Brukerparametere** setter du **Kjøringsinnstillinger** til **Ja**, og deretter velger du **OK**.
4. Velg **Rediger** for å gjøre gjeldende side redigerbar, og deretter, i konfigurasjonstreet i venstre rute, velger du **Tilpasset fritekstfaktura (Excel)**.
5. Sett **Kjør utkast**-alternativet til **Ja**.

![Merking av det egendefinerte formatet som kjørbart på Konfigurasjoner-siden.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Skrive ut en fritekstfaktura ved hjelp av det egendefinerte ER-formatet

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Definer utskriftsbehandling

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På **Fritekstfaktura**-siden velger du **FTI-00000002**-fakturaen, og deretter, i handlingsruten på **Faktura**-fanen i **Utskriftsbehandling**-gruppen, velger du **Utskriftsbehandling**.
3. På siden **Oppsett for utskriftsbehandling**, i treet til venstre, utvider du **Modul - kunder** \> **Dokumenter** \> **Fritekstfaktura**, og velger deretter elementet **Original** **\<Default\>**.
4. I **Rapportformat**-feltet velger du **Tilpasset fritekstfaktura (Excel)**.
5. Velg **Esc** for å gå ut av siden **Oppsett for utskriftsbehandling** og gå tilbake til **Fritekstfaktura**-siden.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Skriv ut en fritekstfaktura

1. På **Fritekstfaktura**-siden kontrollerer du at **FTI-00000002**-fakturaen fremdeles er valgt, og deretter, i handlingsruten på **Faktura**-fanen i **Dokument**-gruppen, velger du **Skriv ut** \> **Valgt**.
2. Last ned den genererte fakturaen i Excel-format, og åpne den for forhåndsvisning.
3. Legg merke til at bunnteksten på den genererte fakturaen inneholder et firmalogobilde i tillegg til informasjon om rapportens sideveksling, i samsvar med strukturen til det egendefinerte ER-formatet.

![Generert fritekstfaktura med et firmalogobilde i bunnteksten på siden.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Tilleggsressurser

- [Utform en konfigurasjon til å generere dokumenter i Excel-format](er-fillable-excel.md)
- [Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md)
