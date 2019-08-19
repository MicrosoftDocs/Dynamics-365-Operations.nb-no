---
title: Oppdatere Kanban-status
description: Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97b6eea4e93967dbe1eea5eac9fe3fbf6b336a49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838469"
---
# <a name="update-kanban-status"></a>Oppdatere Kanban-status

[!include [task guide banner](../../includes/task-guide-banner.md)]

Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for verkstedslederen.


## <a name="find-the-kanban"></a>Finn kanbanen.
1. Gå til Produksjonskontroll > Kanban > Kanbaner.
2. Åpne kolonnefilteret Status for håndteringsenhet.
3. Klikk Fjern.
    * Dette tilbakestiller filtrene.  
4. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Kortnummer-feltet med verdien 000149.

## <a name="change-emptied-status-to-received-status"></a>Endre tømtstatus til mottattstatus
1. Klikk Reverser tom håndteringsenhet.
2. Klikk OK.
    * Legg merke til at statusen Håndteringsenhet er Mottatt.  

## <a name="change-received-status-to-emptied-status"></a>Endre mottattstatus til tømtstatus
1. Klikk Tøm Kanban.
2. Merk den valgte raden i listen.
    * Legg merke til at statusen Håndteringsenhet er Tømt.  

