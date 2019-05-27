---
title: Opprette et hierarki for produktklassifisering
description: Denne fremgangsmåten viser hvordan du oppretter et nytt kategorihierarki og tilordner en varekodehierarkitype.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb49f5f3f8a5a788cb4c6d1be69534ba808e3675
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568426"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="2401c-103">Opprette et hierarki for produktklassifisering</span><span class="sxs-lookup"><span data-stu-id="2401c-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2401c-104">Denne fremgangsmåten viser hvordan du oppretter et nytt kategorihierarki og tilordner en varekodehierarkitype.</span><span class="sxs-lookup"><span data-stu-id="2401c-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="2401c-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="2401c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2401c-106">Denne fremgangsmåten er ment for kategorilederen.</span><span class="sxs-lookup"><span data-stu-id="2401c-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="2401c-107">Opprette det nye kategorihierarkiet</span><span class="sxs-lookup"><span data-stu-id="2401c-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="2401c-108">Gå til Behandling av produktinformasjon > Oppsett > Kategorier og attributter > Kategorihierarkier.</span><span class="sxs-lookup"><span data-stu-id="2401c-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="2401c-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2401c-109">Click New.</span></span>
3. <span data-ttu-id="2401c-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2401c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2401c-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2401c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2401c-112">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="2401c-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="2401c-113">Bygge hierarkiet</span><span class="sxs-lookup"><span data-stu-id="2401c-113">Build the hierarchy</span></span>
1. <span data-ttu-id="2401c-114">Klikk Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="2401c-114">Click New category node.</span></span>
2. <span data-ttu-id="2401c-115">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2401c-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="2401c-116">Skriv inn en verdi i feltet Kode.</span><span class="sxs-lookup"><span data-stu-id="2401c-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="2401c-117">Skriv inn en verdi i feltet Egendefinert navn.</span><span class="sxs-lookup"><span data-stu-id="2401c-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="2401c-118">Klikk Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="2401c-118">Click New category node.</span></span>
6. <span data-ttu-id="2401c-119">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2401c-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="2401c-120">Skriv inn en verdi i feltet Kode.</span><span class="sxs-lookup"><span data-stu-id="2401c-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="2401c-121">Skriv inn en verdi i feltet Egendefinert navn.</span><span class="sxs-lookup"><span data-stu-id="2401c-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="2401c-122">Klikk Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="2401c-122">Click New category node.</span></span>
10. <span data-ttu-id="2401c-123">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2401c-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="2401c-124">Skriv inn en verdi i feltet Kode.</span><span class="sxs-lookup"><span data-stu-id="2401c-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="2401c-125">Skriv inn en verdi i feltet Egendefinert navn.</span><span class="sxs-lookup"><span data-stu-id="2401c-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="2401c-126">Klikk Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="2401c-126">Click New category node.</span></span>
14. <span data-ttu-id="2401c-127">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2401c-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="2401c-128">Skriv inn en verdi i feltet Kode.</span><span class="sxs-lookup"><span data-stu-id="2401c-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="2401c-129">Skriv inn en verdi i feltet Egendefinert navn.</span><span class="sxs-lookup"><span data-stu-id="2401c-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="2401c-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2401c-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="2401c-131">Klassifisere hierarkiet</span><span class="sxs-lookup"><span data-stu-id="2401c-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="2401c-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2401c-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="2401c-133">I handlingsruten, klikker du Kategorihierarki.</span><span class="sxs-lookup"><span data-stu-id="2401c-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="2401c-134">Klikk Tilknytt hierarkitype.</span><span class="sxs-lookup"><span data-stu-id="2401c-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="2401c-135">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2401c-135">Click New.</span></span>
5. <span data-ttu-id="2401c-136">Velg et alternativ i feltet Kategorihierarkitype.</span><span class="sxs-lookup"><span data-stu-id="2401c-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="2401c-137">Velg kategorihierarkitype for artikkelkode for produktklassifisering.</span><span class="sxs-lookup"><span data-stu-id="2401c-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="2401c-138">Klikk rullegardinknappen i feltet Kategorihierarki for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="2401c-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2401c-139">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2401c-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2401c-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2401c-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2401c-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2401c-141">Close the page.</span></span>

