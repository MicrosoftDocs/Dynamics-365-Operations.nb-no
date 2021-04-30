---
title: Endre et ER-formatet for å generere et egendefinert elektronisk dokument
description: Dette emnet beskriver hvordan du justerer et Microsoft-levert format for elektronisk rapportering (ER) slik at det genererer et egendefinert elektronisk dokument.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60b318ab03bc1bb47517a206e8b2afd9c13cf273
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891725"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Endre et ER-formatet for å generere et egendefinert elektronisk dokument

[!include[banner](../includes/banner.md)]

Fremgangsmåtene i dette emnet forklarer hvordan en bruker i rollen systemansvarlig eller funksjonsrådgiver for elektronisk rapportering kan utføre disse oppgavene:

- Konfigurere parametere for [rammeverket for elektronisk rapportering (ER)](general-electronic-reporting.md).
- Importer ER-konfigurasjoner som leveres av Microsoft, og som brukes til å generere en betalingsfil mens en [leverandørbetaling](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) blir behandlet.
- Opprett en egendefinert versjon av en standard ER-formatkonfigurasjon som leveres av Microsoft.
- Endre den egendefinerte ER-formatkonfigurasjonen slik at den genererer betalingsfiler som oppfyller kravene til en bestemt bank.
- Ta i bruk endringer som er gjort i standard ER-formatkonfigurasjon i den egendefinert ER-formatkonfigurasjonen.

Alle disse fremgangsmåtene kan utføres i **GBSI**-firmaet. Ingen koding er nødvendig.

- [Konfigurere ER-rammeverket](#ConfigureFramework)

    - [Konfigurere ER-parametere](#ConfigureParameters)
    - [Aktivere en ER-konfigurasjonsleverandør](#ActivateProvider)

        - [Se gjennom listen over ER-konfigurasjonsleverandører](#ReviewProvidersList)
        - [Legg til en ny ER-konfigurasjonsleverandør](#ActivateProvider)
        - [Aktivere en ER-konfigurasjonsleverandør](#ActivateAddedProvider)

- [Importer standard ER-formatkonfigurasjoner](#ImportERSolution1)

    - [Importer standard ER-konfigurasjoner](#ImportERFormat1)
    - [Se gjennom importerte ER-konfigurasjoner](#ReviewImportedERSolution)

- [Klargjøre en leverandørbetaling for behandling](#PrepareVendorPayment)

    - [Legg til bankinformasjon for en leverandørkonto](#AddBankAccount)
    - [Angi en leverandørbetaling](#EnterVendorPayment)

- [Behandle en leverandørbetaling ved hjelp av standard ER-format](#ProcessVendorPayment1)

    - [Konfigurere den elektroniske betalingsmåten](#ConfigureMethodOfPayment1)
    - [Behandle en leverandørbetaling](#ProcessPayment1)

- [Tilpasse standard ER-format](#CustomizeProvidedFormat)

    - [Opprette et egendefinert format](#DeriveProvidedFormat)
    - [Redigere et egendefinert format](#ConfigureDerivedFormat)
    - [Merke et egendefinert format som kjørbart](#MarkFormatRunnable)

- [Behandle en leverandørbetaling ved hjelp av egendefinert ER-format](#ProcessVendorPayment2)

    - [Konfigurere den elektroniske betalingsmåten](#ConfigureMethodOfPayment2)
    - [Behandle en leverandørbetaling](#ProcessPayment2)

- [Importer nye versjoner av standard ER-formatkonfigurasjoner](#ImportERSolution2)

    - [Importer nye versjoner av standard ER-konfigurasjoner](#ImportERFormat2)
    - [Se gjennom importerte ER-formatkonfigurasjoner](#ReviewImportedERFormat)

- [Ta i bruk endringene i den nye versjonen av et importert format i et egendefinert format](#AdoptNewBaseVersion)

    - [Fullfør gjeldende utkastversjon av et egendefinert format](#CompleteDerivedFormat)
    - [Rebasere et egendefinert format på nytt til en ny grunnversjon](#RebaseDerivedFormat)
    - [Behandle en leverandørbetaling ved hjelp av et rebasert ER-format](#ProcessPayment3)

- [Tilleggsressurser](#References)

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
> Bare eieren av en ER-konfigurasjon kan redigere den. Derfor, før en ER-konfigurasjon kan redigeres, må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Se gjennom listen over ER-konfigurasjonsleverandører

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.
3. På **Konfigurasjonsleverandørtabell**-siden har hver leverandørpost et unikt navn og en unik URL-adresse. Se gjennom innholdet på denne siden. Hvis det allerede finnes en post for **Litware, Inc.** (`https://www.litware.com`), hopper du over den neste fremgangsmåten og [legger til en ny ER-konfigurasjonsleverandør](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Legg til en ny ER-konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.
3. Velg **Ny** på siden **Konfigurasjonsleverandører**.
4. I **Navn**-feltet angir du **Litware, Inc.**
5. I **Internett-adresse**-feltet angir du `https://www.litware.com`.
6. Velg **Lagre**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivere en ER-konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Litware, Inc.**-flisen og deretter **Angi aktiv**.

Hvis du ha mer informasjon om ER-konfigurasjonsleverandører, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Importer standard ER-formatkonfigurasjoner

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Importer standard ER-konfigurasjoner

Hvis du vil legge til standard ER-konfigurasjoner i den gjeldende forekomsten av Microsoft Dynamics 365 Finance, må du importere dem fra ER-[repositoriet](general-electronic-reporting.md#Repository) som ble konfigurert for den forekomsten.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Microsoft**-flisen og deretter **Repositorier** for å vise listen over repositorier for Microsoft-leverandøren.
3. På **Konfigurasjonsrepositorier**-siden velger du repositoriet for **Global**-typen, og deretter velger du **Åpne**. Hvis du blir spurt om godkjenning for å koble til Regulatory Configuration Service, følger du godkjenningsinstruksjonene.
4. På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet i venstre rute og velger **BBS (Storbritannia)**-formatkonfigurasjonen.
5. I **Versjoner**-hurtigkategorien velger du versjon **1.1** for den valgte ER-formatkonfigurasjonen.
6. Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet til den gjeldende forekomsten av Finance.

![Konfigurasjonsrepositorium-side](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Hvis du har problemer med å få tilgang til det [globale repositoriet](er-download-configurations-global-repo.md), kan du [laste ned konfigurasjoner](download-electronic-reporting-configuration-lcs.md) fra Microsoft Dynamics Lifecycle Services (LCS) i stedet.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Se gjennom importerte ER-konfigurasjoner

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell**.
4. Legg merke til at i tillegg til det valgte ER-formatet for **BBS (Storbritannia)**, ble andre ER-konfigurasjoner importert. Kontroller at følgende ER-konfigurasjoner er tilgjengelige i konfigurasjonstreet:

    - **Betalingsmodell** – denne konfigurasjonen inneholder ER-komponenten for [datamodell](general-electronic-reporting.md#data-model-and-model-mapping-components) som representerer datastrukturen til betalingsforretningsdomenet.
    - **Betalingsmodelltilordning 1611** – denne konfigurasjonen inneholder ER-komponenten for [modelltilordning](general-electronic-reporting.md#data-model-and-model-mapping-components) som beskriver hvordan datamodellen fylles ut med programdata ved kjøring.
    - **BBS (Storbritannia)** – denne konfigurasjonen inneholder ER-komponenter for [format](general-electronic-reporting.md#FormatComponentOutbound) og formattilordning. Formatkomponenten angir rapportoppsettet. Formattilordningskomponenten inneholder modelldatakilden og angir hvordan rapportoppsettet fylles ut ved hjelp av denne datakilden under kjøring.

![Siden Konfigurasjoner](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Klargjøre en leverandørbetaling for behandling

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Legg til bankinformasjon for en leverandørkonto

Du må legge til bankinformasjon for en leverandørkonto som skal refereres til senere i en registrert betaling.

1. Gå til **Leverandører** \> **Leverandører** \> **Alle leverandører**.
2. På **Alle leverandører**-siden velger du **GB_SI_000001**-leverandørkontoen og, i handlingsruten, på **Leverandør**-fanen, i **Definer**-gruppen, velger du **Bankkontoer**.
3. På **Leverandørbankkontoer**-siden velger du **Ny** og angir deretter følgende informasjon:

    1. Angi **GBP OPER** i feltet **Bankkonto**.
    2. Velg **BankGBP** i feltet **Bankgrupper**.
    3. Angi **202015** i feltet **Bankkontonummer**.
    4. Angi <a id="DefineSWIFTCode"></a>**CHASDEFXXXX** i **SWIFT**-feltet.
    5. Angi **GB33BUKB20201555555555** i feltet **IBAN**.
    6. I **Rutingsnummer**-feltet beholder du standardverdien <a id="DefineRoutingNumber"></a>**123456**.

    ![Leverandørbankkontoer-side](./media/er-quick-start2-bank-account.png)

4. Velg **Lagre**.
5. Lukk siden.
6. På **Alle leverandører**-siden åpner du **GB_SI_000001**-leverandørkontoen.
7. På leverandørdetaljersiden velger du **Rediger** for å gjøre siden redigerbar, ved behov.
8. På **Betaling**-hurtigfanen velger du **GBP OPER** i **Bankkonto**-feltet.

    ![Leverandørdetaljerside](./media/er-quick-start2-bank-account-reference.png)

9. Velg **Lagre**.
10. Lukk siden.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Angi en leverandørbetaling

Du må angi en ny leverandørbetaling ved å bruke et [betalingsforslag](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).

1. Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.
2. Velg **Ny** på siden **Leverandørbetalingsjournal**.
3. Velg **VendPay** i **Navn**-feltet.
4. Velg **Linjer**.
5. Velg **Betalingsforslag** \> **Opprett betalingsforslag**.
6. I **Leverandørbetalingsforslag**-dialogboksen konfigurerer du betingelser for å filtrere poster bare for **GB_SI_000001**-leverandørkontoen, og velg deretter **OK**.
7. Velg linjen for **00000007_Inv**-fakturaen, og velg deretter **Opprett betaling**.

    ![Dialogboksen Leverandørbetalingsforslag](./media/er-quick-start2-payment-proposal.png)

8. Kontroller at betalingen som er angitt, er konfigurert til å bruke **elektronisk** som betalingsmåten.

    ![Leverandørbetalinger-siden](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Behandle en leverandørbetaling ved hjelp av standard ER-format

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Konfigurere den elektroniske betalingsmåten

Du må konfigurere den elektroniske betalingsmåten slik at den bruker den importerte ER-formatkonfigurasjonen.

1. Gå til **Leverandører** \> **Betalingsoppsett** \> **Betalingsmåter**.
2. På **Betalingsmåter – leverandører**-siden velger du **elektronisk** betalingsmåte i ruten til venstre.
3. Velg **Rediger**.
4. I hurtigfanen **Filformater** setter du alternativet **Generelt elektronisk eksportformat** til **Ja**.
5. I feltet **Eksportformatkonfigurasjon** velger du formatkonfigurasjonen **BBS (Storbritannia)**.

    ![Siden Betalingsmåter – leverandører](./media/er-quick-start2-method-of-payment1.png)

6. Velg **Lagre**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Behandle en leverandørbetaling

1. Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.
2. På siden **Leverandørbetalingsjournal** velger du betalingsjournalen du la til tidligere, og deretter velger du **Linjer**.
3. På **Leverandørbetalinger**-siden velger du **Generer betalinger**.
4. Angi følgende informasjon i dialogboksen **Generer betalinger**:

    - Velg **Elektronisk** i feltet **Betalingsmåte**.
    - Velg **GBSI OPER** i feltet **Bankkonto**.

5. Velg **OK**.
6. I **Parametere for elektronisk rapport**-dialogboksen setter du **Skriv ut kontrollrapport** til **Ja**, og deretter velger du **OK**.

    ![Dialogsiden Parametere for elektronisk rapport](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > I tillegg til betalingsfilen kan du nå generere kontrollrapporten.

7. Last ned zip-filen, og pakk deretter ut følgende filer:

    - Kontrollrapporten i Excel-format
    - Betalingsfilen i TXT-format

        Legg merke til at i henhold til [strukturen](#PositionRoutingNumber) for angitt ER-format, vil betalingslinjen i den genererte filen starte med rutingsnummeret som ble [definert](#DefineRoutingNumber) for den konfigurerte bankkontoen.

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Tilpasse standard ER-format

For eksemplet som vises i denne delen, vil du bruke ER-konfigurasjonene som leveres av Microsoft, til å generere leverandørbetalingsfiler i BBS-format, men du må legge til en tilpasning for å støtte kravene til en bestemt bank. Du vil også ha muligheten til å oppgradere det egendefinerte formatet når nye versjoner av ER-konfigurasjoner blir tilgjengelige. Du vil imidlertid ha muligheten til å utføre oppgraderingen til den laveste kostnaden.

I dette tilfellet må du som representanten for Litware, Inc., opprette (avlede) en ny ER-formatkonfigurasjon ved å bruke **BBS (Storbritannia)**-konfigurasjonen fra Microsoft som et grunnlag.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Opprette et egendefinert format

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **BBS (Storbritannia)**. Litware, Inc. bruker versjon 1.1 av denne ER-formatkonfigurasjonen som grunnlaget for den egendefinerte versjonen.
3. Velg **Opprett konfigurasjon** for å åpne nedtrekksdialogen. Du kan bruke denne dialogboksen til å opprette en ny konfigurasjon for et egendefinert betalingsformat.
4. I **Ny**-feltgruppen velger du alternativet **Avled fra navn: BBS (Storbritannia), Microsoft**.
5. Angi **BBS (Storbritannia egendefinert)** i **Navn**-feltet.

    ![Rullegardinlisten Opprett konfigurasjon](./media/er-quick-start2-add-derived-format.png)

6. Velg **Opprett konfigurasjon**.

Versjon 1.1.1 av ER-formatkonfigurasjonen **BBS (Storbritannia egendefinert)** er opprettet. Denne versjonen har [statusen](general-electronic-reporting.md#component-versioning) **Utkast** og kan redigeres. Det gjeldende innholdet i egendefinert ER-format samsvarer med innholdet i formatet som leveres av Microsoft.

![Siden Konfigurasjoner](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Redigere et egendefinert format

Du må konfigurere det egendefinerte formatet slik at det overholder bankspesifikke krav. En bank kan for eksempel kreve at betalingsfiler som genereres, omfatter SWIFT-koden (Society for Worldwide Interbank Financial Telecommunication) til en bank som er tilordnet agentrollen i den behandlede leverandørbetalingen. SWIFT-koder er internasjonale bankkoder som identifiserer bestemte banker over hele verden. De kalles også bank-ID-koder (BIC-er). SWIFT-koden må ha en lengde på 11 tegn, og den må angis på begynnelsen av hver betalingslinje i en generert betalingsfil.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **BBS (Storbritannia egendefinert)**.
3. I **Versjoner**-hurtigkategorien velger du versjon **1.1.1** for den valgte konfigurasjonen.
4. Velg **Utforming**.
5. På **Formatutforming**-siden velger du **Vis detaljer** for å vise mer informasjon om formatelementene.
6. Vis og gå gjennom følgende elementer:

    - **BACSReportsFolder**-elementet for **Mappe**-typen. Dette elementet brukes til å generere utdata i ZIP-format.
    - **Fil**-elementet for **Fil**-typen. Dette elementet brukes til å generere en betalingsfil i TXT-format.
    - **Transaksjoner**-elementet for **Sekvens**-typen. Dette elementet brukes til å generere en enkelt betalingslinje i en betalingsfil.
    - **Transaksjon**-elementet for **Sekvens**-typen. Dette elementet brukes til å generere individuelle felter for en enkelt betalingslinje.

7. Velg **transaksjon**-elementet.

    ![Transaksjonselement i ER-operasjonsutforming](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Den angitte rapporten er konfigurert slik at <a id="PositionRoutingNumber"></a>alle betalingslinjer starter med bankregistreringsnummeret. **VendBankRouteNum**-formatelementet brukes til dette formålet. 

8. Velg **Legg til**, og velg deretter **Tekst\\streng**-typen for formatelementet du legger til:

    1. I **Navn**-feltet angir du **vendBankSWIFT**.
    2. Angi **11** i feltet **Minimumslengde**.
    3. Angi **11** i feltet **Maksimumslengde**.
    4. Velg **OK**.

    > [!NOTE]
    > **VendBankSWIFT**-elementet vil bli brukt til å angi SWIFT-koden til en leverandørbank i genererte filer.

9. Velg **vendBankSWIFT** i formatstrukturtreet.
10. Velg **Flytt opp** for å flytte det valgte formatelementet opp ett nivå. Gjenta dette trinnet til **vendBankSWIFT**-elementet er det <a id="PositionSWIFTCode"></a>første elementet under det overordnede **transaksjons** elementet.

    ![VendBankSWIFT som det første elementet under transaksjon i ER-operasjonsutforming](./media/er-quick-start2-derived-format1.png)

11. Mens **vendBankSWIFT** fremdeles er valgt i formatstrukturtreet, velger du **Tilordning**-fanen og utvider datakilden **modell**.
12. Utvid **model.Payment** \> **model.Payment.CreditorAgent**, og velg **model.Payment.CreditorAgent.BICFI**-datakildefelt. Dette datakildefeltet viser SWIFT-koden til en leverandørbank som er tilordnet agentrollen i den behandlede leverandørbetalingen.
13. Velg **Bind**. Formatelementet **vendBankSWIFT** er nå bundet med **model.CreditorAgent.BICFI** -datakilden, slik at SWIFT-koder blir angitt i genererte betalingsfiler.

    ![vendBankSWIFT-formatelementet som er bundet til model.Payment.CreditorAgent.BICFI-datakildefeltet i ER-operasjonsutforming](./media/er-quick-start2-derived-format2.png)

14. Velg **Lagre**.
15. Lukk utformingssiden.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Merke et egendefinert format som kjørbart

Nå som den første versjonen av det egendefinerte formatet er opprettet og har statusen **Utkast**, kan du kjøre det for testformål. Når du skal kjøre rapporten, må du behandle en leverandørbetaling ved å bruke betalingsmåten som refererer til det egendefinerte ER-formatet. Som standard [vurderes](general-electronic-reporting.md#component-versioning) bare versjonene som har statusen **Fullført** eller **Delt** når du kaller opp et ER-format fra programmet. Denne virkemåten hjelper til med å forhindre at ER-formater som har uferdige utforminger, brukes. Testingen kjøres imidlertid ved at du kan tvinge programmet til å bruke versjonen av ER-formatet som har statusen **Utkast**. På denne måten kan du justere gjeldende formatversjon hvis det kreves endringer. Hvis du vil ha mer informasjon, kan du se [Relevans](electronic-reporting-destinations.md#applicability).

Hvis du vil bruke utkastversjonen av et ER-format, må du eksplisitt markere ER-formatet.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. I dialogboksen **Brukerparametere** setter du **Kjøringsinnstillinger** til **Ja**, og deretter velger du **OK**.
4. Velg **Rediger** for å gjøre gjeldende side redigerbar, hvis nødvendig.
5. I konfigurasjonstreet i venstre rute velger du **BBS (Storbritannia)**.
6. Sett **Kjør utkast**-alternativet til **Ja**.

    ![Alternativet Kjør utkast på Konfigurasjoner-siden](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Behandle en leverandørbetaling ved hjelp av egendefinert ER-format

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Konfigurere den elektroniske betalingsmåten

Du må konfigurere den elektroniske betalingsmåten slik at det egendefinerte ER-formatet brukes til å behandle leverandørbetalinger.

1. Gå til **Leverandører** \> **Betalingsoppsett** \> **Betalingsmåter**.
2. På **Betalingsmåter – leverandører**-siden velger du **elektronisk** betalingsmåte i ruten til venstre.
3. Velg **Rediger**.
4. I hurtigfanen **Filformat** setter du alternativet **Generelt elektronisk eksportformat** til **Ja**.
5. I feltet **Eksportformatkonfigurasjon** velger du formatkonfigurasjonen **BBS (Storbritannia egendefinert)**.

    ![Siden Betalingsmåter – leverandører](./media/er-quick-start2-method-of-payment2.png)

6. Velg **Lagre**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Behandle en leverandørbetaling

1. Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.
2. På siden **Leverandørbetalingsjournal** velger du betalingsjournalen du opprettet tidligere.
3. Velg **Linjer**.
4. På **Leverandørbetalinger**-siden velger du **Betalingsstatus** \> **Ingen** over rutenettet.
5. Velg **Generer betaling**.
6. Angi følgende informasjon i dialogboksen **Generer betalinger**:

    - Velg **Elektronisk** i feltet **Betalingsmåte**.
    - Velg **GBSI OPER** i feltet **Bankkonto**.

7. Velg **OK**.
8. I **Parametere for elektronisk rapport**-dialogboksen setter du **Skriv ut kontrollrapport** til **Ja**, og deretter velger du **OK**.

    > [!NOTE]
    > I tillegg til betalingsfilen kan du bare generere kontrollrapporten.

9. Last ned zip-filen, og pakk deretter ut følgende filer:

    - Kontrollrapporten i Excel-format
    - Betalingsfilen i TXT-format

        Legg merke til at i henhold til strukturen i egendefinert ER-format, [starter](#PositionSWIFTCode) betalingslinjen i den genererte filen nå med SWIFT-koden som ble [angitt](#DefineSWIFTCode) for bankkontoen til leverandøren som har utført betalingen.

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Importer nye versjoner av standard ER-formatkonfigurasjoner

For eksemplet som vises i denne delen, mottar du en melding om Kunnskapsbaseartikkel [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). Dette varselet informerer deg om den nye versjonen av ER-formatet **BBS (Storbritannia)** er publisert av Microsoft. I tillegg til kontrollrapporten lar denne nye versjonen brukere generere betalingsmeldingsrapporten og deltakernotatrapporten mens en leverandørbetaling blir behandlet. Du vil begynne å bruke denne funksjonaliteten.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Importer nye versjoner av standard ER-konfigurasjoner

Hvis du vil legge til nye versjoner av ER-konfigurasjoner i den gjeldende Finance-forekomsten, må du importere dem fra ER-[repositoriet](general-electronic-reporting.md#Repository) som du har konfigurert.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Microsoft**-flisen og deretter **Repositorier** for å vise listen over repositorier for Microsoft-leverandøren.
3. På **Konfigurasjonsrepositorier**-siden velger du repositoriet for **Global**-typen, og deretter velger du **Åpne**. Hvis du blir spurt om godkjenning for å koble til Regulatory Configuration Service, følger du godkjenningsinstruksjonene.
4. På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet i venstre rute og velger **BBS (Storbritannia)**-formatkonfigurasjonen.
5. I **Versjoner**-hurtigkategorien velger du versjon **3.3** for den valgte ER-formatkonfigurasjonen.
6. Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet til den gjeldende forekomsten av Finance.

![Konfigurasjonsrepositorium-side](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Hvis du har problemer med å få tilgang til det [globale repositoriet](er-download-configurations-global-repo.md), kan du [laste ned konfigurasjoner](download-electronic-reporting-configuration-lcs.md) fra LCS i stedet.

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Se gjennom importerte ER-formatkonfigurasjoner

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **BBS (Storbritannia)**.
4. Velg versjon **3.3** på hurtigfanen **Versjoner**.
5. Velg **Utforming**.
6. På **Formatutforming**-siden utvider du **BACSReportsFolder**-formatelement.
7.  Legg merke til at versjon 3.3 inneholder **PaymentAdviceReport**-formatelementet som brukes til å generere en betalingsmeldingsrapport når en leverandørbetaling behandles.

    ![PaymentAdviceReport-formatelement i ER-operasjonsutforming](./media/er-quick-start2-imported-solution2.png)

8. Lukk utformingssiden.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Ta i bruk endringene i den nye versjonen av et importert format i et egendefinert format

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Fullfør gjeldende utkastversjon av et egendefinert format

Hvis du vil beholde gjeldende tilstand for det egendefinerte formatet, må du fullføre utkastversjonen 1.1.1 ved å endre statusen fra **Utkast** til **Fullført**.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og utvider **BBS (Storbritannia)** og velger **BBS (Storbritannia egendefinert)**.
4. I **Versjon**-hurtigfanen velger du **Endre status** \> **Fullført**, og deretter velger du **OK**.

Statusen for versjon 1.1.1 endres fra **Utkast** til **Fullført**, og versjonen blir skrivebeskyttet. En ny redigerbar versjon, 1.1.2, har blitt lagt til og har statusen **Utkast**. Du kan bruke denne versjonen til å gjøre ytterligere endringer i det egendefinerte ER-formatet.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Rebasere et egendefinert format på nytt til en ny grunnversjon

Hvis du vil begynne å bruke den nye funksjonaliteten i versjon 3.3 av **BBS (Storbritannia)**-formatet i tilpasningen, må du endre basiskonfigurasjonsversjonen for den egendefinerte konfigurasjonen, **BBS (Storbritannia egendefinert)**. Denne prosessen kalles [rebasering](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase). Bruk den nye versjon 3.3 i stedet for versjon 1.1 av **BBS (Storbritannia)**.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **BBS (Storbritannia egendefinert)**.
3. På **Versjoner**-hurtigfanen velger du versjon **1.1.2** og deretter **Rebaser**.
4. I **Rebaser**-dialogboksen i **Målversjon**-feltet velger du versjon **3.3** av den grunnkonfigurasjonen for å bruke den som det nye grunnlaget, og bruker den til å oppdatere konfigurasjonen.

    ![Dialogboksen Rebaser](./media/er-quick-start2-rebase1.png)

5. Velg **OK**.
6. Legg merke til at nummeret til utkastversjonen er endret fra **1.1.2** til **3.3.2** for å gjenspeile endringen i grunnversjonen.

    Når den egendefinerte versjonen og en ny grunnleggende versjon slås sammen, kan enkelte konflikter oppdages på grunn av formatendringer som ikke kan slås sammen automatisk.

    ![Rebasert konfigurasjon med konflikter på Konfigurasjoner-siden](./media/er-quick-start2-rebase2.png)

    Hvis det oppdages konflikter, må de løses manuelt i formatutformingen.

7. Velg versjon **3.3.2** på hurtigfanen **Versjoner**.
8. Velg **Utforming**.
9. På **Formatutforming**-siden, på **Detaljer**-hurtigfanen, velger du en rebaseringskonfliktpost og velger **Bruk basisverdi**.

    ![Rebaseringskonfliktposten i ER-operasjonsutforming](./media/er-quick-start2-rebase3.png)

10. Velg **Lagre**.

    Rebaseringskonfliktposten skal ikke lenger vises i **Detaljer**-hurtigfanen.

    ![Konflikt løst i ER-operasjonsutforming](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Du løste konflikten ved å bekrefte at versjon 3 av basismodellen må brukes i dette ER-formatet.

11. Utvid **BACSReportsFolder** \> **fil** \> **transaksjoner** \> **transaksjon**.
12. Legg merke til at versjon 3.3.2 av det egendefinerte formatet i **Tilordning**-fanen inneholder både tilpasningen (**vendBankSWIFT**-formatelementet og bindingen) og den nye funksjonaliteten til versjon 3.3 av basis-ER-formatet som ble levert av Microsoft (**PaymentAdviceReport**-formatelementet sammen med nestede og konfigurerte bindinger). Med bare noen få museklikk har du tatt i bruk endringene i en ny basisversjon ved å slå dem sammen med tilpasning.

    ![Sammenslått format i ER-operasjonsutforming](./media/er-quick-start2-rebase5.png)

13. Lukk utformingssiden.

> [!NOTE]
> Rebaseringshandlingen er reversibel. Hvis du vil avbryte denne rebaseringen, velger du **1.1.1** av **BBS (Storbritannia egendefinert)**-formatet i **Versjoner**-hurtigfanen, og deretter velger du **Hent denne versjonen**. Versjon 3.3.2 blir deretter omnummerert 1.1.2, og innholdet i utkastversjon 1.1.2 vil samsvare med innholdet i versjon 1.1.1.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Behandle en leverandørbetaling ved hjelp av et rebasert ER-format

1. Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.
2. På siden **Leverandørbetalingsjournal** velger du betalingsjournalen du opprettet tidligere.
3. Velg **Linjer**.
4. På **Leverandørbetalinger**-siden velger du **Betalingsstatus** \> **Ingen** over rutenettet.
5. Velg **Generer betaling**.
6. Angi følgende informasjon i dialogboksen **Generer betalinger**:

    - Velg **Elektronisk** i feltet **Betalingsmåte**.
    - Velg **GBSI OPER** i feltet **Bankkonto**.

7. Velg **OK**.
8. Angi følgende informasjon i dialogboksen **Parametere for elektronisk rapportering**:

    - Sett alternativet **Skriv ut kontrollrapport** til **Ja**.
    - Sett alternativet **Skriv ut betalingsmelding** til **Ja**.

    ![Dialogboksen Parametere for elektronisk rapport](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > I tillegg til betalingsfilen kan du nå generere både kontrollrapporten og betalingsmeldingsrapporten.

9. Velg **OK**.
10. Last ned zip-filen, og pakk deretter ut følgende filer:

    - Kontrollrapporten i Excel-format
    - Betalingsmeldingsrapporten i Excel-format

        ![Betalingsmeldingsrapport i Excel-format](./media/er-quick-start2-payment-advice-report.png)

    - Betalingsfilen i TXT-format

        Legg merke til at betalingslinjen i den genererte filen nå starter med SWIFT-koden som ble angitt for bankkontoen til en leverandør som har utført betalingen.

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Laste ned ER-konfigurasjoner fra Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]