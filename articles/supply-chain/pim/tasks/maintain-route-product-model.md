---
title: Vedlikeholde rute for en produktmodell
description: Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921271"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="da2ef-103">Vedlikeholde rute for en produktmodell</span><span class="sxs-lookup"><span data-stu-id="da2ef-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da2ef-104">Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes.</span><span class="sxs-lookup"><span data-stu-id="da2ef-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="da2ef-105">Denne fremgangsmåten bruker modellen for High-end-høyttaler i demofirmaet USMF til å lede deg gjennom prosessen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="da2ef-106">Legge til en ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="da2ef-106">Add a route operation</span></span>

1. <span data-ttu-id="da2ef-107">Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="da2ef-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da2ef-109">Velg High-end-høyttalermodellen for denne øvelsen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="da2ef-110">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="da2ef-111">Utvid delen **Ruteoperasjoner**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="da2ef-112">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-112">Select **Add**.</span></span>
1. <span data-ttu-id="da2ef-113">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2ef-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="da2ef-114">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2ef-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="da2ef-115">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="da2ef-116">Angi detaljer om ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="da2ef-116">Enter route operation details</span></span>

1. <span data-ttu-id="da2ef-117">Velg **Detaljer om ruteoperasjon**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="da2ef-118">Angi eller velg en verdi i feltet **Operasjon**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="da2ef-119">I feltet **Oper.nr.**</span><span class="sxs-lookup"><span data-stu-id="da2ef-119">In the **Oper. No.**</span></span> <span data-ttu-id="da2ef-120">angir du et nummer.</span><span class="sxs-lookup"><span data-stu-id="da2ef-120">field, enter a number.</span></span>
    * <span data-ttu-id="da2ef-121">Operasjonsnumre fastsetter rutesekvensen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="da2ef-122">Hver egenskap for en ruteoperasjon kan få en statisk verdi eller tilordnes til et attributt.</span><span class="sxs-lookup"><span data-stu-id="da2ef-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="da2ef-123">Tilordning til et attributt fører til at verdien blir definert som en del av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="da2ef-124">Angi eller velg en verdi i **Rutegruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="da2ef-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="da2ef-125">Rutegruppen bestemmer grunnleggende virkemåte for etterkalkulering, forbruk og oppsett.</span><span class="sxs-lookup"><span data-stu-id="da2ef-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="da2ef-126">Velg **Oppsett**-fanen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="da2ef-127">Velg **Tider**-fanen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="da2ef-128">I feltet **Prosessantall** angir du et nummer.</span><span class="sxs-lookup"><span data-stu-id="da2ef-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="da2ef-129">Bestem hvor mange som skal bli behandlet i løpet av én operasjon.</span><span class="sxs-lookup"><span data-stu-id="da2ef-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="da2ef-130">Angi et tall i feltet **Timer/tid**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="da2ef-131">Angi tidsforholdet.</span><span class="sxs-lookup"><span data-stu-id="da2ef-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="da2ef-132">Merk av for **Sett**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="da2ef-133">Angi et tall i feltet **Kjøretid**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="da2ef-134">Bestem behandlingstiden for antallet som du har angitt.</span><span class="sxs-lookup"><span data-stu-id="da2ef-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="da2ef-135">Velg fanen **Ressursbehov**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="da2ef-136">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-136">Select **Add**.</span></span>
1. <span data-ttu-id="da2ef-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da2ef-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="da2ef-138">Velg et alternativ i feltet **Behovstype**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="da2ef-139">Bestem om du vil angi bestemte ressurser eller egenskaper som de må inneha.</span><span class="sxs-lookup"><span data-stu-id="da2ef-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="da2ef-140">Angi eller velg en verdi i feltet **Behov**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="da2ef-141">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="da2ef-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]