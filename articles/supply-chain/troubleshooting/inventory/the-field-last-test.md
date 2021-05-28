---
title: Sist testet dato-feltet oppdateres ikke når flere kvalitetsordrer opprettes
description: Sist testet dato-feltet oppdateres ikke når flere kvalitetsordrer opprettes.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026790"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="6ce82-103">Sist testet dato-feltet oppdateres ikke når flere kvalitetsordrer opprettes</span><span class="sxs-lookup"><span data-stu-id="6ce82-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="6ce82-104">KB-nummer: 4612803</span><span class="sxs-lookup"><span data-stu-id="6ce82-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="6ce82-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="6ce82-105">Symptoms</span></span>

<span data-ttu-id="6ce82-106">**Sist testet dato**-feltet oppdateres ikke når flere kvalitetsordrer opprettes.</span><span class="sxs-lookup"><span data-stu-id="6ce82-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="6ce82-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="6ce82-107">Resolution</span></span>

<span data-ttu-id="6ce82-108">Systemet fungerer som tiltenkt.</span><span class="sxs-lookup"><span data-stu-id="6ce82-108">The system is behaving as designed.</span></span> <span data-ttu-id="6ce82-109">Sist testet dato er ikke knyttet til kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="6ce82-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="6ce82-110">Den lagrer datoen da de ferdige varene først ble kjøpt eller produsert.</span><span class="sxs-lookup"><span data-stu-id="6ce82-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="6ce82-111">Denne datoen brukes til å beregne den anbefalte holdbarhetsdatoen.</span><span class="sxs-lookup"><span data-stu-id="6ce82-111">This date is used to calculate the shelf life advice date.</span></span>
