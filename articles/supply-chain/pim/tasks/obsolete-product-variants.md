---
title: Finne utdaterte produktvarianter
description: Denne prosedyren viser hvordan du finner foreldede frigitte produkter og produktvarianter og hvordan du knytter en produktlivssyklustilstand til de foreldede produktene.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b212a6b4268776893d4e018cab605e6441080fa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986860"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="a9c8d-103">Finne utdaterte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="a9c8d-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9c8d-104">Denne prosedyren viser hvordan du finner foreldede frigitte produkter og produktvarianter og hvordan du knytter en produktlivssyklustilstand til de foreldede produktene.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="a9c8d-105">Forutsetning: Du må definere minst én produktlivssyklustilstand som er inaktiv for planlegging før du kan spille av denne oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="a9c8d-106">Kjøre en simulering</span><span class="sxs-lookup"><span data-stu-id="a9c8d-106">Run a simulation</span></span>
1. <span data-ttu-id="a9c8d-107">Gå til Behandling av produktinformasjon > Periodiske oppgaver > Endre livssyklustilstand for utdaterte produkter.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="a9c8d-108">Angi eller velg en verdi i feltet Ny livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="a9c8d-109">Velg Ja i Kjør simulering uten å oppdatere produktdata-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="a9c8d-110">Angi et tall i Utelat produkter som er opprettet innen dette antallet dager.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="a9c8d-111">Angi et tall i feltet Utelat produkter som brukes i transaksjoner (i antall dager).</span><span class="sxs-lookup"><span data-stu-id="a9c8d-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="a9c8d-112">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="a9c8d-113">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-113">Click Filter.</span></span>
8. <span data-ttu-id="a9c8d-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a9c8d-115">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="a9c8d-116">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-116">Click OK.</span></span>
11. <span data-ttu-id="a9c8d-117">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="a9c8d-118">Det anbefales å kjøre simuleringen satsvis hvis du forventer å søke etter et stort antall produkter.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="a9c8d-119">Kontroller også at simuleringen ikke kjøres i den mest aktive arbeidstiden i firmaet.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="a9c8d-120">Se gjennom simuleringsresultatene</span><span class="sxs-lookup"><span data-stu-id="a9c8d-120">Review the simulation results</span></span>
1. <span data-ttu-id="a9c8d-121">Gå til Behandling av produktinformasjon > Forespørsler og rapporter > Vedlikeholdshistorikk for livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="a9c8d-122">På denne siden kan du gå gjennom simuleringsresultatene og vurdere hvor mange produkter og produktvarianter som skal være tilknyttet en ny produktlivssyklustilstand når du kjører oppdateringen uten simulering.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="a9c8d-123">Kjøre oppdateringen av produktlivssyklustilstanden for utdaterte produkter</span><span class="sxs-lookup"><span data-stu-id="a9c8d-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="a9c8d-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-124">Close the page.</span></span>
2. <span data-ttu-id="a9c8d-125">Gå til Behandling av produktinformasjon > Periodiske oppgaver > Endre livssyklustilstand for utdaterte produkter.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="a9c8d-126">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="a9c8d-127">Legg merke til at det siste valget er lagret.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="a9c8d-128">Velg Nei i Kjør simulering uten å oppdatere produktdata-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="a9c8d-129">Utvid Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="a9c8d-130">Avhengig av hvor mange produkter og produktvarianter som berøres, bør du vurdere å kjøre denne jobben satsvis.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="a9c8d-131">Pass på at du ikke kjører en stor oppdateringsjobb i den mest aktive arbeidstiden i firmaet.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="a9c8d-132">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-132">Click OK.</span></span>
7. <span data-ttu-id="a9c8d-133">Gå til Behandling av produktinformasjon > Forespørsler og rapporter > Vedlikeholdshistorikk for livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="a9c8d-134">Se gjennom de endrede frigitte produktene og produktvariantene.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="a9c8d-135">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="a9c8d-135">In the list, find and select the desired record.</span></span>

