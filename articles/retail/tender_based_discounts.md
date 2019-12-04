---
title: Betalingsmiddelbaserte rabatter
description: Dette emnet gir en oversikt over funksjoner som gjør det mulig for forhandlerne å konfigurere rabatter for bestemte betalingsmidler.
author: bebeale
manager: AnnBe
ms.date: 10/30/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: ed17b43ac16ebcd310716271b84bbbd904a3253a
ms.sourcegitcommit: dc31a0f0d9216aa05be76046ac7410702b20706f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692229"
---
# <a name="tender-based-discounts"></a>Betalingsmiddelbaserte rabatter

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Det er en vanlig måte blant forhandlere å gi ut private, varemerkede kredittkort. Fordelene for forhandlere er at de får foretrukne satser fra banker. Dessuten, siden disse kredittkortene kan oppmuntre kunder til å gå til butikken oftere, bidrar de til å forbedre forhandlerens resultater. Derfor har forhandlere et insentiv til å øke kundens bruk av sine varemerkekredittkort. For å oppnå dette målet gir de ofte ekstra rabatter til kunder som bruker disse kredittkortene.

Det kan også hende at forhandlere som ikke leverer varemerkekredittkort, vil oppmuntre kunder til å betale ved å bruke andre betalingsmidler, for eksempel kontanter, gavekort eller fordelspoeng. På denne måten kan de bidra til å redusere utgiftene til behandlingsgebyr for kredittkort. Derfor kan forhandlere gi rabatter til kunder som bruker disse alternative betalingsmidlene.

I Microsoft Dynamics 365 Retail kan forhandlere konfigurere en rabattprosent som brukes på kvalifiserte linjer, hvis kunden betaler ved hjelp av det foretrukne betalingsmiddelet. Kunden kan bestemme om det skal foretas for en delbetaling eller en fullstendig betaling, og Retail bestemmer det riktige rabattbeløpet. Merk at rabatten alltid er gis på avgiftsbeløpet for de kvalifiserte varene.

Betalingsmiddelbaserte rabatter konkurrerer ikke med varebaserte rabatter, for eksempel periodiske eller manuelle rabatter. De er alltid sammensatt over varerabattene. Selv om en eksklusiv tidsbestemt rabatt blir brukt på en vare, blir den betalingsbaserte rabatten fremdeles tatt i bruk på toppen av den eksklusive periodiske rabatten. Hvis en terskelrabatt skal brukes på transaksjonen, og den betalingsbaserte rabatten reduserer totalen under terskelen, blir terskelrabatten fremdeles brukt på transaksjonen.

Selv om betalingsbaserte rabatter reduserer delsummen for transaksjonen, påvirkes ikke automatiske tillegg som er brukt på transaksjonen. Hvis for eksempel leveringstilleggene er beregnet til $5 fordi delsummen var mer enn $100, og den betalingsbaserte rabatten reduserer beløpet slik at det er mindre enn $100, blir leveringskostnadene fortsatt $5 for ordren.


> [!NOTE]
> Betalingsbaserte rabatter er proporsjonalt fordelt på de kvalifiserte salgslinjene og reduserer forhåndsavgiftsbeløpet for de enkelte linjene. Hvis flere betalingsbaserte rabatter konfigureres for et betalingsmiddel (for eksempel kontant), brukes bare den beste betalingsbaserte rabatten.

Betalingsbaserte rabatter kan bare brukes på salgslinjer der prisene ikke er låst. Hvis nye salgslinjer legges til i en ordre, brukes den betalingsbaserte rabatten som er basert på de nye salgslinjene, bare under betaling. Mens en kundeordre for plukking eller forsendelse blir satt opp, brukes den betalingsbaserte rabatten bare på depositumbeløpet. Under oppfyllelse, når ordren er plassert, låses prisene i salgslinjene. Derfor blir ingen betalingsbaserte rabatter brukt for noen saldoer som betales under plukking eller autoriseres under forsendelse. Den betalingsbaserte rabatten kan bare brukes på hele beløpet til en kundeordre hvis forhandleren samler hele beløpet som et innskudd mens ordren blir plassert.

> [!IMPORTANT]
> I Retail er betalingsbaserte rabatter nå begrenset til to betalingstyper: kredittkort og kontakter.

## <a name="pos-user-experience"></a>Brukeropplevelse for salgssted

Hvis betalingsbasert rabatt er definert for kontanter, og kassereren ved salgsstedet (POS) velger en knapp som er tilordnet en Betal kontant-operasjon, brukes den betalingsbaserte rabatten automatisk på transaksjonen. Det reduserte beløpet vises deretter som saldoen. Hvis kassereren imidlertid velger **Tilbake**-knappen på betalingsskjermen, fjernes rabatten, og det opprinnelige beløpet vises på transaksjonsskjermen. Den betalingsbaserte rabatten blir fjernet hvis betalingslinjen annulleres.

Når det gjelder kortbetalinger, kan forhandlere definere betalingsbasert rabatt på én eller flere typer kredittkort. Systemet kan imidlertid ikke kontrollere typen kredittkort som brukes, hvis ikke kortet er godkjent. Hvis rabatten er brukt etter godkjenning, vil betalingsautorisasjonen være et større beløp, men betalingsregistreringen vil være for et mindre beløp.

For å unngå denne situasjonen vil kassereren se en dialogboks som viser kredittkort, som vil føre til ytterligere besparelse for kunden hvis vedkommende betaler med et kredittkort. Kassereren kan deretter spørre om kunden ønsker å bruke et av de foretrukne kortene for å få en ekstra rabatt. Hvis kassereren bruker et foretrukket kort, brukes den betalingsbaserte rabatten på transaksjonen, og det reduserte beløpet vises på betalingsskjermen. Autorisasjonen vil gjelde for det reduserte beløpet. Hvis kunden setter inn et kort som er forskjellig fra kortet som kassereren valgte, vises det en feilmelding, og autorisasjonen blir annullert.


## <a name="call-center-user-experience"></a>Brukeropplevelse for kundesenter

Når brukeren velger **Ferdig** under en telefonsenterordre, vises **Totaler**-skjermen. Først inkluderer ikke totalsummene på denne skjermen noen betalingsbasert rabatt fordi betalingsmåten ikke er valgt ennå. Hvis brukeren velger betalingsmetoden som den betalingsbaserte rabatten er konfigurert for, på **Legg til betaling**-skjermen, vil betalingsbeløpet automatisk bli justert, slik at det gjenspeiler rabattbeløpet. På lik linje med kunden på salgsstedet kan telefonsenterkunden bestemme seg for fullstendige betaling eller delbetaling. Basert på beløpet som betales, brukes den betalingsbaserte rabatten på salgsordren.

> [!NOTE]
> Kortvalidering utføres ikke for telefonsenterordrer. Hvis for eksempel brukeren av telefonsenteret velger Visa som kredittkort, men kunden bruker MasterCard, brukes rabatten likevel av systemet.

## <a name="exclude-items-from-discounts"></a>Utelate varer fra rabatter

Forhandlere velger ofte å utelate noen produkter, for eksempel nye varer eller varer med stor etterspørsel, fra rabatter. De kan imidlertid fremdeles bruke betalingsbaserte rabatter. En detaljhandler konfigurerer for eksempel Retail slik at den ikke tillater varebaserte rabatter eller manuelle rabatter. Hvis kunden betaler ved hjelp av det foretrukne betalingsmiddelet, vil Retail likevel bruke den betalingsbaserte rabatten. For å sette opp Retail på denne måten må forhandlere gå til **Behandling av produktinformasjon > Produkter > Frigitte produkter**, velge varen, og deretter, i **Retail**-hurtigfanen, sette alternativene **Hindre alle rabatter** og **Hindre betalingsbaserte rabatter** til **Nei**, og **Hindre detaljhandelsrabatter** og **Hindre manuelle rabatter** til **Ja**.

> [!NOTE]
> Når konfigurasjonen **Hindre alle rabatter** er satt til **Ja**, vil det ikke bli brukt noen rabatter på produktet. Ikke engang betalingsbaserte rabatter vil bli brukt.
