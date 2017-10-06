--- 
title: "Overføre materialer med Kanban-jobber (bare februar 2016)"
description: "Denne prosedyren fokuserer på å utføre en kanban-jobb for uttak for å overføre materialer."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
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
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 72403aa502cadf2a727bdd67ad8cd612dafd502b
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a>Overføre materialer med Kanban-jobber (bare februar 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på å utføre en kanban-jobb for uttak for å overføre materialer. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for Lagermedarbeideren.


## <a name="display-transfer-jobs"></a>Vis overføringsjobber
1. Gå til Produksjonskontroll > Kanban > Kanban-tavle for overføringsjobber.
2. Vis eller skjul delen Filtre.
    * I delen Filtre, kan du angi hvilke jobber som du vil se ved å filtrere etter produksjonsflyten, Aktivitetsnavn, fra lageret og lokasjonen, og til lager og lokasjon.  
3. Skriv inn 11 i Fra lager-feltet.
4. Skriv inn 12 i Til lokasjon-feltet.

## <a name="start-a-transfer-job"></a>Start en overføringsjobb
1. I listen, fjerner du merket for den merkede raden - hvis det finnes.
2. Velg rad 4 i listen.
    * Velg den første jobben med statusen Ikke planlagt. Kontroller at dette er den eneste jobben som er valgt.  
3. Klikk Start.
    * Legg merke til at et ikon angir at jobben er startet.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Velg en annen overføringsjobb og endre antallet
1. Finn og velg ønsket post i listen.
    * Du kan har flere jobber som er valgt, men denne gangen velger du rad 5.  
2. Finn og velg ønsket post i listen.
    * Kontroller at jobben i det forrige trinnet, er den eneste som er valgt. Fjern merket for alle andre jobber.  
3. Merk deg verdien i Jobbantall-feltet for senere bruk
4. Sett Jobbantall til 30.
    * Legg merke til advarselen. Du kan ikke overføre 30. Du kan bare overføre det opprinnelige antallet i henhold til oppsettet for kanban-regelen.  
5. Bruk verdien du merket deg tidligere i Jobbantall-feltet
    * Sett jobbantallet til den forrige verdien.  

## <a name="start-the-second-transfer-job"></a>Start den andre overføringsjobben
1. Klikk Start.
    * Dette vil starte overføringen av jobben i rad 5.  

## <a name="complete-both-transfer-jobs"></a>Fullfør begge overføringsjobbene
1. Velg rad 4 i listen.
    * Nå er to overføringsjobber valgt i rad 4 og rad 5.  
2. Klikk Fullført.
    * Dette vil fullføre overføringen av begge jobber.  

