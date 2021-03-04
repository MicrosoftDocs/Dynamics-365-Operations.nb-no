---
title: Klargjøre en Kanban-prosessjobb når materialer ikke er tilgjengelige for arbeidscellen
description: Denne prosedyren fokuserer på å klargjøre en kanban-prosessjobb når noen materialer ikke er tilgjengelige for arbeidscellen. Derfor er det nødvendig å plukker materialer fra lageret.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d57df6188aacc2f8a56a7ba91c4ab50a90901a7e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434105"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Klargjøre en Kanban-prosessjobb når materialer ikke er tilgjengelige for arbeidscellen

[!include [banner](../../includes/banner.md)]

Denne prosedyren fokuserer på å klargjøre en kanban-prosessjobb når noen materialer ikke er tilgjengelige for arbeidscellen. Derfor er det nødvendig å plukker materialer fra lageret. Fremgangsmåten "Klargjøre en kanban-prosessjobb når materialer er tilgjengelige" er en forutsetning for oppretting av denne fremgangsmåten. Denne prosedyren er ment for maskinoperatøren. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til Produksjonskontroll > Kanban > Kanban-tavle for prosessjobber.
2. Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.
3. Klikk koblingen i den valgte raden i listen.
    * Velg arbeidscellen 1250.  
4. Finn og velg ønsket post i listen.
    * Velg Kanban 000356.  
5. Finn og velg ønsket post i listen.
    * Opphev valget av rad 4 i listen. Velg eventuelt rad 4 hvis du ikke har fullført oppgaven "Klargjøre en kanban-prosessjobb når materialer er tilgjengelige."  
6. Aktiver/deaktiver utvidelsen av delen Plukkliste.
    * Ingen oppføring-ikonet i forsyningsstatusen angir at 48 stk. av vare P0002 mangler for arbeidscellen.  

## <a name="transfer-materials-to-work-cell"></a>Overføre materialer til arbeidscellen
1. Aktiver/deaktiver utvidelsen av delen Overføringsjobber.
2. Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P0002.
3. Finn og velg ønsket post i listen.
4. Klikk Start.
    * Overføring pågår.  
5. Klikk Fullført.
    * Vare P0002 er nå tilgjengelig i plukklisten for kanban-jobben. Dette betyr at vi kan forberede kanban med alle de nødvendige materialene.  
6. Klikk Klargjør.
    * Legg merke til at et ikon i jobbstatusen angir at jobben er klar.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]