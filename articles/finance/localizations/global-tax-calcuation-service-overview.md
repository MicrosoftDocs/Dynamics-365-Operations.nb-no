---
title: Oversikt over avgiftsberegning
description: Denne artikkelen forklarer det helhetlige omfanget og funksjonene i avgiftsberegning.
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: cafc4c7089e0c042fc65c1e3fd21f8f1e930b785
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689891"
---
# <a name="tax-calculation-overview"></a>Oversikt over avgiftsberegning

[!include [banner](../includes/banner.md)]

Avgiftsberegning er en hyperskalerbar flerleiertjeneste som gjør det mulig for Global Tax Engine å automatisere og forenkle fastsettelses- og beregningsprosessen for avgifter. Avgiftsmotoren er fullt konfigurerbar. Elementene som kan konfigureres, inkluderer, men er ikke begrenset til avgiftspliktig datamodell, avgiftskode, relevansmatrise og avgiftsberegningsformel. Avgiftsmotoren kjører på Microsoft Azure-kjernetjenesteplattformen og tilbyr teknologi og eksponentiell skalerbarhet.

Avgiftsberegning er integrert med Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Til slutt vil den også integreres med Dynamics 365 Project Operations, Dynamics 365 Commerce og andre førsteparts- og tredjepartsprogrammer.

> [!IMPORTANT]
> Når du aktiverer avgiftsberegning, kan det hende at enkelte operasjoner på tilknyttede data utføres i et annet datasenter enn datasenteret som vedlikeholder tjenestedataene. Gå gjennom [Vilkår og betingelser](https://go.microsoft.com/fwlink/?linkid=2156043) før du aktiverer avgiftsberegning. Personvernet er viktig for oss. Les [personvernerklæringen](https://go.microsoft.com/fwlink/?LinkId=521839) for å finne ut mer.

Avgiftsberegning er en mikroservicebasert avgiftsmotor som tilbyr eksponentiell skalerbarhet, og kan hjelpe deg med å utføre følgende oppgaver:

- Fastgjør automatisk riktig mva-gruppe, mva-gruppe for vare og avgiftskoder ved hjelp av en utvidet bestemmelsesmekanisme.
- Støtte flere avgiftsregistreringsnumre i én juridisk enhet, og fastsetter automatisk det riktige avgiftsregistreringsnummeret på avgiftspliktige transaksjoner.
- Støtte fastsettelse av skatt, beregning, postering og utligning for overføringsordrer.
- Definer formler og betingelser for avgiftsberegning som kan konfigureres for dine bestemte forretningsbehov.
- Del løsningen for fastsettelse av skatt og beregning på tvers av juridiske enheter for å spare vedlikeholdsarbeid og unngå feil.
- Støtte fastsettelse av kundens og leverandørens avgiftsregistreringsnummer.
- Støtte fastsettelse av listekode.
- Støtte avgiftsberegningsparametere på mva-jurisdiksjonsnivå.

Hvis du vil avgiftsberegning, installerer du tillegget for avgiftsberegning fra prosjektet i Microsoft Dynamics Lifecycle Services. Deretter fullfører du oppsettet i [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) og aktiverer Avgiftsberegning i Finance og Supply Chain Management. Hvis du vil ha mer informasjon, kan du se [Komme i gang med avgiftstjenesten](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Tilgjengelighet

Avgiftsberegning er vanligvis tilgjengelig i produksjonsmiljøer for alle kunder per versjon 10.0.21.

Nye funksjoner vil fortsatt bli levert. Sjekk den mest oppdaterte lanseringsplanen ofte for å finne ut om dekningen og omfanget av funksjoner som støttes.

Avgiftsberegning distribueres i følgende Azure-geografier. Flere Azure-geografier blir lagt til, basert på kundebehov.

- Asia/Stillehavskysten
- Australia
- Brasil
- Canada
- Europa
- Frankrike
- India
- Japan
- Sør-Afrika
- Sveits
- De forente arabiske emirater
- Storbritannia
- USA

> [!NOTE]
> Avgiftsberegning støtter ikke en tidligere versjon av Dynamics 365, for eksempel Dynamics AX 2012, eller lokale distribusjoner av Dynamics 365.

## <a name="versions"></a>Versjoner
Vi anbefaler at du importerer og konfigurerer avgiftsberegningskonfigurasjonen med versjonen som samsvarer med Finance- eller Supply Chain Management-versjonen.

| Finance- eller Supply Chain Management-versjon | Avgiftskonfigurasjonsversjon               |
| --------------- | --------------------------------------- |
| 10.0.31         | Konfigurasjon 40.56.240 for avgiftsberegning |
| 10.0.30         | Konfigurasjon 40.55.239 for avgiftsberegning |
| 10.0.29         | Konfigurasjon 40.55.236 for avgiftsberegning |
| 10.0.28         | Konfigurasjon 40.54.234 for avgiftsberegning |
| 10.0.27         | Konfigurasjon 40.54.234 for avgiftsberegning |


## <a name="data-flow"></a>Dataflyt

Her er en oversikt over dataflytprosessen for Avgiftsberegning. 

1. I RCS kan du vise og importere avgiftspliktige dokumentmodellkonfigurasjoner og modelltilordningskonfigurasjoner. Hvis du må utvide konfigurasjoner for et avansert scenario, kan du se [Legg til datafelt i avgiftskonfigurasjoner](tax-service-add-data-fields-tax-configurations.md).
2. I RCS oppretter eller vedlikeholder du skattefunksjoner. Du kan bruke avgiftsfunksjoner til å vedlikeholde skattesatser og regler for avgiftspliktig bruk.
3. Når oppsettet for avgiftsfunksjonen er fullført, publiserer du mva-konfigurasjonene og avgiftsfunksjonene fra RCS til det globale repositoriet.
4. I Finance velger du hvilken oppsettversjon for avgiftsfunksjonen som skal brukes for en bestemt juridisk enhet.
5. Bruk transaksjoner på vanlig måte i Finance og Supply Chain Management. Når det er nødvendig med avgiftsberegning, vil klienten samle inn informasjon fra transaksjonen, for eksempel salgsordren eller bestillingen, og pakke informasjonen som nyttelast. Deretter sendes en forespørsel om å beregne avgiften.
6. Forespørselen om avgiftsberegning mottas fra klienten og beregningen er fullført. Resultatet av avgiften returneres deretter til klienten.
7. Dynamics 365-klienten mottar avgiftsresultatet og presenterer resultatet av avgiftsberegningen på en mva-side.

## <a name="supported-transactions"></a>Transaksjoner som støttes

Avgiftsberegning kan aktiveres via transaksjoner. 

Tabellen nedenfor viser transaksjonene som støttes i den tilsvarende versjonen.

| Versjon | Transaksjoner |
|---------|--------------|
| 10.0.29 | Periodiske journaler |
| 10.0.28 | Leverandørbetalingsjournal<br> Kundebetalingsjournal | 
| 10.0.26 | Økonomijournaler<br> Leverandørfakturajournal |
| 10.0.23 | Fritekstfaktura |
| 10.0.21| Salg<br><ul><li>Salgstilbud</li><li>Salgsordre</li><li>Bekreftelse</li><li>Plukkliste</li><li>Følgeseddel</li><li>Salgsfaktura</li><li>Kreditnota</li><li>Returordre</li><li>Diverse tillegg for overskrift</li><li>Diverse linjetillegg</li></ul>Kjøp<br><ul><li>Bestilling</li><li>Bekreftelse</li><li>Tilgangsliste</li><li>Produktkvittering</li><li>Innkjøpsfaktura</li><li>Diverse tillegg for overskrift</li><li>Diverse linjetillegg</li><li>Kreditnota</li><li>Returordre</li><li>Innkjøpsrekvisisjon</li><li>Diverse tillegg på innkjøpsrekvisisjonslinje</li><li>Tilbudsforespørsel</li><li>Diverse tillegg på tilbudsforespørselshode</li><li>Diverse tillegg på tilbudsforespørselslinje</li></ul>Lager<ul><li>Overføringsordre – send</li><li>Overføringsordre – motta</li></ul>|

## <a name="supported-countriesregions"></a>Støttede land/områder

Avgiftsberegning kan kjøres med lokaliseringsfunksjoner som støttes. Følgende tabell viser landene/områdene for primæradressen til en juridisk enhet.

| Versjon | Land/område |
|---------|----------------|
| 10.0.26 | - Kina <br>- Tsjekkia<br>- Spania |
| 10.0.24 | Mexico |
| 10.0.23 | - Thailand <br>- Japan <br>- Malaysia <br>- Singapore |
| 10.0.22 | - Australia<br>- Bahrain <br>- Canada<br>- Egypt <br>- Hongkong SAR <br>- Kuwait <br>- New Zealand <br>- Oman <br>- Qatar <br>- Saudi-Arabia <br>- Sør-Afrika <br>- De forente arabiske emirater |
| 10.0.21 | - Østerrike <br>- Belgia <br>- Danmark <br>- Estland <br>- Finland <br>- Frankrike <br>- Tyskland <br>- Ungarn <br>- Island <br>- Irland <br>- Italia <br>- Latvia <br>- Litauen <br>- Nederland <br>- Norge <br>- Polen <br>- Sverige <br>- Sveits <br>- Storbritannia <br>- USA |

For land/områder som ikke er lokalisert av Microsoft, kan avgiftsberegning også aktiveres og kjøres med andre globale funksjoner.

## <a name="related-resources"></a>Relaterte ressurser

[Komme i gang med avgiftstjenesten](./global-get-started-with-tax-calculation-service.md)

[Flere mva-registreringsnumre](./emea-multiple-vat-registration-numbers.md)

[Støtte for avgiftsfunksjon for overføringsordre](./tasks/tax-feature-support-for-transfer-order.md)

[Slik bygger du utvidelse i avgiftstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md)
