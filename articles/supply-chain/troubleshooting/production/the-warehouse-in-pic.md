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
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026770"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Lageret i plukklistejournalen oppdateres ikke på en stykklistelinje

KB-nummer: 4614848

## <a name="symptoms"></a>Symptomer

Lageret i plukklistejournalen oppdateres ikke på en stykklistelinje.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt. Hvis det blir opprettet en journallinje for en plukkliste som har en referanse (via parti-IDen) til en produksjonsstykklistelinje, blir ikke lageret på produksjonsstykklistelinjen oppdatert hvis lagerdimensjonen på linjen i plukklistejournalen endres senere.
