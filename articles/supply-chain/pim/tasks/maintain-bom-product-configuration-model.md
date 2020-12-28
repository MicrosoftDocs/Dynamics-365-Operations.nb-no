---
title: Vedlikeholde stykkliste for en produktkonfigurasjonsmodell
description: Kjører du denne prosedyren krever det en eksisterende produktmodellkonfigurasjon.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcdf4b735587b76b7f761f59c56da1ca358a2e37
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434266"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="d2598-103">Vedlikeholde stykkliste for en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="d2598-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2598-104">Kjører du denne prosedyren krever det en eksisterende produktmodellkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d2598-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="d2598-105">Modellen for High-end-høyttaler i demofirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d2598-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="d2598-106">Legge til en stykklistelinje</span><span class="sxs-lookup"><span data-stu-id="d2598-106">Add a BOM line</span></span>
1. <span data-ttu-id="d2598-107">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="d2598-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="d2598-108">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="d2598-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="d2598-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d2598-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2598-110">Velg High-end-høyttaleren for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="d2598-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="d2598-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d2598-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d2598-112">Utvid delen Stykklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="d2598-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="d2598-113">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="d2598-113">Click Add.</span></span>
7. <span data-ttu-id="d2598-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d2598-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="d2598-115">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d2598-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="d2598-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d2598-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="d2598-117">Legge til detaljer om stykklistelinje</span><span class="sxs-lookup"><span data-stu-id="d2598-117">Add BOM line details</span></span>
1. <span data-ttu-id="d2598-118">Klikk Detaljer om stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="d2598-118">Click BOM line details.</span></span>
2. <span data-ttu-id="d2598-119">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="d2598-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="d2598-120">Du kan for eksempel velge varen M0055.</span><span class="sxs-lookup"><span data-stu-id="d2598-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="d2598-121">For hver Stykklistelinjeegenskap kan du velge om den tar en fast verdi eller er tilordnet til et attributt.</span><span class="sxs-lookup"><span data-stu-id="d2598-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="d2598-122">Merk av for Sett.</span><span class="sxs-lookup"><span data-stu-id="d2598-122">Select the Set check box.</span></span>
4. <span data-ttu-id="d2598-123">Velg Ja i feltet Beregning.</span><span class="sxs-lookup"><span data-stu-id="d2598-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="d2598-124">Når du setter Beregning-egenskapen til Ja, sikrer du at stykklistelinjen er inkludert i kostnadsberegning.</span><span class="sxs-lookup"><span data-stu-id="d2598-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="d2598-125">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="d2598-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="d2598-126">Merk av for Sett.</span><span class="sxs-lookup"><span data-stu-id="d2598-126">Select the Set check box.</span></span>
7. <span data-ttu-id="d2598-127">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="d2598-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d2598-128">Antall-feltet bestemmer hvor mye av varen som inngår i stykklisten.</span><span class="sxs-lookup"><span data-stu-id="d2598-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="d2598-129">Dette kan være en opplagt kandidat for en attributtilordning.</span><span class="sxs-lookup"><span data-stu-id="d2598-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="d2598-130">Klikk kategorien Dimensjon.</span><span class="sxs-lookup"><span data-stu-id="d2598-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="d2598-131">Verifiser om noen av produktdimensjonene er aktive, og derfor må ha en verdi eller et attributt tilordnet.</span><span class="sxs-lookup"><span data-stu-id="d2598-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="d2598-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="d2598-132">Click OK.</span></span>

