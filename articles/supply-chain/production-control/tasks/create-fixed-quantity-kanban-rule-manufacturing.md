---
title: Opprette en Kanban-regel med fast antall for produksjon
description: Denne prosedyren fokuserer på oppsettet som kreves for å opprette en Kanban-regel for fast produksjon for utløsing av transformasjonsaktiviteter, på en arbeidscelle, i et lean-miljø.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a2edce5ac4506dead8d150e9f332e00817f35ce7a16910d30b9c77203518b07
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775561"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Opprette en Kanban-regel med fast antall for produksjon

[!include [banner](../../includes/banner.md)]

Denne prosedyren fokuserer på oppsettet som kreves for å opprette en Kanban-regel for fast produksjon for utløsing av transformasjonsaktiviteter, på en arbeidscelle, i et lean-miljø. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt.


## <a name="create-new-kanban-rule"></a>Opprette ny Kanban-regel
1. Gå til Kanban-regler.
2. Klikk på Ny.
    * Legg merke til at standardtype er Produksjon, og etterfyllingsstrategi er Fast. Du trenger ikke å endre disse parameterne.  
3. Angi eller velg en verdi i feltet Første planaktivitet.
    * Dette er aktiviteten som skal utføres for Kanbaner opprettet basert på denne kanban-regelen.  Velg "SpeakerTestAndPackaging".  
4. Vis delen Detaljer.
5. Angi eller velg en verdi i feltet Produkt.
    * Velg L0050.  
6. I Måleenhet-feltet angir eller velger du en verdi.
    * Velg minutter.  
7. Angi et tall i feltet Leveringstid.
    * Angi 5.  

## <a name="set-quantities"></a>Angi antall
1. Utvid delen Antall.
2. Angi Standardantall som 10.
    * Dette er antallet som skal overføres til hver kanban.  
3. Merk av for Produktantallsavvik.
    * Med dette kan valgte Kanbaner fullføres med et avvik fra standardantallet.  For å tillate Kanbaner å fullføres med et antall fra 8 til 12, setter du begge avvik til 2.  
4. Sett Avvik under til 2.
    * Dette tillater fullføring ned til 10 - 2 = 8  
5. Sett Avvik over til 2.
    * Dette tillater fullføring opp til 10 + 2 = 12  
6. Angi et nummer i feltet Fast Kanban-antall.
    * Dette er antall Kanbaner som skal være aktive. I dette tilfellet 5 Kanbaner som hver behandler 10.  
7. Angi 2 i feltet Nedre varslingsgrense.
    * Brukes til å holde oversikt over minimumsbeløpet for alle Kanbaner som skal være på målet. Dette brukes for eksempel brukes i oversikten over kanban-antall.  
8. Angi 4 i feltet Øvre varslingsgrense.
    * Brukes til å holde oversikt over maksimumsbeløpet for alle Kanbaner som skal være på målet. Dette brukes for eksempel brukes i oversikten over kanban-antall.  
9. Angi 1 feltet Antall for automatisk planlegging.
    * Hvis du setter dette til 1, betyr det at hver kanban planlegges på nytt automatisk.   Hvis vi angir 3, vil ikke Kanbanene planlegges før 3 tomme Kanbaner er klar til planlegging. Dette er nyttig for å gruppere arbeidet og unngå for mange oppsett.  

## <a name="create-kanbans"></a>Opprette Kanbaner
1. Vis delen Kanbaner.
2. Klikk på Lagre.
    * Kanban-regelen må lagres før du kan opprette Kanbaner.  
3. Klikk på Legg til.
    * Legg merke til at det ikke finnes noen aktive Kanbaner, og på grunn av dette er det foreslåtte "antallet nye Kanbaner" 5. Dette er lik "Fast Kanban-antall".  
4. Klikk på Opprett.
    * Dette vil opprette 5 Kanbaner.  
    * Legg merke til at 5 Kanbaner, hver for 10, ble opprettet for denne kanban-regel for produksjon. Dette er det siste trinnet i prosedyren.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]