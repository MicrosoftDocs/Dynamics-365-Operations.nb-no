--- 
title: Tilbakestill Kanban-jobbstatus
description: "Denne prosedyren fokuserer på å tilbakestille en ugyldig Kanban-jobbstatus."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 00b6ae872e60a322c994420ab69236abef7fb312
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="revert-kanban-job-status"></a>Tilbakestill Kanban-jobbstatus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på å tilbakestille en ugyldig Kanban-jobbstatus. Dette er nyttig hvis maskinoperatøren oppdaterer feil jobb, eller angir feil status ved en feiltakelse. I denne prosedyren er Kanban-jobben registrert som klargjort ved et uhell, og statusen tilbakestilles. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren er ment for verkstedsleder eller maskinoperatør som arbeider i et lean manufacturing-firma.


## <a name="open-process-board-for-the-work-cell"></a>Åpne prosesstavlen for arbeidscellen
1. Gå til Kanban-tavle for prosessjobber.
2. Angi eller velg en verdi i Arbeidscelle-feltet.
    * Velg arbeidscellen 1260.  

## <a name="prepare-kanban-job"></a>Klargjør kanban-jobben
1. Klikk Klargjør.
    * Hvis du ikke kan klikke Klargjør fordi det er nedtonet, må du kontrollere at den valgte Kanban-jobben har statusen Planlagt, som er angitt av Tøm Kanban-ikonet. Hvis Klargjør mislykkes, må du kontrollere at alle materialene i plukklisten er tilgjengelige.  
2. Velg den klargjorte jobben i listen.
    * Velg den første jobben som du nettopp har klargjort.  
    * Legg merke til at jobbstatusen er klargjort, noe som angis med en trekant inni Kanban-ikonet.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Tilbakestill statusen for klargjorte Kanban-jobben
1. Merk den valgte raden i listen.
    * Velg den første jobben som ble klargjort.  
2. Klikk Produksjon i handlingsruten.
3. Klikk Tilbakestill status.
    * Du kan bruke en alternativ Kanban-regel når følgende betingelser er oppfylt: – Strategien for etterfylling er den samme for begge reglene.  - Versjonen for produksjonsflyten er den samme for begge reglene.  - Produktet som leveres, er det samme for begge reglene.  - Nedstrømsaktiviteter som konfigureres for den siste aktiviteten i Kanban-reglene, må være de samme for begge reglene.  - De samme lagerdimensjonene som er angitt, må konfigureres for begge reglene.  - Statusen for håndteringsenheten må være Ikke tilordnet.  - Konfigurasjonen for hendelses-Kanbaner må være den samme.  
    * Kontroller at den nye statusen er Planlagt.  
4. Klikk OK.
5. Fjern merket for den valgte raden i listen.
    * Velg den samme jobben.  
    * Legg merke til at jobbstatusen for Kanban-jobben tilbakestilles til Planlagt, som angis av Tøm Kanban-ikonet.  


