---
title: Kostnadsobjekter
description: Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93220208384ccb1a3cc8ff43d83577293e1f029e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672465"
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

## <a name="additional-resources"></a>Tilleggsressurser

[Produktdimensjonsgruppe](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[Lagringsdimensjonsgruppe](/dynamicsax-2012//storage-dimension-groups-form)

[Sporingsdimensjonsgruppe](/dynamicsax-2012//tracking-dimension-groups-form)

[Hva er nytt eller endret?](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[Kostnadsoppføringer](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]