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
ms.openlocfilehash: 48dd5c3a878efb7413f461e76fde086030015b60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146681"
---
# <a name="update-kanban-status"></a>Oppdatere Kanban-status

[!include [banner](../../includes/banner.md)]

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

