---
title: Opprette bunkeattributter for et produkt
description: Denne prosedyren viser hvordan du oppretter et bunkeattributt, tilordner standard verdiområder og tar med attributtet i en gruppe.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d874b6b6e53164c00d9b4656d27b1060f4e3ba06
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934941"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="6bd37-103">Opprette bunkeattributter for et produkt</span><span class="sxs-lookup"><span data-stu-id="6bd37-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6bd37-104">Denne prosedyren viser hvordan du oppretter et bunkeattributt, tilordner standard verdiområder og tar med attributtet i en gruppe.</span><span class="sxs-lookup"><span data-stu-id="6bd37-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="6bd37-105">Demonstrasjonsdatafirmaet som brukes til å opprette denne prosedyren, er firmaet USP2.</span><span class="sxs-lookup"><span data-stu-id="6bd37-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="6bd37-106">Gå til Lagerstyring > Oppsett > Parti > Partiattributter.</span><span class="sxs-lookup"><span data-stu-id="6bd37-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="6bd37-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6bd37-107">Click New.</span></span>
3. <span data-ttu-id="6bd37-108">Skriv inn en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="6bd37-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="6bd37-109">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6bd37-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6bd37-110">Velg Brøk i Attributtype-feltet.</span><span class="sxs-lookup"><span data-stu-id="6bd37-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="6bd37-111">Denne prosedyren bruker typen Brøk for å aktivere desimalverdier.</span><span class="sxs-lookup"><span data-stu-id="6bd37-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="6bd37-112">Du kan velge andre attributtyper.</span><span class="sxs-lookup"><span data-stu-id="6bd37-112">You can select other attribute types.</span></span> <span data-ttu-id="6bd37-113">Hvis du har valgt typen Opplisting, må du angi verdier i opplistingslisten før du kan angi en verdi i Mål-feltet.</span><span class="sxs-lookup"><span data-stu-id="6bd37-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="6bd37-114">Angi et tall i feltet Minimum.</span><span class="sxs-lookup"><span data-stu-id="6bd37-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="6bd37-115">Angi et tall i feltet Maksimum.</span><span class="sxs-lookup"><span data-stu-id="6bd37-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="6bd37-116">Angi et tall i feltet Trinnvis.</span><span class="sxs-lookup"><span data-stu-id="6bd37-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="6bd37-117">Skriv inn en verdi i feltet Mål.</span><span class="sxs-lookup"><span data-stu-id="6bd37-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="6bd37-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6bd37-118">Click Save.</span></span>
11. <span data-ttu-id="6bd37-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6bd37-119">Close the page.</span></span>
12. <span data-ttu-id="6bd37-120">Gå til Lagerstyring > Oppsett > Parti > Partiattributtgrupper.</span><span class="sxs-lookup"><span data-stu-id="6bd37-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="6bd37-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6bd37-121">Click New.</span></span>
14. <span data-ttu-id="6bd37-122">Skriv inn en verdi i Attributtgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="6bd37-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="6bd37-123">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6bd37-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="6bd37-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6bd37-124">Click Save.</span></span>
17. <span data-ttu-id="6bd37-125">Klikk Gruppeattributter.</span><span class="sxs-lookup"><span data-stu-id="6bd37-125">Click Group attributes.</span></span>
18. <span data-ttu-id="6bd37-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6bd37-126">Click New.</span></span>
19. <span data-ttu-id="6bd37-127">Klikk rullegardinknappen i feltet Attributt for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6bd37-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6bd37-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6bd37-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6bd37-129">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6bd37-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6bd37-130">Et attributt kan inkluderes i alle gruppene.</span><span class="sxs-lookup"><span data-stu-id="6bd37-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="6bd37-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6bd37-131">Click Save.</span></span>
23. <span data-ttu-id="6bd37-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6bd37-132">Close the page.</span></span>

