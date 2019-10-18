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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185411"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="b892e-103">Konfigurere standardkostnader for arbeid og utgifter</span><span class="sxs-lookup"><span data-stu-id="b892e-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b892e-104">Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="b892e-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="b892e-105">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="b892e-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b892e-106">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time)**.</span><span class="sxs-lookup"><span data-stu-id="b892e-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="b892e-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b892e-107">Select **New**.</span></span>
3. <span data-ttu-id="b892e-108">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="b892e-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="b892e-109">Angi et tall i **Kostpris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b892e-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="b892e-110">Du kan definere en standard kostpris for prosjektkategorien, eller du kan definere kostpriser etter arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="b892e-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="b892e-111">Den faktiske kostprisen som brukes, er kostprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="b892e-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="b892e-112">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b892e-112">Select **Save**.</span></span>
6. <span data-ttu-id="b892e-113">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time)**.</span><span class="sxs-lookup"><span data-stu-id="b892e-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="b892e-114">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b892e-114">Select **New**.</span></span>
8. <span data-ttu-id="b892e-115">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="b892e-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="b892e-116">Velg et alternativ i feltet **Gjelder for**.</span><span class="sxs-lookup"><span data-stu-id="b892e-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="b892e-117">Angi et tall i **Prissetting**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b892e-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="b892e-118">Du kan definere en standard salgspris for timetransaksjoner eller for en prosjektkategori.</span><span class="sxs-lookup"><span data-stu-id="b892e-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="b892e-119">Alternativt kan du definere salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="b892e-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="b892e-120">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="b892e-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b892e-121">Hvis det for eksempel defineres både en generell salgspris og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="b892e-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="b892e-122">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b892e-122">Select **Save**.</span></span>
12. <span data-ttu-id="b892e-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b892e-123">Close the page.</span></span>
13. <span data-ttu-id="b892e-124">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="b892e-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="b892e-125">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b892e-125">Select **New**.</span></span>
15. <span data-ttu-id="b892e-126">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="b892e-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="b892e-127">Angi et tall i **Kostpris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b892e-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="b892e-128">Flere felt kan fylles ut, men dette er det minste antallet som kreves for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="b892e-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="b892e-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b892e-129">Select **Save**.</span></span>
18. <span data-ttu-id="b892e-130">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="b892e-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="b892e-131">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b892e-131">Select **New**.</span></span>
20. <span data-ttu-id="b892e-132">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="b892e-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="b892e-133">Velg et alternativ i feltet **Gjelder for**.</span><span class="sxs-lookup"><span data-stu-id="b892e-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="b892e-134">Angi et tall i **Prissetting**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b892e-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="b892e-135">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i en utgiftsjournal, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="b892e-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b892e-136">Hvis det for eksempel defineres både en generell og en arbeiderspesifikk salgspris, bruker systemet den arbeiderspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="b892e-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="b892e-137">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b892e-137">Select **Save**.</span></span>

