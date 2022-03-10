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
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713500"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Antallet i en startet karanteneordre oppdateres ikke når ordren deles

KB-nummer: 4613113

## <a name="symptoms"></a>Symptomer

Når du oppretter en karanteneordre og prøver å dele den, oppdateres ikke ordreantallet til restantallet etter delingen.

## <a name="resolution"></a>Oppløsning

Systemet endrer ikke det opprinnelige antallet fra en karanteneordre, for å sikre at du kan spore det opprinnelige antallet som ble opprettet for karanteneordren. Systemet sporer imidlertid antallet som deles fra en karanteneordre. For å gjøre denne sporingen bruker det et databasefelt med navnet `QuantityThatHasSplitIntoOtherQuarantineOrders`. Dette feltet er imidlertid ikke synlig i brukergrensesnittet.
