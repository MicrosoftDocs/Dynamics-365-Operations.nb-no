---
title: Avgiftsberegningstjeneste (forhåndsversjon)
description: Dette emnet forklarer det helhetlige omfanget og funksjonene i avgiftsberegningstjenesten.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818230"
---
# <a name="tax-calculation-service-preview"></a>Avgiftsberegningstjeneste (forhåndsversjon)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Avgiftsberegningstjenesten er en hyperskalerbar flerleiertjeneste som gjør det mulig for Global Tax Engine å automatisere og forenkle fastsettelses- og beregningsprosessen for avgifter. Avgiftsmotoren er fullt konfigurerbar. Elementene som kan konfigureres, inkluderer, men er ikke begrenset til avgiftspliktig datamodell, avgiftskode, relevansmatrise og avgiftsberegningsformel. Avgiftsmotoren kjører på Microsoft Azure-kjernetjenesteplattformen og tilbyr teknologi og eksponentiell skalerbarhet.

Tjenesten for avgiftsberegning er integrert med Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Til slutt vil den også integreres med Dynamics 365 Project Operations, Dynamics 365 Commerce og andre førsteparts- og tredjepartsprogrammer.

Tjenesten for avgiftsberegning er en Microsoft-basert avgiftsmotor som tilbyr eksponenentiell skalerbarhet. Den kan hjelpe dem med å utføre følgende oppgaver:

- Konfigurer avgiftsberegningstjenesten via RCS (Regulatory Configuration Service). RCS er en utvidet versjon av ER-designeren (elektronisk rapportering) og er tilgjengelig som en frittstående tjeneste.
- Konfigurer avgiftsmatrisen slik at avgiftskoder og -satser bestemmes automatisk.
- Konfigurer avgiftsmatrisen slik at avgiftsregistreringsnummeret bestemmes automatisk.
- Konfigurer avgiftsberegningsdesigneren for å definere formler og betingelser.
- Del løsningen for avgiftsfastsettelse og -beregning på tvers av juridiske enheter.

Hvis du vil bruke tjenesten for avgiftsberegning, installerer du tillegget for avgiftsberegningstjenesten fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS). Deretter fullfører du oppsettet i RCS og aktiverer avgiftsberegningstjenesten i Finance og Supply Chain Management. Hvis du vil ha mer informasjon, kan du se [Komme i gang med avgiftstjenesten](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Tilgjengelighet

Tjenesten for avgiftsberegning er bare tilgjengelig i sandkassemiljøer og for utvalgte kunder via et program som offentlig forhåndsversjon. Til slutt vil det bli allment tilgjengelig for alle kunder og i produksjonsmiljøer.

Nye funksjoner vil fortsatt bli levert i avgiftsberegningstjenesten. Pass derfor på at du ofte kontrollerer den mest oppdaterte dokumentasjonen for å finne ut om dekningen og omfanget av funksjoner som støttes.

Tjenesten for avgiftsberegning distribueres i følgende Azure-geografier. Det vil også bli distribuert til flere Azure-geografier, basert på kundebehov:

- USA
- Europa
- Frankrike
- Storbritannia

> [!NOTE]
> Avgiftsberegningstjenesten støtter ikke lokale distribusjoner av Dynamics 365. Den støtter heller ikke tidligere versjoner, for eksempel Dynamics AX 2012.

## <a name="feature-highlights"></a>Funksjonsfremhevinger

- En konfigurerbare avgiftsmatrise for automatisk bestemming og beregning av avgifter
- Støtte for flere mva-registreringsnumre
- Overføringsordrestøtte for fastsettelse og beregning av avgift
- Støtte for overføringsordre for fastsettelse av flere mva-registreringsnumre

## <a name="supported-transactions"></a>Transaksjoner som støttes

Avgiftsberegningstjenesten kan aktiveres ved hjelp av juridisk enhet og transaksjon. Følgende transaksjoner støttes:

- Salgsprosess

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

- Innkjøpsprosess

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

- Beholdningsprosess

    - Overføringsordre – send
    - Overføringsordre – motta

## <a name="related-resources"></a>Relaterte ressurser

[Komme i gang med avgiftstjenesten](https://go.microsoft.com/fwlink/?linkid=2138482)

[Flere mva-registreringsnumre](https://go.microsoft.com/fwlink/?linkid=2153387)

[Støtte for avgiftsfunksjon for overføringsordre](https://go.microsoft.com/fwlink/?linkid=2153388)

[Slik bygger du utvidelse i avgiftstjeneste](https://go.microsoft.com/fwlink/?linkid=2138483)
