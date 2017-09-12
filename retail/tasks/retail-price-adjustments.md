--- 
title: " Prisjusteringer for detaljhandel"
description: Denne prosedyren viser hvordan du oppretter en utsalgsprisjustering.
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dab14468713f9f23d20e7ca648711e2a4337cf7c
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="retail-price-adjustments"></a><span data-ttu-id="1dead-103"> Prisjusteringer for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="1dead-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1dead-104">Denne prosedyren viser hvordan du oppretter en utsalgsprisjustering.</span><span class="sxs-lookup"><span data-stu-id="1dead-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="1dead-105">En utsalgsprisjustering kan angi varens salgspris direkte eller endre basissalgsprisen eller avtalesalgsprisen.</span><span class="sxs-lookup"><span data-stu-id="1dead-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="1dead-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="1dead-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="1dead-107">Klikk Prisings- og rabattstyring.</span><span class="sxs-lookup"><span data-stu-id="1dead-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="1dead-108">Klikk kategorien Prisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="1dead-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="1dead-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1dead-109">Click New.</span></span>
    * <span data-ttu-id="1dead-110">Herfra kan du opprette alle de vanligste prisings- og rabattreglene, inkludert detaljhandelsrabatter, prisjusteringer, journaler for forretningsavtale og kategoriprisregler.</span><span class="sxs-lookup"><span data-stu-id="1dead-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="1dead-111">Klikk Prisjustering.</span><span class="sxs-lookup"><span data-stu-id="1dead-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="1dead-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="1dead-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="1dead-113">Vis Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="1dead-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="1dead-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="1dead-114">Click Add.</span></span>
    * <span data-ttu-id="1dead-115">I dette eksemplet angir du 81126 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="1dead-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="1dead-116">Deretter angir du 10,0 i Rabattprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="1dead-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="1dead-117">En prisjustering av typen rabattprosent reduserer basissalgsprisen eller avtalesalgsprisen.</span><span class="sxs-lookup"><span data-stu-id="1dead-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="1dead-118">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="1dead-118">Click Add.</span></span>
    * <span data-ttu-id="1dead-119">I dette eksemplet angir du 81125 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="1dead-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="1dead-120">Velg deretter Kontantrabattbeløp i feltet Rabattmetode.</span><span class="sxs-lookup"><span data-stu-id="1dead-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="1dead-121">Angi til slutt 5,0 i feltet Kontantrabattbeløp.</span><span class="sxs-lookup"><span data-stu-id="1dead-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="1dead-122">En rabattype av typen kontantrabatt er et beløp som trekkes fra en basispris eller en forretningsavtalepris.</span><span class="sxs-lookup"><span data-stu-id="1dead-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="1dead-123">Klikk Prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="1dead-123">Click Price groups.</span></span>
    * <span data-ttu-id="1dead-124">Velg RP-Houston i Prisgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="1dead-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="1dead-125">Dette vil knytte prisjusteringen til Houston-butikken.</span><span class="sxs-lookup"><span data-stu-id="1dead-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="1dead-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="1dead-126">Click Save.</span></span>
11. <span data-ttu-id="1dead-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1dead-127">Close the page.</span></span>
12. <span data-ttu-id="1dead-128">Velg Aktivert i Status-feltet.</span><span class="sxs-lookup"><span data-stu-id="1dead-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="1dead-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="1dead-129">Click Save.</span></span>
14. <span data-ttu-id="1dead-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1dead-130">Close the page.</span></span>
15. <span data-ttu-id="1dead-131">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="1dead-131">Refresh the page.</span></span>


