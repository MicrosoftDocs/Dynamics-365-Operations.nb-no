---
title: Opprette en policy for opprullet kost
description: Denne prosedyren viser hvordan du oppretter en policy for opprullet kost og oppretter regler for policyen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d32cc2c1844c6c334dd00b249c736e153f13d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977653"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="c33e2-103">Opprette en policy for opprullet kost</span><span class="sxs-lookup"><span data-stu-id="c33e2-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c33e2-104">Denne prosedyren viser hvordan du oppretter en policy for opprullet kost og oppretter regler for policyen.</span><span class="sxs-lookup"><span data-stu-id="c33e2-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="c33e2-105">Demonstrasjonsdataene USP2 brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="c33e2-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="c33e2-106">Opprette en policy</span><span class="sxs-lookup"><span data-stu-id="c33e2-106">Create a policy</span></span>
1. <span data-ttu-id="c33e2-107">Gå til Kostnadsregnskap > Policyer > Policyer for opprullet kost.</span><span class="sxs-lookup"><span data-stu-id="c33e2-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="c33e2-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c33e2-108">Click New.</span></span>
3. <span data-ttu-id="c33e2-109">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="c33e2-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="c33e2-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c33e2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c33e2-111">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c33e2-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-112">Velg Opprullet kost CC.</span><span class="sxs-lookup"><span data-stu-id="c33e2-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="c33e2-113">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="c33e2-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-114">Velg Opprullet kost CC.</span><span class="sxs-lookup"><span data-stu-id="c33e2-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="c33e2-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c33e2-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="c33e2-116">Opprette regler for policyen for opprullet kostnad</span><span class="sxs-lookup"><span data-stu-id="c33e2-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="c33e2-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c33e2-117">Click New.</span></span>
2. <span data-ttu-id="c33e2-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c33e2-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c33e2-119">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c33e2-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-120">Velg 007.</span><span class="sxs-lookup"><span data-stu-id="c33e2-120">Select 007.</span></span>  
4. <span data-ttu-id="c33e2-121">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="c33e2-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-122">Velg Opprullet kost CE.</span><span class="sxs-lookup"><span data-stu-id="c33e2-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="c33e2-123">Angi eller velg en verdi i feltet Sekundært kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="c33e2-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-124">I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-007 til kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="c33e2-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="c33e2-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c33e2-125">Click New.</span></span>
7. <span data-ttu-id="c33e2-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c33e2-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c33e2-127">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c33e2-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-128">Velg 008.</span><span class="sxs-lookup"><span data-stu-id="c33e2-128">Select 008.</span></span>  
9. <span data-ttu-id="c33e2-129">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="c33e2-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-130">Velg Opprullet kost CE.</span><span class="sxs-lookup"><span data-stu-id="c33e2-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="c33e2-131">Angi eller velg en verdi i feltet Sekundært kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="c33e2-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-132">I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-008 til kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="c33e2-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="c33e2-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c33e2-133">Click New.</span></span>
12. <span data-ttu-id="c33e2-134">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c33e2-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c33e2-135">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c33e2-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-136">Velg 009.</span><span class="sxs-lookup"><span data-stu-id="c33e2-136">Select 009.</span></span>  
14. <span data-ttu-id="c33e2-137">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="c33e2-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-138">Velg Opprullet kost CE.</span><span class="sxs-lookup"><span data-stu-id="c33e2-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="c33e2-139">Angi eller velg en verdi i feltet Sekundært kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="c33e2-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="c33e2-140">I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-009 til kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="c33e2-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="c33e2-141">Fortsett til alle kostsentre er tilordnet de tilhørende sekundære kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="c33e2-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="c33e2-142">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c33e2-142">Click Save.</span></span>

