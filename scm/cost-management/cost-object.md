---
title: Kostnadsobjekter
description: "Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8043c81057b5bb79f405642b199f80fc2fbcd8d4
ms.lasthandoff: 03/31/2017


---

# <a name="cost-objects"></a>Kostnadsobjekter

Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.  

<a name="cost-objects"></a>Kostnadsobjekter
------------

**Kostnadsobjekter**-siden viser alle kostnadsobjekter som er registrert for et produkt. Kostnadsobjektene er definert av data fra følgende kilder:

-   Produkt
-   Produktdimensjonsgruppe
-   Lagringsdimensjonsgruppe
-   Sporingsdimensjonsgruppe

**Obs! ** Et kostnadsobjekt representerer bare et kostnadselement av typen **Direkte materialer**. Et kostnadsobjekt og et beholdningsobjekt er ulike ved at et kostnadsobjekt defineres av lagerdimensjonene som er valgt for økonomisk lager. En vare har for eksempel følgende konfigurasjon:

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

**Merk:** den ** ta med fysisk verdi ** parameteren har ingen innvirkning på de foregående beregningene.

<a name="see-also"></a>Se også
--------

[Product dimension group](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Storage dimension group](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Tracking dimension group](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Hva er ny eller endret i Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

[Cost entries](cost-entries.md)


