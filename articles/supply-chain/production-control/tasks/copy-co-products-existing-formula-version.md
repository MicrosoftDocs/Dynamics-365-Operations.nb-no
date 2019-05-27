---
title: Kopiere koprodukter fra en eksisterende formelversjon
description: Denne prosedyren viser hvordan du kopierer koprodukter fra en eksisterende formelversjon til en annen formelversjon for et frigitt produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179c12da0c2ddc7b5e2f2fdddd21168eac121811
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557808"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="a39db-103">Kopiere koprodukter fra en eksisterende formelversjon</span><span class="sxs-lookup"><span data-stu-id="a39db-103">Copy co-products from an existing formula version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a39db-104">Denne prosedyren viser hvordan du kopierer koprodukter fra en eksisterende formelversjon til en annen formelversjon for et frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="a39db-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="a39db-105">Det er en forutsetning at det finnes minst én formelversjonen knyttet til koprodukter.</span><span class="sxs-lookup"><span data-stu-id="a39db-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="a39db-106">Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="a39db-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="a39db-107">Finne et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="a39db-107">Find a released product</span></span>
1. <span data-ttu-id="a39db-108">Gå til Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="a39db-108">Go to Released products.</span></span>
2. <span data-ttu-id="a39db-109">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="a39db-109">Click Show filters.</span></span>
    * <span data-ttu-id="a39db-110">Du er i ferd med å legge til feltet Produksjonstype i filterdialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a39db-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="a39db-111">Klikk Legg til et filtreringsfelt for å legge til feltet Produksjonstype.</span><span class="sxs-lookup"><span data-stu-id="a39db-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="a39db-112">Du må manuelt angi formelen i produksjonstypefeltet før du velger Bruk i neste trinn.</span><span class="sxs-lookup"><span data-stu-id="a39db-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="a39db-113">Dette bruker filteret på listen over frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="a39db-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="a39db-114">Angi formel manuelt i feltet Produksjonstype.</span><span class="sxs-lookup"><span data-stu-id="a39db-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="a39db-115">Klikk Bruk.</span><span class="sxs-lookup"><span data-stu-id="a39db-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="a39db-116">Velge et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="a39db-116">Select a released product</span></span>
1. <span data-ttu-id="a39db-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="a39db-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="a39db-118">Klikk Formelversjoner.</span><span class="sxs-lookup"><span data-stu-id="a39db-118">Click Formula versions.</span></span>
    * <span data-ttu-id="a39db-119">Klikk Formelversjoner i handlingsruten Byggeteknikk.</span><span class="sxs-lookup"><span data-stu-id="a39db-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="a39db-120">Kopiere koprodukter</span><span class="sxs-lookup"><span data-stu-id="a39db-120">Copy co-products</span></span>
1. <span data-ttu-id="a39db-121">Klikk Formelversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a39db-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="a39db-122">Klikk Koprodukter.</span><span class="sxs-lookup"><span data-stu-id="a39db-122">Click Co-products.</span></span>
3. <span data-ttu-id="a39db-123">Klikk Kopier.</span><span class="sxs-lookup"><span data-stu-id="a39db-123">Click Copy.</span></span>
4. <span data-ttu-id="a39db-124">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="a39db-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="a39db-125">Angi eller velg en verdi i Formelversjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="a39db-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="a39db-126">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a39db-126">Click OK.</span></span>
7. <span data-ttu-id="a39db-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a39db-127">Close the page.</span></span>

