---
title: Endre Kanban-regler for en prosessjobb
description: Denne prosedyren fokuserer på å endre den brukte Kanban-regelen for en gitt Kanban.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4c8fd8251aca2cc53e59afe4c104f2e5198426
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434138"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Endre Kanban-regler for en prosessjobb

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]