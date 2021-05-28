---
title: Antallet i en startet karanteneordre oppdateres ikke når ordren deles
description: Når du oppretter en karanteneordre og prøver å dele den, oppdateres ikke ordreantallet som er oppdatert til det delte restantallet.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026792"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Antallet i en startet karanteneordre oppdateres ikke når ordren deles

KB-nummer: 4613113

## <a name="symptoms"></a>Symptomer

Når du oppretter en karanteneordre og prøver å dele den, oppdateres ikke ordreantallet til restantallet etter delingen.

## <a name="resolution"></a>Oppløsning

Systemet endrer ikke det opprinnelige antallet fra en karanteneordre, for å sikre at du kan spore det opprinnelige antallet som ble opprettet for karanteneordren. Systemet sporer imidlertid antallet som deles fra en karanteneordre. For å gjøre denne sporingen bruker det et databasefelt med navnet `QuantityThatHasSplitIntoOtherQuarantineOrders`. Dette feltet er imidlertid ikke synlig i brukergrensesnittet.
