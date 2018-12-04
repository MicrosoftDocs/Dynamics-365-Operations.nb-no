---
title: "Utføre fakturaoppdateringer for returer"
description: "Denne funksjonaliteten i støtter forretningsprosessene i organisasjoner som velger å fakturere returordrer og salgsordrer samtidig og utført av samme person."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 53ae1c3bda06d07a0ca633981ddd46092eae507e
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---


# <a name="perform-invoice-updates-for-returns"></a>Utføre fakturaoppdateringer for returer 

[!include [banner](../includes/banner.md)]


En returordre er en type salgsordre som er merket som en returordre. Derfor brukes listesiden **Alle salgsordrer** til å generere fakturaer for returordrer i stedet for skjemaet **Returordrer**. Denne funksjonaliteten i støtter forretningsprosessene i organisasjoner som velger å fakturere returordrer og salgsordrer samtidig og utført av samme person.

Fordi fakturaen for en returnert vare er for et negativt beløp, kalles en kreditnota.

Når du setter opp fakturaoppdateringen for satsvis behandling, må salgsordren av typen **Returordre** ha returlinjestatusen **Mottatt**, som viser at ordrens følgeseddel er oppdatert.

## <a name="post-an-invoice-for-a-return-order"></a>Postere en faktura for en returordre

1.  Klikk **Kunder** \> **Felles** \> **Salgsordrer** \> **Alle salgsordrer**.

2.  Velg en salgsordre som **Returordre** vises for i **Ordretype**-feltet.

3.  I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen klikker du **Faktura**.

4.  På **Parametere**-fanen merker du av for **Postering**.

5.  Gå gjennom informasjonen i skjemaet, og gjør eventuelle nødvendige endringer.

6.  Klikk **OK**. Kreditnotaen er postert.

## <a name="see-also"></a>Se også

[Følgesedddeloppdateringer for returer](packing-slip-updates-returns.md)

  



