--- 
title: Opprette en Kanban-regel for uttak
description: "Denne fremgangsmåten viser oppsettet som kreves for å opprette en kanban-regel for uttak for overføring av materialer i en lean-miljø."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02c7133d2e02b27fb428874deeda21e2bab28fb6
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a>Opprette en Kanban-regel for uttak

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser oppsettet som kreves for å opprette en kanban-regel for uttak for overføring av materialer i en lean-miljø. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for prosessingeniøren eller verdistrømlederen, når de klargjør etterfylling av et nytt eller endret materiale.


## <a name="create-new-kanban-rule"></a>Opprette ny Kanban-regel
1. Gå til Kanban-regler.
2. Klikk Ny.
3. Velg Uttak i Type-feltet.
    * Typen Uttak brukes for kanban-regler for å overføre materialer eller varer.  
4. Angi eller velg en verdi i feltet Første planaktivitet.
    * Velg ReplenishSpeakerComponents.   Denne aktiviteten er konfigurert til å flytte komponenter fra lager 11, lokasjon 11 til lager 12 og lokasjon 12.  
5. Angi eller velg en verdi i feltet Produkt.
    * Velg M0007.  
6. Angi et tall i feltet Leveringstid.
    * For eksempel 60.  
7. I Måleenhet-feltet angir eller velger du en verdi.
    * For eksempel Minutter.  

## <a name="set-quantities-for-kanban"></a>Angi antall for Kanban
1. Angi Standardantall som 5.
    * Dette er antallet som skal overføres til hver kanban.  
2. Angi 2 i feltet Fast Kanban-antall.
    * Dette er antall Kanbaner som skal være aktive. I dette tilfellet overfører 2 Kanbaner 5 hver.  
3. Angi 1 i feltet Nedre varslingsgrense.
    * Brukes til å holde oversikt over minimumsbeløpet for alle Kanbaner som skal være på målet. Dette brukes for eksempel brukes i oversikten over kanban-antall.  
4. Angi 2 i feltet Øvre varslingsgrense.
    * Brukes til å holde oversikt over maksimumsbeløpet for alle Kanbaner som skal være på målet. Dette brukes for eksempel brukes i oversikten over kanban-antall.  

## <a name="create-kanbans"></a>Opprett Kanbaner
1. Klikk Lagre.
    * Kanban-regelen må lagres før du kan opprette Kanbaner.  
2. Klikk Legg til.
    * Legg merke til at det ikke finnes noen aktive Kanbaner fordi foreslått antall nye Kanban er 2, og dette er lik Fast Kanban-antall.  
3. Klikk Opprett.
    * Dette vil opprette to Kanbaner.  
    * Legg merke til at 2 Kanbaner, for 5 hver, ble opprettet for denne kanban-regelen for uttak.  Dette er det siste trinnet i prosedyren.  


