--- 
title: Konfigurere standardkostnader for arbeid og utgifter
description: Denne prosedyren viser hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 432b5b195b29fb03786cb0560e277735b531b7d7
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="4167f-103">Konfigurere standardkostnader for arbeid og utgifter</span><span class="sxs-lookup"><span data-stu-id="4167f-103">Configure standard costs for labor and expenses</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4167f-104">Denne prosedyren viser hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4167f-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="4167f-105">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="4167f-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4167f-106">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time).</span><span class="sxs-lookup"><span data-stu-id="4167f-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="4167f-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4167f-107">Click New.</span></span>
3. <span data-ttu-id="4167f-108">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="4167f-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="4167f-109">Angi et tall i Kostpris-feltet.</span><span class="sxs-lookup"><span data-stu-id="4167f-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="4167f-110">Du kan definere en standard kostpris for prosjektkategorien, eller du kan definere kostpriser etter arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="4167f-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="4167f-111">Den faktiske kostprisen som brukes, er kostprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="4167f-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="4167f-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4167f-112">Click Save.</span></span>
6. <span data-ttu-id="4167f-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4167f-113">Close the page.</span></span>
7. <span data-ttu-id="4167f-114">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time).</span><span class="sxs-lookup"><span data-stu-id="4167f-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="4167f-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4167f-115">Click New.</span></span>
9. <span data-ttu-id="4167f-116">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="4167f-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="4167f-117">Velg et alternativ i feltet Gjelder for.</span><span class="sxs-lookup"><span data-stu-id="4167f-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="4167f-118">Angi et tall i Prissetting-feltet.</span><span class="sxs-lookup"><span data-stu-id="4167f-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="4167f-119">Du kan definere en standard salgspris for timetransaksjoner eller for en prosjektkategori.</span><span class="sxs-lookup"><span data-stu-id="4167f-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="4167f-120">Alternativt kan du definere salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="4167f-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="4167f-121">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="4167f-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4167f-122">Hvis det for eksempel defineres både en generell salgspris og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="4167f-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="4167f-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4167f-123">Click Save.</span></span>
13. <span data-ttu-id="4167f-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4167f-124">Close the page.</span></span>
14. <span data-ttu-id="4167f-125">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift).</span><span class="sxs-lookup"><span data-stu-id="4167f-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="4167f-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4167f-126">Click New.</span></span>
16. <span data-ttu-id="4167f-127">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="4167f-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="4167f-128">Angi et tall i Kostpris-feltet.</span><span class="sxs-lookup"><span data-stu-id="4167f-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="4167f-129">Flere felt kan fylles ut, men dette er det minste antallet som kreves for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="4167f-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="4167f-130">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4167f-130">Click Save.</span></span>
19. <span data-ttu-id="4167f-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4167f-131">Close the page.</span></span>
20. <span data-ttu-id="4167f-132">Gå til Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (utgift).</span><span class="sxs-lookup"><span data-stu-id="4167f-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="4167f-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4167f-133">Click New.</span></span>
22. <span data-ttu-id="4167f-134">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="4167f-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="4167f-135">Velg et alternativ i feltet Gjelder for.</span><span class="sxs-lookup"><span data-stu-id="4167f-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="4167f-136">Angi et tall i Prissetting-feltet.</span><span class="sxs-lookup"><span data-stu-id="4167f-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="4167f-137">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i en utgiftsjournal, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="4167f-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4167f-138">Hvis det for eksempel defineres både en generell og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="4167f-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="4167f-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4167f-139">Click Save.</span></span>


