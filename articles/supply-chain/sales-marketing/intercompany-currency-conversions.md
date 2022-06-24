---
title: Konserninterne valutaomregninger
description: Denne artikkelen forklarer valutaomregninger for konserninterne transaksjoner
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851485"
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
