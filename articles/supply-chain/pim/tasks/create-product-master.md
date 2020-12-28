---
title: Opprette en produktstandard
description: Opprett en produktstandard for de forhåndsdefinerte variantene.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdb30b46a0e5a6d4fac997588dd47148f2664c03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434406"
---
# <a name="create-a-product-master"></a><span data-ttu-id="ecb0c-103">Opprette en produktstandard</span><span class="sxs-lookup"><span data-stu-id="ecb0c-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ecb0c-104">Opprett en produktstandard for de forhåndsdefinerte variantene.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="ecb0c-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ecb0c-106">Denne fremgangsmåten er ment for produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="ecb0c-107">Opprette en ny produktstandard</span><span class="sxs-lookup"><span data-stu-id="ecb0c-107">Create a new product master</span></span>
1. <span data-ttu-id="ecb0c-108">Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Produktstandarder**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="ecb0c-109">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-109">Click **New**.</span></span>
3. <span data-ttu-id="ecb0c-110">Skriv inn en verdi i feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="ecb0c-111">Nummeret må være unikt.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-111">The number must be unique.</span></span> <span data-ttu-id="ecb0c-112">Du kan angi en nummerserie for feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="ecb0c-113">I så fall trenger ikke brukeren å angi en verdi.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="ecb0c-114">Skriv inn en verdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="ecb0c-115">Angi et beskrivende produktnavn.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-115">Enter a descriptive product name.</span></span> <span data-ttu-id="ecb0c-116">Verdien angis som standard til søkenavnet, men dette kan endres av brukeren.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="ecb0c-117">Klikk på rullegardinknappen i feltet **Produktdimensjonsgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ecb0c-118">Produktdimensjonsgruppen bestemmer hvilke 4 produktdimensjoner som kan brukes til å opprette produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="ecb0c-119">Dette eksemplet brukes en gruppe med farge og størrelse.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="ecb0c-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ecb0c-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="ecb0c-122">Standard **Konfigurasjonsteknologi** er Forhåndsdefinert variant.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="ecb0c-123">Denne vil bli brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-123">This will be used for this example.</span></span>
8. <span data-ttu-id="ecb0c-124">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="ecb0c-125">Velg produktdimensjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="ecb0c-125">Select product dimension groups</span></span>
1. <span data-ttu-id="ecb0c-126">Klikk på rullegardinknappen i feltet **Fargegruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="ecb0c-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ecb0c-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ecb0c-129">Klikk på rullegardinknappen i feltet **Størrelsesgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ecb0c-130">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ecb0c-131">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="ecb0c-132">Legge til dimensjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="ecb0c-132">Add dimension groups</span></span>
1. <span data-ttu-id="ecb0c-133">I **handlingsruten** klikker du på **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="ecb0c-134">Klikk på **Dimensjonsgrupper** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="ecb0c-135">Klikk rullegardinknappen i **Lagringsdimensjonsgruppe**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ecb0c-136">Lagringsdimensjoner hjelper deg styre hvordan varer lagres og hentes fra lageret.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="ecb0c-137">En lagringsdimensjon kan for eksempel inkludere Område og lager.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="ecb0c-138">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ecb0c-139">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ecb0c-140">Klikk rullegardinknappen i **Sporingsdimensjonsgruppe**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ecb0c-141">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du kan legge til et produkt.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="ecb0c-142">Parti- eller serienummer brukes for eksempel til å spore varer på lager.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="ecb0c-143">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ecb0c-144">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ecb0c-145">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-145">Click **OK**.</span></span>
10. <span data-ttu-id="ecb0c-146">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-146">Click **Save**.</span></span>
11. <span data-ttu-id="ecb0c-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ecb0c-147">Close the page.</span></span>

