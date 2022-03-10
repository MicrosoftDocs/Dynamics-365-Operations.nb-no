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
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756757"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Du kan ikke fakturere en kunderettet salgsordre

KB-nummer: 4611793

## <a name="symptoms"></a>Symptomer

Du kan ikke lenger fakturere den opprinnelige salgsordren og den opprinnelige direkteleveringsbestillingen etter at du har aktivert alternativet **Poster faktura automatisk** på siden **Konsernintern** for leverandøren.

## <a name="resolution"></a>Oppløsning

Synkroniseringsvirkemåten for konserninterne fakturaer og fakturaer for direkteleveringsordrer styres og tvinges av parameterne som er beskrevet i [Definere parametere for å postere en konsernintern ordre](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Når du har definert disse parameterne, må du fakturere den konserninterne salgsordren først. De opprinnelige salgsordrene og bestillingene vil deretter synkroniseres.
