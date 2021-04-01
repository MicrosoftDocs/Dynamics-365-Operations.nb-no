---
title: Delvis lokasjonssyklustelling
description: Syklustellingsplaner styrer de faktiske telleoperasjonene. Du kan be om at bare bestemte produkter og produktvarianter telles, i stedet for all lagerbeholdning på et sted.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abafe64a17b7b284e5e045da33bb15cf3c42800b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234687"
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

For den delvise syklusopptellingsprosessen blir ikke dato-/klokkeslettverdien for **Siste syklustelling** oppdatert for den siste syklusen for lokasjonen, selv om alle varene på en gitt lokasjon telles. Det delvise syklusantallet bruker ikke parameteren **Dager mellom syklustellinger** på siden **Planer for syklustelling**. Delvis syklusantall støtter ikke opptelling av flere elementer samtidig på samme sted. Funksjonaliteten for delvis syklustelling kan resultere i at samme sted telles flere ganger for en vare når **Behandle syklustellingsplan** kjøres. Hvis du vil unngå dette scenarioet, angir du filtre i feltet **Velg lokasjoner**.

> [!NOTE]
> Lagerappen har ikke knappen **Legg til LP eller vare** når du bruker en delvis syklusopptellingsprosess.

## <a name="example"></a>Eksempel

I dette eksemplet må bare varenummeret A0001 telles i lager 61.

1. Det opprettes en ny mal for syklustelling. Alternativet **arbeidslinjeskift** brukes til å gruppere opptellingsarbeidslinjer etter varenummer. Derfor får arbeidet som er opprettet for syklustelling, linjer per varenummer. Du kan også gruppere linjene etter produktvariantnummer.
1. Det opprettes en ny plan for syklustelling som refererer til den nylig opprettede arbeidsmalen. Syklustellingsplanen inkluderer alle lokasjoner på lager 61 (spørringen **Veg lokasjoner**) som rommer beholdningen for varenummer A0001. Valg av bestemte produkter er definert i delen **Produktvalg for syklustellingsplan**.
1. Du kan velge produkter for planer for syklustelling ved å sette feltet **Tomme lokasjoner** til **Ekskluder tomme**. Når planen for syklustellingen behandles, opprettes det delvis syklustellingsarbeid for varenummer A0001. Den faktiske telleprosessen kan utføres ved hjelp av et menyelement for mobilenhet for veiledet syklustelling.

## <a name="additional-resources"></a>Tilleggsressurser

[Syklustelling](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]