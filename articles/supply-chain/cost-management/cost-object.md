---
title: Kostnadsobjekter
description: Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50849a173e74ad88dd10c6a30ea66c91b936e165
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201784"
---
# <a name="cost-objects"></a>Kostnadsobjekter

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.  

## <a name="cost-objects"></a>Kostnadsobjekter

**Kostnadsobjekter**-siden viser alle kostnadsobjekter som er registrert for et produkt. Kostnadsobjektene er definert av data fra følgende kilder:

-   Produkt
-   Produktdimensjonsgruppe
-   Lagringsdimensjonsgruppe
-   Sporingsdimensjonsgruppe

**Obs!** Et kostnadsobjekt representerer bare et kostnadselement av typen **Direkte materialer**. Et kostnadsobjekt og et beholdningsobjekt er ulike ved at et kostnadsobjekt defineres av lagerdimensjonene som er valgt for økonomisk lager. En vare har for eksempel følgende konfigurasjon:

-   **Område:** Aktuell beholdning = Ja, Økonomisk lager = Ja
-   **Lager:** Aktuell beholdning = Ja, Økonomisk lager = Nei
-   **Partinr.:** Aktuell beholdning = Ja, Økonomisk lager = Nei

Tabellen nedenfor viser hva et kostnadsobjekt er, og hva et beholdningsobjekt er.

| Objekttype      | Varenummer | Område | Lager | Partinr. |
|------------------|-------------|------|-----------|-----------|
| Kostnadsobjekt      | x           | x    |           |           |
| Beholdningsobjekt | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Akkumulering av kostnader og antall
-   Verdien i **Verdi**-feltet er en sum av følgende verdier:
    -   Fysisk kostbeløp
    -   Økonomisk kostbeløp
    -   Justeringer
-   Verdien i **Antall**-feltet er en sum av følgende verdier:
    -   Mottatt
    -   Fratrukket
    -   Postert antall
-   Feltet **Gjennomsnittlig enhetskostnad** er et beregnet felt. Verdien beregnes ved å dele **Verdi**-verdien på **Antall**-verdien.

**Obs!**   Parameteren **Ta med fysisk verdi** har ingen innvirkning på de foregående beregningene.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Produktdimensjonsgruppe](https://technet.microsoft.com/library/aa499382.aspx)

[Lagringsdimensjonsgruppe](https://technet.microsoft.com/library/hh209317.aspx)

[Sporingsdimensjonsgruppe](https://technet.microsoft.com/library/hh209465.aspx)

[Hva er nytt eller endret?](../../fin-and-ops/get-started/whats-new-changed.md)

[Kostnadsoppføringer](cost-entries.md)



