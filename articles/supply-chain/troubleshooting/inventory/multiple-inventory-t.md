---
title: Flere lagertransaksjoner for partinumre når Ved fysisk oppdatering er deaktivert
description: Det opprettes flere lagertransaksjoner etter at du har justert en bestillingslinje for varer der alternativet Ved fysisk oppdatering for partinummergruppen er satt til Nei.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026793"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="ea31f-103">Flere lagertransaksjoner for partinumre når Ved fysisk oppdatering er deaktivert</span><span class="sxs-lookup"><span data-stu-id="ea31f-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="ea31f-104">KB-nummer: 4613390</span><span class="sxs-lookup"><span data-stu-id="ea31f-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="ea31f-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="ea31f-105">Symptoms</span></span>

<span data-ttu-id="ea31f-106">Det opprettes flere lagertransaksjoner etter at du har justert en bestillingslinje for varer der alternativet **Ved fysisk oppdatering** for partinummergruppen er satt til *Nei*.</span><span class="sxs-lookup"><span data-stu-id="ea31f-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="ea31f-107">Når du oppretter en vare der alternativet **Ved fysisk oppdatering** for partinummergruppen er satt til *Nei*, oppretter systemet automatisk et nytt partinummer hvis du endrer et innkjøpslinjeantall og lagrer bestillingssiden.</span><span class="sxs-lookup"><span data-stu-id="ea31f-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="ea31f-108">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="ea31f-108">Resolution</span></span>

<span data-ttu-id="ea31f-109">Innstillingen **Ved fysisk oppdatering** for partinummergrupper fungerer på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="ea31f-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="ea31f-110">Når alternativet er satt til *Ja*, opprettes det bare nye partinumre etter en fysisk oppdatering (for eksempel når varer sendes eller mottas).</span><span class="sxs-lookup"><span data-stu-id="ea31f-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="ea31f-111">Når alternativet er satt til *Nei*, opprettes det et nytt partinummer hver gang det foretas en gjeldende oppdatering (for eksempel når et nytt antall legges til i en bestilling).</span><span class="sxs-lookup"><span data-stu-id="ea31f-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
