---
title: Varen kan ikke ha en stykkliste eller formel
description: Når du prøver å autorisere en ordre, får du en feilmelding under varevalidering. Den angir at varen ikke kan ha en stykkliste eller formel.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294146"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="eee3f-104">Varen kan ikke ha en stykkliste eller formel</span><span class="sxs-lookup"><span data-stu-id="eee3f-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="eee3f-105">Feilkode: PRO2614</span><span class="sxs-lookup"><span data-stu-id="eee3f-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="eee3f-106">Symptomer</span><span class="sxs-lookup"><span data-stu-id="eee3f-106">Symptoms</span></span>

<span data-ttu-id="eee3f-107">Når du prøver å autorisere en ordre, får du følgende feilmelding under varevalidering:</span><span class="sxs-lookup"><span data-stu-id="eee3f-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="eee3f-108">Varen kan ikke ha en stykkliste eller formel</span><span class="sxs-lookup"><span data-stu-id="eee3f-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="eee3f-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="eee3f-109">Resolution</span></span>

<span data-ttu-id="eee3f-110">Varer som har en stykkliste eller formel, må være av typen *Planleggingselement*, *Stykkliste* eller *formel*.</span><span class="sxs-lookup"><span data-stu-id="eee3f-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="eee3f-111">Hvis du vil endre typen for en vare, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="eee3f-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="eee3f-112">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="eee3f-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="eee3f-113">Åpne det relevante produktet.</span><span class="sxs-lookup"><span data-stu-id="eee3f-113">Open the relevant product.</span></span>
1. <span data-ttu-id="eee3f-114">I hurtigfanen **Utvikle** setter du feltet **Produksjonstype** til *Planleggingselement*, *BOM* eller *formel*.</span><span class="sxs-lookup"><span data-stu-id="eee3f-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
