---
title: Betalingsmiddelbaserte rabatter
description: Denne artikkelen beskriver funksjonen for betalingsbasert rabatt som gjør det mulig for å konfigurere rabatter for bestemte betalingsmidler i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: b11145c0c12f973b437ebf87921a5686d217d327
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473828"
---
# <a name="tender-based-discount"></a>Betalingsbasert rabatt

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver funksjonen for betalingsbasert rabatt som gjør det mulig for å konfigurere rabatter for bestemte betalingsmidler i Microsoft Dynamics 365 Commerce.

Det er en vanlig måte blant forhandlere å gi ut private, varemerkede kredittkort. Fordelene for forhandlere er at de får foretrukne satser fra banker. Dessuten, siden disse kredittkortene kan oppmuntre kunder til å gå til butikken oftere, bidrar de til å forbedre forhandlerens resultater. Derfor har forhandlere et insentiv til å øke kundens bruk av sine varemerkekredittkort. For å oppnå dette målet gir de ofte ekstra rabatter til kunder som bruker disse kredittkortene.

Det kan også hende at forhandlere som ikke leverer varemerkekredittkort, vil oppmuntre kunder til å betale ved å bruke andre betalingsmidler, for eksempel kontanter, gavekort eller fordelspoeng. På denne måten kan de bidra til å redusere utgiftene til behandlingsgebyr for kredittkort. Derfor kan forhandlere gi rabatter til kunder som bruker disse alternative betalingsmidlene.

## <a name="tender-based-discount"></a>Betalingsbasert rabatt

Commerce støtter en *betalingsbasert rabatt* som gjør det mulig for forhandlerne å konfigurere en rabattprosent som skal brukes på en transaksjon hvis totalbeløpet overskrider et bestemt beløp, og kunden betaler ved hjelp av den foretrukne betalingstypen. Den betalingsbaserte rabatten er lagbasert slik at ulike rabattprosenter kan knyttes til ulike beløpsterskler. Kunden kan bestemme om det skal foretas for en delbetaling eller en fullstendig betaling, og prismotoren bestemmer det riktige rabattbeløpet. Den betalingsmiddelbaserte rabatten gis alltid på føravgiftsbeløpet for salgslinjene.

Den betalingsbaserte rabatten kan bare brukes på salgslinjer der prisene ikke er låst, og den er proporsjonalt fordelt på de kvalifiserte linjene. Hvis nye salgslinjer legges til i en ordre, brukes den betalingsbaserte rabatten som er basert på de nye salgslinjene, bare under betaling. Når en kundeordre for plukking eller levering blir satt opp, brukes den betalingsbaserte rabatten bare på depositumbeløpet. Under oppfyllelse, når ordren er plassert, låses prisene i salgslinjene. Ingen betalingsbaserte rabatter brukt for noen saldoer som betales under plukking eller autoriseres under forsendelse. Den betalingsbaserte rabatten kan bare brukes på hele beløpet til en kundeordre hvis forhandleren samler hele beløpet som et innskudd mens ordren blir plassert.

Betalingsbaserte rabatter konkurrerer ikke med varebaserte rabatter, for eksempel enkle rabatter, antallsrabatter, terskelrabatter, samlerabatter og manuelle rabatter. Betalingsbaserte rabatter blir alltid sammensatt over de varebaserte rabattene. Selv om en eksklusiv tidsbestemt rabatt blir brukt på en vare, kan den betalingsbaserte rabatten fremdeles tas i bruk på toppen av den eksklusive rabatten. Hvis en terskelrabatt skal brukes på transaksjonen, og den betalingsbaserte rabatten reduserer totalen under terskelen, blir terskelrabatten fremdeles brukt på transaksjonen.

Selv om betalingsbaserte rabatter reduserer delsummen for en transaksjon, påvirkes ikke automatiske tillegg som er brukt på transaksjonen. Hvis for eksempel leveringstilleggene er beregnet til $ 5 fordi delsummen var mer enn $ 100, og den betalingsbaserte rabatten reduserer beløpet slik at det er mindre enn $ 100, blir leveringskostnadene fortsatt $ 5 for ordren.

Den betalingsbaserte rabatten er nå begrenset til to betalingstyper: kredittkort og kontakter. Hvis flere betalingsbaserte rabatter konfigureres for et betalingsmiddel, brukes bare den beste betalingsbaserte rabatten.

## <a name="pos-user-experience"></a>Brukeropplevelse for salgssted

Hvis en betalingsbasert rabatt er definert for kontanter, og en kasserer ved salgsstedet velger **Betal kontant**-knappen for å betale med en kontant- og overføringstransaksjoner, brukes den betalingsbaserte rabatten automatisk på transaksjonen. Det reduserte beløpet vises deretter som saldoen. Hvis kassereren imidlertid velger **Tilbake**-knappen på betalingsskjermen, fjernes rabatten, og det opprinnelige beløpet vises på transaksjonsskjermen. Den betalingsbaserte rabatten blir fjernet hvis betalingslinjen annulleres.

Når det gjelder kredittkortbetalinger, kan forhandlere definere betalingsbasert rabatt på én eller flere typer kredittkort. Systemet kan imidlertid ikke kontrollere typen kredittkort som brukes, hvis ikke kortet er godkjent. Hvis rabatten er brukt etter godkjenning, vil betalingsautorisasjonen være et større beløp, men betalingsregistreringen vil være for et mindre beløp. For å unngå denne situasjonen vil kassereren se en dialogboks som viser foretrukne kredittkort, som vil føre til en ytterligere rabatt for kunden hvis vedkommende betaler med et kredittkort. Kassereren kan deretter spørre om kunden ønsker å bruke et av de foretrukne kortene for å få en ekstra rabatt. Hvis kassereren velger et foretrukket kort, brukes den betalingsbaserte rabatten på transaksjonen, og det reduserte beløpet vises på betalingsskjermen. Autorisasjonen vil gjelde for det reduserte beløpet. Hvis kunden setter inn et kort som er forskjellig fra kortet som kassereren valgte, vises det en feilmelding, og autorisasjonen blir annullert.

## <a name="call-center-user-experience"></a>Brukeropplevelse for kundesenter

Hvis en kundesenterbruker velger **Ferdig** under en telefonsenterordre, vises **Totaler**-skjermen. Først inkluderer ikke totalsummene på denne skjermen noen betalingsbasert rabatt fordi betalingsmåten ikke er valgt ennå. Hvis brukeren velger betalingsmetoden som den betalingsbaserte rabatten er konfigurert for, på **Legg til betaling**-skjermen, vil betalingsbeløpet automatisk bli justert, slik at det gjenspeiler rabattbeløpet. På lik linje med en kunde på salgsstedet kan telefonsenterkunden bestemme seg for fullstendige betaling eller delbetaling. Basert på beløpet som betales, brukes den betalingsbaserte rabatten på salgsordren.

> [!NOTE]
> Kortvalidering utføres ikke for telefonsenterordrer. Hvis for eksempel brukeren av telefonsenteret velger Visa som kredittkort, men kunden bruker MasterCard, brukes rabatten likevel av systemet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
