---
title: Oversikt over avgiftsberegning
description: Dette emnet forklarer det helhetlige omfanget og funksjonene i avgiftsberegning.
author: wangchen
ms.date: 11/17/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1dff1767b8e19215a2b27f87c45325e6abd1266e
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105443"
---
# <a name="tax-calculation-overview"></a>Oversikt over avgiftsberegning

[!include [banner](../includes/banner.md)]

Avgiftsberegning er en hyperskalerbar flerleiertjeneste som gjør det mulig for Global Tax Engine å automatisere og forenkle fastsettelses- og beregningsprosessen for avgifter. Avgiftsmotoren er fullt konfigurerbar. Elementene som kan konfigureres, inkluderer, men er ikke begrenset til avgiftspliktig datamodell, avgiftskode, relevansmatrise og avgiftsberegningsformel. Avgiftsmotoren kjører på Microsoft Azure-kjernetjenesteplattformen og tilbyr teknologi og eksponentiell skalerbarhet.

Avgiftsberegning er integrert med Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Til slutt vil den også integreres med Dynamics 365 Project Operations, Dynamics 365 Commerce og andre førsteparts- og tredjepartsprogrammer.

> [!IMPORTANT]
> Når du aktiverer avgiftsberegning, kan det hende at enkelte operasjoner på tilknyttede data utføres i et annet datasenter enn datasenteret som vedlikeholder tjenestedataene. Gå gjennom [Vilkår og betingelser](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) før du aktiverer avgiftsberegning. Personvernet er viktig for oss. Les [personvernerklæringen](https://go.microsoft.com/fwlink/?LinkId=521839) for å finne ut mer.

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
- Canada
- Europa
- Japan
- Storbritannia
- USA

> [!NOTE]
> Avgiftsberegning støtter ikke en tidligere versjon av Dynamics 365, for eksempel Dynamics AX 2012, eller lokale distribusjoner av Dynamics 365.

## <a name="versions"></a>Versjoner
Vi anbefaler at du importerer og konfigurerer avgiftsberegningskonfigurasjonen med versjonen som samsvarer med Finance- eller Supply Chain Management-versjonen.

| Finance- eller Supply Chain Management-versjon | Avgiftskonfigurasjonsversjon               |
| --------------- | --------------------------------------- |
| 10.0.18         | Avgiftskonfigurasjon - Europa 30.12.82     |
| 10.0.19         | Konfigurasjon 36.38.193 for avgiftsberegning |
| 10.0.20         | Konfigurasjon 40.43.208 for avgiftsberegning |
| 10.0.21         | Konfigurasjon 40.48.215 for avgiftsberegning |
| 10.0.22         | Konfigurasjon 40.48.215 for avgiftsberegning |
| 10.0.23         | Konfigurasjon 40.50.221 for avgiftsberegning |
| 10.0.24         | Konfigurasjon 40.50.225 for avgiftsberegning |
| 10.0.25         | Konfigurasjon 40.50.225 for avgiftsberegning |


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

Følgende transaksjoner støttes i versjon 10.0.21: 

- Salg

    - Salgstilbud
    - Salgsordre
    - Bekreftelse
    - Plukkliste
    - Følgeseddel
    - Salgsfaktura
    - Kreditnota
    - Returordre
    - Diverse tillegg for overskrift
    - Diverse linjetillegg

- Kjøp

    - Bestilling
    - Bekreftelse
    - Tilgangsliste
    - Produktkvittering
    - Innkjøpsfaktura
    - Diverse tillegg for overskrift
    - Diverse linjetillegg
    - Kreditnota
    - Returordre
    - Innkjøpsrekvisisjon
    - Diverse tillegg på innkjøpsrekvisisjonslinje
    - Tilbudsforespørsel
    - Diverse tillegg på tilbudsforespørselshode
    - Diverse tillegg på tilbudsforespørselslinje

- Lager

    - Overføringsordre – send
    - Overføringsordre – motta

Følgende transaksjoner støttes i versjon 10.0.23: 

- Fritekstfaktura

## <a name="supported-countriesregions"></a>Støttede land/områder

Avgiftsberegning kan aktiveres etter juridisk enhet. 

Følgende land/områder for primæradressen til en juridisk enhet støttes i versjon 10.0.21:

- Østerrike
- Belgia
- Danmark
- Estland
- Finland
- Frankrike
- Tyskland
- Ungarn
- Island
- Italia
- Latvia
- Litauen
- Nederland
- Norge
- Polen
- Sverige
- Sveits
- Storbritannia
- USA

Følgende land/områder for primæradressen til en juridisk enhet støttes i versjon 10.0.22:

- Australia
- Bahrain
- Canada
- Egypt
- Hongkong SAR
- Kuwait
- New Zealand
- Oman
- Qatar
- Saudi-Arabia
- Sør-Afrika
- De forente arabiske emirater

Følgende land/områder for primæradressen til en juridisk enhet støttes i versjon 10.0.23:

- Thailand
- Japan
- Malaysia
- Singapore

Følgende land/områder for primæradressen til en juridisk enhet støttes i versjon 10.0.24:

- Mexico

## <a name="related-resources"></a>Relaterte ressurser

[Komme i gang med avgiftstjenesten](./global-get-started-with-tax-calculation-service.md)

[Flere mva-registreringsnumre](./emea-multiple-vat-registration-numbers.md)

[Støtte for avgiftsfunksjon for overføringsordre](./tasks/tax-feature-support-for-transfer-order.md)

[Slik bygger du utvidelse i avgiftstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md)
