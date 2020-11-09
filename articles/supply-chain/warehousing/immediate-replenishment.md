---
title: Umiddelbar etterfylling
description: Dette emnet beskriver hvordan du kan bruke umiddelbar etterfylling for å etterfylle beholdningen når et lokasjonsdirektiv ikke kan tilordne beholdning.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c69a9c9fd595280ba4f05a11409a3e672e4b1691
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017513"
---
# <a name="immediate-replenishment"></a>Umiddelbar etterfylling

[!include [banner](../includes/banner.md)]

Umiddelbar etterfylling lar deg etterfylle beholdning umiddelbart etter at en lokasjonsdirektivlinje ikke kan tilordne beholdning. Etterfyllingen er basert på én linje i oppsettet av lokasjonsdirektivet. Hvis lager ikke er tilgjengelig i måleenheten som er angitt av denne linjen, skjer etterfylling av denne målenheten umiddelbart.

Umiddelbar etterfylling gir et alternativ til metoden der tildelingen av lager er basert på flere linjer i lokasjonsdirektivet, og der behovet er summert på slutten av tildelingen og etterfylles i måleenheten som er angitt av den siste linjen i lokasjonsdirektivet.

Fordelene ved å bruke umiddelbar etterfylling er at etterfylling kan begrenses av bestemte enheter, og antallet kan sendes til bestemte lokasjoner.

## <a name="business-scenario"></a>Forretningsscenario

Du har for eksempel et lager som har egne plukkeområder for målenheten "boks" og "enkelt". Du vil optimalisere plukkeprosessen ved å plukke så mange bokser som mulig, og deretter plukke gjenværende antall som er mindre enn en boks, fra området "enkelt".

I dette tilfellet kan du bruke umiddelbar etterfylling. I lokasjonsdirektivet kan du definere umiddelbar etterfylling for bokser slik at behovsetterfylling brukes så snart det er manko på bokser som kan plukkes for behovsantallet. På denne måten kan du optimalisere plukkeprosessen slik at plukkingen inkluderer så mange bokser som mulig. Umiddelbar etterfylling genererer etterfylling av boksene, og behovet sendes ikke videre slik at antallene plukkes i målenheten "enkelt. Med andre ord så er det bare antallene som er ment å plukkes i "enkelt"-måleenheten (det vil si antall som er mindre enn en boks), som blir plukket fra "enkelt"-området. Hvis det oppstår manko i "boks"-området, kan du plukke så mange bokser som mulig ut av det totale behovet. De gjenstående antallene plukkes deretter fra området "enkelt".

## <a name="where-it-applies"></a>Der det er aktuelt

Umiddelbar etterfylling brukes under bølgeutførelse hvis tildelingen mislykkes for en lokasjonsdirektivlinje som en etterfyllingsmal er definert for.

## <a name="set-up-immediate-replenishment"></a>Konfigurere umiddelbar etterfylling

- Gå til **Lagerstyring** \> **Oppsett** \> **Lokasjonsdirektiver** , og deretter i **Linjer** -kategorien i **Mal for umiddelbar etterfylling** -listen velger du en etterfyllingsmal for bølgebehov.

Etterfyllingsmalen brukes hvis lokasjonsdirektivlinjen ikke kan tildele en angitt målenhet.

## <a name="troubleshooting"></a>Feilsøking

Hvis umiddelbar etterfylling er valgt for en lokasjonsdirektivlinje, men ikke noe etterfyllingsarbeid genereres når du bruker maler for behovsetterfylling for denne lokasjonsdirektivlinjen, må to hovedårsaker undersøkes:

- Kontroller at behovsetterfyllingsmalen som brukes, er konfigurert til å bruke de riktige lokasjonsmalene og arbeidsmalene for **Etterfylling** -typen.
- Kontroller at det er stor nok lagerbeholdning på stedene der behovsetterfyllingsmalen søker etter lagerbeholdning for etterfylling.
