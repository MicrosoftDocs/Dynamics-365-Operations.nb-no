---
title: Du kan ikke fakturere en kunderettet salgsordre
description: Du kan ikke lenger fakturere den opprinnelige salgsordren og den opprinnelige direkteleveringsbestillingen etter at du har aktivert alternativet Poster faktura automatisk.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026775"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Du kan ikke fakturere en kunderettet salgsordre

KB-nummer: 4611793

## <a name="symptoms"></a>Symptomer

Du kan ikke lenger fakturere den opprinnelige salgsordren og den opprinnelige direkteleveringsbestillingen etter at du har aktivert alternativet **Poster faktura automatisk** på siden **Konsernintern** for leverandøren.

## <a name="resolution"></a>Oppløsning

Synkroniseringsvirkemåten for konserninterne fakturaer og fakturaer for direkteleveringsordrer styres og tvinges av parameterne som er beskrevet i [Definere parametere for å postere en konsernintern ordre](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Når du har definert disse parameterne, må du fakturere den konserninterne salgsordren først. De opprinnelige salgsordrene og bestillingene vil deretter synkroniseres.
