---
title: Utføre fakturaoppdateringer for returer
description: Denne funksjonaliteten i støtter forretningsprosessene i organisasjoner som velger å fakturere returordrer og salgsordrer samtidig og utført av samme person.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 736496a0499e70987f80f3d4687414371606cd8c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578758"
---
# <a name="perform-invoice-updates-for-returns"></a>Utføre fakturaoppdateringer for returer 

[!include [banner](../includes/banner.md)]


En returordre er en type salgsordre som er merket som en returordre. Derfor brukes listesiden **Alle salgsordrer** til å generere fakturaer for returordrer i stedet for skjemaet **Returordrer**. Denne funksjonaliteten i støtter forretningsprosessene i organisasjoner som velger å fakturere returordrer og salgsordrer samtidig og utført av samme person.

Fordi fakturaen for en returnert vare er for et negativt beløp, kalles en kreditnota.

Når du setter opp fakturaoppdateringen for satsvis behandling, må salgsordren av typen **Returordre** ha returlinjestatusen **Mottatt**, som viser at ordrens følgeseddel er oppdatert.

## <a name="post-an-invoice-for-a-return-order"></a>Postere en faktura for en returordre

1.  Klikk på **Kunder** \> **Felles** \> **Salgsordrer** \> **Alle salgsordrer**.

2.  Velg en salgsordre som **Returordre** vises for i **Ordretype**-feltet.

3.  I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen klikker du **Faktura**.

4.  På **Parametere**-fanen merker du av for **Postering**.

5.  Gå gjennom informasjonen i skjemaet, og gjør eventuelle nødvendige endringer.

6.  Klikk på **OK**. Kreditnotaen er postert.

## <a name="see-also"></a>Se også

[Følgesedddeloppdateringer for returer](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]