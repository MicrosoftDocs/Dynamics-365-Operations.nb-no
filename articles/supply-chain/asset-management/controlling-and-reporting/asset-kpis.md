---
title: KPI-er for aktivum
description: Dette emnet beskriver KPI-er for aktivum i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0cd83bf70d867f40bca018386cb3f8c581e162ce
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216396"
---
# <a name="asset-kpis"></a>KPI-er for aktivum

[!include [banner](../../includes/banner.md)]

 

I Aktivastyring kan du beregne forskjellige KPIer for aktiva og aktivatyper. Du bruker KPIer til å få en oversikt over ytelse på anleggsmidler i forbindelse med for eksempel oppetid, nedetid, reparasjonstid og gjennomsnittstid mellom feil (MTBF).

1. Klikk **Aktivastyring** > **Forespørsler** > **Aktiva** > **KPI-er for aktivum**.

2. I dialogboksen **Beregn KPI-er for aktivum** velger du **tidsskalaen** som skal brukes i beregningen, og en periode i feltene **Fra dato** og **Til dato**. 

3. I hurtigfanen **Poster som skal inkluderes** kan du velge å inkludere aktiva og aktivatyper i beregningen, hvis det er nødvendig.

4. Klikk på **OK** for å starte beregningen.

5. I hurtigfanen **Oversikt** vises resultatene av beregningen i rutenettvisning. Hvert anleggsmiddel vises på en egen linje.

6. På hurtigfanen **KPI-er for valgt linje** ser du beregninger for aktivumet som er valgt i hurtigfanen **Oversikt**. KPI-verdiene kategoriseres med hensyn til **Tid**, **Tilgjengelighet**, **Arbeidsordrer**, **Vedlikehold**, **Feil**, **Nedetid ved vedlikehold** og **Kostnad**.

I tabellen nedenfor finner du en beskrivelse av feltene på siden **KPI-er for aktivum**.

| Felt                   | Beskrivelse                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktivum                   | Aktivum-ID.                                                                                                                                                                                                                                                                                             |
| Samlet tid              | Total tid som er definert i kalenderen som brukes i beregningen. Hvis aktivumet er knyttet til en ressurs, brukes den tilknyttede ressurskalenderen. Hvis aktivumet ikke er knyttet til en ressurs, brukes kalenderen som er valgt i feltet **Standardkalender** i **Aktivabehandlingsparametere**. |
| Oppetid                  | Total tid minus nedetid.                                                                                                                                                                                                                                                                            |
| Nedetid                | Registreringer av nedetid ved vedlikehold som er gjort for aktivumet i den valgte perioden.                                                                                                                                                                                                                              |
| Reparasjonstid             | Totalt antall arbeidstimer brukt på reparasjonsarbeidsordrer.                                                                                                                                                                                                                                            |
| Tilgjengelighet i %          | Oppetid delt på total tid og multiplisert med 100.                                                                                                                                                                                                                                                   |
| Antall feil        | Antall feilårsaker som er registrert om feilsymptomer på aktivumet i den valgte perioden.                                                                                                                                                                                                             |
| MTBF                    | Gjennomsnittstid mellom feil, som er total tid delt på antall feil som registreres for aktivumet i den valgte perioden. Hvis antall feil er null, settes MTBF til total tid.                                                                                                                   |
| Feilsats               | 1 delt på MTBF.                                                                                                                                                                                                                                                                                    |
| MRT                     | Gjennomsnittlig tid for reparasjon, som er reparasjonstid delt på antall feil som registreres for aktivumet i den valgte perioden. Hvis antall feil er null, settes MRT til reparasjonstid.                                                                                                                           |
| Antall stopp         | Antall registreringer av nedetid ved vedlikehold som er opprettet på aktivumet.                                                                                                                                                                                                                                     |
| MTBS                    | Gjennomsnittstid mellom stopp, som er total tid delt på antall registreringer av nedetid ved vedlikehold. Hvis antall registreringer av nedetid ved vedlikehold er null i den valgte perioden, settes MTBS-verdien til total tid.                                                                                      |
| Forebyggende kostnad         | Kostnader postert for aktivumet som er knyttet til kostnadstypen "Forebyggende" i den valgte perioden. Kosttyper defineres på arbeidsordretyper.                                                                                                                                                                       |
| Korrigeringskostnad         | Kostnader postert for aktivumet som er knyttet til kostnadstypen "Korrigerende" i den valgte perioden. Kosttyper defineres på arbeidsordretyper.                                                                                                                                                                       |
| Erstatningsverdi       | Verdi definert for aktivumet som erstatningskostnaden.                                                                                                                                                                                                                                                  |
| Aktivumtype             | Identifikasjon av aktivatypen som er valgt for aktivumet.                                                                                                                                                                                                                                             |
| Produsent           | Identifikasjon av produsenten som er valgt for aktivumet.                                                                                                                                                                                                                                                 |
| Modell                   | Identifikasjon av produsentmodellen som er valgt for aktivumet.                                                                                                                                                                                                                                           |
| Fra dato               | Startdato for KPI-beregningen. Hvis aktivumet ble opprettet etter startdatoen som er valgt for beregningen, vises startdatoen for aktivumet i dette feltet.                                                                                                                                  |
| Til dato                 | Sluttdato for KPI-beregningen. Hvis aktivumet ble registrert som inaktivt før sluttdatoen som er valgt for beregningen, vises datoen da aktivumet ikke lenger er aktivt fra, i dette feltet.                                                                                               |
| Tidsskala              | Under beregningen av KPIene velger du en tidsskala som skal brukes: timer, dager eller uker.                                                                                                                                                                                                            |
| Tilgjengelighet            | Oppetid delt på total tid.                                                                                                                                                                                                                                                                         |
| Arbeidsordrer             | Totalt antall arbeidsordrer som er inkludert i KPI-beregningen.                                                                                                                                                                                                                                          |
| Arbeidsordretid         | Totalt antall arbeidstimer brukt på arbeidsordrene.                                                                                                                                                                                                                                               |
| Primære arbeidsordrer     | Antall primære arbeidsordrer som er inkludert i KPI-beregningen.                                                                                                                                                                                                                                        |
| Sekundære arbeidsordrer   | Antall sekundære arbeidsordrer som er inkludert i KPI-beregningen.                                                                                                                                                                                                                                      |
| Arbeidsordrer for vedlikehold | Antall arbeidsordrer for vedlikehold som er inkludert i KPI-beregningen. En arbeidsordre for vedlikehold er en arbeidsordre uten relaterte feilårsaker.                                                                                                                                                             |
| Vedlikeholdstid        | Totalt antall arbeidstimer brukt på arbeidsordrer for vedlikehold.                                                                                                                                                                                                                                       |
| Arbeidsordrer for reparasjon      | Antall arbeidsordrer for reparasjon som er inkludert i KPI-beregningen. En arbeidsordre for reparasjon er en arbeidsordre med en relatert feilårsak.                                                                                                                                                                        |
| Pålitelighet i %           | Beregning basert på den forventede eksponentielle utviklingen i feilregistreringer på et aktivum, som betyr at over tid blir aktivumet mindre pålitelig på grunn av slitasje. Beregningen av denne KPIen er basert på MTBF og total tid.                                                            |
| MTPS                    | Gjennomsnittstid mellom produksjonsstopp, som er nedetid ved vedlikehold delt på antall registreringer av nedetid ved vedlikehold. Hvis antall registreringer av nedetid ved vedlikehold er null i den valgte perioden, settes MTPS-verdien til null.                                                                               |
| Total kostnad              | Totale kostnader postert for aktivumet i den valgte perioden.                                                                                                                                                                                                                                              |
| Investeringskostnad         | Kostnader postert for aktivumet som er knyttet til kostnadstypen "Investering" i den valgte perioden. Kosttyper defineres på arbeidsordretyper.                                                                                                                                                                       |

Figuren nedenfor viser et skjermbilde av en KPI-beregning for fire aktiva.

![Skjermbilde av en KPI-beregning for fire aktiva](media/11-controlling-and-reporting.png)

- Du kan velge flere aktiva i **Alle aktiva** og klikke knappen **KPI-er for aktiva** i fanen **Generelt**. Deretter klikker du **OK** i dialogboksen **Beregn KPI-er for aktivum** for å beregne KPIer for de valgte aktivaene.  
- Resultater fra en KPI-beregning kan omfatte [registreringer av nedetid ved vedlikehold](../work-orders/maintenance-downtime.md), avhengig av oppsettet og bruken av årsakskoder for nedetid ved vedlikehold. 

