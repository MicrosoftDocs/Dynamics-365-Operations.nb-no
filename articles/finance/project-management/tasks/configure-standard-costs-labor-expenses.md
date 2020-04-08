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
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140099"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="e5180-103">Konfigurere standardkostnader for arbeid og utgifter</span><span class="sxs-lookup"><span data-stu-id="e5180-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5180-104">Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="e5180-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="e5180-105">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="e5180-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e5180-106">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time)**.</span><span class="sxs-lookup"><span data-stu-id="e5180-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="e5180-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5180-107">Select **New**.</span></span>
3. <span data-ttu-id="e5180-108">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="e5180-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="e5180-109">Angi et tall i **Kostpris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e5180-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="e5180-110">Du kan definere en standard kostpris for prosjektkategorien, eller du kan definere kostpriser etter arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="e5180-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="e5180-111">Den faktiske kostprisen som brukes, er kostprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="e5180-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="e5180-112">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e5180-112">Select **Save**.</span></span>
6. <span data-ttu-id="e5180-113">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time)**.</span><span class="sxs-lookup"><span data-stu-id="e5180-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="e5180-114">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5180-114">Select **New**.</span></span>
8. <span data-ttu-id="e5180-115">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="e5180-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="e5180-116">Velg et alternativ i feltet **Gjelder for**.</span><span class="sxs-lookup"><span data-stu-id="e5180-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="e5180-117">Angi et tall i **Prissetting**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e5180-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="e5180-118">Du kan definere en standard salgspris for timetransaksjoner eller for en prosjektkategori.</span><span class="sxs-lookup"><span data-stu-id="e5180-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="e5180-119">Alternativt kan du definere salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="e5180-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="e5180-120">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="e5180-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e5180-121">Hvis det for eksempel defineres både en generell salgspris og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="e5180-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="e5180-122">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e5180-122">Select **Save**.</span></span>
12. <span data-ttu-id="e5180-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e5180-123">Close the page.</span></span>
13. <span data-ttu-id="e5180-124">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="e5180-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="e5180-125">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5180-125">Select **New**.</span></span>
15. <span data-ttu-id="e5180-126">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="e5180-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="e5180-127">Angi et tall i **Kostpris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e5180-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="e5180-128">Flere felt kan fylles ut, men dette er det minste antallet som kreves for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="e5180-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="e5180-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e5180-129">Select **Save**.</span></span>
18. <span data-ttu-id="e5180-130">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="e5180-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="e5180-131">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5180-131">Select **New**.</span></span>
20. <span data-ttu-id="e5180-132">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="e5180-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="e5180-133">Velg et alternativ i feltet **Gjelder for**.</span><span class="sxs-lookup"><span data-stu-id="e5180-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="e5180-134">Angi et tall i **Prissetting**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e5180-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="e5180-135">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i en utgiftsjournal, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="e5180-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e5180-136">Hvis det for eksempel defineres både en generell og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="e5180-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="e5180-137">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e5180-137">Select **Save**.</span></span>

