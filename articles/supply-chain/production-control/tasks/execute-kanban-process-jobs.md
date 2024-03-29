---
title: Kjøre Kanban-prosessjobber
description: Denne prosedyren fokuserer på utfører Kanban-prosessjobber.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ac6f0f6139fe17532f6fbd996b314e0b14f3d90
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566585"
---
# <a name="execute-kanban-process-jobs"></a>Kjøre Kanban-prosessjobber

[!include [banner](../../includes/banner.md)]

Denne prosedyren fokuserer på utfører Kanban-prosessjobber. Den første jobben fullføres med det forventede antallet og har ingen feil. Den andre jobben fullføres med feil. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren er ment for maskinoperatøren.


## <a name="select-a-kanban-job"></a>Merke en Kanban-jobb
1. Gå til Produksjonskontroll > Kanban > Kanban-tavle for prosessjobber.
2. Klikk på rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.
3. Klikk på raden med ressursgruppe 1250. Dette filtrerer jobblisten slik at bare jobbene for arbeidscelle 1250 vises.
    * Merke raden som har jobbstatusen Planlagt.  

## <a name="complete-a-job-with-expected-quantity"></a>Fullføre en jobb med forventet antall
1. Vis eller skjul delen Detaljer.
    * Denne delen viser viktig informasjon om kortnummer, varenummer, antall bestilt og aktivitetsnavn.  
2. Vis eller skjul delen Produksjonsinstruksjoner.
    * Denne delen viser produksjonsinstruksjoner for aktiviteten. Instruksjonene kan være tekst, bilder, tegninger og andre dokumenter.  
3. Klikk på Start.
    * Velg en jobb som ikke er fullført. Bruk statusikoner i statusfeltet for jobben for å vise jobbstatus.      
4. Klikk på Fullført.
    * Jobben er fullført med den forventede kvaliteten.  

## <a name="complete-a-job-with-errors"></a>Fullføre en jobb med feil
1. Klikk på Start.
    * Når en jobb er fullført, velges den neste jobben i listen automatisk. Dette er grunnen til at du ikke trenger å velge en jobb før du klikker Start.  
2. Klikk på Produksjon i handlingsruten.
3. Klikk på Fullfør (detaljer).
4. Merk den valgte raden i listen.
5. Angi et tall i Antall feil-feltet.
6. Angi et tall i feltet Antall korrekte-antall.
7. Klikk på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]