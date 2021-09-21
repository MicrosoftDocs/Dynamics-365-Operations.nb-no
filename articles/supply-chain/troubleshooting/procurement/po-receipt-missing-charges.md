---
title: En bestillingskvittering omfatter ikke alle gebyrer
description: En bestillingskvittering omfatter ikke alle gebyrer
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477158"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>En bestillingskvittering omfatter ikke alle gebyrer

## <a name="symptoms"></a>Symptomer

Når du mottar en bestilling, blir ikke alle tillegg tatt med i mottaket.

### <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. På siden for **Parametere for innkjøp og leverandører**, i fanen **Levering**, må du kontrollere at alternativet for **Generer tillegg på produktkvittering** er satt til *Ja*.
1. Opprette en bestilling som inkluderer tillegg.
1. Bekreft bestillingen.
1. Motta bestillingen.
1. Se på det kvitteringstotalen, og sammenlign den med forventet totalbeløp.
1. Legg merke til at ikke alle gebyrene er inkludert i bestillingskvitteringen.

## <a name="resolution"></a>Løsning

Oppløsningen avhenger av hvordan tilleggene er definert. Hvis du vil ha informasjon om hvordan du definerer tillegg for å oppfylle dine behov, kan du se følgende blogginnlegg: [Poster tilleggskostnader på tidspunktet for produktkvitteringen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
