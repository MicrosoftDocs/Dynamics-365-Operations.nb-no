---
title: Advarsler eller feil vises når du endrer en status for en finansperiode uten å lukke lager
description: Advarsler eller feil vises når du endrer en status for en finansperiode uten å lukke lager
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477186"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Advarsler eller feil vises når du endrer en status for en finansperiode uten å lukke lager

Microsoft innførte følgende valideringer for å forhindre problemer som skyldes feil periodeavslutningsprosess rundt etterkalkulering. Hvis du får en av følgende feilmeldinger, kan du se [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) for å få mer informasjon om hvordan du løser disse problemene.

- Du er i ferd med å utføre en omberegning med en dato %1 (10-02-2019). Den siste registrerte omberegningen ble utført i en foregående periode med en dato %2 (20-01-2019). Ingen kjøringer av en lagerlukking med en dato %3 (31-01-2019) som samsvarer med periodeslutt, er registrert. Husk å kjøre en lagerlukking per %3 (31-01-2019) som samsvarer med periodeslutt. Verdien av lagerbeholdningene, solgte varers kost og avvik blir kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført.

- Du er i ferd med å endre statusen for finansperioden %1 til %2. Ingen kjøringer av lagerlukking med en dato %3 som samsvarer med periodeslutt, er registrert. Utfør en lagerlukking per %3 som samsvarer med periodeslutt før, du endrer statusen. Verdien av lagerbeholdningene, solgte varers kost og avvik blir kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført. Rapportert fra juridisk enhet %4. For øyeblikket er den bare til informasjon, men senere blir det nødvendig å utføre en slik handling.

- Kontostrukturen %1 er endret. En eller flere hovedkontoer %2 finnes ikke lenger. Disse hovedkontoene kreves av %3 med en dato %4. Legg til disse hovedkontoene i kontostrukturen %1 før du kan gjenoppta %3-jobben. For øyeblikket er den bare til informasjon, men senere blir det nødvendig å utføre en slik handling.

- Du er i ferd med å utføre en lagerlukking med en dato %1 (31-01-2019). Ingen kjøringer av beregning av backflush-etterkalkulering med en dato %2 (31-01-2019) som samsvarer med periodeslutt, er registrert. Husk å kjøre en beregning av backflush-etterkalkulering med en dato for %3 (31-01-2019) som samsvarer med periodeslutt. Verdien av lagerbeholdningene, solgte varers kost og avvik blir kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført.

- Du er i ferd med å utføre en beregning av backflush-etterkalkulering med en dato %1 (28-02-2019). Den siste registrerte beregningen av backflush-etterkalkulering ble utført i en foregående periode med en dato %2 (31-01-2019). Ingen kjøringer av en lagerlukking med en dato %3 (31-01-2019) som samsvarer med en periodeslutt, er registrert.

Husk å kjøre en lagerlukking per %3 (31-01-2019) som samsvarer med en periodeslutt. Verdien av lagerbeholdningene, solgte varers kost og avvik er kanskje ikke riktige i underfinansjournaler eller økonomimodulen før lagerlukkingen er utført.