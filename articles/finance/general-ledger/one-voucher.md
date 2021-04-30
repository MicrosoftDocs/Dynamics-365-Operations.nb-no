---
title: Ett bilag
description: Med ett bilag for finansjournaler (generell journal, anleggsmiddeljournal, leverandørbetalingsjournal og så videre) kan du angi flere underfinansjournaltransaksjoner i forbindelse med ett bilag.
author: kweekley
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 8229dc84040b1f3bd46d75c13795f0dc9b7e71f1
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897774"
---
# <a name="one-voucher"></a>Ett bilag

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>Hva er Ett bilag?

Med den eksisterende funksjonaliteten for finansjournaler (generell journal, anleggsmiddeljournal, leverandørbetalingsjournal og så videre) kan du angi flere underfinansjournaltransaksjoner (kunde, leverandør, anleggsmidler, prosjekt og bank) i forbindelse med ett bilag. Microsoft refererer til denne funksjonaliteten som *Ett bilag*. Du kan opprette ett bilag på en av følgende måter:

- Definer journalnavnet (**Økonomimodul** \> **Journaloppsett** \> **Journalnavn**) slik at feltet **Nytt bilag** er satt til **Bare ett bilagsnummer**. Hver linje du legger til i journalen, inkluderes nå i det samme bilaget. Derfor kan bilaget angis som et bilag med flere linjer, som en konto/motkonto på samme linje eller som en kombinasjon.

    [![Enkeltlinje](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Definisjonen av Ett bilag dekker **ikke** tilfeller der journalnavnene er angitt som **Bare ett bilagsnummer**, men brukeren angir deretter et bilag som bare inkluderer finanskontotyper. I dette emnet betyr Ett bilag at det er ett enkelt bilag som inneholder mer enn én leverandør, kunde, bank, aktiva eller prosjekt.

- Angi et bilag med flere linjer der det ikke er noen motkonto.

    [![Bilag med flere linjer](./media/Multi-line.png)](./media/Multi-line.png)

- Angi et bilag der både kontoen og motkontoen inneholder en underfinansjournalkontotype, for eksempel **Leverandør**/**Leverandør**, **Kunde**/**Kunde**, **Leverandør**/**Kunde** eller **Bank**/**Bank**.

    [![Underfinansbilag](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Problemer med Ett bilag

Funksjonen Ett bilag forårsaker problemer under utligning, avgiftsberegning, transaksjonstilbakeføring, avstemming av en underfinansjournal til økonomimodulen, finansrapportering og så videre. (Hvis du for eksempel vil ha mer informasjon om problemer som kan oppstå under utligning, kan du se [Enkelt bilag med flere poster for kunde eller leverandør](../accounts-payable/single-voucher-multiple-customer-vendor-records.md).) Hvis du vil arbeide og rapportere riktig, krever disse prosessene og rapportene transaksjonsdetaljer. Selv om noen scenarier fremdeles kanskje fungerer på riktig måte, avhengig av oppsettet i organisasjonen, er det ofte problemer når flere transaksjoner er angitt på ett bilag.

La oss for eksempel si at du posterer følgende bilag med flere linjer.

[![Eksempel på et bilag med flere linjer](./media/example.png)](./media/example.png)

Deretter genererer du rapporten **Utgifter etter leverandør** i arbeidsområdet **Økonomisk innsikt**. På denne rapporten er utgiftskontosaldoer gruppert etter leverandørgruppe og deretter leverandør. Når du genererer rapporten, kan ikke systemet fastslå hvilken leverandørgruppe/leverandører som påløp utgiften på 250,00. Det mangler transaksjonsdetaljer, og derfor forutsetter systemet at hele summen på 250,00 ble påløpt av den første leverandøren på bilaget. Utgiften 250,00, som er inkludert på saldoen for hovedkontoen 600120, vises derfor under den leverandørgruppen/leverandøren. Men det er svært sannsynlig at den første leverandøren på bilaget ikke var den riktige leverandøren. Rapporten er derfor sannsynligvis feil.

[![Utgifter etter leverandørrapport](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Fremtiden for Ett bilag

På grunn av problemer som kan oppstå når Ett bilag brukes, vil denne funksjonaliteten til slutt bli avskrevet. Men fordi det er funksjonshull som avhenger av denne funksjonaliteten, vil ikke avskrivingen skje med én gang. I stedet bruker vi følgende tidsplan:

- **Versjonen våren 2018** – Denne funksjonen ble deaktivert som standard via parameteren **Tillat flere transaksjoner i ett bilag** i kategorien **Generelt** på siden **Parametere for økonomimodul**. Du kan imidlertid aktivere den igjen hvis organisasjonen har et scenario som faller inn under et av funksjonshullene som er oppført tidligere i dette emnet.

    - Hvis forretningsscenariet ikke krever Ett bilag, anbefaler vi at du lar funksjonaliteten være avslått. Hvis du bruker den selv om en annen løsninge eksisterer, kommer ikke Microsoft ikke å reparere "feil" på områder som er identifisert senere i dette emnet.
    - Vi anbefaler at du slutter å bruke Ett bilag for integreringer, med mindre funksjonen kreves for et av de dokumenterte funksjonshullene.

- **Senere versjoner** – Flere forretningsbehov kan oppfylles ved hjelp av Ett bilag. Microsoft må sikre at alle de identifiserte forretningskravene fremdeles kan oppfylles i systemet etter at funksjonaliteten er avskrevet. Derfor må nye funksjoner sannsynligvis legges til for å fylle funksjonshullene. Microsoft kan ikke oppgi en bestemt løsning, fordi hver funksjonsforskjell er forskjellig og må evalueres basert på forretningskravene. Noen funksjonshull vil sannsynligvis bli erstattet med funksjoner som hjelper til med å oppfylle bestemte forretningskrav. Andre hull kan imidlertid fylles ved å fortsette å tillate registrering i en journal, som når Ett bilag brukes, men systemet kan etterhvert spore flere detaljer etter behov.

Når alle funksjonshullene er fylt, vil Microsoft kommunisere at funksjonen vil bli avskrevet. Avskrivningen vil imidlertid ikke være gyldig i minst ett år etter den gjeldende kommunikasjonen. Selv om Microsoft ikke kan gi et estimat for når Ett bilag-funksjonaliteten vil bli avskrevet, vil det sannsynligvis være minst to år før avskrivelsen finner sted. Microsofts policy er å la det være minst 12 måneder mellom kunngjøringen av avskrivningsfunksjonaliteten og den faktiske avskrivningen, slik at kunder og uavhengige programvareleverandører har tid til å reagere på endringen. En organisasjon må for eksempel kanskje oppdatere sine forretningsprosesser, enheter og integreringer.

Avskrivningen av Ett bilag er en betydelig endring som vil bli kommuniseret bredt. Som et ledd i den kommunikasjonen vil Microsoft oppdatere dette emnet, postere et blogginnlegg på Microsoft Dynamics 365 Finance-bloggen, oppdatere emnet "Funksjoner som er fjernet eller avskrevet", kommunisere endringen på passende Microsoft-konferanser og så videre.

## <a name="why-use-one-voucher"></a>Hvorfor bruke Ett bilag?

Basert på samtaler med kunder har Microsoft kompilert følgende liste over scenarier der kunder bruker funksjonen Ett bilag, eller årsaker til hvorfor de bruker funksjonen. Noen av disse forretningsbehovene kan oppfylles ved hjelp av Ett bilag. I mange scenarier kan imidlertid alternativer oppfylle de samme forretningsbehovene.

### <a name="scenarios-that-require-one-voucher"></a>Scenarier som krever Ett bilag

Følgende scenarier kan gjennomføre bare ved hjelp av funksjonen Ett bilag. Hvis organisasjonen har noen av disse scenariene, må du aktivere flere transaksjoner som skal angis i et bilag, ved å endre innstillingen for parameteren **Tillat flere transaksjoner i ett bilag** på siden **Parametere for økonomimodul**. Disse funksjonshullene vil bli fylt med andre funksjoner i senere versjoner.

> [!Note]
> [For hvert av følgende scenarier må feltet **Tillat flere transaksjoner i ett bilag** settes til Ja i hurtigfanen **Generelt** på siden **Parametere for økonomimodul**.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Postere leverandør- eller kundebetalinger i forenklet form til en bankkonto

**Scenario** En organisasjon sender en liste over leverandører og beløp til banken, og banken bruker denne listen til å betale leverandører på organisasjonens vegne. Banken posterer summen av betalingene som ett enkelt uttak for bankkontoen.

Oppsummering for leverandørbetalinger støttes bare ved hjelp av Ett bilag. Hver leverandør angis som en egen linje for å opprettholde detaljene i underfinansjournalen Leverandører. Det samlede beløpet for alle betalingene motposteres imidlertid til én linje for bankkontoen. Derfor vises uttaket som ett enkelt samlet beløp i bankens underfinansjournal.

**Scenario** En organisasjon betaler inn kundebetalinger, eller banken betaler inn kundebetalinger på vegne av organisasjonen, og innbetalingen vises som et engangsbeløp for bankkontoen.

Oppsummering av kundebetalinger støttes vanligvis via funksjonaliteten for betalingsbilag. Hvis du bruker "mellomkontoen" for den valgte betalingsmåten, støttes imidlertid dette scenariet bare gjennom Ett bilag. Kundebetalingene angis på samme måte som er beskrevet for oppsummering av leverandørbetaling.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Mekanisme for å gruppere transaksjoner fra en forretningshendelse

**Scenario** En organisasjon har én forretningshendelse som utløser flere transaksjoner. Regnskapsavdelingen ønsker imidlertid å vise poster sammen for å få bedre kvalitet på regnskapsføringen.

Hvis en organisasjon må vise regnskapspostene fra en forretningshendelse sammen, må den bruke Ett bilag. 

### <a name="country-specific-features"></a>Landspesifikke funksjoner

**Scenario** SAD-funksjonen (Single Administrative Document) for Polen krever for øyeblikket at ett bilag brukes. Inntil et grupperingsalternativ er tilgjengelig for denne funksjonen, må du fortsette å bruke funksjonen Ett bilag. Det kan være flere landspesifikke funksjoner som krever funksjonen ett bilag.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Forskuddsbetaling for kundebetalingsjournal som har avgifter på flere "linjer"

I dette scenariet er kundene på enkeltbilaget den samme kunden, fordi transaksjonen simulerer linjene i en kundeordre. Forskuddsbetalingen må angis på ett bilag, fordi mva-beregningen må utføres på "linjene" for enkeltbetalingen som kunden utførte.

### <a name="customer-reimbursement"></a>Kunderefusjon

**Scenario** En kunde gjør et forskudd for en ordre, og linjene i ordren har ulike avgifter som må registreres for forskuddsbetalingen. Kundeforskuddsbetalingen er én transaksjon som simulerer linjene i ordren slik at den aktuelle avgiften kan registreres for beløpet på hver linje.

Hvis refusjonens periodiske oppgave kjøres fra kundemodulen, opprettes det en transaksjon for å flytte saldoen fra en kunde til en leverandør. I dette scenariet må Ett bilag brukes til å refundere kunden.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Vedlikehold av anleggsmiddel: oppsamlingsavskrivning, delt anleggsmiddel, beregn avskrivning ved avhending
Følgende anleggsmiddeltransaksjoner oppretter også flere transaksjoner i et enkelt bilag:

- En ekstra anskaffelse gjøres på et anleggsmiddel og "oppsamlingsavskrivning" beregnes.
- Et anleggsmiddel er delt.
- En parameter for å beregne avskrivning ved avhending aktiveres, og deretter avhendes anleggsmiddelet.
- Servicedatoen for et anleggsmiddel er før anskaffelsesdatoen. Derfor posteres en avskrivningsjustering.

> [!Note]
> Når du angir transaksjoner, må du kontrollere at alle transaksjonene gjelder det samme anleggsmidlet. Bilaget blir ikke postert hvis det inneholder mer enn ett anleggsmiddel, selv om **Nytt bilag**-feltet er satt til Bare ett bilagsnummer på **Journalnavn**-siden i økonomimodulen. Hvis du tar med flere anleggsmidler i bilaget, vises meldingen **Det kan bare være én anleggsmiddeltransaksjon per bilag**, og du vil ikke kunne postere bilaget.  

### <a name="bills-of-exchange-and-promissory-notes"></a> Veksel og egenveksler
Veksler og egenveksler krever at Ett bilag brukes, fordi transaksjonene flytter kunde- eller leverandørsaldoen fra én Kunder/Leverandører-finanskonto til en annen basert på statusen for betalingen.

## <a name="scenarios-that-dont-require-one-voucher"></a>Scenarier som ikke krever Ett bilag

Følgende scenarier kan utføres på andre måter, og bør ikke bruke Ett bilag-funksjonaliteten.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Postere kundebetalinger i forenklet form til bankkontoen

En organisasjon betaler inn kundebetalinger, eller bankens betaler inn kundebetalinger på vegne av organisasjonen, og innbetalingen vises som et engangsbeløp for bankkontoen.

Oppsummering av kundebetalinger støttes gjennom innskuddsfunksjonaliteten når bruk av "mellompostering" ikke brukes for betalingsmåten.

### <a name="netting"></a>Motregning

I motregningen beregnes saldoer for en leverandør og kunde mot hverandre, fordi leverandøren og kunden er den samme parten. Denne fremgangsmåten reduserer utveksling av penger mellom en organisasjon og kunde-/leverandørparten.

Motregning kan gjøres ved å angi tillegget og reduksjonen på egne bilag, og deretter postere forskyvningen til en klareringsfinanskonto.

### <a name="post-in-summary-to-the-general-ledger"></a>Postere i forenklet form til økonomimodulen

Organisasjoner vil ofte postere til økonomimodulen i forenklet form for å redusere mengden data. Slike organisasjoner krever imidlertid vanligvis fortsatt at transaksjonsdetaljer opprettholdes. Når postering er utført i forenklet form til ett bilag, er ikke transaksjonsdetaljene kjent og kan ikke opprettholdes.

- Ettersom transaksjonsdetaljene for øyeblikket ikke kan opprettholdes, anbefales det at organisasjonen **ikke** bruker Ett bilag til å postere i forenklet form.
- Etter at støtte for Ett bilag har opphørt, kan rammeverkene Kildedokument og Regnskapsrammeverk implementeres i journalene. Disse rammeverkene vil deretter opprettholde transaksjonsdetaljene og støtte oppsummering til økonomimodulen.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Utligne flere ikke-posterte betalinger til den samme fakturaen

Dette scenariet finnes vanligvis i organisasjoner der kunder kan bruke flere betalingsmåter for å betale for innkjøp. I dette scenariet kan organisasjonen registrere flere uposterte betalinger og utligne dem mot kundefakturaen.

En ny funksjon som ble lagt til i Microsoft Dynamics 365 for Operations versjon 1611 (november 2016), gjør at flere uposterte betalinger kan utlignes mot én enkelt faktura. Flere kundebetalinger må ikke lenger registreres på ett bilag.

### <a name="import-bank-statement-transactions"></a>Importere bankkontoutdragstransaksjoner

Banker betaler og mottar ofte betalinger på vegne av en organisasjon, og disse transaksjonene registreres i Finance via en fil som er mottatt fra banken. Organisasjoner vil ofte gruppere disse transaksjonene ved hjelp av nummeret på bankkontoutdraget i filen. Hver transaksjon vises detaljert på bankkontoutdraget, og derfor kreves det ingen oppsummering i den bankens underfinansjournal.

Transaksjoner kan grupperes ved hjelp av andre felt i journalen, for eksempel selve journalpartinummeret eller bilagsnummeret.


### <a name="transfer-balances"></a>Overfør saldoer

En organisasjon må kanskje overføre en saldo fra én leverandør til en annen leverandør, enten på grunn av en feil, eller fordi en annen leverandør har overtatt hele ansvaret. Overføringer av denne typen kan også forekomme for kontotyper som **Kunde** og **Bank**.

Saldooverføringer fra én konto (leverandør, kunde, bank og så videre) til en annen konto kan gjøres via egne bilag, og forskyvningen kan posteres til en klareringsfinanskonto.

### <a name="enter-beginning-balances"></a>Registrere startsaldoer

Organisasjoner registrerer ofte startsaldoer for underfinansjournalkontoer (leverandører, kunder, anleggsmidler og så videre) som én bilagstransaksjon. Startsaldoer for hver konto for underfinansjournal kan angis som egne bilag, og forskyvningen kan posteres til en klareringsfinanskonto.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Korrigere regnskapsposten i et bokført kunde- eller leverandørdokument

En organisasjon må kanskje korrigere kundereskontro eller leverandøreskontro for en regnskapspost av en bokført faktura, men den fakturaen kan ikke tilbakeføres eller korrigeres via en annen mekanisme.

Hvis en korrigering må utføres i Kunde- eller Leverandørfinanskontoen, må en justering gjøres direkte på finanskontoen. Justeringen kan ikke gjøres ved postering til leverandøren eller kunden. Denne fremgangsmåten krever at justeringen gjøres under "nedetid", slik at finanskontoen kan tillate manuell registrering midlertidig.

### <a name="the-system-allows-it"></a>"Systemet tillater det"

Organisasjoner bruker ofte funksjonaliteten Ett bilag bare fordi systemet lar dem bruke den, uten å forstå implikasjonene.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]