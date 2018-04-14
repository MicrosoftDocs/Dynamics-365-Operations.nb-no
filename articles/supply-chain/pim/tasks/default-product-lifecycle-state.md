--- 
title: Opprette en standard livssyklustilstand for produkt
description: "Denne fremgangsmåten beskriver hvordan du oppretter en standard produktlivssyklustilstand samt hvordan du knytter standardtilstanden til frigitte produkter."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 099adbbb9cdb32e0db2daf13f83dc748b09fc61c
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="47857-103">Opprette en standard livssyklustilstand for produkt</span><span class="sxs-lookup"><span data-stu-id="47857-103">Create a default product lifecycle state</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47857-104">Denne fremgangsmåten beskriver hvordan du oppretter en standard produktlivssyklustilstand samt hvordan du knytter standardtilstanden til frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="47857-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="47857-105">Opprette en standard livssyklustilstand</span><span class="sxs-lookup"><span data-stu-id="47857-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="47857-106">Gå til Behandling av produktinformasjon > Oppsett > Livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="47857-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="47857-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="47857-107">Click New.</span></span>
3. <span data-ttu-id="47857-108">Skriv inn en verdi i feltet Tilstand.</span><span class="sxs-lookup"><span data-stu-id="47857-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="47857-109">Velg Ja i Standard når frigitt til juridisk enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="47857-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="47857-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="47857-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="47857-111">Velg Nei i Er aktiv for planlegging-feltet.</span><span class="sxs-lookup"><span data-stu-id="47857-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="47857-112">Hvis et nytt frigitt produkt ikke skal inkluderes i Hovedplanlegging, velger du Nei.</span><span class="sxs-lookup"><span data-stu-id="47857-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="47857-113">Hvis det skal være med i Hovedplanlegging, lar du kontrollen ha standardverdien Ja.</span><span class="sxs-lookup"><span data-stu-id="47857-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="47857-114">Opprette et nytt frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="47857-114">Create a new released product</span></span>
1. <span data-ttu-id="47857-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="47857-115">Close the page.</span></span>
2. <span data-ttu-id="47857-116">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="47857-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="47857-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="47857-117">Click New.</span></span>
4. <span data-ttu-id="47857-118">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="47857-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="47857-119">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="47857-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="47857-120">Skriv inn en verdi i Søkenavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="47857-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="47857-121">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="47857-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="47857-122">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="47857-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="47857-123">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="47857-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="47857-124">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="47857-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="47857-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="47857-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="47857-126">Standard produktlivssyklustilstand er en global definisjon.</span><span class="sxs-lookup"><span data-stu-id="47857-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="47857-127">Endre produktet til en aktiv tilstand</span><span class="sxs-lookup"><span data-stu-id="47857-127">Change the product to an active state</span></span>
1. <span data-ttu-id="47857-128">Angi eller velg en verdi i feltet Livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="47857-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="47857-129">Anta at du har definert en aktiv tilstand og at du nå kan velge den aktive tilstanden slik at produktet kan brukes i Hovedplanlegging og stykklistenivåberegningen.</span><span class="sxs-lookup"><span data-stu-id="47857-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="47857-130">Åpenbart så gir dette bare mening hvis alle produktdetaljene som kreves for konsekvent planlegging, er angitt.</span><span class="sxs-lookup"><span data-stu-id="47857-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  


