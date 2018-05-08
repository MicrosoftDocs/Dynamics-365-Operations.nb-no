---
title: Ett bilag
description: "Med ett bilag for finansjournaler (generell journal, anleggsmiddeljournal, leverandørbetalingsjournal og så videre) kan du angi flere underfinansjournaltransaksjoner i forbindelse med ett bilag."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Ett bilag

[!include [banner](../includes/banner.md)]

> [!NOTE]
>  Denne funksjonaliteten blir tilgjengelig i Dynamics 365 for Finance and Operations versjon 8.0, som vil være tilgjengelig våren 2018.   

<a name="what-is-one-voucher"></a>Hva er "Ett bilag"?
======================

Den eksisterende funksjonaliteten for finansjournaler (generell journal, anleggsmiddeljournal, leverandørbetalingsjournal og så videre) kan du angi flere underfinansjournaltransaksjoner i forbindelse med ett bilag. Vi refererer til denne funksjonaliteten som "Ett bilag." Du kan opprette Ett bilag på en av følgende måter:

-   Definere journalnavnet (**Økonomimodul** \> **Journaloppsett** \>**Journalnavn**) slik at feltet **Nytt bilag** er satt til **Bare ett bilagsnummer**. * Hver linje du legger til journalen, inkluderes nå på det samme bilaget. Hver linje legges inn på samme bilag, og derfor kan bilaget angis som et bilag med flere linjer, som en konto/motkonto på samme linje eller som en kombinasjon.

[![Enkeltlinje](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Legg merke til at definisjonen av Ett bilag ikke inneholder journalnavnene som bare er angitt som **Ett bilagsnummer** og brukeren angir deretter et bilag som bare inkluderer finanskontotyper.  I dette dokumentet betyr Ett bilag at det er ett bilag som inneholder mer enn én leverandør, kunde, bank, aktiva eller prosjekt. 

-   Angi et bilag med flere linjer der det ikke er noen motkonto.

[![Bilag med flere linjer](./media/Multi-line.png)](./media/Multi-line.png)

-   Angi et bilag der både kontoen og motkontoen inneholder en underfinansjournalkontotype, for eksempel leverandør/leverandør, kunde/kunde, leverandør/kunde eller bank/bank.

[![Underfinansbilag](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Problemer med Ett bilag
=======================

Funksjonen Ett bilag forårsaker problemer under utligning, avgiftsberegning, avstemming av en underfinansjournal til økonomimodulen, finansrapportering og så videre. (Hvis du for eksempel vil ha mer informasjon om problemer som kan oppstå under utligning, kan du se [Enkelt bilag med flere poster for kunde eller leverandør](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Hvis du vil arbeide og rapportere riktig, krever disse prosessene og rapportene transaksjonsdetaljer. Selv om noen scenarier fremdeles kanskje fungerer på riktig måte, basert på oppsettet i organisasjonen, er det ofte problemer når flere transaksjoner er angitt på ett bilag.

La oss for eksempel si at du posterer følgende bilag med flere linjer.

[![Eksempel](./media/example.png)](./media/example.png)

Deretter genererer du rapporten **Utgifter etter leverandør** i arbeidsområdet **Økonomisk innsikt**. Rapporten grupperer utgiftskontosaldoer under leverandørgruppe og deretter leverandør. Når du genererer rapporten, kan ikke systemet fastslå hvilken leverandørgruppe/leverandører som påløp utgiften på 250,00. Det mangler transaksjonsdetaljer, og derfor forutsetter systemet at hele summen på 250,00 ble påløpt av den første leverandøren på bilaget. 250,00, som er inkludert på saldoen for hovedkontoen 600120, vises deretter under den leverandørgruppen/leverandøren. Det er svært sannsynlig at den første leverandøren på bilaget ikke var den riktige leverandøren, og dermed er rapporten feil.

[![Utgifter](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Fremtiden for Ett bilag
=========================

På grunn av problemene som ble nevnt tidligere, vil funksjonen Ett bilag bli foreldet. Men fordi det er funksjonshull som avhenger av denne funksjonaliteten, foreldes ikke funksjonaliteten samtidig. I stedet bruker vi følgende tidsplan: 

- **Versjonen våren 2018** – Funksjonaliteten blir deaktivert som standard via en parameter for økonomimodul. Du kan imidlertid aktivere funksjonen hvis organisasjonen har et scenario som faller inn under hullene i forretningsscenarier som er oppført tidligere i dette emnet.

  -   Hvis en kunde har et forretningsscenario som ikke krever Ett bilag, må du ikke aktivere funksjonen. Vi kommer ikke til å reparere "feil" i områder som ble identifisert senere i dette emnet, hvis denne funksjonaliteten brukes selv om det finnes en annen løsning.

  -   Slutt å bruke Ett bilag for integreringer i Microsoft Dynamics 365 Finance and Operations, med mindre funksjonen kreves for et av funksjonshullene.

- **Høsten 2018 og senere versjoner** – Funksjonshullene er fylt ut. Etter at funksjonshullene er fylt ut, deaktiveres funksjonen Ett bilag permanent.

- > [!IMPORTANT]
  > Vær oppmerksom på at **Bare ett bilagsnummer**-alternativet ikke er fjernet fra journalnavnoppsettet.  Dette alternativet støttes fortsatt når bilaget bare inneholder finanskontotyper.  Kunder må være forsiktige når de bruker denne innstillingen fordi bilaget ikke posteres hvis de bruker **Bare ett bilagsnummer**, men deretter angir mer enn én kunde, leverandør, bank, aktiva eller prosjekt.  Kunder kan også fremdeles angi en blanding av underfinansjournalkontotyper, for eksempel en betaling i en enkelt bilag som inneholder kontotyper fra leverandør/bank.  

<a name="why-use-one-voucher"></a>Hvorfor bruke Ett bilag?
====================

Basert på samtaler med kunder, har vi kompilert følgende liste over scenarier der kunder bruker funksjonen Ett bilag eller årsaker til hvorfor de bruker funksjonen. Noen av disse forretningsbehovene kan oppfylles ved hjelp av Ett bilag. I mange scenarier kan imidlertid alternativer oppfylle de samme forretningsbehovene.

<a name="scenarios-that-require-one-voucher"></a>Scenarier som krever Ett bilag
----------------------------------

Følgende scenarier kan gjennomføre bare ved hjelp av funksjonen Ett bilag. Disse funksjonshullene vil bli fylt med andre funksjoner i versjonen høsten 2018 samt senere versjoner.

-   **Postere leverandør- eller kundebetalinger i forenklet form til en bankkonto**

    -   En organisasjon sender en liste over leverandører og beløp til banken, og banken bruker denne listen til å betale leverandører på organisasjonens vegne. Banken posterer summen av betalingene som ett enkelt uttak for bankkontoen.

>   Oppsummering for leverandørbetalinger støttes bare ved hjelp av Ett bilag. Hver leverandør er angitt som en egen linje for å opprettholde detaljene i underfinansjournalen Leverandører, men det samlede beløpet for alle betalingene motposteres til én linje for bankkontoen. Derfor vises uttaket som ett enkelt samlet beløp i bankens underfinansjournal.

-   En organisasjon betaler inn kundebetalinger, eller bankens betaler inn kundebetalinger på vegne av organisasjonen, og innbetalingen vises som et engangsbeløp for bankkontoen.

>   Oppsummering av kundebetalinger støttes vanligvis via funksjonaliteten for betalingsbilag. Hvis du bruker "mellomkontoen" for den valgte betalingsmåten, støttes imidlertid dette scenariet bare gjennom Ett bilag. Kundebetalingene angis på samme måte som er beskrevet for oppsummering av leverandørbetaling.

-   **Mekanisme for å gruppere transaksjoner fra en forretningshendelse**

    -   En organisasjon har én forretningshandling som utløser flere transaksjoner. Regnskapsavdelingen ønsker imidlertid å vise poster sammen for å få bedre kvalitet på regnskapsføringen.

>   Hvis en organisasjon må vise regnskapspostene fra en forretningshendelse sammen, må den bruke Ett bilag. 

- **Landspesifikke funksjoner**

  -   SAD-funksjonen (Single Administrative Document) for Polen krever for øyeblikket at ett bilag brukes. Inntil et grupperingsalternativ er tilgjengelig for denne funksjonen, må du fortsette å bruke funksjonen Ett bilag. Det kan være flere landspesifikke funksjoner som krever funksjonen ett bilag.

- **Forskuddsbetaling for kundebetalingsjournal som har avgifter på flere "linjer"**

  -   En kunde gjør et forskudd for en ordre, og linjene i ordren har ulike avgifter som må registreres for forskuddsbetalingen. Kundeforskuddsbetalingen er én transaksjon som simulerer linjene i ordren slik at den aktuelle avgiften kan registreres for beløpet på hver linje.

I dette scenariet er kundene på enkeltbilaget den samme kunden, fordi transaksjonen simulerer linjene i en kundeordre. Forskuddsbetalingen må angis på ett bilag, fordi mva-beregningen må utføres på "linjene" for enkeltbetalingen som kunden utførte.

-   **Vedlikehold av anleggsmiddel: oppsamlingsavskrivning, delt anleggsmiddel, beregn avskrivning ved avhending**

Følgende anleggsmiddeltransaksjoner opprette også flere transaksjoner i et enkelt bilag:
-   En ekstra anskaffelse gjøres på et anleggsmiddel og "oppsamlingsavskrivning" beregnes.
-   Et anleggsmiddel er delt.
-   En parameter for å beregne avskrivning ved avhending aktiveres, og deretter avhendes anleggsmiddelet.

<a name="scenarios-that-dont-require-one-voucher"></a>Scenarier som ikke krever Ett bilag
----------------------------------------

Følgende scenarier kan utføres på andre måter, og bør ikke bruke Ett bilag.

-   **Postere kundebetalinger i forenklet form til bankkontoen**

En organisasjon betaler inn kundebetalinger, eller bankens betaler inn kundebetalinger på vegne av organisasjonen, og innbetalingen vises som et engangsbeløp for bankkontoen.

Oppsummering av kundebetalinger støttes gjennom innskuddsfunksjonaliteten når bruk av mellomkonto ikke brukes for den valgte betalingsmåten.

-   **Motregning**

I motregningen beregnes saldoer for en leverandør og kunde mot hverandre fordi leverandøren og kunden er den samme parten. Denne fremgangsmåten reduserer utveksling av penger mellom en organisasjon og kunde-/leverandørparten.

Motregning kan gjøres ved å angi tillegget og reduksjonen på egne bilag, og deretter postere forskyvningen til en klareringsfinanskonto.

-   **Postere i forenklet form til økonomimodulen**

Organisasjoner vil ofte postere til økonomimodulen i forenklet form for å redusere mengden data. Organisasjonene krever imidlertid vanligvis fortsatt at transaksjonsdetaljene opprettholdes. Når postering er utført i forenklet form til ett bilag, er ikke transaksjonsdetaljene kjent og kan ikke opprettholdes.

   -   Ettersom transaksjonsdetaljene for øyeblikket ikke kan opprettholdes, anbefales det at Ett bilag ikke brukes til å postere i forenklet form.
   -   Etter at støtte for Ett bilag har opphørt, kan vi implementere rammeverkene Kildedokument og Regnskapsrammeverk i journalene. Disse rammeverkene vil deretter opprettholde transaksjonsdetaljene og støtte oppsummering til økonomimodulen.

-   **Utligne flere ikke-posterte betalinger til den samme fakturaen**

Dette scenariet finnes vanligvis i Retail-organisasjoner der kunder kan bruke flere betalingsmåter for å betale for innkjøp. I dette scenariet kan organisasjonen registrere flere uposterte betalinger og utligne dem mot kundefakturaen.

En ny funksjon som ble lagt til i Microsoft Dynamics 365 for Operations versjon 1611 (november 2016), gjør at flere uposterte betalinger kan utlignes mot én enkelt faktura. Flere kundebetalinger må ikke lenger registreres på ett bilag.

-   **Importere bankkontoutdragstransaksjoner**

Banker betaler og mottar ofte betalinger på vegne av en organisasjon, og disse transaksjonene registreres i Finance and Operations via en fil som er mottatt fra banken. Organisasjoner vil ofte gruppere disse transaksjonene ved hjelp av nummeret på bankkontoutdraget i filen. Hver transaksjon vises detaljert på bankkontoutdraget, og derfor kreves det ingen oppsummering i den bankens underfinansjournal.

Transaksjoner kan grupperes ved hjelp av andre felt i journalen, for eksempel selve journalpartinummeret eller bilagsnummeret.

-   **Overfør saldoer**

En organisasjon må kanskje overføre en saldo fra én leverandør til en annen leverandør, enten på grunn av en feil, eller fordi en annen leverandør har overtatt hele ansvaret. Overføringer av denne typen kan også forekomme for kontotyper som kunder og bankkontoer.

Saldooverføringer fra én konto (leverandør, kunde, bankkonto og så videre) til en annen konto kan gjøres via egne bilag og forskyvningen kan posteres til en klareringsfinanskonto.

-   **Registrere startsaldoer**

Organisasjoner registrerer ofte startsaldoer for underfinansjournalkontoer (leverandører, kunder, anleggsmidler og så videre) som én bilagstransaksjon. Startsaldoer for hver konto for underfinansjournal kan angis som egne bilag, og forskyvningen kan posteres til en klareringsfinanskonto.

-   **Korrigere regnskapsposten i et bokført kunde- eller leverandørdokument**

En organisasjon må kanskje korrigere kundereskontro eller leverandøreskontro for en regnskapspost av en bokført faktura, men den fakturaen kan ikke tilbakeføres eller korrigeres via en annen mekanisme.

Hvis en korrigering må utføres i Kundereskontro eller Leverandørreskontro, må en justering gjøres direkte på finanskontoen. Justeringen kan ikke gjøres ved postering til leverandøren eller kunden. Denne fremgangsmåten krever at justeringen gjøres under "nedetid", slik at finanskontoen kan tillate manuell registrering midlertidig.

-   **"Systemet tillater det"**

Organisasjoner bruker ofte funksjonaliteten Ett bilag bare fordi systemet lar dem bruke den, uten å forstå implikasjonene.

