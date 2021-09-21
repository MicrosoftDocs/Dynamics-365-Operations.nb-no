---
title: Transaksjoner kan posteres til en suspendert finanskonto
description: Hvis en produktkvittering avlyses, tillater systemet at transaksjoner posteres til utestengte finanskontoer, selv om hovedkontoene er deaktivert
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477248"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Transaksjoner kan posteres til en suspendert finanskonto

## <a name="symptoms"></a>Symptomer

Hvis en produktkvittering avlyses, tillater systemet at transaksjoner posteres til utestengte finanskontoer, selv om hovedkontoene er deaktivert.

## <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. På siden for **Leverandørparametere**, i fanen **Generelt**, må du kontrollere at alternativet **Poster produktkvittering i finans** er satt til *Ja*.
1. Opprett en bestilling, og legg til en ordrelinje som har et antall på *1000* for et produkt.
1. Bekreft bestillingen.
1. Poster produktkvitteringen, og sjekk bilagene.
1. Stopp de aktuelle hovedkontoene, *200140* og *140200*.
1. Avbryt den posterte produktkvitteringen.
1. Legg merke til at transaksjoner kan posteres til de suspenderte finanskontoene.

## <a name="resolution"></a>Løsning

Transaksjoner kan posteres til de suspenderte finanskontoene når produktkvitteringer avbrytes, fordi denne virkemåten sørger for riktige posteringer.
