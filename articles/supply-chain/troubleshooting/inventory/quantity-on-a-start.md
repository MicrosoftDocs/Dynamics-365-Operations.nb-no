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
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="ad8b2-103">Antallet i en startet karanteneordre oppdateres ikke når ordren deles</span><span class="sxs-lookup"><span data-stu-id="ad8b2-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="ad8b2-104">KB-nummer: 4613113</span><span class="sxs-lookup"><span data-stu-id="ad8b2-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="ad8b2-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="ad8b2-105">Symptoms</span></span>

<span data-ttu-id="ad8b2-106">Når du oppretter en karanteneordre og prøver å dele den, oppdateres ikke ordreantallet til restantallet etter delingen.</span><span class="sxs-lookup"><span data-stu-id="ad8b2-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="ad8b2-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="ad8b2-107">Resolution</span></span>

<span data-ttu-id="ad8b2-108">Systemet endrer ikke det opprinnelige antallet fra en karanteneordre, for å sikre at du kan spore det opprinnelige antallet som ble opprettet for karanteneordren.</span><span class="sxs-lookup"><span data-stu-id="ad8b2-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="ad8b2-109">Systemet sporer imidlertid antallet som deles fra en karanteneordre.</span><span class="sxs-lookup"><span data-stu-id="ad8b2-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="ad8b2-110">For å gjøre denne sporingen bruker det et databasefelt med navnet `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span><span class="sxs-lookup"><span data-stu-id="ad8b2-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="ad8b2-111">Dette feltet er imidlertid ikke synlig i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="ad8b2-111">However, this field isn't visible in the user interface (UI).</span></span>
