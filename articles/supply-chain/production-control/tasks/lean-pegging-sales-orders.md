---
title: Lean-utligning fra salgsordrer
description: Denne prosedyren fokuserer på å validere utligningstreet fra en salgslinje der varen produseres med Kanbaner.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5142fe552147a9b2988a8828ba1206fad9e252e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146750"
---
# <a name="lean-pegging-from-sales-orders"></a>Lean-utligning fra salgsordrer

[!include [banner](../../includes/banner.md)]

Denne prosedyren fokuserer på å validere utligningstreet fra en salgslinje der varen produseres med Kanbaner. Alle Kanban-jobbene planlegges etter valideringen av utligningstreet. Dette er nyttig for ordrescenarier der ordremottakeren må sikre at produksjonen kan starte umiddelbart. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren er ment for avanserte ordremottakere som jobber i et lean-firma.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Opprette en salgsordre for en Kanban-styrt vare
1. Gå til Alle salgsordrer.
2. Klikk Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
    * Bruk US-001.  
4. Klikk OK.
5. Skriv inn L0001 i feltet Varenummer.
6. Sett verdien for Antall til 30.
    * Det er viktig at antallet er høyere enn 24 for å utløse Kanban-regelen for hendelse.  

## <a name="open-a-pegging-tree"></a>Åpne et utligningstre 
1. Klikk Produkt og forsyning.
2. Klikk Vis utligningstre.
    * Legg merke til at utligningstreet viser alle nivåer av utligningen som kreves for salgsordrelinjen. I dette tilfellet er det to nivåer med Kanbaner og alle de nødvendige komponentene.  

## <a name="plan-the-pegging-tree"></a>Planlegge utligningstreet
1. Velg Salgslinje 000832 \ Kanban 000558.
2. Vis delen Kanban-jobber.
    * Legg merke til at jobbstatusen for Kanban-jobben er Ikke planlagt.  
3. Klikk Planlegg helt utligningstre.
    * Dette vil planlegge alle Kanban-jobber i utligningstreet, og endre jobbstatusen fra Ikke planlagt til Planlagt.  
4. Oppdater siden.
    * Legg merke til at Kanban-jobbstatusen endres fra Ikke planlagt til Planlagt.  
5. Velg Salgslinje 000832 \ Kanban 000558\ Problem for L0001\ Kanban 000559 i treet.
    * Jobben for den andre Kanbanen planlegges også fordi hele utligningstreet planlegges. Legg merke til at Kanban-jobbstatusen endres fra Ikke planlagt til Planlagt.  

