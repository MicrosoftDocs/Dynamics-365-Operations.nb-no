---
title: Konfigurere standardkostnader for arbeid og utgifter
description: Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867732"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="3658c-103">Konfigurere standardkostnader for arbeid og utgifter</span><span class="sxs-lookup"><span data-stu-id="3658c-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3658c-104">Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3658c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="3658c-105">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="3658c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="3658c-106">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time)**.</span><span class="sxs-lookup"><span data-stu-id="3658c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="3658c-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3658c-107">Select **New**.</span></span>
3. <span data-ttu-id="3658c-108">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="3658c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="3658c-109">Angi et tall i **Kostpris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3658c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="3658c-110">Du kan definere en standard kostpris for prosjektkategorien, eller du kan definere kostpriser etter arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="3658c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="3658c-111">Den faktiske kostprisen som brukes, er kostprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="3658c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="3658c-112">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3658c-112">Select **Save**.</span></span>
6. <span data-ttu-id="3658c-113">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time)**.</span><span class="sxs-lookup"><span data-stu-id="3658c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="3658c-114">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3658c-114">Select **New**.</span></span>
8. <span data-ttu-id="3658c-115">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="3658c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="3658c-116">Velg et alternativ i feltet **Gjelder for**.</span><span class="sxs-lookup"><span data-stu-id="3658c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="3658c-117">Angi et tall i **Prissetting**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3658c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="3658c-118">Du kan definere en standard salgspris for timetransaksjoner eller for en prosjektkategori.</span><span class="sxs-lookup"><span data-stu-id="3658c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="3658c-119">Alternativt kan du definere salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="3658c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="3658c-120">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="3658c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="3658c-121">Hvis det for eksempel defineres både en generell salgspris og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="3658c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="3658c-122">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3658c-122">Select **Save**.</span></span>
12. <span data-ttu-id="3658c-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3658c-123">Close the page.</span></span>
13. <span data-ttu-id="3658c-124">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="3658c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="3658c-125">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3658c-125">Select **New**.</span></span>
15. <span data-ttu-id="3658c-126">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="3658c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="3658c-127">Angi et tall i **Kostpris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3658c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="3658c-128">Flere felt kan fylles ut, men dette er det minste antallet som kreves for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="3658c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="3658c-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3658c-129">Select **Save**.</span></span>
18. <span data-ttu-id="3658c-130">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="3658c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="3658c-131">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3658c-131">Select **New**.</span></span>
20. <span data-ttu-id="3658c-132">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="3658c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="3658c-133">Velg et alternativ i feltet **Gjelder for**.</span><span class="sxs-lookup"><span data-stu-id="3658c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="3658c-134">Angi et tall i **Prissetting**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3658c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="3658c-135">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i en utgiftsjournal, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="3658c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="3658c-136">Hvis det for eksempel defineres både en generell og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="3658c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="3658c-137">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3658c-137">Select **Save**.</span></span>

