---
title: Produksjonspostering
description: Denne artikkelen inneholder informasjon om ulike typer posteringer i produksjonsprosessen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4a400463c4b84ac8e3e5300bd710fb330458cafd
ms.lasthandoff: 03/31/2017


---

# <a name="production-posting"></a>Produksjonspostering

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om ulike typer posteringer i produksjonsprosessen.

Aktiviteter for produksjonspostering følger produksjonsprosesser som er beskrevet i delene nedenfor.

## <a name="material-consumption"></a>Materialforbruk
Materialer registreres som forbruk under produksjon når produksjonsplukklistejournalen posteres. Denne prosessen genererer avgangstransaksjoner som trekkes fra i lagerbeholdningen. I produksjonsparametrene kan du angi om verdien av råvarer som pågår (varer i arbeid \[VIA\]) skal posteres i Finans. Verdien av råvarer i arbeid (VIA) posteres deretter til en egen plukklistekonto og en dedikert plukklistemotkonto.

## <a name="time-consumption"></a>Tidsforbruk
Tiden som arbeidere bruker på produksjonsjobber registreres i rutekortjournalen eller jobbkortjournalen. Når disse journalene posteres, behandles finansposteringen til en egen konto for ressurser som er i arbeid (VIA). Denne posteringen representerer verdien av tiden som er brukt på produksjonsordren. Etter at produksjonsordren er registrert som avsluttet, utlignes via-kontoene.

## <a name="reporting-finished-goods-and-error-quantities"></a>Rapportere ferdige varer og antall feil
Når en produksjonsordre rapporteres som ferdig, oppdateres antallet av de fullførte, ferdige varene i Lagerstyring via ferdigmeldingsjournalen. Hvis du bruker VIA-regnskap, som kan defineres i produksjonsparameterne, lages det en finansjournal for å redusere VIA-kontoene og øke beholdningen av de ferdige varene. Journalen bruker standardkostnaden som er definert for produktet.

## <a name="ending-the-production-order"></a>Avslutte produksjonsordren
Før avslutning av en produksjonsordre beregnes faktiske kostnader for antallet som ble produsert. Alle estimerte kostnader i forbindelse med materialer, arbeid og administrasjonskostnader tilbakeføres og erstattes med faktiske kostnader. Hele kostnaden på ferdigvaren debiteres fra lagertilgangskontoen og krediteres til lageravgangskontoen. Hvis du merker av for **Avslutt jobb** når du kjører kostnadsberegningen, endres status for produksjonsordren til **Avsluttet**. Denne statusen hindrer at det posteres tilleggskostnader til en fullført produksjonsordre ved en feiltakelse. Du kan angi at verdien for antall feil som ferdigmeldes under rapportering skal tilordnes til de gode antallene som er rapportert som ferdige. Du kan også angi at verdien for antall feil skal posteres til en dedikert svinnkonto.

## <a name="controlling-the-level-of-ledger-posting"></a>Kontrollere nivået for finanspostering
I **Parametere for produksjonskontroll** kan du bruke feltet **Finanspostering** for å angi nivået for finanspostering for produksjonsprosesser. Følgende verdier er tilgjengelige:

-   **Vare og ressurs** – Bruk finanskontoene som er definert for varegrupper for råvarer og ferdigvarer. VIA for tidsforbruk hentes fra ressurs eller ressursgruppe fra ruteoperasjonene.
-   **Vare og kategori** – Bruk finanskontoene som er definert for varegrupper for råvarer og ferdigvarer. VIA for tidsforbruk hentes fra kostnadskategoriene som er knyttet til ruteoperasjoner.
-   **Produksjonsgrupper** – Bruk finanskontoene som er definert for produksjonsgruppene for både material- og tidsforbruk. Produksjonsgrupper er knyttet til de frigitte produktene og kopiert til produksjonsordrene ved opprettelse av disse ordrene. Postering på produksjonsordrer vil deretter følge produksjonsgrupper som er knyttet til produksjonsordren.

**Obs!** Hvis standardmetoden for beregning av kostnaden på ferdigvaren ble brukt, gjenspeiler de siste transaksjonene dette. Hvis faktiske kostnader og kostnadene som beregnes ved hjelp av standardmetoden er forskjellige, posteres differansen til kontoen som viser resultat.




