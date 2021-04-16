---
title: Generer fritekstfakturaskjemaer som kan skrives ut
description: Dette emnet forklarer hvordan du bruker elektronisk rapportering-rammeverket (ER) til å generere utskrivbare fritekstfakturaskjemaer (FTI) som Microsoft Office-dokumenter.
author: NickSelin
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 9e64899e0bbdb5a9d8899e865de9ee32aae59382
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751662"
---
# <a name="generate-printable-fti-forms"></a>Generere FTI-skjemaer som kan skrives ut

[!include[banner](../includes/banner.md)]

Elektronisk rapportering-rammeverket (ER) lar deg generere utskrivbare fritekstfakturaskjemaer (FTI) som Microsoft Office-dokumenter. Dette emnet gir informasjon om hvordan du bygger dine egne konfigurasjoner, samt detaljer om tilgjengelige konfigurasjonsmaler.

## <a name="overview"></a>Oversikt

I tillegg til den eksisterende funksjonen for generering av utskrivbare FTI-skjemaer ved hjelp av Microsoft SQL Server Reporting Services (SSRS), kan du nå bruke ER-rammeverket. Du kan administrere utskrivbare FTI-skjemaer i Microsoft Office Excel og Word. Du kan også endre oppsettet, dataflyt og formatering for å dekke bestemte behov uten å gjøre endringer i koden.

> [!NOTE]
> Hvis du vil starte med en oversikt over eksisterende ER-konfigurasjoner for dette eksemplet av den utskrivbare FTI-skjemaløsningen, kan du gå direkte til delen **Laste ned eksempel-ER-konfigurasjoner for å generere utskrivbare FTI-skjemaer** senere i dette emnet.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Opprette egendefinerte konfigurasjoner for utskrivbare FTI-skjemaer
Som en del av din egendefinerte løsning for utskrivbare FTI-skjemaer må du opprette et sett med ER-konfigurasjoner.

### <a name="configure-the-er-data-model"></a>Konfigurere ER-datamodellen
Programmet ditt må inkludere ER-datamodellkonfigurasjonen som inneholder en datamodell som beskriver forretningsområdet for kundefakturering. Som et krav må navnet på datamodellen være **Kundefakturering**. For informasjon om hvordan du utformer ER-datamodeller, se [ER Utforme domenespesifikk datamodell](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>Konfigurere ER-modelltilordningen
Programmet må inneholde modellen ER-tilordningen for Kundefakturering-datamodellen. Modelltilordningen kan være enten ER-datamodellkonfigurasjonen eller ER-modelltilordningskonfigurasjonen. Men navnet på rotbeskrivelsen for modelltilordningen må være **Fritekstfaktura**.

Tilordningen må inneholde følgende datakilder:

- Datakildetype: **Tabellposter**

    - Denne datakilden må ha navnet **CustInvoiceJour**.
    - Det må referere til CustInvoiceJour-programtabellen.
    - Den brukes under kjøring til å overføre listen over fakturaer som er valgt for utskrift, fra programmet til ER-modelltilordningen.

- Datakildetype: **Objekt**

    - Denne datakilden må ha navnet **PrintMgmtPrintSettingDetail**.
    - Den må referere til **PrintMgmtPrintSettingDetail**-programklassen.
    - Den brukes under kjøring til å overføre utskriftsbehandlingsinnstillinger for ER-formatet som kjører, fra programmet til ER-modelltilordningsinformasjonen.

Detaljer om programintegreringen med ER-rammeverket finnes i **ERPrintMgmtReportFormatSubscriber**-klassen (integreringsmodell for ER-programserie) i kildekoden for programmet.

Hvis du vil ha mer informasjon om utformingen av ER-modelltilordningene, se [Definere ER-modelltilordninger og velge datakilder for dem](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>Konfigurere ER-format
I din forekomst av programmet må du ha ER-formatkonfigurasjonen som skal brukes til å generere FTI-skjemaer. 

> [!NOTE]
> Denne formatkonfigurasjonen må opprettes for datamodellen Kundefakturering, og den må bruke modelltilordningen som har rotbeskrivelsen **Fritekstfaktura**.

Hvis du vil ha informasjon om hvordan du konfigurerer ER-formater, se [ER Opprette en formatkonfigurasjon (november 2016)](tasks/er-format-configuration-2016-11.md). Hvis du vil ha informasjon om hvordan du utformer ER-formater for å generere rapporter i OpenXML-format, kan du se [ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Konfigurere utskriftsbehandling
Hvis du vil generere FTI-skjemaer ved hjelp av ER-rammeverket, må du tilordne ER-formater på samme måte som du tilordner SSRS-rapporter. Hvis du vil tilknytte ER-formatet til alle Kunde-FTI-er, kan du gå til **Kunder** \> **Oppsett** \> **Skjemaer** \> **Skjemaoppsett** \> **Generelt** \> **Utskriftsbehandling** \> **Fritekstfaktura** \> **Original**. Bruk følgende fremgangsmåte for å knytte ER-formatet til en bestemt kunde eller faktura.

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Velg FTI-en som ER-formatet skal tilknyttes, og åpne **Oppsett for utskriftsbehandling**-siden.
3. Velg dokumentnivået for å angi omfanget av fakturaer for behandling.
4. Velg ER-formatet for det angitte dokumentnivået.

![Oppsett for utskriftsbehandling](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Bare ER-formater som bruker rotbeskrivelsen **Fritekstfaktura** for datamodellen **Kundefakturering**, vises i feltet **Rapportformat-oppslag** for det valgte formatet.

## <a name="generate-fti-forms"></a>Generere FTI-skjemaer
FTI-skjemaer genereres i ER-rammeverket på samme måte som SSRS-rapporter genereres.

Hvis du vil generere FTI-skjemaer, kan du velge fakturaer etter område eller valg. 

![Fakturavalg](media/FTIbyGER-InvoiceSelection.png)

![Forhåndsvisning av faktura](media/FTIbyGER-InvoiceExcelPreview.png)

Når du bruker ER-formater til å skrive ut FTI-skjemaer på denne måten, brukes standard ER-filmål. Du kan ikke endre målet. Hvis du vil ha mer informasjon om hvordan du konfigurerer ER-målene for ER-formater, se [Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md).

Du kan også generere FTI-skjemaer når du posterer en FTI, ved å slå på **Skriv ut faktura** og slå av **Bruk utskriftsbehandlingsmål**.

> [!NOTE]
> Når du bruker ER-formater til å skrive ut FTI-skjemaer på denne måten, brukes standard ER-filmål. Hvis målet er allerede konfigurert, kan du endre standardmålet under kjøring. Hvis du vil endre målet, må du ha følgende sikkerhetsrettighet:
>
> - **Navn:** ERFormatDestinationRuntimeMaintain
> - **Etikett:** Vedlikehold mål for elektronisk rapporteringsformat under kjøretid

![Mål for elektronisk rapportering](media/FTIbyGER-ERFileDestinationSetting.png)

![Mål for elektronisk rapporteringsformat](media/FTIbyGER-ERFileDestinationUsage.png)

ER-rammeverket støtter for øyeblikket følgende mål for genererte dokumenter:

- **Nedlastet fil** – Genererte skjemaer tilbys som nedlastinger som du kan lagre ved hjelp av nettleseren.
- **Skjerm** – Microsoft 365 Excel brukes til å forhåndsvise genererte FTI-skjemaer i Excel-format.
- **SharePoint-mappe** – Genererte skjemaer lagres basert på innstillingene for dokumentbehandlingsrammeverket.
- **Programarkiv** – Genererte skjemaer lagres som vedlegg til utførelsesloggposter i Microsoft Azure Storage.
- **E-post** – Genererte skjemaer sendes som e-postvedlegg.

> [!NOTE]
> Du kan ikke sende FTI-skjemaene som genereres, direkte til skriveren, fordi direkte utskrift som bruker rutingsagenten for Dynamics-skriveren, ikke støttes for øyeblikket.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Laste ned eksempel-ER-konfigurasjoner for å generere utskrivbare FTI-skjemaer
Du kan laste ned eksempel-ER-konfigurasjoner å bruke som en mal for FTI-løsningen. Konfigurasjonene lagres i det delte aktivabibliotek i Microsoft Dynamics Lifecycle Services (LCS). Konfigurasjonene omfatter:

- **Kundefakturamodell**-konfigurasjonen inneholder den nødvendige datamodellen og modelltilordningen.
- **Kunde-FTI-rapport (GER)**-konfigurasjonen inneholder eksempelformatet.

> [!NOTE]
> Disse konfigurasjonene har blitt opprettet som eksempler for å være til hjelp med mulige scenarier. Fremtidige konfigurasjoner er avhengige av resultatene av denne evalueringen og eventuell tilbakemelding som mottas.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Funksjoner som er implementert i eksempel-ER-formatetet
I eksempel-ER-formatkonfigurasjonen brukes en Excel-fil som en mal for å generere FTI-skjemaer.

![Formatutforming](media/FTIbyGER-ERFormat.png)

Dette eksempel-ER-formatet støtter for øyeblikket følgende funksjoner for generering av FTI-skjemaer:

- FTI-skjemaer genereres for både opprinnelige fakturaer som er postert, og opprinnelige fakturaer som ennå ikke er postert. Korrigerte fakturaer og kreditnotaer støttes ikke.
- FTI-skjemaer genereres på fakturaspråket. Formatet for verdier og datoer i de genererte skjemaene er basert på innstillingene for brukerens nasjonale innstillinger i klienten.
- Genererte fakturaer viser varslinger om datautilgjengelighet hvis det ikke finnes noen linjer i fakturaene som er behandlet.
- Genererte fakturahoder er basert på papirformatet som er valgt for FTI-skjemaet på siden **Kundeparametere**. Opplysninger om selskap vises i fakturahodet i det genererte fakturaskjemaet bare hvis papirformatet er tomt.
- Genererte fakturaskjemaer viser firma- og kundenumre for avgiftsfritak når det riktige alternativet er valgt for FTI-skjemaet på siden **Kundeparametere**.
- De genererte seksjonene for fakturalinjer og fakturatotaler viser standardfakturaens monetære detaljer i registreringsvalutaen for fakturaen.
- Den genererte fakturaens totaler-del kan vise monetære detaljer i eurovaluta og fakturaens registreringsvaluta når alternativet **Skriv ut beløp i valutaen som representerer euroen** er aktivert på siden **Kundeparametere**.
- Genererte fakturaskjemaer viser prosessfakturamerknader som er tilgjengelige, basert på innstillinger på siden **Kundeparametere**. Merknader er inkludert for både hele fakturaen og hver fakturalinje.
- Genererte fakturaskjemaer inneholder merknader for kunde-FTI-skjemaet og språket for fakturabehandlingen når dette er konfigurert i merknadslisten for AR-skjemaet.
- Avhengig av utskriftsbehandlingsinnstillingene inneholder genererte fakturaer egendefinert bunntekst når den er konfigurert for fakturaspråket, ER-formatet og FTI-dokumentområdet.
- Totaler-delen for genererte fakturaskjemaer inneholder kontantrabattinformasjon som er tilgjengelig.
- Delen for betalingsplan for genererte fakturaskjemaer inneholder alle betalingsplandetaljer som er tilgjengelige.
- Påslag-delen for de genererte fakturaskjemaene inneholder eventuelle tilleggstransaksjoner som er tilgjengelige.
- Genererte fakturaskjemaer inneholder merverdiavgiftsdetaljer basert på innstillingen **Mva-spesifikasjon** på siden **Kundeparametere**. Denne delen kan vise merverdiavgiftsdetaljer bare i fakturaregistreringsvalutaen eller i fakturaens registreringvaluta og firmaets regnskapsvaluta samtidig.
- Genererte fakturaskjemaer viser detaljer om avtalegirovarsler. De kan for eksempel vise når betalingsmåten som har obligatorisk avtalegiromandat-ID, ble valgt for fakturaen, når fakturabehandlingen ble registrert i eurovalutaen, og når avtalegiromandat-ID-en ble definert for fakturaen.
- Genererte fakturaer viser eventuelle detaljer om forskuddsbetaling som er tilgjengelige for posterte fakturaer.
- Genererte fakturaskjemaer kan sendes til en fakturakunde som et e-postvedlegg. Riktig ER-filmål må være konfigurert for ER-formatet som er i bruk.

### <a name="countryregion-specific-features"></a>Lands-/områdespesifikke funksjoner 
Følgende land-/områdespesifikke funksjoner er inkludert i eksempel-ER-formatet for å vise hvordan bestemte krav kan håndteres i ER-konfigurasjoner.

#### <a name="norway"></a>Norge
Begrepet Foretaksregister plasseres i overskriften til det genererte fakturaskjemaet når fakturaen behandles for en juridisk enhet som konfigureres på følgende måte:

- Land/område-kontekst for Norge blir brukt.
- **Skriv ut Foretaksregisteret**-parameteren er aktiv på salgsdokumenter.

#### <a name="spain"></a>Spania
Begrepet **Spesialordning for kontantregnskapsmetode** plasseres i overskriften til det genererte fakturaskjemaet når fakturaen behandles for en juridisk enhet som konfigureres på følgende måte:

- Land/område-kontekst for Spania blir brukt.
- Spesialordningen for kontantregnskapsmetode aktiveres på fakturabehandlingsdatoen.

Når informasjon om kontantrabatt, for eksempel kontantrabattbeløp og nettobeløp på fakturalinje, er tilgjengelig, vises de i delen for fakturatotaler i det genererte fakturaskjemaet når den behandles for en juridisk enhet som konfigureres på følgende måte:

- Land/område-kontekst for Spania blir brukt.
- **Kontantrabatt brukes i fakturaen** aktiveres i faktureringsalternativet (**Parametere for økonomimodul** \> **Merverdiavgift-delen**).

#### <a name="italy"></a>Italia
Varerabattmerket er inkludert på fakturalinjene i den genererte fakturaen når den behandles for en juridisk enhet som er konfigurert ved hjelp av konteksten land/område for Italia.

#### <a name="finland"></a>Finland
I tillegg til det genererte fakturaskjemaet kan overføringsseddelelen for girokort genereres på følgende måte:

- For den juridiske enheten som bruker land/område-konteksten for Finland, og som har minst én bankkonto som er merket som **Girokonto** og **Bankstrekkode**. 
- For en faktura som er merket som påkrevd for det **finske** tilknyttede betalingsvedlegget.

![Giroblankett](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> Eksempel-ER-formatet er konfigurert for eventuelt å generere girokort i separate regneark.

> [!NOTE]
> Du må først installere skriften som brukes til å generere strekkoden på den lokale maskinen der det genererte fakturaskjemaet i Excel-format skal forhåndsvises.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>Bruk eksempel-ER-formatet til å konfigurere e-postdestinasjoner
Bruk følgende elementer i eksempel-ER-formatet til å konfigurere e-postdestinasjoner:

- E-postadressen til en kundekontakt kan nås via følgende ER-uttrykk: **model.InvoiceBase.Contact.ElectronicMail**.
- Emneteksten for e-posten kan nås via følgende ER-uttrykk: **Emailing.TxtToUse.Subject**.
- Brødteksten for e-posten kan nås via følgende ER-uttrykk: **Emailing.TxtToUse.Body**.

![Innstillinger for mål](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Standardteksten for emne og brødtekst i e-posten er definert i eksempel-ER-formatet. Språket er avhengig av formatetikettene. Denne standardteksten brukes for e-post hvis en egendefinert organisasjons-e-postmal med den forhåndsdefinerte **ERFTITMP**-ID-en ikke er lagt til.

> [!NOTE]
> **ERFTITMP**-e-postmal-ID-en er definert i eksempel-ER-formatet. Den kan endres etter behov i et nytt ER-format som opprettes fra dette eksempelformatet.

Hvis organisasjonse-postmalen som har den forhåndsdefinerte **ERFTITMP**-ID-en, er lagt til for den juridiske enheten du behandler fakturaen for, brukes malen for e-postemnet og brødteksten til å generere e-postmeldingen. 

![Maler for e-post til organisasjon](media/FTIbyGER-EmailTemplate.png)

![Last opp e-postmal](media/FTIbyGER-EmailTemplateBody.png)

ER-uttrykket **Emailing.TxtToUse.Subject** for eksempel-ER-formatet konfigureres for å erstatte eventuelle forekomster av plassholderen %1 av behandlingsfaktura-ID-en.

**Emailing.TxtToUse.Body**-uttrykket for eksempelformatet konfigureres for følgende erstatninger for plassholdere:

- "%1" erstattes med navnet til kundens kontaktperson.
- "%2" erstattes med firmanavnet.
- "%3" erstattes med kundenavnet.
- "%4" erstattes med navnet til firmaets kontaktperson.
- "%5" erstattes med jobbtittelen til firmaets kontaktperson.
- "%6" erstattes med e-postadressen til firmaets kontaktperson.

![E-post](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Tilleggsressurser
[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]