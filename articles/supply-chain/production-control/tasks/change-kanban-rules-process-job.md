--- 
title: Endre Kanban-regler for en prosessjobb
description: "Denne prosedyren fokuserer på å endre den brukte Kanban-regelen for en gitt Kanban."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a>Endre Kanban-regler for en prosessjobb

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på å endre den brukte Kanban-regelen for en gitt Kanban. Dette er nyttig for å nivåbelaste ressurser eller ved nedbryting. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren er ment for planleggeren, som arbeider i et lean manufacturing-selskap, og som er ansvarlig for verdistrømmen.


## <a name="copy-kanban-rule"></a>Kopiere Kanban-regel
1. Gå til Kanban-regler.
2. Finn og velg ønsket post i listen.
    * Velg Kanban-regel for hendelse 000022 for L0001.  
3. Klikk Dupliser Kanban-regel.
4. Klikk OK.

## <a name="change-kanban-rule"></a>Endre Kanban-regel
1. Lukk siden.
2. Gå til Kanban-jobbplanlegging.
3. Merk den valgte raden i listen.
    * Velg linjen med Kanban 000177.  
4. Klikk Bruk alternativ Kanban-regel.
5. Klikk Neste.
6. Angi eller velg en verdi i feltet Kanban-regel.
    * Velg Kanban-regelen som ble opprettet tidligere. Dette er Kanban-regelen med det høyeste nummeret.  
7. Klikk Finish.
    * Kanban-jobben bruker nå en annen Kanban-regel. Dette kan være nyttig for å nivålaste arbeidsceller.  


