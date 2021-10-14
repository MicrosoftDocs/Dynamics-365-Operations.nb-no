---
title: Konserninterne valutaomregninger
description: Dette emnet forklarer valutaomregninger for konserninterne transaksjoner
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548456"
---
# <a name="intercompany-currency-conversions"></a>Konserninterne valutaomregninger

[!include [banner](../../includes/banner.md)]

Når valutakoden i den opprinnelige salgsordren og i den konserninterne bestillingen er forskjellig, blir valutaene i følgende felt regnet om hvis synkronisering er aktivert:

- **Enhetspris**
- **Salgsgebyrer** eller **Innkjøpstillegg**
- **Rabatt**
- **Samkjøpsrabatt**

Disse feltene synkroniseres deretter med den konserninterne salgsordrelinjen.

Fordi valutaen i den konserninterne bestillingen og den konserninterne salgsordren alltid synkroniseres, vil imidlertid følgende felt synkroniseres uten valutaomregning:

- **Enhetspris**
- **Salgsgebyrer** eller **Innkjøpstillegg**
- **Rabatt**
- **Rabattprosent**
- **Samkjøpsrabatt**
- **Samkjøpsrabatt i prosent**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
