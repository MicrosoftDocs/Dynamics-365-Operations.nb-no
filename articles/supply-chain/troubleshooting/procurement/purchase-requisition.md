---
title: Du kan ikke legge til en linje i en innkjøpsrekvisisjon etter at du har bedt om en endring
description: Systemet tillater ikke at du legget til en linje i en innkjøpsrekvisisjon etter at du har bedt om en endring.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchReqTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: jeyao
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5dbb55a6a352a7acf16729c1cfe1afdac2e2eef8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026784"
---
# <a name="you-cant-add-a-line-to-a-purchase-requisition-after-you-request-a-change"></a>Du kan ikke legge til en linje i en innkjøpsrekvisisjon etter at du har bedt om en endring

KB-nummer: 4611211

## <a name="symptoms"></a>Symptomer

Systemet tillater ikke at du legget til en linje i en innkjøpsrekvisisjon etter at du har bedt om en endring.

## <a name="resolution"></a>Oppløsning

Du må tilbakekalle arbeidsflyten. Når innkjøpsrekvisisjonen har status *Utkast*, kan du fortsette å redigere den eller legge til en linje i den.
