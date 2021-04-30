---
title: Avgiftsberegning (forhåndsversjon)
description: Dette emnet forklarer det helhetlige omfanget og funksjonene i avgiftsberegning.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892355"
---
# <a name="tax-calculation-preview"></a>Avgiftsberegning (forhåndsversjon)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Avgiftsberegning er en hyperskalerbar flerleiertjeneste som gjør det mulig for Global Tax Engine å automatisere og forenkle fastsettelses- og beregningsprosessen for avgifter. Avgiftsmotoren er fullt konfigurerbar. Elementene som kan konfigureres, inkluderer, men er ikke begrenset til avgiftspliktig datamodell, avgiftskode, relevansmatrise og avgiftsberegningsformel. Avgiftsmotoren kjører på Microsoft Azure-kjernetjenesteplattformen og tilbyr teknologi og eksponentiell skalerbarhet.

Avgiftsberegning er integrert med Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Til slutt vil den også integreres med Dynamics 365 Project Operations, Dynamics 365 Commerce og andre førsteparts- og tredjepartsprogrammer.

Avgiftsberegning er en Microsoft-basert avgiftsmotor på mikrotjenestenivå som tilbyr eksponenentiell skalerbarhet. Den kan hjelpe dem med å utføre følgende oppgaver:

- Konfigurer avgiftsberegning via RCS (Regulatory Configuration Service). RCS er en utvidet versjon av ER-designeren (elektronisk rapportering) og er tilgjengelig som en frittstående tjeneste.
- Konfigurer avgiftsmatrisen slik at avgiftskoder og -satser bestemmes automatisk.
- Konfigurer avgiftsmatrisen slik at avgiftsregistreringsnummeret bestemmes automatisk.
- Konfigurer avgiftsberegningsdesigneren for å definere formler og betingelser.
- Del løsningen for avgiftsfastsettelse og -beregning på tvers av juridiske enheter.

Hvis du vil bruke tjenesten for avgiftsberegning, installerer du tillegget for avgiftsberegningstjenesten fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS). Deretter fullfører du oppsettet i RCS og aktiverer avgiftsberegningstjenesten i Finance og Supply Chain Management. Hvis du vil ha mer informasjon, kan du se [Komme i gang med avgiftstjenesten](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Tilgjengelighet

Avgiftsberegning er bare tilgjengelig i sandkassemiljøer og for utvalgte kunder via et program som offentlig forhåndsversjon. Til slutt vil det bli allment tilgjengelig for alle kunder og i produksjonsmiljøer.

Nye funksjoner vil bli levert fortløpende, så pass derfor på at du ofte kontrollerer den mest oppdaterte dokumentasjonen for å finne ut om dekningen og omfanget av funksjoner som støttes.

Avgiftsberegning distribueres i følgende Azure-geografier. Det vil også bli distribuert til flere Azure-geografier, basert på kundebehov:

- USA
- Europa

> [!NOTE]
> Avgiftsberegning støtter ikke lokale distribusjoner av Dynamics 365. Den støtter heller ikke tidligere versjoner, for eksempel Dynamics AX 2012.

## <a name="feature-highlights"></a>Funksjonsfremhevinger

- En konfigurerbare avgiftsmatrise for automatisk bestemming og beregning av avgifter
- Støtte for flere mva-registreringsnumre
- Overføringsordrestøtte for fastsettelse og beregning av avgift
- Støtte for overføringsordre for fastsettelse av flere mva-registreringsnumre

## <a name="supported-transactions"></a>Transaksjoner som støttes

Avgiftsberegning kan aktiveres ved hjelp av juridisk enhet og transaksjon. Følgende transaksjoner støttes:

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

[Komme i gang med avgiftstjenesten](./global-get-started-with-tax-calculation-service.md)

[Flere mva-registreringsnumre](./emea-multiple-vat-registration-numbers.md)

[Støtte for avgiftsfunksjon for overføringsordre](./tasks/tax-feature-support-for-transfer-order.md)

[Slik bygger du utvidelse i avgiftstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md)