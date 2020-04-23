---
title: Delvis lokasjonssyklustelling
description: Syklustellingsplaner styrer de faktiske telleoperasjonene. Du kan be om at bare bestemte produkter og produktvarianter telles, i stedet for all lagerbeholdning på et sted.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f07c7754dbe36334e8972d49edf9fb84a78f5d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215683"
---
# <a name="partial-location-cycle-counting"></a>Delvis lokasjonssyklustelling

[!include [banner](../includes/banner.md)]

Syklustellingsplaner styrer de faktiske telleoperasjonene. Du kan be om at bare bestemte produkter og produktvarianter telles, i stedet for all lagerbeholdning på et sted.

Ved å bruke syklustellingsplaner til å opprette opptellingsarbeid, kan du styre de faktiske opptellingsoperasjonene. Du kan be om at bare bestemte produkter og produktvarianter telles, i stedet for all lagerbeholdning på et sted. Ved å filtrere etter bestemte produkter kan lagersjefen redusere indirekte kostnader til gjennomgang, unngå konsolideringsfeil og spare tid.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Slik konfigurerer du delvis lokasjonssyklustelling
Når du bruker arbeidsprosessen for lageret for å telle operasjoner, opprettes et arbeidshode for hver lokasjon. Når du definerer syklustellingsplanen, kan du bruke spørringen **Velg lokasjoner** for å begrense syklustellingsarbeidet som er opprettet. Når du velger produkter for syklustellingsplanen, kan du velge både produkt- og produktetvariantspørringer for å begrense hva som telles. 

Du kan tilknytte en **arbeidsmalen** til en syklustellingsplan for å definere hvordan syklustellingsarbeidet skal opprettes. Arbeidsmalen for opptellingsoperasjoner refereres direkte fra syklustellingsplanen. 

Når du definerer detaljer for arbeidsmalen, kan du bruke **arbeidslinjeskift**-alternativet for å angi om arbeidslinjene i opptellingn må grupperes etter varenummer eller produktvariantnummer. Dette oppsettet er nødvendig hvis du vil telle lagerbeholdningen bare for bestemte produkter på et sted. Linjene som opprettes for syklustellingsarbeidet, vil ha det informasjonsnivået du angir her, og den styrte opptellingsoperasjonen blir håndtert baser tpå dette nivået. 

Hvis du knytter syklustellingsplaner til arbeidsmaler ved hjelp av alternativet **arbeidslinjeskift**, velges feltet **Delvis syklustelling** for syklustellingsarbeidet som er opprettet, og flere arbeidslinjer for syklustelling opprettes basert på arbeidsmalens definisjon. 

Før delvis syklustellingsarbeid kan behandles, må du, som et minimum velge **Vis varenummer** for menyelementet mobilenhet som en del av oppsettet for syklustelling. Lageroperatøren vil bli bedt om bare å registrere opptellingsinformasjon som er knyttet til opptellingslinjer (varenumre og produktdimensjoner). Alle andre lagerbeholdninger vil bli ignorert for denne opptellingsprosessen. 

For den delvise syklustellingsprosessn blir ikke dato/klokkeslett for **Siste syklustelling** oppdatert for lokasjonen.

## <a name="example"></a>Eksempel
I dette eksemplet må bare varenummeret A0001 telles i lager 61.

1.  Det opprettes en ny mal for syklustelling. Alternativet **arbeidslinjeskift** brukes til å gruppere opptellingsarbeidslinjer etter varenummer. Derfor får arbeidet som er opprettet for syklustelling, linjer per varenummer. Du kan også gruppere linjene etter produktvariantnummer.
2.  Det opprettes en ny plan for syklustelling som refererer til den nylig opprettede arbeidsmalen. Syklustellingsplanen inkluderer alle lokasjoner på lager 61 (spørringen **Veg lokasjoner**) som rommer beholdningen for varenummer A0001. Valg av bestemte produkter er definert i delen **Produktvalg for syklustellingsplan**.
3.  Du kan velge produkter for planer for syklustelling ved å sette feltet **Tomme lokasjoner** til **Ekskluder tomme**. Når planen for syklustellingen behandles, opprettes det delvis syklustellingsarbeid for varenummer A0001. Den faktiske telleprosessen kan utføres ved hjelp av et menyelement for mobilenhet for veiledet syklustelling.



<a name="additional-resources"></a>Tilleggsressurser
--------

[Syklustelling](cycle-counting.md)

