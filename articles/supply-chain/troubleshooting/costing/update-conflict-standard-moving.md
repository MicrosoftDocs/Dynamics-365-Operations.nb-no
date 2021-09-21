---
title: Det oppstår en oppdateringskonflikt når lagervurderingsmetoden er Standardkostnad eller Glidende gjennomsnitt
description: Det oppstår en oppdateringskonflikt når lagervurderingsmetoden er enten Standardkostnad eller Glidende gjennomsnitt
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477230"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Det oppstår en oppdateringskonflikt når lagervurderingsmetoden er enten Standardkostnad eller Glidende gjennomsnitt

## <a name="symptoms"></a>Symptomer

Når du posterer dokumenter, for eksempel lagerjournaler, bestillingsfakturaer eller salgsordrefakturaer parallelt for å forbedre skalerbarhet og ytelse, kan det hende at du får en feilmelding om en oppdateringskonflikt, og det kan hende at enkelte dokumenter ikke posteres. Dette problemet kan oppstå når lagervurderingsmetoden er enten *Standardkostnad* eller *Glidende gjennomsnitt*. Begge disse metodene er permanente etterkalkuleringsmetoder. Den endelige kostnaden fastsettes med andre ord ved postering.

Hvis du bruker metoden *Glidende gjennomsnitt*, ligner feilmeldingen på dette eksemplet:

> Lagerverdien xx,xx forventes ikke etter den proporsjonale utgiftsberegningen

Hvis du bruker metoden *Standardkostnad*, ligner feilmeldingen på dette eksemplet:

> Standardkostnaden samsvarer ikke med den økonomiske lagerverdien etter oppdateringen. Verdi = xx,xx, Ant. = yy,yy, Standardkostnad = zz,zz

## <a name="workaround"></a>Løsning

Før Microsoft gir ut en løsning på problemet, må du vurdere å bruke følgende midlertidige løsninger for å unngå eller minimere disse feilene:

- Poster de mislykkede dokumentene på nytt.
- Opprett dokumenter med færre linjer.
- Unngå desimalverdier i standardkostnaden. Prøv å definere standardkostnaden slik at **Prisantall**-feltet settes til *1*. Hvis du må angi en verdi for **Prisantall** som er større enn *1*, kan du prøve å redusere antallet desimalplasser i enhetens standardkostnad. (Ideelt sett bør det være færre enn to desimalplasser.) Unngå å definere innstillinger for standardkostnad der for eksempel **Pris** = *10* og **Prisantall** = *3*, fordi disse vil gi en standardkostnad for en enhet på 3,333333 (der desimalverdien gjentas).
- I de fleste dokumenter bør du unngå å ha flere linjer som har samme kombinasjon av produkt og økonomiske lagerdimensjoner.
- Reduser graden av parallellisering. (I dette tilfellet kan systemet bli raskere fordi det oppstår færre oppdateringskonflikter og nye forsøk.)
