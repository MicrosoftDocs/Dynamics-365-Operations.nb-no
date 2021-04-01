---
title: " Prisjusteringer for detaljhandel"
description: Denne prosedyren viser hvordan du oppretter en prisjustering i Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbd2f818930424313e1d76aea4a257efa7c7b3be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232791"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="5a117-103"> Prisjusteringer for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="5a117-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a117-104">Denne prosedyren viser hvordan du oppretter en prisjustering i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5a117-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="5a117-105">En prisjustering kan angi varens salgspris direkte eller endre basissalgsprisen eller avtalesalgsprisen.</span><span class="sxs-lookup"><span data-stu-id="5a117-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="5a117-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="5a117-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="5a117-107">Klikk Prisings- og rabattstyring.</span><span class="sxs-lookup"><span data-stu-id="5a117-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="5a117-108">Klikk kategorien Prisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="5a117-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="5a117-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5a117-109">Click New.</span></span>
    * <span data-ttu-id="5a117-110">Herfra kan du opprette alle de vanligste prisings- og rabattreglene, inkludert rabatter, prisjusteringer, journaler for forretningsavtale og kategoriprisregler.</span><span class="sxs-lookup"><span data-stu-id="5a117-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="5a117-111">Klikk Prisjustering.</span><span class="sxs-lookup"><span data-stu-id="5a117-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="5a117-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a117-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="5a117-113">Vis Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="5a117-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="5a117-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="5a117-114">Click Add.</span></span>
    * <span data-ttu-id="5a117-115">I dette eksemplet angir du 81126 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a117-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="5a117-116">Deretter angir du 10,0 i Rabattprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a117-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="5a117-117">En prisjustering av typen rabattprosent reduserer basissalgsprisen eller avtalesalgsprisen.</span><span class="sxs-lookup"><span data-stu-id="5a117-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="5a117-118">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="5a117-118">Click Add.</span></span>
    * <span data-ttu-id="5a117-119">I dette eksemplet angir du 81125 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a117-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="5a117-120">Velg deretter Kontantrabattbeløp i feltet Rabattmetode.</span><span class="sxs-lookup"><span data-stu-id="5a117-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="5a117-121">Angi til slutt 5,0 i feltet Kontantrabattbeløp.</span><span class="sxs-lookup"><span data-stu-id="5a117-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="5a117-122">En rabattype av typen kontantrabatt er et beløp som trekkes fra en basispris eller en forretningsavtalepris.</span><span class="sxs-lookup"><span data-stu-id="5a117-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="5a117-123">Klikk Prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="5a117-123">Click Price groups.</span></span>
    * <span data-ttu-id="5a117-124">Velg RP-Houston i Prisgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a117-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="5a117-125">Dette vil knytte prisjusteringen til Houston-butikken.</span><span class="sxs-lookup"><span data-stu-id="5a117-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="5a117-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5a117-126">Click Save.</span></span>
11. <span data-ttu-id="5a117-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5a117-127">Close the page.</span></span>
12. <span data-ttu-id="5a117-128">Velg Aktivert i Status-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a117-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="5a117-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5a117-129">Click Save.</span></span>
14. <span data-ttu-id="5a117-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5a117-130">Close the page.</span></span>
15. <span data-ttu-id="5a117-131">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="5a117-131">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]