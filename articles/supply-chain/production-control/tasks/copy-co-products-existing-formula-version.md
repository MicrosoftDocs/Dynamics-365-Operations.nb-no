---
title: Kopiere koprodukter fra en eksisterende formelversjon
description: Denne prosedyren viser hvordan du kopierer koprodukter fra en eksisterende formelversjon til en annen formelversjon for et frigitt produkt.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a16a6c8651b401dddfa47c0eb29efb0c3a49038
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981337"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="f9754-103">Kopiere koprodukter fra en eksisterende formelversjon</span><span class="sxs-lookup"><span data-stu-id="f9754-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9754-104">Denne prosedyren viser hvordan du kopierer koprodukter fra en eksisterende formelversjon til en annen formelversjon for et frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="f9754-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="f9754-105">Det er en forutsetning at det finnes minst én formelversjonen knyttet til koprodukter.</span><span class="sxs-lookup"><span data-stu-id="f9754-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="f9754-106">Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="f9754-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="f9754-107">Finne et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="f9754-107">Find a released product</span></span>
1. <span data-ttu-id="f9754-108">Gå til Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="f9754-108">Go to Released products.</span></span>
2. <span data-ttu-id="f9754-109">Klikk på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="f9754-109">Click Show filters.</span></span>
    * <span data-ttu-id="f9754-110">Du er i ferd med å legge til feltet Produksjonstype i filterdialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f9754-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="f9754-111">Klikk på Legg til et filtreringsfelt for å legge til feltet Produksjonstype.</span><span class="sxs-lookup"><span data-stu-id="f9754-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="f9754-112">Du må manuelt angi formelen i produksjonstypefeltet før du velger Bruk i neste trinn.</span><span class="sxs-lookup"><span data-stu-id="f9754-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="f9754-113">Dette bruker filteret på listen over frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="f9754-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="f9754-114">Angi formel manuelt i feltet Produksjonstype.</span><span class="sxs-lookup"><span data-stu-id="f9754-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="f9754-115">Klikk på Bruk.</span><span class="sxs-lookup"><span data-stu-id="f9754-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="f9754-116">Velge et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="f9754-116">Select a released product</span></span>
1. <span data-ttu-id="f9754-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f9754-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="f9754-118">Klikk på Formelversjoner.</span><span class="sxs-lookup"><span data-stu-id="f9754-118">Click Formula versions.</span></span>
    * <span data-ttu-id="f9754-119">Klikk på Formelversjoner i handlingsruten Byggeteknikk.</span><span class="sxs-lookup"><span data-stu-id="f9754-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="f9754-120">Kopiere koprodukter</span><span class="sxs-lookup"><span data-stu-id="f9754-120">Copy co-products</span></span>
1. <span data-ttu-id="f9754-121">Klikk på Formelversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f9754-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="f9754-122">Klikk på Koprodukter.</span><span class="sxs-lookup"><span data-stu-id="f9754-122">Click Co-products.</span></span>
3. <span data-ttu-id="f9754-123">Klikk på Kopier.</span><span class="sxs-lookup"><span data-stu-id="f9754-123">Click Copy.</span></span>
4. <span data-ttu-id="f9754-124">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9754-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="f9754-125">Angi eller velg en verdi i Formelversjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9754-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="f9754-126">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f9754-126">Click OK.</span></span>
7. <span data-ttu-id="f9754-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f9754-127">Close the page.</span></span>

