---
title: Dobbel valuta
description: Dette emnet gir informasjon om dobbel valuta, der rapporteringsvalutaen brukes som en ekstra regnskapsvaluta for Microsoft Dynamics 365 for Finance and Operations.
author: kweekley
manager: AnnBe
ms.date: 05/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: dfd4c116552510ee42cd2f3e8a0f31100826b9d2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839408"
---
# <a name="dual-currency"></a>Dobbel valuta

[!include [banner](../includes/banner.md)]

Funksjonen som ble innført i Microsoft Dynamics 365 for Finance and Operations versjon 8.1 (oktober 2018), gjør det mulig å bruke rapporteringsvalutaen på nytt som en ekstra regnskapsvaluta. Denne funksjonen kalles *dobbel valuta*. Endringene for dobbel valuta kan ikke slås av ved hjelp av en konfigurasjonsnøkkel eller parameter. Fordi rapporteringsvalutaen brukes som en sekundær regnskapsvaluta, er måten rapporteringsvalutaen beregnes på i posteringslogikken, endret.

I tillegg er forskjellige moduler forbedret for å spore, rapportere og bruke rapporteringsvalutaen i forskjellige prosesser. Modulene som er påvirket, inkluderer **økonomimodul**, **finansrapportering**, **leverandører**, **kunder**, **kontant- og bankbehandling** og **anleggsmidler**. Etter en oppgradering må du utføre bestemte trinn for kontant- og bankbehandling og anleggsmidler. Derfor må du lese de relevante delene i dette emnet nøye.

## <a name="posting-process"></a>Posteringsprosess

Posteringslogikken er endret for alle transaksjoner som genererer en regnskapsoppføring i økonomimodulen. Slik ble rapporteringsvalutaen tidligere beregnet:

Beløp i transaksjonsvaluta \> Regnskapsvalutabeløp \> Rapporteringsvalutabeløp

En transaksjon angis for eksempel i valutaen kanadiske dollar (CAD). CAD-beløpet er oversatt til regnskapsvalutaen, som er emerikanske dollar (USD). USD-beløpet oversettes deretter til rapporteringsvalutaen, som er euro (EUR). Derfor må valutakursene finnes mellom CAD og USD, og mellom USD og EUR.

Her er den nye beregningen:

Beløp i transaksjonsvaluta \> Regnskapsvalutabeløp

Beløp i transaksjonsvaluta \> Rapporteringsvalutabeløp

På grunn av denne endringen må valutakursene nå finnes mellom CAD og USD, og mellom CAD og EUR.

## <a name="reports-and-inquiries"></a>Rapporter og forespørsler

Forskjellige rapporter og forespørsler viser nå både rapporteringsvalutabeløp og regnskapsvalutabeløp. Ikke alle rapporter og forespørsler har blitt oppdatert. Rapporter som bare viser beløp i transaksjonsvalutaen, er for eksempel ikke endret.

Endringene følger ett av to mønstre:

- Hvis rapporten eller forespørselen hadde nok plass til å vise beløp i både regnskapsvalutaen og rapporteringsvalutaen, ble rapporteringvalutabeløpene lagt til.
- Hvis rapporten eller forespørselen ikke har nok plass til å vise beløp i begge valutaer, ble det lagt til et alternativ slik at brukere kan velge hvilken valuta som vises.

For ulike rapporter og forespørsler ble det også lagt til logikk for å skjule rapporteringsvalutabeløpene hvis rapporteringsvalutaen er lik regnskapsvalutaen, eller hvis rapporteringsvalutaen ikke ble definert i finans for den juridiske enheten.

## <a name="financial-journals"></a>Finansjournaler

Finansjournalene, for eksempel økonomijournalen og leverandørfakturajournalen, er oppdatert slik at de inkluderer ytterligere informasjon om rapporteringsvalutaen. Totaler for bilaget og journalen vises nå i rapporteringsvalutaen. I tillegg vises informasjon om valutakursen for rapporteringsvalutaen nå i **Generelt**-kategorien i journallinjene. Derfor kan du overstyre rapporteringsvalutaens valutakurs når du angir transaksjoner.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Leverandørfakturaer, salgsordrer og salgsavtaler
Leverandørfakturaer, salgsordrer og salgsavtaler er oppdatert med en fast valutakurs for rapporteringsvalutaen. Det kan defineres en fast valutakurs for både regnskapsvalutaen og rapporteringsvalutaen når transaksjonsvalutaen er forskjellig. Når regnskapsvalutaen og rapporteringsvalutaen er den samme, vil den faste valutakursen holdes synkronisert ved å bruke regnskapsvalutaens faste kurs som rapporteringsvalutaens faste kurs. Den faste valutakursen for rapporteringsvaluta kan ikke endres for denne konfigurasjonen. Når regnskapsvalutaen og rapporteringsvalutaen er forskjellig, kan den faste valutakursen defineres for både regnskapsvalutaen og rapporteringsvalutaen under transaksjonsregistreringen. Hvis rapporteringsvalutaen ikke er definert i finans, blir ikke feltet **Fast valutakurs for rapporteringsvaluta** aktivert, og ingen rapporteringsvalutabeløp blir beregnet.

## <a name="module-changes"></a>Modulendringer

Følgende moduler bruker rapporteringsvalutaen som en sekundær regnskapsvaluta:

- [Økonomimodul](#general-ledger)
- [Finansrapportering](#financial-reporting)
- [Leverandører](#accounts-payable-and-accounts-receivable)
- [Kunder](#accounts-payable-and-accounts-receivable)
- [Kontant- og bankbehandling](#cash-and-bank-management)
- [Anleggsmidler](#fixed-assets)

### <a name="general-ledger"></a>Økonomimodul

Hvis en rapporteringsvaluta er definert i Finans, har økonomimodulen allerede sporet rapporteringsvalutabeløp for hver regnskapspost. Disse beløpene oversettes nå fra transaksjonsvalutabeløpene.

Følgende ytterligere endringer ble gjort i **økonomimodulen**:

- Du kan definere en separat valutakurstype for rapporteringsvalutaen i Finans. Hvis en organisasjon ikke vil bruke en annen valutakurstype, kan du la feltet for valutakurstype for rapporteringsvalutaen stå tomt. Du kan også velge den samme valutakurstypen som brukes for regnskapsvalutaen. Hvis du lar feltet stå tomt, bruker systemet valutakurstypen for regnskapsvalutaen.
- En ny journal, Justeringsjournal for rapporteringsvaluta, gjør det mulig bare å postere justeringer til finanskontoer i rapporteringsvalutaen. Denne journalen gjør det mulig bare å postere til finanskontoer. Det støtter ikke konsernintern, og valutaen må være rapporteringsvalutaen for den juridiske enheten der journalen posteres. Når journalen posteres, er transaksjonsvalutaen og transaksjonsvalutabeløpene 0 (null), og rapporteringsvalutabeløpet posteres med beløpet som er angitt for transaksjonen. Fordi måten rapporteringsvalutaen brukes på i modulene **leverandører**, **kunder** og **anleggsmidler**, er endret, kan denne journalen brukes for justeringer etter en oppgradering. Se delene for disse modulene for eksempler som viser hvordan denne journalen kan brukes.
- Prosessen for periodetilordning er oppdatert slik at den tilordner beløpene i transaksjons-, regnskaps- og rapporteringsvalutaer. Tidligere ble beløp tildelt i transaksjons- og regnskapvalutaer, og deretter ble regnskapsvalutabeløpet oversatt til rapporteringsvalutaen. Denne virkemåten kan føre til at en saldo beholdes på finanskontoen i rapporteringsvalutaen. Når beløp nå beregnes og brukes i regnskapsposten, skjer det ingen oversettelse.
- Prosessen for revaluering av utenlandsk valuta har allerede revaluert beløp i rapporteringsvaluta. Rapporteringsvalutabeløpet beregnes nå via transaksjonsvalutabeløpet, som beskrevet i [Posteringsprosess](#posting-process)-delen tidligere i dette emnet.
- Mange rapporter og forespørsler i økonomimodulen hadde allerede rapporteringsvalutaen, men noen få hadde det ikke. Ett eksempel er **Råbalanse**-listesiden. Denne listesiden inneholder nå kolonner for både regnskapsvalutaen og rapporteringsvalutaen. Legg merke til at kolonnene for rapporteringsvalutaen skjules hvis regnskapsvalutaen og rapporteringsvalutaen er det samme, eller hvis ingen rapporteringsvaluta ble definert i Finans.

### <a name="financial-reporting"></a>Finansrapportering

En forbedring av **Finansrapportering**-modulen gjør at du kan inkludere rapporteringsvalutabeløp i et regnskapsoppgjør på to måter. I kolonnedefinisjonen kan du rapportere direkte på rapporteringsvalutabeløpene som er postert til finans (ny funksjonalitet). Eventuelt kan du fortsette å oversette beløpene fra regnskapsvalutaen til rapporteringsvalutaen (eksisterende funksjonalitet).

Denne endringen er tilgjengelig gjennom **Valutavisning**-innstillingen i kolonnedefinisjonen. Hvis du velger **Rapporteringsvaluta fra Finans**, oversettes ikke beløpene i kolonnen. I stedet rapporteres de direkte fra økonomimodulen. Hvis du vil at kolonnen skal vise oversatte beløp, velger du **Oversett til XXXX**-alternativet, der *XXXX* er rapporteringsvalutaen som skal vises i kolonnen. I så fall oversettes regnskapsvalutabeløpene til den valgte valutaen ved å bruke den eksisterende oversettelsesfunksjonen.

### <a name="accounts-payable-and-accounts-receivable"></a>Leverandører og kunder

Modulene **leverandører** og **kunder** har allerede sporet rapporteringsvalutabeløp. Beløpene ble imidlertid ikke vist eller brukt for forskjellige prosesser. Følgende endringer ble gjort:

- Rapporteringsvalutabeløp vises nå på transaksjoner for både kunder og leverandører. Rapporteringsvalutabeløp vises også for den åpne saldoen for hver transaksjon.
- Aldersfordelingsprosessen er oppdatert slik at en organisasjon kan vise aldersfordelingsperiodene i regnskapsvalutaen eller rapporteringsvalutaen.
- Forskjellige forespørsler og rapporter ble oppdatert slik at de viser rapporteringsvalutabeløp. Eksempler omfatter rapportene **Kunde-/kontoavstemming** og **Leverandør-/kontoavstemming**.
- Prosessen for revaluering av utenlandsk valuta har allerede revaluert beløp i rapporteringsvaluta. Rapporteringsvalutabeløpet beregnes nå via transaksjonsvalutabeløpet, som beskrevet i [Posteringsprosess](#posting-process)-delen.
- **Hensyn ved oppgradering:** Før en oppgradering beregnes rapporteringsvalutabeløpene for dokumenter (fakturaer, betalinger og så videre) via regnskapsvalutaen. En faktura posteres for eksempel før en organisasjon oppgraderer, og fakturaen ikke er betalt. Under oppgraderingen endres ikke fakturaens regnskapsoppføring. Etter oppgraderingen er imidlertid endringene for dobbel valuta aktivert. Når en betaling gjøres for fakturaen, beregnes derfor nå betalingens rapporteringsvalutabeløp gjennom transaksjonsvalutabeløpet. Når betalingen og fakturaen utlignes, kan en liten forskjell beregnes i realisert fortjeneste/tap, fordi rapporteringsvalutabeløp nå beregnes på en annen måte. Hvis differansen som er beregnet, regnes som betydelig, kan den nye justeringsjournalen for rapporteringsvaluta brukes til bare å justere saldoen for realisert gevinst/tap og finanskontoene leverandører/kunder kundesamlekonto i rapporteringsvalutaen.

### <a name="cash-and-bank-management"></a>Kontant- og bankbehandling

Tidligere sporet ikke **Kontant- og bankbehandling**-modulen noen rapporteringsvalutabeløp for transaksjoner som ble postert mot hver bankkonto. Etter en oppgradering spores automatisk rapporteringsvalutabeløp for alle nye transaksjoner som er postert. Rapporteringsvalutabeløp må imidlertid legges til tidligere posterte transaksjoner i underfinansjournalen.

- **Hensyn ved oppgradering:** Fordi bankkontotransaksjoner ikke har sporet rapporteringsvalutabeløp i underfinansjournal tidligere, er en veiviser lagt til slik at du kan legge til rapporteringsvalutabeløp i bankkontotransaksjoner. Denne veiviseren posterer **ikke** til økonomimodulen på nytt. I stedet tar den rapporteringsvalutabeløpene fra økonomimodulen og oppdaterer dem i underfinanstabellene.

    - For å starte veiviseren velger du **Kontant- og bankbehandling** \>**Oppsett** \> **Legg til rapporteringsvalutabeløp i bankkontotransaksjoner**.
    - Veiviseren viser transaksjoner for alle bankkontoer i det gjeldende firmaet som har et rapporteringsvalutabeløp på 0 (null). Bare transaksjoner som ble postert før oppgraderingen, inkluderes.
    - Veiviseren finner tilsvarende regnskapsoppføringer i økonomimodulen for hver bankkontotransaksjon og angir et standard reportingsvalutabeløp. Selv om beløpene kan redigeres, anbefaler vi at du **ikke** redigerer dem. Hvis ikke kan du kanskje ikke avstemme bankkontosaldoene til økonomimodulen. Den eneste gangen du bør redigere et beløp, er hvis rapporteringsvalutabeløpet ikke blir funnet i økonomimodulen. I så fall viser veiviseren et beløp på 0 (null) for rapporteringsvalutaen.
    - Hvis du velger **Avbryt** i veiviseren, lagres bankkontotransaksjonene og eventuelle endringer i rapporteringsvalutabeløpene til neste gang du kjører veiviseren. Rapporteringsvalutabeløpene oppdateres imidlertid ikke i bankkontotransaksjonene. Den oppdateringen skjer bare når du velger **Fullfør** i veiviseren. Du kan kjøre veiviseren flere ganger. Du kan derfor rette eventuelle feil rapporteringsvalutabeløp hvis du gjør en feil.

- Ingen prosesser i Kontant- og bankbehandling ble endret, men forskjellige rapporter og forespørsler ble oppdatert slik at de viser rapporteringsvalutabeløp. Kontantstrømmens prognoserapporter er et unntak. De ble ikke oppdatert for å inkludere rapporteringsvalutabeløpene.

### <a name="fixed-assets"></a>Anleggsmidler

Tidligere sporet ikke **Anleggsmidler**-modulen noen rapporteringsvalutabeløp for transaksjoner som ble postert mot hvert anleggsmiddeltablå. Etter en oppgradering spores automatisk rapporteringsvalutabeløp for alle nye transaksjoner som er postert. Rapporteringsvalutabeløp må imidlertid legges til tidligere posterte transaksjoner i underfinansjournalen.

I tillegg er store endringer gjort i avskrivningsprosessen. Disse endringene krever brukerhandling etter en oppgradering. Det er viktig at du leser og forstår følgende endringer, selv om du ennå ikke bruker anleggsmidler.

- Måten avskrivningsprosessen bestemmer rapporteringsvalutabeløpet på, er endret. Følgende scenario sammenligner hvordan avskrivning tidligere bestemte rapporteringsvalutabeløpet og hvordan den bestemmer rapporteringsvalutabeløpet nå.

    **Scenario for avskrivning**

    Et anleggsmiddel anskaffes og posteres med følgende beløp. Legg merke til at rapporteringsvalutabeløpet posteres i Finans, men det lagres ikke i underfinanstabellene for anleggsmidler.

    | transaksjonstype | Transaksjonsbeløp | Valutakurs | Regnskapsvalutabeløp | Valutakurs | Rapporteringsvalutabeløp |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Anskaffelse      | 1 000 000 DKK      | 2,0           | 500 000 USD                | 2,5           | 200 000 EUR               |

    **Tidligere avskrivning for rapporteringsvalutaen**

    Avskrivningsforslaget kjøres på slutten av året og beregner disse tallene.

    | transaksjonstype | Transaksjonsbeløp | Valutakurs | Regnskapsvalutabeløp | Valutakurs | Rapporteringsvalutabeløp |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Avskrivning     | 50 000 USD         | 1.0           | 50 000 USD                 | 2.6           | 19 230,77 EUR             |

    Når avskrivningsforslaget kjøres, beregner det regnskapsvalutabeløpet ved hjelp av avskrivningsmetoden. Deretter oversettes beløpet i rapporteringsvalutaen ved hjelp av den gjeldende valutakursen mellom USD og EUR. Denne oversettelsen forårsaker problemer, ettersom anleggsmidlet ikke kan avskrives helt i rapporteringsvalutaen når spotkurs brukes.

    **Ny avskrivning for rapporteringsvalutaen**

    Avskrivningsprosessen er endret slik at rapporteringsvalutabeløpet også beregnes ved hjelp av avskrivningsmetoden. Her er resultatet når avskrivning kjøres på et anleggsmiddel.

    | transaksjonstype | Transaksjonsbeløp | Valutakurs | Regnskapsvalutabeløp | Valutakurs                                                       | Rapporteringsvalutabeløp |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Avskrivning     | 50 000 USD         | 1.0           | 50 000 USD                 | 2,5<blockquote>[!NOTE] Selv om valutakursen vises, brukes den ikke til å oversette til rapporteringsvalutaen.</blockquote> | 20 000 EUR                |

    Når avskrivningsforslaget kjøres, beregnes både regnskapsvalutabeløpet og rapporteringsvalutabeløpet ved hjelp av avskrivningsmetoden. Beløpene brukes deretter i regnskapsposten i økonomimodulen. Ingen oversettelse gjøres for å bestemme rapporteringsvalutabeløpet.

- **Hensyn ved oppgradering:** Fordi tablåtransaksjoner for anleggsmiddel ikke sporet rapporteringsvalutaen tidligere, er en veiviser lagt til slik at du kan legge til rapporteringsvalutabeløp i tablåtransaksjoner for anleggsmiddel. Denne veiviseren posterer **ikke** til økonomimodulen på nytt. Fordi måten avskrivningsforslaget beregner rapporteringsvalutabeløp på, er endret, **må** veiviseren kjøres og fullføres for hvert selskap før en organisasjon kan angi avskrivningstransaksjoner.

    - Starte veiviseren ved å velge **Anleggsmidler** \> **Oppsett** \> **Legg til rapporteringsvalutabeløp i anleggsmiddeltablåer**.
    - Veiviseren viser transaksjoner for alle anleggsmiddeltablåer i det gjeldende firmaet som har et rapporteringsvalutabeløp på 0 (null). Bare transaksjoner som ble postert før oppgraderingen, inkluderes.
    - Veiviseren henter **ikke** rapporteringsvalutabeløpene fra økonomimodulen. Som beskrevet i det forrige eksemplet, brukte rapporteringsvalutabeløpene som opprinnelig ble postert til økonomimodulen, feil spotkurs. Disse beløpene skal ikke vises i underfinansjournal av anleggsmiddel, fordi den neste avskrivningsberegningen bruker feil beløp. I stedet søker veiviseren etter valutakursen på datoen for den første anskaffelsen. Denne valutakursen brukes deretter til å anbefale rapporteringsvalutabeløpet som skal posteres i underfinansjournalen. Her er hva veiviseren kan vise for det forrige scenariet.

        | Anleggsmiddel | Bestill      | transaksjonstype | Transaksjonsdato | Valuta. | Beløp i transaksjonsvaluta | Beløp  | Valutakurs | Rapporteringsvalutabeløp |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Anskaffelse      | 3/6/2016         | DKK      | 1 000 000                      | 500 000 | 2,5       | 250 000                   |
        | BUIL-00001  | 200\_SLLT | Avskrivning     | 3/6/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250 000                   |
        | BUIL-00001  | 200\_SLLT | Avskrivning     | 3/6/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250 000                   |
        | BUIL-00001  | 200\_SLLT | Avskrivning     | 3/6/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250 000                   |

    - Mange kunder sporet detaljene for anleggsmiddeltransaksjon i arbeidsbøker. Disse opplysningene omfatter valutakurser og beløp. Hvis du har disse dataene i en arbeidsbok, kan du opprette en egendefinert valutakurs og oppdatere den med valutakursene fra arbeidsboken. Denne valutakurstypen brukes deretter til å angi en standard valutakurs på anskaffelsesdatoen og beregne rapporteringsvalutabeløpet. Hvis en valutakurstype ikke er valgt, bruker veiviseren valutakurstypen som er definert i Finans.
    - Valutakursen og rapporteringsvalutabeløpene kan endres. Hvis valutakursen endres, beregnes rapporteringsvalutabeløpet på nytt ved hjelp av den nye kursen.
    - Hvis du velger **Avbryt** i veiviseren, lagres tablåtransaksjoner for anleggsmiddel og eventuelle endringer i valutakursen eller rapporteringsvalutabeløpene til neste gang du kjører veiviseren. Rapporteringsvalutabeløpene oppdateres imidlertid ikke i tablåtransaksjonene for anleggsmiddel. Den oppdateringen skjer bare når du velger **Fullfør** i veiviseren. Du kan kjøre veiviseren flere ganger. Du kan derfor rette eventuelle feil rapporteringsvalutabeløp hvis du gjør en feil.
    - Når rapporteringsvalutabeløpene er helt oppdatert i underfinansjournalen, **må** du angi **Har du oppdatert alle beløp i rapporteringsvaluta på tablåtransaksjonene for anleggsmidler?** til **Ja** og deretter velge **Fullfør**. Avskrivningsberegninger kan ikke fullføres før du angir **Har du oppdatert alle beløp i rapporteringsvaluta på tablåtransaksjonene for anleggsmidler?** til **Ja**. Når dette alternativet er satt til **Ja**, er ikke veiviseren lenger tilgjengelig.
    - Når anleggsmiddeltransaksjonene i underfinansjournal er oppdatert med rapporteringsvalutabeløp, stemmer ikke disse beløpene overens med beløpene som opprinnelig ble postert til økonomimodulen. Justeringsjournaler for rapporteringsvaluta kan imidlertid brukes til å oppdatere saldoene for avskrivningsfinanskontoene i Finans, slik at de samsvarer med beløpene som opprinnelig ble postert.
    - En ny enhet kalt **Rapporteringsvalutabeløp for anleggsmiddeltransaksjon** som er lagt til i arbeidsområdet **Databehandling**, gjør det mulig å eksportere dataene fra veiviseren. Du kan deretter bruke dataene til å bestemme saldoen i underfinansjournalen for anleggsmiddel for avskrivningstransaksjonene. Denne saldoen kan deretter brukes til å bestemme beløpet i justeringsjournalen for rapporteringsvaluta i økonomimodulen.

- **Hensyn ved oppgradering:** Nye oppsettfelt er lagt til i anleggsmidler, og brukes i avskrivningsberegningen. Du må kanskje oppdatere disse feltene før neste avskrivningsberegning.

    - På anleggsmiddeltablået (**Anleggsmidler** \> **Tablåer**) har **Generelt**-hurtigfanen et nytt felt kalt **Anskaffelsespris i rapporteringsvaluta**.
    - På anleggsmiddeltablået (**Anleggsmidler** \> **Tablåer**) har **Avskrivning**-hurtigfanen et nytt felt kalt **Forventet svinnverdi i rapporteringsvaluta**.
    - I parametere for anleggsmidler (**Anleggsmidler** \> **Oppsett** \> **Parametere for anleggsmidler**) har **Generelt**-hurtigfanen et nytt felt kalt **Minste avskrivningsbeløp i rapporteringsvaluta**.
    - I tablåer (**Anleggsmidler** \> **Oppsett** \> **Tablåer**) har **Generelt**-hurtigfanen to nye felt: **Avrund avskrivning i rapporteringsvaluta** og **Bruk netto bokført verdi i rapporteringsvaluta**.

- Fordi avskrivningsforslaget nå beregner beløp i både regnskapsvalutaen og rapporteringsvalutaen, er anleggsmiddeljournalen oppdatert slik at den viser avskrivningsbeløpene i rapporteringsvalutaen. For avskrivningstransaksjoner er transaksjonsvalutaen alltid regnskapsvalutaen. Disse beløpene vil derfor fortsatt vises i **Debet**- og **Kredit**-kolonner. To nye kolonner, **Debet i rapporteringsvaluta** og **Kredit i rapporteringsvaluta**, er lagt til i rutenettet.

    - De nye feltene er bare tilgjengelig når transaksjonstypen er en av de fire typene avskrivning: **Avskrivning**, **Avskrivningsjustering**, **Ekstraordinær avskrivning** eller **Særskilt avskrivningsfradrag**.
    - Hvis en type avskrivningstransaksjon angis i anleggsmiddeljournalen, vises rapporteringvalutabeløpene i de nye kolonnene. Disse beløpene kan endres.
    - Hvis regnskapsvalutaen og rapporteringsvalutaene i finans er identiske, vil beløpene holdes synkroniserte. Hvis du endrer **kredit**-beløpet, endres **Kredit i rapporteringsvaluta**-beløpet automatisk slik at det samsvarer.
    - Hvis en annen transaksjonstype angis i anleggsmiddeljournalen, vises aldri beløpene **Debet i rapporteringsvaluta** og **Kredit i rapporteringsvaluta**, verken før eller etter postering. Regnskapsvaluta- og rapporteringsvalutabeløpene er fremdeles tilgjengelige på bilaget som posteres til økonomimodulen.
