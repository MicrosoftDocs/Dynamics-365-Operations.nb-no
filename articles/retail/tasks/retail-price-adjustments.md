--- 
title: " Prisjusteringer for detaljhandel"
description: Denne prosedyren viser hvordan du oppretter en utsalgsprisjustering.
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: edfb9a1515f0af7d3272ea3fbb362bd0e6b0f129
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---
# <a name="retail-price-adjustments"></a><span data-ttu-id="0dbe2-103"> Prisjusteringer for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="0dbe2-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0dbe2-104">Denne prosedyren viser hvordan du oppretter en utsalgsprisjustering.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="0dbe2-105">En utsalgsprisjustering kan angi varens salgspris direkte eller endre basissalgsprisen eller avtalesalgsprisen.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="0dbe2-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="0dbe2-107">Klikk Prisings- og rabattstyring.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="0dbe2-108">Klikk kategorien Prisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="0dbe2-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-109">Click New.</span></span>
    * <span data-ttu-id="0dbe2-110">Herfra kan du opprette alle de vanligste prisings- og rabattreglene, inkludert detaljhandelsrabatter, prisjusteringer, journaler for forretningsavtale og kategoriprisregler.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="0dbe2-111">Klikk Prisjustering.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="0dbe2-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0dbe2-113">Vis Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="0dbe2-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-114">Click Add.</span></span>
    * <span data-ttu-id="0dbe2-115">I dette eksemplet angir du 81126 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="0dbe2-116">Deretter angir du 10,0 i Rabattprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="0dbe2-117">En prisjustering av typen rabattprosent reduserer basissalgsprisen eller avtalesalgsprisen.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="0dbe2-118">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-118">Click Add.</span></span>
    * <span data-ttu-id="0dbe2-119">I dette eksemplet angir du 81125 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="0dbe2-120">Velg deretter Kontantrabattbeløp i feltet Rabattmetode.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="0dbe2-121">Angi til slutt 5,0 i feltet Kontantrabattbeløp.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="0dbe2-122">En rabattype av typen kontantrabatt er et beløp som trekkes fra en basispris eller en forretningsavtalepris.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="0dbe2-123">Klikk Prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-123">Click Price groups.</span></span>
    * <span data-ttu-id="0dbe2-124">Velg RP-Houston i Prisgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="0dbe2-125">Dette vil knytte prisjusteringen til Houston-butikken.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="0dbe2-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-126">Click Save.</span></span>
11. <span data-ttu-id="0dbe2-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-127">Close the page.</span></span>
12. <span data-ttu-id="0dbe2-128">Velg Aktivert i Status-feltet.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="0dbe2-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-129">Click Save.</span></span>
14. <span data-ttu-id="0dbe2-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-130">Close the page.</span></span>
15. <span data-ttu-id="0dbe2-131">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="0dbe2-131">Refresh the page.</span></span>


