---
title: Reservere lagerantall
description: Dette emnet beskriver de forskjellige alternativene som er tilgjengelige for reservering av lager.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 942a1e9ddcf6e0952da66b239e1884cb83369175
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="reserve-inventory-quantities"></a>Reservere lagerantall

[!include[banner](../includes/banner.md)]


Dette emnet beskriver de forskjellige alternativene som er tilgjengelige for reservering av lager.

Du kan reservere lagerantall automatisk for en bestemt salgsordre. Dette betyr at reservert lager ikke kan trekkes tilbake fra lageret for andre ordrer hvis ikke lagerreserveringen, eller deler av lagerreserveringen, avbrytes.

Det er flere årsaker til reservering av lager:
-   Først bestilt, først levert, som betyr at kunder mottar tilgjengelige varer i den samme rekkefølgen som de legger inn ordrene.
-   Mangel på varer på grunn av lang eller ukjent leveringstid fra leverandøren. Det kan hende at du vil sikre at bestemte kunder eller ordrer får levering av de første varene som er tilgjengelige.
-   Bestemte kunder eller bestemte typer ordrer har førsteprioritet ved levering.
-   Varer med serie- eller partinumre. Du kan merke bestemte varer som er eller vil bli levert til bestemte ordrer.
-   Spesialbestilte varer som reserveres for bestemte ordrer.
-   Produksjonsordrer. Du kan for eksempel merke varer som produseres for og justeres til bestemte ordrer.

Lager kan reserveres automatisk når det opprettes en ny ordrelinje, eller du kan reservere lager manuelt for enkeltordrene. Det er også mulig å reservere lager på forskjellige stadier i produksjonsprosessen. Bare lagerførte produkter kan reserveres. Tjenester kan ikke reserveres, fordi det ikke finnes noen lagerbeholdning. Både fysisk lagerbeholdning og bestilt, men ikke mottatt, lager kan reserveres. Hvis det er reservert et større antall en lagerbeholdningen inneholder, vises det en melding som sier at du ikke kan reservere et slikt stort antall. Du kan deretter velge å reservere antallet likevel eller endre det bestilte antallet. Antallet kan enten reserveres eller endres. Hvis det er reservert flere varer enn det som er tilgjengelig, dekkes mangelen neste gang det er tilgengelige varer for levering.

## <a name="inventory-reservation-policies"></a>Policyer for lagerreservasjon
Policyer for lagerreservasjon settes på sidene **Varemodellgrupper**, **Parametere for beholdnings- og lagerstyring** og **Produksjonsparametere**.
### <a name="policies-on-the-item-model-groups-page"></a>Policyer på siden Varemodellgrupper

Delen **Beholdningspolicyer** inneholder policyene for lagerreservasjon som vises nedenfor.
|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Policy for reservasjon**  | **Beskrivelse**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| FIFO-datokontrollert    | Hvis du velger alternativet **FIFO-datokontrollert** kontrolleres lagerreservasjonen av en sorteringsdato i henhold til FIFO-prinsippet. Partier reserveres, basert på den tidligste datoen for mottak av varer, i henhold til prinsippet først-inn-først-ut (FIFO).                                                                                                                                                                                                                                                                       |
| Bakover fra forsendelsesdato | Dette alternativet er bare tilgjengelig hvis du har valgt alternativet **FIFO-datokontrollert**. Hvis du velger **Bakover fra forsendelsesdato**, reserveres lageret bakover fra den ønskede forsendelsesdatoen i henhold til prinsippet om sist-inn-først-ut (LIFO). Hvis ingen mottak er tilgjengelige før forsendelsesdatoen, brukes FIFO-reservering.                                                                                                                                                                                                           |
| Varesalgreservasjon  | Bestemmer om varereservasjon er manuell eller automatisk. Hvis en reservasjon er automatisk, reserveres lageret når ordrelinjer opprettes. Det er mulig å reservere på varenummernivå for stykklister (alternativet **Automatisk**), eller for enkeltvarene i en stykkliste (alternativet **Nedbryting**). Standardverdien for **Varesalgreservasjon** kan arves fra **Kundeparametere**. På denne siden settes verdien i Reservering-feltet i **delen** **Salg - standardverdier** i kategorien **Generelt**. |
| Samme partivalg    | Samme partireservasjon gjør at du kan reservere beholdning for en salgsordrelinje mot ett lagerparti. Hvis du vil bruke dette alternativet, må du også sette alternativet **Konsolider krav** til **Ja**. Det finnes flere innstillinger som kreves for sporingsdimensjonsgruppen og lagringsdimensjonsgruppen. Hvis du vil ha mer informasjon, kan du se [Reservere samme parti for en salgsordre](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Konsolider krav | Dette alternativet ligner på alternativet **Samme partivalg**, og det konsoliderer lageret som er reservert for salgsordrelinjer til ett krav.                                                                                                                                                                                                                                                                                                                                                                                      |
| FEFO-datokontrollert    | Dette alternativet gjør det mulig å reservere partier som er nær sin utløpsdato eller best før-dato. Du må også sette **Plukkekriterier**-feltet for å velge en **utløpsdato** eller **best før-dato**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Eksempel på FIFO-datokontrollert og Bakover fra forsendelsesdato

I dette eksemplet finnes lagerbeholdning for varenummer A for tre ulike partinumre.
| Varenummer | Partinummer | Antall | Dato             |
|-------------|--------------|----------|------------------|
| A           | 1000         | 5        | 2. februar 2016 |
| A           | 1001         | 3        | 1. januar 2016  |
| A           | 1 002         | 7        | 3. mars 2016    |

En salgsordre som skal reserveres automatisk og leveres 4. april 2016, reserveres følgende parti:
-   Hvis merket er fjernet for **FIFO-datokontrollert** og **Bakover fra forsendelsesdato**, reserveres parti 1000 fordi dette er partiet med det laveste nummeret.
-   Hvis det er merket av for **FIFO-datokontrollert** og det ikke er merket av for **Bakover fra forsendelsesdato**, reserveres parti 1001 fordi dette er partiet med den første mottaksdatoen (FIFO).
-   Hvis merket er fjernet for **FIFO-datokontrollert** og **Bakover fra forsendelsesdato**, reserveres parti 1002 fordi dette er partimottaket nærmest forsendelsesdatoen for salgsordren.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Policyer på siden Parametere for beholdnings- og lagerstyring

Det finnes to alternativer relatert til reservasjoner for siden **Parametere for beholdnings- og lagerstyring**:
-   Alternativet **Reserver bestilte varer** i kategorien **Generelt** lar deg reservere varemottak som er bestilt mot vareavganger i Kunder, Prosjektstyring og regnskap og Produksjonskontroll. Hvis du ikke velger dette alternativet, kan du bare reservere varer som er fysisk mottatt. Hvis en bestemt vare er definert til å godta negativ beholdning, er ikke dette feltet relevant.
-   Alternativet **Reserver varer automatisk** i kategorien **Transport** fastsetter standardinnstillingen hvis varene reserveres automatisk for overføringsordrer. Standardinnstillingen kan overstyres på individuelle overføringsordrer.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Policyer for lagerreservasjon på siden Produksjonsparametere

Verdien for **Reservering**-feltet i kategorien **Generelt** på siden **Produksjonsparametere** bestemmer standardpunktet i produksjonsprosessen der lageret skal reserveres. Lageret kan for eksempel reserveres når arbeid planlegges eller når arbeid startes.




