---
title: Mål for elektronisk rapportering (ER)
description: Dette emnet inneholder informasjon om administrasjon av mål for elektronisk rapportering, måltypene som støttes, og sikkerhetshensyn.
author: nselin
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e3154cb62531bf956365b420b454c98ead7f7335
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780467"
---
# <a name="electronic-reporting-er-destinations"></a>Mål for elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Du kan konfigurere et mål for hver formatkonfigurasjon for elektronisk rapportering (ER) og utdatakomponenten (en mappe eller en fil). Brukere som har riktige tilgangsrettigheter kan også endre målinnstillingene ved kjøretid. Dette emnet beskriver administrasjon av mål for elektronisk rapportering, måltyper som støttes og sikkerhetsvurderinger.

Formatkonfigurasjoner for elektronisk rapportering (ER) inneholder vanligvis minst én utdatakomponent: en fil. Konfigurasjoner inneholder vanligvis flere filutdatakomponenter av forskjellige typer (for eksempel XML, TXT, XLSX, DOCX eller PDF) som er gruppert i én eller flere mapper. Administrasjon av mål for elektronisk rapportering lar deg forhåndsdefinere hva som skjer når hver komponent kjøres. Når en konfigurasjon kjøres, vises det som standard en dialogboks som kan brukes til å lagre eller åpne filen. Den samme atferden forekommer også når du importerer en ER-konfigurasjon og ikke konfigurerer noen bestemte mål for den. Når et mål opprettes for en hovedutdatakomponent, overstyrer dette målet standard virkemåte, og mappen eller filen sendes i henhold til innstillingene for målet.

## <a name="availability-and-general-prerequisites"></a>Tilgjengelighet og generelle forutsetninger

Funksjonaliteten for mål for elektronisk rapportering er ikke tilgjengelig i Microsoft Dynamics AX 7.0 (februar 2016). Du må derfor installere Microsoft Dynamics 365 for Operations-versjon 1611 (november 2016) eller nyere for å kunne bruke følgende måltyper:

- [E-post](er-destination-type-email.md)
- [Arkiver](er-destination-type-archive.md)
- [Fil](er-destination-type-file.md)
- [Skjerm](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Du kan også installere én av følgende forutsetninger. Vær imidlertid oppmerksom på at disse alternativene gir en mer begrenset ER-målopplevelse.

- Microsoft Dynamics AX programversjon 7.0.1 (mai 2016)
- [Hurtigreparasjon for administrasjonsapp for mål for elektronisk rapportering](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Det finnes også en [Skriv ut](er-destination-type-print.md)-måltype. Hvis du vil bruke den, må du installere Microsoft Dynamics 365 Finance versjon 10.0.9 (april 2020).

## <a name="overview"></a>Oversikt

Du kan definere mål bare for ER-konfigurasjoner som er [importert](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) til gjeldende Finans-forekomst, og for formatene som er tilgjengelige på **Konfigurasjoner for elektronisk rapportering**-siden. Funksjonaliteten for ER-måladministrasjon er tilgjengelig på **Organisasjonsadministrasjon** \> **Elektronisk rapportering** \> **Mål for elektronisk rapportering**.

### <a name="default-behavior"></a>Standard virkemåte

Standard virkemåte for en ER-formatkonfigurasjonen er avhengig av utførelsestypen du angir når et ER-format starter.

Hvis du setter alternativet **Satsvis behandling** til **Nei** i dialogboksen **Intrastat-rapport** i hurtigfanen **Kjør i bakgrunnen**, kjøres et ER-format umiddelbart i interaktivt modus. Når utførelsen er fullført, gjøres et generert utgående dokument tilgjengelig for nedlasting.

Hvis du setter **Satsvis behandling**-alternativet til **Ja**, kjøres et ER-format i [satsvis](../sysadmin/batch-processing-overview.md) modus. Den riktige satsvise jobben opprettes basert på parameterne du angir for fanen **Kjør i bakgrunnen** i dialogboksen **ER-parametere**.

> [!NOTE]
> Jobbeskrivelsen informerer deg om kjøringen av en ER-formattilordning. Det inneholder også navnet på ER-komponenten som kjøres.

[![Kjøre et ER-format.](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Du kan finne informasjon om denne jobben på flere steder:

- Gå til **Felles** \> **Forespørsler** \> **Satsvise jobber** \> **Mine satsvise jobber** for å kontrollere statusen for den planlagte jobben.
- Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjobber** for å kontrollere statusen for den planlagte jobben og utførelsesresultatene for den fullførte jobben. Når jobbutførelsen er fullført, velger du **Vis filer** på siden **Elektroniske rapporteringsjobber** for å hente et generert utgående dokument.

    > [!NOTE]
    > Dette dokumentet er lagret som et vedlegg av den gjeldende jobbposten og styres av rammeverket for [Dokumentbehandling](../../fin-ops/organization-administration/configure-document-management.md). [Dokumenttypen](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) som brukes til å lagre ER-artefakter av denne typen, er konfigurert i [ER-parameterne](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- På siden **Elektroniske rapporteringsjobber** velger du **Vis filer** for å vise listen over eventuelle feil og advarsler som ble generert under jobbutførelsen.

    [![Se gjennom ER-jobblisten.](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Brukerkonfigurert virkemåte

På **Mål for elektronisk rapportering**-siden kan du overstyre standardatferden for en konfigurasjon. Importerte konfigurasjoner vises ikke på denne siden før du velger **Ny** og deretter velger du en konfigurasjon å opprette innstillinger for i feltet **Referanse**.

[![Velge en konfigurasjon i referansefeltet.](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Når du har opprettet en referanse, kan du opprette et filmål for hver **Mappe**- eller **Fil**-komponent i ER-referanseformatet.

[![Opprette et filmål.](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Deretter kan du i **Målinnstillinger**-dialogboksen aktivere og deaktivere individuelle mål for filmålet. **Innstillinger**-knappen brukes til å kontrollere alle mål for et valgt filmål. I dialogboksen **Innstillinger for mål** kan du kontrollere hver målet separat ved å sette alternativet **Aktivert** for det.

I versjoner av Finans **før versjon 10.0.9** kan du opprette **ett filmål** for hver utdatakomponent av samme format, for eksempel en mappe eller en fil som er valgt i **Filnavn**-feltet. I **versjon 10.0.9 og nyere** kan du imidlertid opprette **flere filmål** for hver utdatakomponent av samme format.

Du kan for eksempel bruke denne funksjonaliteten til å konfigurere filmål for en filkomponent som brukes til å generere et utgående dokument i Excel-format. Ett mål ([Arkiv](er-destination-type-archive.md)) kan konfigureres til å lagre den opprinnelige Excel-filen i ER-jobberarkivet, og et annet mål ([E-post](er-destination-type-email.md)) kan konfigureres til samtidig å [konvertere](#OutputConversionToPDF) Excel-filen til PDF-format og sende PDF-filen per e-post.

[![Konfigurere flere mål for ett enkelt formatelement.](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Når du kjører et ER-format, kjøres alltid alle målene som ble konfigurert for komponentene for formatet. I Finance **versjon 10.0.17 og nyere** er i tillegg funksjonaliteten for ER-mål forbedret og lar deg nå konfigurere ulike sett med mål for ett ER-format. Denne konfigurasjonen merker hvert sett som konfigurert for en bestemt brukerhandling. API-en for ER er [utvidet](er-apis-app10-0-17.md), slik at en handling som brukeren utfører ved å kjøre et ER-format, kan tilbys. Handlingskoden som tilbys, sendes til ER-mål. Du kan kjøre ulike mål for et ER-format, avhengig av handlingskoden som tilbys. Hvis du vil ha mer informasjon, kan du se [Konfigurere handlingsavhengige ER-mål](er-action-dependent-destinations.md).

## <a name="destination-types"></a>Måltyper

Følgende mål støttes for øyeblikket for ER-formater. Du kan deaktivere eller aktivere alle typer samtidig. På denne måten kan du enten ikke gjør noe eller sende komponenten til alle konfigurerte mål.

- [E-post](er-destination-type-email.md)
- [Arkiver](er-destination-type-archive.md)
- [Fil](er-destination-type-file.md)
- [Skjerm](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Skriv ut](er-destination-type-print.md)

## <a name="applicability"></a>Relevans

Du kan definere mål bare for ER-konfigurasjoner som er importert, og formater som er tilgjengelige på siden **Elektroniske rapporteringskonfigurasjoner**.

> [!NOTE]
> Konfigurerte mål er selskapsspesifikke. Hvis du planlegger å bruke et ER-format i forskjellige selskaper for gjeldende Finans-forekomst, må du konfigurere mål for dette ER-formatet for hvert av disse selskapene.

Når du konfigurerer filmål for et valgt format, kan du konfigurere dem for hele formatet.

[![Konfigurasjonskobling.](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Samtidig har du kanskje flere [versjoner](general-electronic-reporting.md#component-versioning) av formatet som er importert til gjeldende Finans-forekomst. Du kan vise dem hvis du velger **Konfigurasjon**-koblingen som tilgjengeliggjøres når du velger **Referanse**-feltet.

[![Konfigurasjonsversjoner.](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Som standard brukes konfigurerte mål bare når du kjører en ER-formatversjon som har statusen **Fullført** eller **Delt**. Noen ganger må du imidlertid bruke konfigurerte mål når utkastversjonen av et ER-format kjøres. Du kan for eksempel endre en utkastversjon av formatet, og det er lurt å bruke konfigurerte mål til å teste hvordan genererte utdata vil bli levert. Følg disse trinnene for å bruke mål for et ER-format når utkastversjonen kjøres.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. Sett **Bruk mål for utkaststatus**-alternativet til **Ja**.

[![Bruk mål for utkaststatus-alternativet.](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Hvis du vil bruke utkastversjonen av et ER-format, må du markere ER-formatet tilsvarende.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. Sett **Kjør innstilling**-alternativet til **Ja**.

[![Kjør innstilling-alternativet.](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Når du har fullført dette oppsettet, blir **Kjør utkast**-alternativet tilgjengelig for ER-formatene du endrer. Sett dette alternativet til **Ja** for å begynne å bruke utkastversjonen av formatet når formatet kjøres.

[![Kjør utkast-alternativet.](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Håndtering av målfeil

Vanligvis kjøres et ER-format innenfor omfanget til en bestemt bedriftsprosess. Leveringen av et utgående dokument som genereres under kjøring av et ER-format, må imidlertid noen ganger anses som en del av denne bedriftsprosessen. I dette tilfellet gjelder følgende: Hvis levering av et generert utgående dokument til et konfigurert mål mislykkes, må kjøringen av bedriftsprosessen avbrytes. Hvis du vil konfigurere riktig ER-mål, velger du **Stopp behandling ved feil**-alternativet.

Du konfigurerer for eksempel behandling av leverandørbetaling slik at ER-formatet for **ISO20022-kredittoverføring** kjøres for å generere betalingsfilen og tilleggsdokumentene (for eksempel følgeskrivet og kontrollrapporten). Hvis behandlingen av en betaling skal anses som fullført bare hvis følgeskrivet er levert via e-post, må du merke av i **Stopp behandling ved feil**-avmerkingsboksen for **Følgeskriv**-komponenten i riktig filmål, som vist i følgende illustrasjon. I dette tilfellet vil statusen til betalingen som er valgt for behandling, bli endret fra **Ingen** til **Sendt** bare når følgeskrivet som genereres, godtas for levering av en e-postleverandør som er konfigurert i Finans-forekomsten.

[![Konfigurere prosesshåndtering for filmålfeil.](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Hvis du opplever avmerkingen i **Stopp behandling ved feil**-avmerkingsboksen for **Følgeskriv**-komponenten i målet, vil en betaling bli ansett som behandlet selv når levering av følgeskrivet via e-post mislykkes. Status for betalingen vil bli endret fra **Ingen** til **Sendt** selv når følgeskrivet ikke kan sendes fordi mottakerens eller avsenderens e-postadresse eksempelvis mangler eller er feil.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Utdatakonvertering til PDF

Du kan bruke alternativet PDF-konvertering til å konvertere utdata i Microsoft Office-format (Excel eller Word) til PDF-format.

### <a name="make-pdf-conversion-available"></a>Gjøre PDF-konvertering tilgjengelig

Hvis du vil gjøre alternativet PDF-konvertering tilgjengelig i gjeldende Finans-forekomst, åpner du **Funksjonsadministrering**-arbeidsområdet og aktiverer funksjonen **Konverter utgående dokumenter for elektronisk rapportering fra Microsoft Office-formater til PDF**.

[![Aktivere PDF-konvertering av utgående dokumenter-funksjonen i Funksjonsadministrering.](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Relevans

I versjoner av Finance **før versjon 10.0.18** kan PDF-konverteringsalternativet bare slås på for **Excel\\Fil**-komponentene som blir brukt til å generere utdata i Office-format (Excel eller Word). Når dette alternativet er aktivert, konverteres utdata som genereres i Office-format, automatisk til PDF-format. I **versjon 10.0.18 og senere** kan du imidlertid også aktivere dette alternativet for komponenter av typen **Felles\\Fil**.

> [!NOTE]
> Vær oppmerksom på advarselsmeldingen du mottar når du aktiverer PDF-konverteringsalternativet for en ER-komponent av **Felles\\Fil**. Denne meldingen informerer deg om at det ikke finnes noen måte å garantere at den valgte filkomponenten vil eksponere innholdet i PDF-format eller PDF-konverterbart innhold ved kjøretid. Du bør derfor bare aktivere alternativet hvis du er sikker på at den valgte filkomponenten er konfigurert til å vise innholdet i PDF-format eller PDF-konverterbart innhold ved kjøretid.
> 
> Hvis du aktiverer PDF-konverteringsalternativet for en formatkomponent, hvis komponenten viser innhold i et annet format enn PDF-format, og hvis det viste innholdet ikke kan konverteres til PDF-format, vil det oppstå et unntak ved kjøretid. Meldingen du mottar, informerer deg om at det genererte innholdet ikke kan konverteres til PDF-format.

### <a name="limitations"></a>Begrensninger

Fra og med Finance **versjon 10.0.9** er PDF-konvertering bare tilgjengelig for skydistribusjoner. Fra og med Finance versjon **10.0.27** er PDF-konverteringsalternativet tilgjengelig for lokal distribusjon der [Internett-tilkobling](../user-interface/client-disconnected.md) er aktivert.

PDF-dokumentet som genereres, er begrenset til en maksimumslengde på 300 sider.

Fra og med Finance **versjon 10.0.9** støttes bare liggende papirretning i PDF-dokumentet som genereres fra Excel-utdata. Fra og med Finance **versjon 10.0.10** kan du [angi papirretningen](#SelectPdfPageOrientation) i PDF-dokumentet som genereres fra Excel-utdata mens du konfigurerer et ER-mål.

Bare de vanlige systemskriftene i Windows-operativsystemet brukes til å konvertere utdata som ikke inneholder innebygde skrifter.

### <a name="use-the-pdf-conversion-option"></a>Bruke alternativet PDF-konvertering

Hvis du vil aktivere PDF-konvertering for et filmål, merker du av i **Konverter til PDF**-avmerkingsboksen.

[![Aktivere PDF-konvertering for et filmål.](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Velg en sideretning for PDF-konvertering</a>

Hvis du genererer en ER-konfigurasjon i Excel-format og vil konvertere den til PDF-format, kan du eksplisitt angi papirretningen til PDF-dokumentet. Når du merker av for **Konverter til PDF** for å slå på PDF-konvertering for en fildestinasjon som produserer en utdatafil i Excel-format, blir **Sresultatproduktideretning**-feltet tilgjengelig på hurtigfanen **PDF-konverteringsinnstillinger**. Velg den foretrukne retningen i **Sideretning**-feltet.

[![Velge en sideretning for PDF-konvertering.](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

Hvis du vil ha muligheten til å velge PDF-papirretningen, installerer du Finance versjon 10.0.10 eller nyere. I versjoner av Finance **før versjon 10.0.23** tilbyr dette alternativet følgende alternativer for sideretning:

- Stående
- Liggende

Den valgte sideretningen brukes på alle sider for et utgående dokument som genereres i Excel-format, og deretter konverteres til PDF-format.

I **versjon 10.0.23 og senere** er imidlertid listen over alternativer for sideretning utvidet slik:

- Stående
- Liggende
- Regnearkspesifikk

Når du velger alternativet **Regnearkspesifikk**, konverteres hvert regneark i en generert Excel-arbeidsbok til PDF-format ved hjelp av en sideretning som er konfigurert for dette regnearket i den brukte Excel-malen. Det kan derfor hende at du har et endelig PDF-dokument som inneholder stående og liggende sider. 

Hvis en ER-konfigurasjon i Word-format konverteres til PDF-format, hentes papirretningen for PDF-dokumentet alltid fra Word-dokumentet.

## <a name="output-unfolding"></a>Oppheve folding av utdata

Når du konfigurerer et mål for **Mappe**-komponenten i ER-formatet, kan du angi hvordan utdataene for denne komponenten skal leveres til det konfigurerte målet.

### <a name="make-output-unfolding-available"></a>Gjøre oppheving av folding av utdata tilgjengelig

Hvis du vil gjøre alternativet for oppheving av folding tilgjengelig i gjeldende Finance-forekomst, åpner du arbeidsområdet **Funksjonsbehandling** og slår på funksjonen for **Tillat konfigurasjon av ER-mål for å sende mappeinnhold som separate filer**.

### <a name="applicability"></a>Relevans

Alternativet for oppheving av folding av utdata kan bare konfigureres for formatkomponentene for **Mappe**-typen. Når du begynner å konfigurere en **Mappe**-komponent, blir hurtigfanen **Generelt** tilgjengelig på siden **Mål for elektronisk rapportering**. 

### <a name="use-the-output-unfolding-option"></a>Bruke alternativet for oppheving av folding av utdata

I hurtigfanen **Generelt** i feltet **Send mappe som** velger du en av følgende verdier:

- **ZIP-arkiv** – Lever en generert fil som en zip-fil.
- **Separate filer** – Lever hver fil av en generert zipfil som en individuell fil.

    > [!NOTE]
    > Når du velger **Separate filer**, samles de genererte utdataene i minnet i zippet tilstand. Derfor brukes maksimum [filstørrelsesgrense](er-compress-outbound-files.md) for zipped utdata når den reelle filstørrelsen kan overskride denne grensen. Vi anbefaler at du velger denne verdien når du forventer at størrelsen på de genererte utdataene er ganske stor.

[![Konfigurere et mål for en mappeformatkomponent.](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>Begrensninger

Hvis du angir **Send mappe som**-feltet til **Separate filer** for en **Mappe**-komponent som inneholder andre nestede **Mappe**-komponenter, blir ikke innstillingene brukt rekursivt på de nestede **Mappe**-komponentene.

## <a name="security-considerations"></a>Sikkerhetshensyn

To typer rettigheter og plikter brukes for ER-mål. Én type styrer brukerens mulighet til å opprettholde målene som er konfigurert for en juridisk enhet (det vil si tilgang til siden **Mål for elektronisk rapportering**). Den andre typen styrer en applikasjonsbrukers mulighet til – under kjøretid – å overstyre målinnstillingene som en ER-utvikler eller ER-funksjonskonsulent har konfigurert.

| Rolle (AOT-navn)                     | Rollenavn                                  | Plikt (AOT-navn)                     | Pliktnavn                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Utvikler av elektronisk rapportering             | ERFormatDestinationConfigure        | Konfigurer mål for elektronisk rapporteringsformat                |
| ERFunctionalConsultant              | Funksjonell konsulent for elektronisk rapportering | ERFormatDestinationConfigure        | Konfigurer mål for elektronisk rapporteringsformat                |
| PaymAccountsPayablePaymentsClerk    | Leverandørbetalingsassistent            | ERFormatDestinationRuntimeConfigure | Konfigurer mål for elektronisk rapporteringsformat under kjøretid |
| PaymAccountsReceivablePaymentsClerk | Kundebetalingsassistent         | ERFormatDestinationRuntimeConfigure | Konfigurer mål for elektronisk rapporteringsformat under kjøretid |

> [!NOTE]
> To rettigheter brukes i de forrige pliktene. Disse rettighetene har samme navn som tilsvarende plikter: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Jeg har importert elektroniske konfigurasjoner, og jeg kan se dem på siden Elektroniske rapporteringskonfigurasjoner. Hvorfor jeg kan ikke se dem på siden Mål for elektronisk rapportering?

Pass på at du velger **Ny** og velger en konfigurasjon i feltet **Referanse**. Siden **Mål for elektronisk rapportering** viser bare konfigurasjoner som det er konfigurert mål for.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Er det mulig å definere hvilken Microsoft Azure Storage-konto og Azure Blob Storage som brukes?

Nei. Standard Microsoft Azure Blob Storage som er definert og brukes for dokumentbehandlingssystemet, brukes.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hva er formålet med filmålet i målinnstillingene? Hva gjør innstillingen?

**Fil**-målet brukes til å styre en dialogboks i nettleseren når du kjører et ER-format i interaktiv modus. Hvis du aktiverer dette målet, eller hvis ingen mål er definert for en konfigurasjon, vises en dialogboks for lagring eller åpning i nettleseren etter at en utdatafil er opprettet.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kan du gi et eksempel på en formel som refererer til en leverandørkonto som jeg kan sende e-post til?

Formelen er spesifikk for ER-konfigurasjonen. Hvis du for eksempel bruker konfigurasjonen ISO 20022 Kredittoverføring, kan du bruke **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** eller **modell. Payments.Creditor.Identification.SourceID** for å hente en tilknyttet leverandørkonto.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>En av mine formatkonfigurasjoner inneholder flere filer som er gruppert i én mappe (Mappe1 inneholder for eksempel Fil1, Fil2 og Fil3). Hvordan konfigurerer jeg mål slik at Mappe1.ZIP ikke opprettes i det hele tatt, Fil1 sendes via e-post, Fil2 sendes til SharePoint og jeg kan åpne Fil3 umiddelbart etter at konfigurasjonen er kjørt?

Formatet ditt må først være tilgjengelig i ER-konfigurasjonene. Hvis denne forutsetningen er oppfylt, åpner du **Mål for elektronisk rapportering**-siden og oppretter en ny referanse til konfigurasjonen. Deretter må du ha fire filmål, ett for hver utdatakomponent. Opprette første filmålet, gi det et navn, for eksempel **Mappe**, og velg et filnavn som representerer en mappe i konfigurasjonen. Velg deretter **Innstillinger**, og kontroller at alle mål er deaktivert. Mappen opprettes ikke for dette filmålet. Som standard, på grunn av hierarkiske avhengigheter mellom filer og overordnede mapper, vil filer fungere på samme måte. Med andre ord, de blir ikke sendt noe sted. Hvis du vil overstyre denne standard virkemåten, må du opprette tre filmål til, ett for hver fil. Du må aktivere målet som filen skal sendes til i målinnstillingene for hver av dem.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Konfigurere handlingsavhengige ER-mål](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
