---
title: Delvis lokasjonssyklustelling
description: "Syklustellingsplaner styrer de faktiske telleoperasjonene. Du kan be om at bare bestemte produkter og produktvarianter telles, i stedet for all lagerbeholdning på et sted."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 856ac2a61bc06a772b586a0cf77496fc360db623
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="partial-location-cycle-counting"></a>Delvis lokasjonssyklustelling

[!include[banner](../includes/banner.md)]


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
3.  Du kan velge produkter for syklustellingsplaner ved å sette feltet **Tomme lokasjoner** til **Utelat tomme**. Når syklustellingsplanen behandles, opprettes en delvis syklustellingl for varenummer A0001. Den faktiske telleprosessen kan utføres ved hjelp av et menyelement for mobilenhet for veiledet syklustelling.



<a name="see-also"></a>Se også
--------

[Syklustelling](cycle-counting.md)

