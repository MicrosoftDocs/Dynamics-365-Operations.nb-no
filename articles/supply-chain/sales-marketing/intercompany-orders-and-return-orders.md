---
title: Konserninterne ordrer og returordrer
description: Dette emnet forklarer konserninterne ordrer og returordrer
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
ms.openlocfilehash: 1c22c021adce5f892ccb6c2ff8735f9e647e8b81
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671849"
---
# <a name="intercompany-orders-and-return-orders"></a>Konserninterne ordrer og returordrer

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan konserninterne bestillinger, salgsordrer, returordrer, innkjøpsavtaler og salgsavtaler opprettes og oppdateres.

## <a name="about-intercompany-orders"></a>Konserninterne ordrer

Når du oppretter en konsernintern salgsordre, oppretter Microsoft Dynamics 365 Supply Chain Management automatisk en tilsvarende bestilling. Det motsatte skjer også, det vil si at når du oppretter en konsernintern bestilling, utløses en automatisk opprettelse av en tilsvarende konsernintern salgsordre.

Dette gjelder ordrer som har to parter (transaksjoner mellom to relaterte firmaer) og for de fleste ordrer som har tre parter (når en konsernintern transaksjon har sin opprinnelse i en salgsordre for en ekstern kunde).

## <a name="intercompany-order-example"></a>Eksempel på konsernintern ordre

Du har to relaterte firmaer. Firma A er et datterselskap som driver med salg, og firma B er en distribusjonsenhet. Konserninterne salgsordrer og bestillinger opprettes automatisk i følgende scenarier:

- Når firma A oppretter en bestilling og leverandøren er firma B, opprettes en konsernintern salgsordre automatisk hos firma B. Ordrekjeden med to parter består av en bestilling hos firma A og en konsernintern salgsordre hos firma B.
- Når firma B oppretter en salgsordre og kunden er firma A, opprettes en konsernintern kjøpsordre automatisk hos firma A. Ordrekjeden med to parter består av en salgsordre hos firma B og en konsernintern kjøpsordre hos firma A.
- Når firma A først oppretter en salgsordre for en ekstern kunde, kan en bestilling opprettes automatisk hos firma A. Dette utløser i neste omgang en automatisk opprettelse av en konsernintern salgsordre hos firma B. Ordrekjeden med tre parter består av en salgsordre og en bestilling hos firma A, og en konsernintern salgsordre hos firma B.

## <a name="about-intercompany-return-orders"></a>Konserninterne returordrer

Du kan returnere konserninterne varer på en måte som har mye til felles med vanlige returer. Forskjellen er at med konserninterne varer oppretter returordren fra en ekstern kunde en konsernintern bestilling. Dette fører i sin tur til automatisk oppretting av en konsernintern salgsreturordre. Du kan også returnere en konsernintern vare uten en returordre fra en ekstern kunde.

På samme måte som vanlige returordrer, startes konserninterne returordrer på siden **Opprett returordre**.

I Microsoft Dynamics 365 Supply Chain Management oppdateres konserninterne salgs- og kjøpsavtaler automatisk for å gjenspeile en returnert vare. Salget eller kjøpsavtaleforpliktelsen for denne varen justeres automatisk for å gjenspeile endringen i antallet eller beløpet når en vare returneres.

## <a name="intercompany-return-order-example"></a>Eksempel på konsernintern returordre

Firma A oppretter en bestilling som er knyttet til en kjøpsavtale for en konsernintern vare. En konsernintern salgsordre opprettes automatisk i firma B som er knyttet til den tilsvarende salgsavtalen. Kjøpsavtalen og salgsavtalen er relatert som konserninterne avtaler.

Firma A returnerer den konserninterne varen til firma B. Firma B oppretter en returordre for varen, og en innkjøpsreturordre opprettes automatisk i firma A. Forpliktelsene i kjøpsavtalen og salgsavtalen som er knyttet til de opprinnelige ordrene, justeres automatisk for å gjenspeile endringen i antall eller beløp.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
