---
title: Tildele tid til jobber i en jobbunt
description: I produksjonsutførelse kan du bunte jobber. Deretter kan du starte flere jobber samtidig på Jobbliste-siden.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33d6bab9beb28d18e2094d7fb5e670e9425aac39
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552982"
---
# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Tildele tid til jobber i en jobbunt

[!include [banner](../includes/banner.md)]

I produksjonsutførelse kan du bunte jobber. Deretter kan du starte flere jobber samtidig på Jobbliste-siden.

Hvis du bunter jobber, må du definere hvordan den totale tiden som er registrert for alle jobbene, skal fordeles til hver jobb. Du definerer tildelingen ved å velge ett av følgende alternativer i feltet **Bunttype** på siden **Tilordningsnøkler**:

-   **Anslag** – Tiden deles mellom jobbene basert på den estimerte tiden for jobbene.
-   **Jobber** – Tiden deles i henhold til totalt antall buntede jobber og hvor mye tid som gikk med til å fullføre alle jobbene.
-   **Nettotid** – Tiden deles likt mellom jobbene som er i bunten til ethvert tidspunkt.
-   **Sanntid** – Faktisk jobbtid tilordnes. Kostnaden beregnes på grunnlag av den faktiske lønnskostnaden. **Obs!** Tildelingsnøkkelen **Sanntid** er bare tilgjengelig hvis firmaet ditt bruker funksjonen lønn i tidsregistrering.

Eksemplene nedenfor viser resultatet av de forskjellige tildelingsnøklene.

## <a name="example-scenario"></a>Eksempelscenario
Tre jobber i jobbkøen din må være fullført. Du starter den første jobben, og mens denne jobben pågår, starter du den andre og tredje jobben. Det er derfor en bunt av tre jobber. Tabellen nedenfor viser den estimerte produksjonstiden for hver jobb.

| Jobb   | Produksjonstid |
|-------|-----------------|
| Jobb 1 | 1 time          |
| Jobb 2 | 3 timer         |
| Jobb 3 | 4 timer         |
| Sum | 8 timer         |

Tabellen nedenfor viser de faktiske arbeidstimene som er brukt på hver jobb.

| Jobb    | Starttidspunkt | Sluttidspunkt | Gruppetid |
|--------|------------|----------|-------------|
| Jobb 1  | 09:00:00      | 11:00:00    | 2 timer     |
| Jobb 2  | 10:00:00      | 13:00:00    | 3 timer     |
| Jobb 3  | 10:00:00      | 15:00:00    | 5 timer     |
| Bunt | 09:00:00      | 15:00:00    | 6 timer     |

Delene nedenfor beskriver resultatet av den beregnede tiden for hver fordelingsnøkkel.

## <a name="estimation-allocation-key"></a>Estimeringstildelingsnøkkel
Følgende tabell viser formelen for beregning av tilordnet tid. Her er formelen: Tid per jobb = Total gruppetid × (Estimert jobbtid ÷ totalt estimert tid)

| Jobb   | Formel           | Tilordnet tid |
|-------|-------------------|----------------|
| Jobb 1 | 6 × (1 ÷ 8) timer | 0,75 time      |
| Jobb 2 | 6 × (3 ÷ 8) timer | 2,25 timer     |
| Jobb 3 | 6 × (4 ÷ 8) timer | 3,00 timer     |

## <a name="jobs-allocation-key"></a>Jobbtildelingsnøkkel
Følgende tabell viser formelen for beregning av tilordnet tid. Her er formelen: tid per jobb = Total bunt tid ÷ antall jobber

| Jobb   | Formel | Tilordnet tid |
|-------|---------|----------------|
| Jobb 1 | 6 ÷ 3   | 2 timer        |
| Jobb 2 | 6 ÷ 3   | 2 timer        |
| Jobb 3 | 6 ÷ 3   | 2 timer        |

## <a name="net-time-allocation-key"></a>Tildelingsnøkkel for nettotid
Følgende tabell viser formelen for beregning av tilordnet tid. Her er formelen: Beregnet tid per rapportering = bunt tid ÷ antall jobber

|                              | 09:00–10:00 (1 time) | 10:00–11:00 (1 time) | 11:00–13:00 (2 timer) | 13:00–15:00 (2 timer) | Tilordnet tid |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Antall jobber i bunten | 1                    | 3                    | 2                     | 1                     | Gjelder ikke her |
| Jobb 1                        | 1 ÷ 1 = 1 time       | 1 ÷ 3 = 0,33 time    | Gjelder ikke her        | Gjelder ikke her        | 1,33 timer     |
| Jobb 2                        | Gjelder ikke her       | 1 ÷ 3 = 0,33 time    | 2 ÷ 2 = 1 time        | Gjelder ikke her        | 1,33 timer     |
| Jobb 3                        | Gjelder ikke her       | 1 ÷ 3 = 0,33 time    | 2 ÷ 2 = 1 time        | 2 ÷ 1 = 2 timer       | 3,33 timer     |

## <a name="real-time-allocation-key"></a>Sanntidsfordelingsnøkkel
Hvis du vil at produksjonskostnadene skal beregnes basert på faktiske kostnader, må du deaktivere **Kostnadskategori** alternativet på siden **Standarder for produksjonsordre**. Følgende tabell viser formelen for beregning av tilordnet tid. Her er formelen: faktisk tid per jobb = faktisk tid i bunt

| Jobb   | Faktisk tidspunkt |
|-------|-------------|
| Jobb 1 | 2 timer     |
| Jobb 2 | 3 timer     |
| Jobb 3 | 5 timer     |

Vurder de tre jobbene som utføres av en arbeider med en timebetaling på USD 12,00. Ingen overtidsbonus eller bonuser ble opptjent i den tiden som er brukt på jobbene. Arbeideren har arbeidet på de tre buntede jobbene i totalt seks timer. Lønnskostnadene er derfor 6 x USD 12,00 = 72,00 USD. Når du bruker sanntidsfordeling, beregnes kostnaden per time på nytt med faktoren fra Nettotid-formelen. Den faktiske tiden som ble brukt på hver jobb, blir deretter overført sammen med den riktige kostprisen per time. I eksempelet er det brukt seks timer, selv om 10 timer ble tildelt. Følgende tabell viser formelen for beregning av kostnad. Her er formelen: Kostnad per time = (Total gruppetid per jobb (Nettotid) ÷ faktisk tid per jobb) × Standard kostpris per time

| Jobb   | Beregning av korrigert kostnad per time | Korrigert kostnad per time | Tilordnet tid | Total kostnad for jobb |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Jobb 1 | (1,33 ÷ 2) × USD 12,00                 | 8,00 USD                | 2 timer        | 16,00 USD         |
| Jobb 2 | (1,33 ÷ 3) × USD 12,00                 | 5,33 USD                | 3 timer        | 16,00 USD         |
| Jobb 3 | (3,33 ÷ 5) × USD 12,00                 | 8,00 USD                | 5 timer        | 40,00 USD         |

Den korrigerte kostnaden per time og jobbtiden posteres i en produksjonsjournal. **Obs!** Hvis du velger **Kostnadskategori** alternativet på **Generelt** kategorien på siden **Standarder for produksjonsordre**, overføres faktisk tid for hver jobb til en produksjonsjournal, der kostnadene brukes i kostnadskategorien for den bestemte jobben.



