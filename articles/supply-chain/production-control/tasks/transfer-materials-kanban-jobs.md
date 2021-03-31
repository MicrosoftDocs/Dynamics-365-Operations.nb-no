---
title: Overføre materialer med Kanban-jobber
description: Denne prosedyren fokuserer på å utføre en kanban-jobb for uttak for å overføre materialer.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df65ea59be29dbe4eaad30558fcff4394737158f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224936"
---
# <a name="transfer-materials-with-kanban-jobs"></a>Overføre materialer med Kanban-jobber

[!include [banner](../../includes/banner.md)]

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
3. Klikk på Start.
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
1. Klikk på Start.
    * Dette vil starte overføringen av jobben i rad 5.  

## <a name="complete-both-transfer-jobs"></a>Fullfør begge overføringsjobbene
1. Velg rad 4 i listen.
    * Nå er to overføringsjobber valgt i rad 4 og rad 5.  
2. Klikk på Fullført.
    * Dette vil fullføre overføringen av begge jobber.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]