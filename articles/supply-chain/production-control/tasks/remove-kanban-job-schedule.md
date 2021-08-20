---
title: Fjerne en Kanban-jobb fra tidsplanen
description: Denne prosedyren fokuserer på å fjerne en planlagt kanban-prosessjobb fra tidsplanen ved å tilbakestille jobbstatusen til Ikke planlagt.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eeedfad5f294f73097fc1b6a973d63125df72209227fc06470663665961af2d4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756925"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Fjerne en Kanban-jobb fra tidsplanen

[!include [banner](../../includes/banner.md)]

Denne prosedyren fokuserer på å fjerne en planlagt kanban-prosessjobb fra tidsplanen ved å tilbakestille jobbstatusen til Ikke planlagt. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren er ment for arbeidsledere eller produksjonsplanleggere.


## <a name="find-a-planned-kanban-job"></a>Finne en planlagt Kanban-jobb
1. Gå til Produksjonskontroll > Kanban > Kanban-jobbplanlegging.
2. Klikk på rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.
3. Klikk på koblingen i den valgte raden i listen.
    * Velg arbeidscellen 1250.  
4. Klikk på Velg.
5. I feltet Vis jobbstatus velger du "Planlagt".

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Fjerne den planlagte kanban-jobb fra tidsplanen
1. Finn og velg ønsket post i listen.
    * Velg en jobb med statusen planlagt, for eksempel en jobb fra 19. desember 2012.  
2. Klikk på Plan i handlingsruten.
3. Klikk på Tilbakestill jobbstatus.
4. Klikk på OK.
    * Dette vil tilbakestille den gjeldende jobbstatusen fra "Planlagt" til "Ikke planlagt" og fjerne den fra prosesstavlen.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]