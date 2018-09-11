--- 
title: Konfigurere standardkostnader for arbeid og utgifter
description: Denne prosedyren viser hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.
author: KimANelson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c0765d531a8d3be28f3bdf5392cdc45db13dd885
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="f6cc8-103">Konfigurere standardkostnader for arbeid og utgifter</span><span class="sxs-lookup"><span data-stu-id="f6cc8-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6cc8-104">Denne prosedyren viser hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="f6cc8-105">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f6cc8-106">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time).</span><span class="sxs-lookup"><span data-stu-id="f6cc8-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="f6cc8-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-107">Click New.</span></span>
3. <span data-ttu-id="f6cc8-108">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="f6cc8-109">Angi et tall i Kostpris-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="f6cc8-110">Du kan definere en standard kostpris for prosjektkategorien, eller du kan definere kostpriser etter arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="f6cc8-111">Den faktiske kostprisen som brukes, er kostprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="f6cc8-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-112">Click Save.</span></span>
6. <span data-ttu-id="f6cc8-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-113">Close the page.</span></span>
7. <span data-ttu-id="f6cc8-114">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time).</span><span class="sxs-lookup"><span data-stu-id="f6cc8-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="f6cc8-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-115">Click New.</span></span>
9. <span data-ttu-id="f6cc8-116">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="f6cc8-117">Velg et alternativ i feltet Gjelder for.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="f6cc8-118">Angi et tall i Prissetting-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="f6cc8-119">Du kan definere en standard salgspris for timetransaksjoner eller for en prosjektkategori.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="f6cc8-120">Alternativt kan du definere salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="f6cc8-121">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f6cc8-122">Hvis det for eksempel defineres både en generell salgspris og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="f6cc8-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-123">Click Save.</span></span>
13. <span data-ttu-id="f6cc8-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-124">Close the page.</span></span>
14. <span data-ttu-id="f6cc8-125">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift).</span><span class="sxs-lookup"><span data-stu-id="f6cc8-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="f6cc8-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-126">Click New.</span></span>
16. <span data-ttu-id="f6cc8-127">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="f6cc8-128">Angi et tall i Kostpris-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="f6cc8-129">Flere felt kan fylles ut, men dette er det minste antallet som kreves for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="f6cc8-130">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-130">Click Save.</span></span>
19. <span data-ttu-id="f6cc8-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-131">Close the page.</span></span>
20. <span data-ttu-id="f6cc8-132">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (utgift).</span><span class="sxs-lookup"><span data-stu-id="f6cc8-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="f6cc8-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-133">Click New.</span></span>
22. <span data-ttu-id="f6cc8-134">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="f6cc8-135">Velg et alternativ i feltet Gjelder for.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="f6cc8-136">Angi et tall i Prissetting-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="f6cc8-137">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i en utgiftsjournal, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f6cc8-138">Hvis det for eksempel defineres både en generell og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="f6cc8-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-139">Click Save.</span></span>


