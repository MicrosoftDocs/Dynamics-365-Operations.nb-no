---
title: Når et faktisk vekt-antall deles, brukes minimumsantallet i stedet for pålydende antall
description: Når et faktisk vekt-antall blir delt inn i partier, bruker Plukkvantitet-feltet det minste antallet som er angitt for varen, ikke det pålydende antallet.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026788"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="f409f-103">Når et faktisk vekt-antall deles, brukes minimumsantallet i stedet for pålydende antall</span><span class="sxs-lookup"><span data-stu-id="f409f-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="f409f-104">KB-nummer: 4612073</span><span class="sxs-lookup"><span data-stu-id="f409f-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="f409f-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="f409f-105">Symptoms</span></span>

<span data-ttu-id="f409f-106">Når et faktisk vekt-antall blir delt inn i partier, bruker **Plukkvantitet**-feltet det minste antallet som er angitt for varen, ikke det pålydende antallet.</span><span class="sxs-lookup"><span data-stu-id="f409f-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="f409f-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="f409f-107">Resolution</span></span>

<span data-ttu-id="f409f-108">Systemet fungerer som tiltenkt.</span><span class="sxs-lookup"><span data-stu-id="f409f-108">The system is behaving as designed.</span></span> <span data-ttu-id="f409f-109">Systemet bruker minimumsoppsettet for vare til plukking.</span><span class="sxs-lookup"><span data-stu-id="f409f-109">The system uses each item's minimum quantity setup for picking.</span></span>
