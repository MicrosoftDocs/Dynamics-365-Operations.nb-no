---
title: Opprette et hierarki for produktklassifisering
description: Denne fremgangsmåten viser hvordan du oppretter et nytt kategorihierarki og tilordner en varekodehierarkitype.
author: ShylaThompson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4e2fdc62d7faa73efa78092d7754d3fa1213a94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809380"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="5a61e-103">Opprette et hierarki for produktklassifisering</span><span class="sxs-lookup"><span data-stu-id="5a61e-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a61e-104">Denne fremgangsmåten viser hvordan du oppretter et nytt kategorihierarki og tilordner en varekodehierarkitype.</span><span class="sxs-lookup"><span data-stu-id="5a61e-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="5a61e-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5a61e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5a61e-106">Denne fremgangsmåten er ment for kategorilederen.</span><span class="sxs-lookup"><span data-stu-id="5a61e-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="5a61e-107">Opprette det nye kategorihierarkiet</span><span class="sxs-lookup"><span data-stu-id="5a61e-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="5a61e-108">Gå til **Navigasjonsrute > Moduler > Gå til Behandling av produktinformasjon > Oppsett > Kategorier og attributter > Kategorihierarkier**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="5a61e-109">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-109">Click **New**.</span></span>
3. <span data-ttu-id="5a61e-110">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a61e-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="5a61e-111">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a61e-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="5a61e-112">Klikk på **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="5a61e-113">Bygge hierarkiet</span><span class="sxs-lookup"><span data-stu-id="5a61e-113">Build the hierarchy</span></span>
1. <span data-ttu-id="5a61e-114">Klikk på **Ny** kategorinode.</span><span class="sxs-lookup"><span data-stu-id="5a61e-114">Click **New** category node.</span></span>
2. <span data-ttu-id="5a61e-115">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a61e-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="5a61e-116">Skriv inn en verdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="5a61e-117">Skriv inn en verdi i feltet **Egendefinert navn**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="5a61e-118">Klikk på **Ny** kategorinode.</span><span class="sxs-lookup"><span data-stu-id="5a61e-118">Click **New** category node.</span></span>
6. <span data-ttu-id="5a61e-119">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a61e-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="5a61e-120">Skriv inn en verdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="5a61e-121">Skriv inn en verdi i feltet **Egendefinert navn**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="5a61e-122">Klikk på **Ny** kategorinode.</span><span class="sxs-lookup"><span data-stu-id="5a61e-122">Click **New** category node.</span></span>
10. <span data-ttu-id="5a61e-123">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a61e-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="5a61e-124">Skriv inn en verdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="5a61e-125">Skriv inn en verdi i feltet **Egendefinert navn**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="5a61e-126">Klikk på **Ny** kategorinode.</span><span class="sxs-lookup"><span data-stu-id="5a61e-126">Click **New** category node.</span></span>
14. <span data-ttu-id="5a61e-127">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a61e-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="5a61e-128">Skriv inn en verdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="5a61e-129">Skriv inn en verdi i feltet **Egendefinert navn**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="5a61e-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5a61e-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="5a61e-131">Klassifisere hierarkiet</span><span class="sxs-lookup"><span data-stu-id="5a61e-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="5a61e-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5a61e-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="5a61e-133">I **handlingsruten** klikker du **Kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="5a61e-134">Klikk på **Tilknytt hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="5a61e-135">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-135">Click **New**.</span></span>
5. <span data-ttu-id="5a61e-136">Velg et alternativ i feltet **Kategorihierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="5a61e-137">Velg **kategorihierarkitype for artikkelkode for produktklassifisering**.</span><span class="sxs-lookup"><span data-stu-id="5a61e-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="5a61e-138">Klikk på rullegardinknappen i feltet **Kategorihierarki** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5a61e-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5a61e-139">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5a61e-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="5a61e-140">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5a61e-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5a61e-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5a61e-141">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]