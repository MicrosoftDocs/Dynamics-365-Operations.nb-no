---
title: Akkumulering av kunderabatter mislykkes når varerabattgrupper brukes
description: Når du bruker kunderabattavtaler sammen med varerabattgrupper, beregnes rabatter, men akkumulering mislykkes.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026769"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="aa2a9-103">Akkumulering av kunderabatter mislykkes når varerabattgrupper brukes</span><span class="sxs-lookup"><span data-stu-id="aa2a9-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="aa2a9-104">KB-nummer: 4611372</span><span class="sxs-lookup"><span data-stu-id="aa2a9-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="aa2a9-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="aa2a9-105">Symptoms</span></span>

<span data-ttu-id="aa2a9-106">Når du bruker kunderabattavtaler (av *beløp*-typen) sammen med varerabattgrupper, beregnes rabatter, men akkumulering mislykkes.</span><span class="sxs-lookup"><span data-stu-id="aa2a9-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="aa2a9-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="aa2a9-107">Resolution</span></span>

<span data-ttu-id="aa2a9-108">Systemet fungerer som tiltenkt.</span><span class="sxs-lookup"><span data-stu-id="aa2a9-108">The system is behaving as designed.</span></span> <span data-ttu-id="aa2a9-109">Varegrupper grupperer bare varer som har samme terskelbetingelse.</span><span class="sxs-lookup"><span data-stu-id="aa2a9-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="aa2a9-110">Rabattbetingelsen (terskel) angis mot beløpet for hver vare, ikke mot det akkumulerte beløpet for en vare i varegruppen.</span><span class="sxs-lookup"><span data-stu-id="aa2a9-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
