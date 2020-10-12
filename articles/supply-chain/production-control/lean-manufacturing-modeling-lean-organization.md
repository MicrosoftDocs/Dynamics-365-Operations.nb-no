---
title: Modellere en lean-organisasjon
description: Denne artikkelen inneholder informasjon om de viktigste begrepene i modellering av en lean-organisasjon.
author: cvocph
manager: tfehr
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, KanbanFlowSelection, KanbanFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c6c6602728ed88e7b293dc6308564493e936ecb
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826364"
---
# <a name="modeling-a-lean-organization"></a>Modellere en lean-organisasjon

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om de viktigste begrepene i modellering av en lean-organisasjon. 

Et scenario for Lean manufacturing er vanligvis mer enn bare en samling av ikke-relaterte kanban-regler eller Policyer for materialforsyning. Flyten av materialer og produkter gjennom arbeidsceller og lokasjoner for en bestemt produksjon eller forsyningsscenario kan beskrives som en sekvens eller lite nettverk av prosess- eller overføringsaktiviteter. Denne serien eller nettverket, kalles en produksjonsflyt.

## <a name="production-flows-in-lean-manufacturing"></a>Produksjonsflyter i lean manufacturing
I produksjonsscenarioer som er basert på produksjonsordrer utstedes materialer til en bestemt produksjonsordre. I løpet av en sekvens med operasjonersom er basert på en stykkliste og ruter, opprettes og mottas til slutt produkter på den angitte lokasjonen. Produksjonstiden for produksjonsordrer varierer i områder fra minutter til uker. Alle tilknyttede kostnader, materiale og arbeid samles på produksjonsordren. 

For å redusere leveringstider og overflødig beholdning mellom arbeidssentre som er forårsaket av partiproduksjon, introduserer lean manufacturing Kanban-etterfylling og supermarkeder i produksjon og lageretterfylling. Disse funksjonene forstyrrer vanligvis produksjonen av delvis uavhengige kanban-sykluser. Etterfylling for en kanban for et halvfabrikata utløses ikke lenger av en ordre for ferdige produkter. 

Hvis du vil gjenopprette en kontekst for produksjon og kostnader for de forskjellige kanban-scenariene som foreslås, introduseres aktivitetsbaserte produksjonsflyter som ryggraden for lean manufacturing. Alle kanban-regler refererer til denne forhåndsdefinerte strukturen. Den aktivitetsbaserte modellen støtter oppsettet av en rekke ulike scenarier. Denne modellen øker imidlertid ikke kompleksiteten for produksjonsarbeidere, fordi alle scenarier bruker samme aktivitetsbaserte brukergrensesnittet.

## <a name="semi-finished-products-non-bom-levels"></a>Halvfabrikata (ikke stykklistenivåer)
Lean manufacturing integrerer Kanbaner for lagerførte produkter og halvfabrikata i ett enkelt rammeverk, og tilbyr derfor en felles brukeropplevelse i alle situasjoner. På grunn av denne arkitekturen trenger ikke lenger flere stykklistenivåer å introduseres for å aktivere kanbaner som skal brukes for halvfabrikata. Denne arkitekturen bidrar også til å redusere lagertransaksjoner til et minimum.

## <a name="products-and-material-in-work-in-progress"></a>Produkter og materialer i varer i arbeid
Reduksjonen av partistørrelser til den ideelle tilstanden for en enkelt flyt i lean manufacturing kan føre til en dramatisk økning av lagertransaksjoner hvis hver plukkingsprosess eller kanban-registrering fører til transaksjoner for de forbrukte varene. Arkitekturen for produksjonsflyten tillater overføringen av materiale til produksjonsflyten med uttak-Kanbaner i lagrings- eller transporthåndteringsenhetsstørrelser. Verdien for det utstedte materialet legges til i VIA-kontoen (varer i arbeid) som er relatert til produksjonsflyten. Denne virkemåten ligner virkemåten for materiale som er tilordnet en produksjonsordre. Det samme prinsippet kan brukes for produkter og halvfabrikata. Med mindre disse produktene opprettes, overføres eller brukes i en produksjonsflyt, er lagertransaksjoner valgfrie. Når varene er postert til lageret, reduseres VIA-kontoen for produksjonsflyten ved å trekke fra den tilknyttede standardkostnaden.

## <a name="value-streams-and-value-stream-mapping"></a>Verdistrømmer og verdistrømtilordning
Arkitekturen for Lean manufacturing for er inspirert av de fem Lean-prinsippene som ble formulert av Womack og Jones: kundeverdi, verdistrøm, flyt, pull og perfeksjon. En godkjent metode for å implementere løsninger for lean manufacturing i den fysiske verdenen på produksjonen, er verdistrømtilordning (VSM). Denne metoden ble innført av Rother og Shook i publikasjonen "Learning to See" ved Lean Manufacturing Institute. 

Den fremtidige tilstanden for verdistrøm modelleres som en produksjonsflytversjon. Alle prosesser i verdistrømmen modelleres som Prosessaktiviteter. Bevegelser eller overføringer kan modelleres som overføringsaktiviteter hvis overføringsstatusen må registreres eller hvis en integrering med lagerplukking eller konsoliderte leveranser er nødvendig. 

Selve verdistrømmen modelleres som en driftsenhet. Derfor kan verdistrømmen brukes som en finansdimensjon.

Hvis du vil ha mer informasjon om driftsenheter, kan du se [Opprette en driftsenhet](../../fin-and-ops/organization-administration/tasks/create-operating-unit.md).

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Etterkalkulering for lean manufacturing basert på produksjonsflyten
Den periodiske konsolideringen av kostnader for en produksjonsflyt retter opp den relaterte VIA-kontoen, og gjør det mulig å fastsette avvik for produktene som kommer fra produksjonsflyten.

## <a name="continuous-improvement"></a>Kontinuerlig forbedring
For å gi bedre støtte for kontinuerlig forbedring implementeres produksjonsflyter i tidseffektive versjoner. Derfor kan en eksisterende produksjonsflytversjon, sammen med alle relaterte kanban-regler, kopieres til en fremtidig versjon av produksjonsflyten. I tillegg kan den fremtidige tilstanden for produksjonsflyten modelleres før den er godkjent og aktivert for produksjon. For å bidra til å garantere en sømløs materialflyt på overgangsdatoen og senere, relateres eksisterende kanbaner fra gamle produksjonsflytversjoner automatisk til den nye versjonen.

## <a name="simplicity"></a>Enkelhet
For implementering av Lean manufacturing har vi valgt tilnærmingen for produksjonsflyt og aktivitet som gjør det mulig å modellere enkle og sammensatte produksjonsscenarier i en enkelt skalerbar arkitektur. En nærmere kikk på aktivitetskonseptet viser en ny enkelhet for brukerne som trenger det: shop floor- og logistikkarbeidere. Ved å rapportere mot aktivitetsbaserte jobber i stedet for lagertransaksjoner, overfører et felles brukergrensesnitt for alle varianter av lean manufacturing forretningskompleksitet fra brukergrensesnittet til der det hører til: produksjonsflyten som ryggraden i lean manufacturing.



