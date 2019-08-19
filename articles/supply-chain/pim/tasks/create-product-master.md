---
title: Opprette en produktstandard
description: Opprett en produktstandard for de forhåndsdefinerte variantene.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21cfc2699fdcd6024286ee16bb60c3cd6dda5b67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844721"
---
# <a name="create-a-product-master"></a><span data-ttu-id="238f2-103">Opprette en produktstandard</span><span class="sxs-lookup"><span data-stu-id="238f2-103">Create a product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="238f2-104">Opprett en produktstandard for de forhåndsdefinerte variantene.</span><span class="sxs-lookup"><span data-stu-id="238f2-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="238f2-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="238f2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="238f2-106">Denne fremgangsmåten er ment for produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="238f2-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="238f2-107">Opprette en ny produktstandard</span><span class="sxs-lookup"><span data-stu-id="238f2-107">Create a new product master</span></span>
1. <span data-ttu-id="238f2-108">Gå til Behandling av produktinformasjon > Produkter > Produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="238f2-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="238f2-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="238f2-109">Click New.</span></span>
3. <span data-ttu-id="238f2-110">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="238f2-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="238f2-111">Nummeret må være unikt.</span><span class="sxs-lookup"><span data-stu-id="238f2-111">The number must be unique.</span></span> <span data-ttu-id="238f2-112">Du kan angi en nummerserie for feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="238f2-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="238f2-113">I så fall trenger ikke brukeren å angi en verdi.</span><span class="sxs-lookup"><span data-stu-id="238f2-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="238f2-114">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="238f2-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="238f2-115">Angi et beskrivende produktnavn.</span><span class="sxs-lookup"><span data-stu-id="238f2-115">Enter a descriptive product name.</span></span> <span data-ttu-id="238f2-116">Verdien angis som standard til søkenavnet, men dette kan endres av brukeren.</span><span class="sxs-lookup"><span data-stu-id="238f2-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="238f2-117">Klikk rullegardinknappen i Produktdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="238f2-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="238f2-118">Produktdimensjonsgruppen bestemmer hvilke 4 produktdimensjoner som kan brukes til å opprette produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="238f2-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="238f2-119">Dette eksemplet brukes en gruppe med farge og størrelse.</span><span class="sxs-lookup"><span data-stu-id="238f2-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="238f2-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="238f2-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="238f2-122">Standardkonfigurasjonsteknologien er Forhåndsdefinert variant.</span><span class="sxs-lookup"><span data-stu-id="238f2-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="238f2-123">Denne vil bli brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="238f2-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="238f2-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="238f2-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="238f2-125">Velg produktdimensjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="238f2-125">Select product dimension groups</span></span>
1. <span data-ttu-id="238f2-126">Klikk rullegardinknappen i feltet Fargegruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="238f2-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="238f2-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="238f2-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="238f2-129">Klikk rullegardinknappen i feltet Størrelsesgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="238f2-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="238f2-130">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="238f2-131">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="238f2-132">Legge til dimensjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="238f2-132">Add dimension groups</span></span>
1. <span data-ttu-id="238f2-133">Klikk Produkt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="238f2-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="238f2-134">Klikk Dimensjonsgrupper for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="238f2-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="238f2-135">Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="238f2-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="238f2-136">Lagringsdimensjoner hjelper deg styre hvordan varer lagres og hentes fra lageret.</span><span class="sxs-lookup"><span data-stu-id="238f2-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="238f2-137">En lagringsdimensjon kan for eksempel inkludere Område og lager.</span><span class="sxs-lookup"><span data-stu-id="238f2-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="238f2-138">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="238f2-139">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="238f2-140">Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="238f2-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="238f2-141">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du kan legge til et produkt.</span><span class="sxs-lookup"><span data-stu-id="238f2-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="238f2-142">Parti- eller serienummer brukes for eksempel til å spore varer på lager.</span><span class="sxs-lookup"><span data-stu-id="238f2-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="238f2-143">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="238f2-144">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="238f2-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="238f2-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="238f2-145">Click OK.</span></span>
10. <span data-ttu-id="238f2-146">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="238f2-146">Click Save.</span></span>
11. <span data-ttu-id="238f2-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="238f2-147">Close the page.</span></span>

