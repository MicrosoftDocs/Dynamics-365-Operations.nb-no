---
title: Ordrefrister
description: Denne artikkelen inneholder informasjon om tidsfrister for ordreregistrering. En tidsfrist for ordreregistrering er en tidsgrense som bestemmer om en kundeordre skal behandles (og oppfylles) som om den ble mottatt på gjeldende dag eller neste dag.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5266e58a0f18141af920100b5f44ce98a3dbc6c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215568"
---
# <a name="order-entry-deadlines"></a>Ordrefrister

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om tidsfrister for ordreregistrering. En tidsfrist for ordreregistrering er en tidsgrense som bestemmer om en kundeordre skal behandles (og oppfylles) som om den ble mottatt på gjeldende dag eller neste dag.

I mange firmaer blir bare salgsordrer som mottas før et bestemt tidspunkt på dagen, behandlet som om de ble mottatt på denne dagen. Alle ordrer som mottas etter dette tidspunktet, behandles som om de ble mottatt neste arbeidsdag. Denne fristen for ordrer kalles tidsfrister for ordreregistrering.  

Tidsfrister for ordreregistrering brukes som inndata for ordrebekreftelsen. De gjør det derfor enklere for deg å administrere kundenes forventninger om levering. Kunder kan for eksempel se at hvis de plasserer en ordre hos deg før et bestemt tidspunkt, vil du sørge for å sende varene på samme dag. Hvis de går glipp av denne tidsfristen, kan de forvente levering bare på neste arbeidsdag. Du kan angi tidsfrister for ordreregistrering basert på lageret muligheter og leveringsadresse transportør tidsplaner.  

Du angir tidsfrister for ordrer for alle dagene i uken på **Ordrefrister**-siden. Hvis ordrer mottas etter angitt tidspunkt, behandles de som om de ble mottatt neste arbeidsdag. Som standard er disse tidspunktene satt til 23.59, det vil si ett minutt før midnatt på slutten av den aktuelle dagen. Du kan endre standardtidspunktene slik at de sammenfaller med tidsfristene for levering og mottak.  

Du kan definere tidsfrister for ordreregistrering for en bestemt gruppe kunder. Du ønsker kanskje at en bestemt gruppe kunder skal ha tidsfrister for ordreregistrering som er senere enn for andre kunder. I dette tilfellet må du først angi grupper for tidsfrister for ordreregistrering på siden **Ordrefristgrupper**. Deretter tilordner du gruppene til kunder på **Kunder**-siden.  

Hvis firmaet består av flere områder, kan du definere tidsfrister for ordre for hvert område. Hvis områdene ligger i ulike tidssoner, er tidsfrister for ordreregistrering definert i hvert områdets tidssone. Når du imidlertid arbeider med salgsordrer og salgstilbud, blir tidsfristen for ordre konvertert til din tidssone på siden **Tilgjengelige leverings- og mottaksdatoer**.  

På siden **Aktiver ordrefristkombinasjoner** definerer du kombinasjoner av områder og ordrefristgrupper som er tillatt.

## <a name="example-order-entry-deadline"></a>Eksempel: Tidsfrist for ordre
Tidsfrister for ordreregistrering på tirsdager er satt til 16.00. På en bestemt tirsdag klokken 17:00 prøver du å angi gjeldende dato som forsendelsesdatoen. (Vær oppmerksom på at det er ingen leveringstiden i dette eksemplet.) Hvis det er merket av for **Leveringsdatokontroll**, vises en advarsel som sier at datoen ikke er gyldig. Denne advarselen vises på siden **Tilgjengelige leverings- og mottaksdatoer**, der du deretter kan velge alternative datoer.

## <a name="example-different-order-entry-deadlines-per-site"></a>Eksempel: Ulike tidsfrister for ordre per område
Firmaet består av to områder. Områdene finnes i ulike tidssoner, som vist i følgende tabell.

| Område A                      | Område B                      |
|-----------------------------|-----------------------------|
| Bergen                  | Florida                     |
| Stillehavskysten (normaltid) | Østkysten (normaltid) |

Område A og B har definert følgende tidsfrister for ordrer.

| Dag i uken             | A: Ordrefrister (PST) | B: Ordrefrister (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Mandag                      | 13:00:00                          | 14:00:00                          |
| Tirsdag                     | 13:00:00                          | 14:00:00                          |
| Onsdag                   | 13:00:00                          | 14:00:00                          |
| Torsdag                    | 13:00:00                          | 14:00:00                          |
| Fredag                      | 13:00:00                          | 14:00:00                          |

Du er ordrebehandler i Utah, der tidssonen er Rocky Mountains (normaltid). Dette betyr at så lenge du legger inn ordrer i område A før tidssonen Rocky Mountains (normaltid) kl. 14:00 og i område B før tidssonen Rocky Mountains (normaltid) kl. 12:00, oppfyller du tidsfristene for ordrer for begge områder.  

Følgende tabell viser tidsfristene for ordrer for område A og B, omregnet til tidssonen Rocky Mountains (normaltid).

| Område A: PST         | Område A: MST        | Område B: EST           | Område B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00:00               | 14:00:00              | 14:00:00                 | 12:00:00              |

**Obs!** Hvis det foreligger justering for sommertid, justeres tidsfristene for ordrer i henhold til dette.

## <a name="example-same-order-entry-deadline-per-site"></a>Eksempel: Samme tidsfrist for ordre per område
Firmaet består av to områder. Områdene finnes i ulike tidssoner, som vist i følgende tabell.

| Område A                      | Område B                      |
|-----------------------------|-----------------------------|
| Bergen                  | Florida                     |
| Stillehavskysten (normaltid) | Østkysten (normaltid) |

Område A og B har definert følgende tidsfrister for ordrer.

| Dag i uken | Stillehavskysten (normaltid) og Østkysten (normaltid) |
|-----------------|-------------|
| Mandag          | 13:00:00       |
| Tirsdag         | 13:00:00       |
| Onsdag       | 13:00:00       |
| Torsdag        | 13:00:00       |
| Fredag          | 13:00:00       |

Du er ordrebehandler i Utah, der tidssonen er Rocky Mountains (normaltid). Dette betyr at så lenge du legger inn ordrer i område A før tidssonen Rocky Mountains (normaltid) kl. 14:00 og i område B før tidssonen Rocky Mountains (normaltid) kl. 11:00, oppfyller du tidsfristene for ordrer for begge områder. 

Følgende tabell viser tidsfristene for ordrer for område A og B, omregnet til tidssonen Rocky Mountains (normaltid).

| Område A: PST         | Område A: MST        | Område B: EST           | Område B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00:00               | 14:00:00              | 13:00:00                 | 11:00:00              |

**Obs!** Hvis det foreligger justering for sommertid, justeres tidsfristene for ordrer i henhold til dette.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Leveringsplaner](delivery-schedules.md)



