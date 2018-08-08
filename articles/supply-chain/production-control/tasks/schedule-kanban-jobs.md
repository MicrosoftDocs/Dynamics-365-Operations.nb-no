--- 
title: Planlegge Kanban-jobber
description: "Denne prosedyren fokuserer på planlegging av kanban-prosessjobber for en bestemt arbeidscelle."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f36544993a9280ae10489a19252bc105abd40ac9
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-kanban-jobs"></a>Planlegge Kanban-jobber

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på planlegging av kanban-prosessjobber for en bestemt arbeidscelle. Fremgangsmåten "Klargjøre en kanban-prosessjobb når materialer ikke er tilgjengelige" er en forutsetning for oppretting av denne fremgangsmåten. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne oppgaven er ment for arbeidsledere og produksjonsplanleggere som arbeider med Kanbaner.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Velge kanban-jobber for en arbeidscelle
1. Gå til Produksjonskontroll > Kanban > Kanban-jobbplanlegging.
2. Vis faktaboksen Periodekapasitet.
    * Vis faktaboksen Kanban.  
3. Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.
4. Merk den valgte raden i listen.
    * Velg arbeidscellen 1250. Dette filtrerer visningen slik at bare jobbene for arbeidscellen 1250 vises.  
5. Klikk koblingen i den valgte raden i listen.
6. Klikk Velg.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Planlegge en kanban-jobb i den første tilgjengelige perioden
1. Merk den valgte raden i listen.
    * Velg den første raden i listen som har Ikke planlagt-status. Det prikkede ikonet i Jobbstatus-feltet angir ikke planlagt.  
2. Klikk Tidsplan.
    * Dette vil planlegg kanban-jobben i den første tilgjengelige perioden.  
    * Legg merke til at kanban-jobben er flyttet til slutten av listen fordi den er lagt til i perioden fra dagens dato.  
    * Hvis perioden fra dagens dato er opptatt, flyttes jobben til den første tilgjengelige perioden.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Planlegge to kanban-jobber for en bestemt dag
1. Velg rad 1 i listen.
    * Du skal se at den første raden har Ikke planlagt-statusen i jobbstatus-feltet.  
2. Velg rad 2 i listen.
    * Du skal se at den andre raden har Ikke planlagt-statusen i jobbstatus-feltet. Nå har du valgt de to første jobbene.  
3. Klikk Planlegg fra dato for å åpne nedtrekksdialogen.
4. Merk av eller fjern merket for Overstyr reaksjon på kapasitetsmangel.
    * Med dette alternativet kan du overstyre standardreaksjonen på kapasitetsmangel.  
5. Velg Legg til i den ønskede perioden i feltet Reaksjon på kapasitetsmangel.
    * Dette alternativet sikrer at jobben er lagt til den ønskede perioden, uansett om arbeidscellen kan være overbelastet.  
6. Klikk Tidsplan.
    * Legg merke til at begge jobber er lagt til den ønskede perioden.  
    * I delen Periodisk kapasitet kan du se belastningen for hver periode. Forbruk-feltet viser det planlagte forbruket i denne perioden. Hvis det planlagte forbruket er høyere enn den tilgjengelige kapasiteten i denne perioden, vil det overbelastede forbruket velges.  


