---
title: " Kategoriprisregler for å opprette forretningsavtaler"
description: Denne prosedyren viser hvordan du oppretter salgsprisforretningsavtaler med en kategoriprisregel.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21b1986aa36aab23f50a5af434435f9e93318e45
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141089"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="d6618-103"> Kategoriprisregler for å opprette forretningsavtaler</span><span class="sxs-lookup"><span data-stu-id="d6618-103">Category pricing rules to create trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6618-104">Denne prosedyren viser hvordan du oppretter salgsprisforretningsavtaler med en kategoriprisregel.</span><span class="sxs-lookup"><span data-stu-id="d6618-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="d6618-105">Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="d6618-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="d6618-106">Denne oppgaven er ment for rollen Varehandelsleder for Commerce.</span><span class="sxs-lookup"><span data-stu-id="d6618-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="d6618-107">Klikk Prisings- og rabattstyring.</span><span class="sxs-lookup"><span data-stu-id="d6618-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="d6618-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d6618-108">Click New.</span></span>
3. <span data-ttu-id="d6618-109">Klikk Kategoriprisregel.</span><span class="sxs-lookup"><span data-stu-id="d6618-109">Click Category price rule.</span></span>
4. <span data-ttu-id="d6618-110">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d6618-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d6618-111">Velg et alternativ i Kontokode-feltet.</span><span class="sxs-lookup"><span data-stu-id="d6618-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="d6618-112">En kontokode av typen Gruppe brukes til å definere salgsprisforretningsavtaler som er spesifikke for kanaler, fordelsprogrammer, kataloger og tilknytninger.</span><span class="sxs-lookup"><span data-stu-id="d6618-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="d6618-113">Angi eller velg en verdi i Kontovalg-feltet.</span><span class="sxs-lookup"><span data-stu-id="d6618-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="d6618-114">Angi eller velg en verdi i Kategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="d6618-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="d6618-115">Angi en verdi i Beløp/prosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="d6618-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="d6618-116">Angi eller velg en verdi i Avrundingsversjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="d6618-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="d6618-117">Klikk Generer forretningsavtaler.</span><span class="sxs-lookup"><span data-stu-id="d6618-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="d6618-118">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d6618-118">Click Next.</span></span>
12. <span data-ttu-id="d6618-119">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="d6618-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="d6618-120">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="d6618-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="d6618-121">Velg Ja i feltet Søk etter neste.</span><span class="sxs-lookup"><span data-stu-id="d6618-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="d6618-122">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d6618-122">Click Next.</span></span>
16. <span data-ttu-id="d6618-123">Klikk Finish.</span><span class="sxs-lookup"><span data-stu-id="d6618-123">Click Finish.</span></span>
    * <span data-ttu-id="d6618-124">Dette oppretter en forretningsavtalejournal og åpner den for gjennomgang.</span><span class="sxs-lookup"><span data-stu-id="d6618-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="d6618-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d6618-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6618-126">Forretningsavtalejournaler som opprettes fra kategoriprisregler, posteres ikke.</span><span class="sxs-lookup"><span data-stu-id="d6618-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="d6618-127">Du kan se gjennom og redigere prisene som genereres, før de bokføres.</span><span class="sxs-lookup"><span data-stu-id="d6618-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="d6618-128">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="d6618-128">Click Edit.</span></span>
19. <span data-ttu-id="d6618-129">Angi en verdi i feltet Beløp i valuta.</span><span class="sxs-lookup"><span data-stu-id="d6618-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="d6618-130">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="d6618-130">Click Post.</span></span>
21. <span data-ttu-id="d6618-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="d6618-131">Click OK.</span></span>
22. <span data-ttu-id="d6618-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d6618-132">Close the page.</span></span>
23. <span data-ttu-id="d6618-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d6618-133">Close the page.</span></span>
24. <span data-ttu-id="d6618-134">Klikk kategorien Kategoriprisregler.</span><span class="sxs-lookup"><span data-stu-id="d6618-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="d6618-135">Kanalspesifikke kategoriprisregler vil vises i denne listen.</span><span class="sxs-lookup"><span data-stu-id="d6618-135">Channel specific Category pricing rules will show in this list.</span></span>  

