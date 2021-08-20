---
title: Lageret i plukklistejournalen oppdateres ikke på en stykklistelinje.
description: Lageret i plukklistejournalen oppdateres ikke på en stykklistelinje.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740557"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Lageret i plukklistejournalen oppdateres ikke på en stykklistelinje

KB-nummer: 4614848

## <a name="symptoms"></a>Symptomer

Lageret i plukklistejournalen oppdateres ikke på en stykklistelinje.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt. Hvis det blir opprettet en journallinje for en plukkliste som har en referanse (via parti-IDen) til en produksjonsstykklistelinje, blir ikke lageret på produksjonsstykklistelinjen oppdatert hvis lagerdimensjonen på linjen i plukklistejournalen endres senere.
