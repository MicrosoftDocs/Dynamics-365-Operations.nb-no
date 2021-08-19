---
title: Lean-utligning fra salgsordrer
description: Denne prosedyren fokuserer på å validere utligningstreet fra en salgslinje der varen produseres med Kanbaner.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 63d3b17d5a5a387d000fbac7f7bbf4431d4febca75cc2a85c2c359ed479c911e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714890"
---
# <a name="lean-pegging-from-sales-orders"></a>Lean-utligning fra salgsordrer

[!include [banner](../../includes/banner.md)]

Denne prosedyren fokuserer på å validere utligningstreet fra en salgslinje der varen produseres med Kanbaner. Alle Kanban-jobbene planlegges etter valideringen av utligningstreet. Dette er nyttig for ordrescenarier der ordremottakeren må sikre at produksjonen kan starte umiddelbart. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren er ment for avanserte ordremottakere som jobber i et lean-firma.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Opprette en salgsordre for en Kanban-styrt vare
1. Gå til Alle salgsordrer.
2. Klikk på Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
    * Bruk US-001.  
4. Klikk på OK.
5. Skriv inn L0001 i feltet Varenummer.
6. Sett verdien for Antall til 30.
    * Det er viktig at antallet er høyere enn 24 for å utløse Kanban-regelen for hendelse.  

## <a name="open-a-pegging-tree"></a>Åpne et utligningstre 
1. Klikk på Produkt og forsyning.
2. Klikk på Vis utligningstre.
    * Legg merke til at utligningstreet viser alle nivåer av utligningen som kreves for salgsordrelinjen. I dette tilfellet er det to nivåer med Kanbaner og alle de nødvendige komponentene.  

## <a name="plan-the-pegging-tree"></a>Planlegge utligningstreet
1. Velg Salgslinje 000832 \ Kanban 000558.
2. Vis delen Kanban-jobber.
    * Legg merke til at jobbstatusen for Kanban-jobben er Ikke planlagt.  
3. Klikk på Planlegg helt utligningstre.
    * Dette vil planlegge alle Kanban-jobber i utligningstreet, og endre jobbstatusen fra Ikke planlagt til Planlagt.  
4. Oppdater siden.
    * Legg merke til at Kanban-jobbstatusen endres fra Ikke planlagt til Planlagt.  
5. Velg Salgslinje 000832 \ Kanban 000558\ Problem for L0001\ Kanban 000559 i treet.
    * Jobben for den andre Kanbanen planlegges også fordi hele utligningstreet planlegges. Legg merke til at Kanban-jobbstatusen endres fra Ikke planlagt til Planlagt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]