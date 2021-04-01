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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6505d658103a4c34dfe7c7eb86ad4ea41515ccfb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261290"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="cbf58-103">Opprette en policy for opprullet kost</span><span class="sxs-lookup"><span data-stu-id="cbf58-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbf58-104">Denne prosedyren viser hvordan du oppretter en policy for opprullet kost og oppretter regler for policyen.</span><span class="sxs-lookup"><span data-stu-id="cbf58-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="cbf58-105">Demonstrasjonsdataene USP2 brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="cbf58-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="cbf58-106">Opprette en policy</span><span class="sxs-lookup"><span data-stu-id="cbf58-106">Create a policy</span></span>
1. <span data-ttu-id="cbf58-107">Gå til Kostnadsregnskap > Policyer > Policyer for opprullet kost.</span><span class="sxs-lookup"><span data-stu-id="cbf58-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="cbf58-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="cbf58-108">Click New.</span></span>
3. <span data-ttu-id="cbf58-109">Skriv inn en verdi i feltet Policynavn.</span><span class="sxs-lookup"><span data-stu-id="cbf58-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="cbf58-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="cbf58-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cbf58-111">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="cbf58-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-112">Velg Opprullet kost CC.</span><span class="sxs-lookup"><span data-stu-id="cbf58-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="cbf58-113">Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="cbf58-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-114">Velg Opprullet kost CC.</span><span class="sxs-lookup"><span data-stu-id="cbf58-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="cbf58-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="cbf58-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="cbf58-116">Opprette regler for policyen for opprullet kostnad</span><span class="sxs-lookup"><span data-stu-id="cbf58-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="cbf58-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="cbf58-117">Click New.</span></span>
2. <span data-ttu-id="cbf58-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cbf58-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="cbf58-119">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="cbf58-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-120">Velg 007.</span><span class="sxs-lookup"><span data-stu-id="cbf58-120">Select 007.</span></span>  
4. <span data-ttu-id="cbf58-121">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="cbf58-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-122">Velg Opprullet kost CE.</span><span class="sxs-lookup"><span data-stu-id="cbf58-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="cbf58-123">Angi eller velg en verdi i feltet Sekundært kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="cbf58-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-124">I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-007 til kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="cbf58-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="cbf58-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="cbf58-125">Click New.</span></span>
7. <span data-ttu-id="cbf58-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cbf58-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="cbf58-127">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="cbf58-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-128">Velg 008.</span><span class="sxs-lookup"><span data-stu-id="cbf58-128">Select 008.</span></span>  
9. <span data-ttu-id="cbf58-129">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="cbf58-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-130">Velg Opprullet kost CE.</span><span class="sxs-lookup"><span data-stu-id="cbf58-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="cbf58-131">Angi eller velg en verdi i feltet Sekundært kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="cbf58-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-132">I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-008 til kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="cbf58-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="cbf58-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="cbf58-133">Click New.</span></span>
12. <span data-ttu-id="cbf58-134">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cbf58-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="cbf58-135">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="cbf58-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-136">Velg 009.</span><span class="sxs-lookup"><span data-stu-id="cbf58-136">Select 009.</span></span>  
14. <span data-ttu-id="cbf58-137">Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="cbf58-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-138">Velg Opprullet kost CE.</span><span class="sxs-lookup"><span data-stu-id="cbf58-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="cbf58-139">Angi eller velg en verdi i feltet Sekundært kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="cbf58-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="cbf58-140">I dette eksemplet kan du tilordne det sekundære kostnadselementet CC-009 til kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="cbf58-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="cbf58-141">Fortsett til alle kostsentre er tilordnet de tilhørende sekundære kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="cbf58-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="cbf58-142">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="cbf58-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]