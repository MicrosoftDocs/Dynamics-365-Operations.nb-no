---
title: Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk
description: Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er ikke obligatorisk.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43e9c1c08258a609cd8461db902c16952e99e4a7
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383326"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="aede7-104">Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aede7-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aede7-105">Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges.</span><span class="sxs-lookup"><span data-stu-id="aede7-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="aede7-106">Lagerdimensjonen er ikke obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="aede7-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="aede7-107">Dette hovedplanleggingsscenarioet omfatter følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="aede7-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="aede7-108">Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="aede7-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="aede7-109">Denne innstillingen kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="aede7-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="aede7-110">Lagerdimensjonen er ikke satt til obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="aede7-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="aede7-111">Lageret kan være kjent, men det brukes ikke i hovedplanleggingsberegningen.</span><span class="sxs-lookup"><span data-stu-id="aede7-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="aede7-112">Site- og lagerdimensjonene er angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="aede7-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="aede7-113">Andre dimensjoner kan også være angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="aede7-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="aede7-114">De berøres imidlertid ikke av multisite-funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="aede7-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="aede7-115">Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår.</span><span class="sxs-lookup"><span data-stu-id="aede7-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="aede7-116">Parameterne det refereres til i grafikken, og plasseringene, er følgende:</span><span class="sxs-lookup"><span data-stu-id="aede7-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="aede7-117">Lageret er satt til Manuell.</span><span class="sxs-lookup"><span data-stu-id="aede7-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="aede7-118">Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="aede7-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="aede7-119">På **Hovedplanlegging**-hurtigkategorien kan du se feltet **Manuelt**.</span><span class="sxs-lookup"><span data-stu-id="aede7-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="aede7-120">Varedekning er definert for varen.</span><span class="sxs-lookup"><span data-stu-id="aede7-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="aede7-121">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="aede7-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="aede7-122">Velg varen og deretter i Handlingsrute i kategorien **Plan** klikker du **Varedekning**.</span><span class="sxs-lookup"><span data-stu-id="aede7-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="aede7-123">Påfyllingsrelasjoner er definert for lageret.</span><span class="sxs-lookup"><span data-stu-id="aede7-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="aede7-124">Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="aede7-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="aede7-125">På **Hovedplanlegging**-hurtigkategorien kan du se feltgruppen **Hovedlager**.</span><span class="sxs-lookup"><span data-stu-id="aede7-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="aede7-126">Standard ordretype er satt til Produksjon, Bestilling eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="aede7-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="aede7-127">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="aede7-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="aede7-128">Velg varen og deretter i Handlingsrute i kategorien **Plan** klikker du **Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="aede7-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="aede7-129">I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.</span><span class="sxs-lookup"><span data-stu-id="aede7-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Behov for site og lager, ikke lager](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="aede7-131">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="aede7-131">Additional resources</span></span>
--------

[<span data-ttu-id="aede7-132">Oversikt over hovedplanlegging og multisite-funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="aede7-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="aede7-133">Hovedplanlegging for områdedekning, obligatorisk lager</span><span class="sxs-lookup"><span data-stu-id="aede7-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="aede7-134">Hovedplanlegging for område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aede7-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="aede7-135">Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aede7-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="aede7-136">Fastslå stykklisteversjonen</span><span class="sxs-lookup"><span data-stu-id="aede7-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



