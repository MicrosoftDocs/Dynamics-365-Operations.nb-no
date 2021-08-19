---
title: Oppdatere Kanban-status
description: Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 741a2a29e6b222c722e94db4e07dee6c8f4014030364753e3352fa30594dac0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715680"
---
# <a name="update-kanban-status"></a>Oppdatere Kanban-status

[!include [banner](../../includes/banner.md)]

Når en kanban tømmes ved en feiltakelse eller en mottatt kanban må tømmes, må du oppdatere kanban-statusen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for verkstedslederen.


## <a name="find-the-kanban"></a>Finn kanbanen.
1. Gå til Produksjonskontroll > Kanban > Kanbaner.
2. Åpne kolonnefilteret Status for håndteringsenhet.
3. Klikk på Fjern.
    * Dette tilbakestiller filtrene.  
4. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Kortnummer-feltet med verdien 000149.

## <a name="change-emptied-status-to-received-status"></a>Endre tømtstatus til mottattstatus
1. Klikk på Reverser tom håndteringsenhet.
2. Klikk på OK.
    * Legg merke til at statusen Håndteringsenhet er Mottatt.  

## <a name="change-received-status-to-emptied-status"></a>Endre mottattstatus til tømtstatus
1. Klikk på Tøm Kanban.
2. Merk den valgte raden i listen.
    * Legg merke til at statusen Håndteringsenhet er Tømt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]