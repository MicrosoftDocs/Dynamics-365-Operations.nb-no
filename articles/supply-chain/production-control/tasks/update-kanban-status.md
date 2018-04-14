--- 
title: Oppdatere Kanban-status
description: "Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.openlocfilehash: 3c2b5a5fbfc5bd83cc68ffafaa243dac9244c003
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="update-kanban-status"></a>Oppdatere Kanban-status

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


