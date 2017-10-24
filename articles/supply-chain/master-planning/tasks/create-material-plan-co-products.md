--- 
title: Opprette en materialplan for koprodukter
description: Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="785f2-103">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="785f2-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="785f2-104">Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.</span><span class="sxs-lookup"><span data-stu-id="785f2-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="785f2-105">Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="785f2-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="785f2-106">Opprett behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="785f2-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="785f2-107">Gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="785f2-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="785f2-108">Klikk Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="785f2-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="785f2-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="785f2-109">Click New.</span></span>
4. <span data-ttu-id="785f2-110">Klikk Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="785f2-110">Click Sales order.</span></span>
5. <span data-ttu-id="785f2-111">Angi en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="785f2-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="785f2-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="785f2-112">Example: US-001</span></span>  
6. <span data-ttu-id="785f2-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="785f2-113">Click OK.</span></span>
7. <span data-ttu-id="785f2-114">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="785f2-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="785f2-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="785f2-115">Example: P6003</span></span>  
8. <span data-ttu-id="785f2-116">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="785f2-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="785f2-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="785f2-117">Example: 50000</span></span>  
9. <span data-ttu-id="785f2-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="785f2-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="785f2-119">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="785f2-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="785f2-120">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="785f2-120">Click Master planning.</span></span>
2. <span data-ttu-id="785f2-121">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="785f2-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="785f2-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="785f2-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="785f2-123">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="785f2-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="785f2-124">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="785f2-124">Click Run.</span></span>
5. <span data-ttu-id="785f2-125">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="785f2-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="785f2-126">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="785f2-126">Click Filter.</span></span>
7. <span data-ttu-id="785f2-127">I listen merker du raden for felt = varenummer.</span><span class="sxs-lookup"><span data-stu-id="785f2-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="785f2-128">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="785f2-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="785f2-129">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="785f2-129">Example: P6003</span></span>  
9. <span data-ttu-id="785f2-130">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="785f2-130">Click OK.</span></span>
10. <span data-ttu-id="785f2-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="785f2-131">Click OK.</span></span>
11. <span data-ttu-id="785f2-132">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="785f2-132">Click Planned orders.</span></span>
12. <span data-ttu-id="785f2-133">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="785f2-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="785f2-134">Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="785f2-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="785f2-135">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="785f2-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="785f2-136">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="785f2-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="785f2-137">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="785f2-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="785f2-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="785f2-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="785f2-139">Vis eller skjul delen Utligning.</span><span class="sxs-lookup"><span data-stu-id="785f2-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="785f2-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="785f2-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="785f2-141">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="785f2-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="785f2-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="785f2-142">Close the page.</span></span>


