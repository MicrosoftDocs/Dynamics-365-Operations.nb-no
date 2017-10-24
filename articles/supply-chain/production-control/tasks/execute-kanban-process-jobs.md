--- 
title: "Kjøre Kanban-prosessjobber"
description: "Denne prosedyren fokuserer på utfører Kanban-prosessjobber."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 752eab976f740606154d416678ba2381641697df
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="execute-kanban-process-jobs"></a>Kjøre Kanban-prosessjobber

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på utfører Kanban-prosessjobber. Den første jobben fullføres med det forventede antallet og har ingen feil. Den andre jobben fullføres med feil. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren er ment for maskinoperatøren.


## <a name="select-a-kanban-job"></a>Merke en Kanban-jobb
1. Gå til Produksjonskontroll > Kanban > Kanban-tavle for prosessjobber.
2. Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.
3. Klikk raden med ressursgruppe 1250. Dette filtrerer jobblisten slik at bare jobbene for arbeidscelle 1250 vises.
    * Merke raden som har jobbstatusen Planlagt.  

## <a name="complete-a-job-with-expected-quantity"></a>Fullføre en jobb med forventet antall
1. Vis eller skjul delen Detaljer.
    * Denne delen viser viktig informasjon om kortnummer, varenummer, antall bestilt og aktivitetsnavn.  
2. Vis eller skjul delen Produksjonsinstruksjoner.
    * Denne delen viser produksjonsinstruksjoner for aktiviteten. Instruksjonene kan være tekst, bilder, tegninger og andre dokumenter.  
3. Klikk Start.
    * Velg en jobb som ikke er fullført. Bruk statusikoner i statusfeltet for jobben for å vise jobbstatus.      
4. Klikk Fullført.
    * Jobben er fullført med den forventede kvaliteten.  

## <a name="complete-a-job-with-errors"></a>Fullføre en jobb med feil
1. Klikk Start.
    * Når en jobb er fullført, velges den neste jobben i listen automatisk. Dette er grunnen til at du ikke trenger å velge en jobb før du klikker Start.  
2. Klikk Produksjon i handlingsruten.
3. Klikk Fullfør (detaljer).
4. Merk den valgte raden i listen.
5. Angi et tall i Antall feil-feltet.
6. Angi et tall i feltet Antall korrekte-antall.
7. Klikk OK.


