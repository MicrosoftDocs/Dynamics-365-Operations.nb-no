---
title: Opprette bunkeattributter for et produkt
description: Denne prosedyren viser hvordan du oppretter et bunkeattributt, tilordner standard verdiområder og tar med attributtet i en gruppe.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66757cdb93c67129c19ae226caa271a44c759206
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218567"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="7bc4f-103">Opprette bunkeattributter for et produkt</span><span class="sxs-lookup"><span data-stu-id="7bc4f-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7bc4f-104">Denne prosedyren viser hvordan du oppretter et bunkeattributt, tilordner standard verdiområder og tar med attributtet i en gruppe.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="7bc4f-105">Demonstrasjonsdatafirmaet som brukes til å opprette denne prosedyren, er firmaet USP2.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="7bc4f-106">Gå til Lagerstyring > Oppsett > Parti > Partiattributter.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="7bc4f-107">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-107">Click New.</span></span>
3. <span data-ttu-id="7bc4f-108">Skriv inn en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="7bc4f-109">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7bc4f-110">Velg Brøk i Attributtype-feltet.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="7bc4f-111">Denne prosedyren bruker typen Brøk for å aktivere desimalverdier.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="7bc4f-112">Du kan velge andre attributtyper.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-112">You can select other attribute types.</span></span> <span data-ttu-id="7bc4f-113">Hvis du har valgt typen Opplisting, må du angi verdier i opplistingslisten før du kan angi en verdi i Mål-feltet.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="7bc4f-114">Angi et tall i feltet Minimum.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="7bc4f-115">Angi et tall i feltet Maksimum.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="7bc4f-116">Angi et tall i feltet Trinnvis.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="7bc4f-117">Skriv inn en verdi i feltet Mål.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="7bc4f-118">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-118">Click Save.</span></span>
11. <span data-ttu-id="7bc4f-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-119">Close the page.</span></span>
12. <span data-ttu-id="7bc4f-120">Gå til Lagerstyring > Oppsett > Parti > Partiattributtgrupper.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="7bc4f-121">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-121">Click New.</span></span>
14. <span data-ttu-id="7bc4f-122">Skriv inn en verdi i Attributtgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="7bc4f-123">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="7bc4f-124">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-124">Click Save.</span></span>
17. <span data-ttu-id="7bc4f-125">Klikk på Gruppeattributter.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-125">Click Group attributes.</span></span>
18. <span data-ttu-id="7bc4f-126">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-126">Click New.</span></span>
19. <span data-ttu-id="7bc4f-127">Klikk på rullegardinknappen i feltet Attributt for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="7bc4f-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="7bc4f-129">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7bc4f-130">Et attributt kan inkluderes i alle gruppene.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="7bc4f-131">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-131">Click Save.</span></span>
23. <span data-ttu-id="7bc4f-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]