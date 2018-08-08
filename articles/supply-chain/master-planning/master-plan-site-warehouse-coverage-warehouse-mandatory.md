---
title: "Hovedplanlegging for område- og lagerdekning, lager obligatorisk"
description: "Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges. Lagerdimensjonen er obligatorisk."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: c52fc9955afe2a7502d0e1f9e7cdfc5b89bbb31d
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="25d61-104">Hovedplanlegging for område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="25d61-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25d61-105">Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges.</span><span class="sxs-lookup"><span data-stu-id="25d61-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="25d61-106">Lagerdimensjonen er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="25d61-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="25d61-107">Dette hovedplanleggingsscenariet omfatter følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="25d61-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="25d61-108">Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="25d61-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="25d61-109">Lagerdimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="25d61-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="25d61-110">Site- og lagerdimensjonene er angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="25d61-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="25d61-111">Andre dimensjoner kan også være angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="25d61-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="25d61-112">De berøres imidlertid ikke av multisite-funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="25d61-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="25d61-113">Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår.</span><span class="sxs-lookup"><span data-stu-id="25d61-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="25d61-114">Parameterne det refereres til i grafikken, og plasseringene, er følgende:</span><span class="sxs-lookup"><span data-stu-id="25d61-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="25d61-115">Lageret er satt til **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="25d61-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="25d61-116">Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="25d61-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="25d61-117">På **Hovedplanlegging**-hurtigkategorien kan du se feltet **Manuelt**.</span><span class="sxs-lookup"><span data-stu-id="25d61-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="25d61-118">Varedekning er definert for varen.</span><span class="sxs-lookup"><span data-stu-id="25d61-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="25d61-119">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="25d61-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="25d61-120">Velg varen og deretter i Handlingsrute i kategorien **Plan** klikker du **Varedekning**.</span><span class="sxs-lookup"><span data-stu-id="25d61-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="25d61-121">Påfyllingsrelasjoner er definert for lageret.</span><span class="sxs-lookup"><span data-stu-id="25d61-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="25d61-122">Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="25d61-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="25d61-123">På **Hovedplanlegging**-hurtigkategorien kan du se feltgruppen **Hovedlager**.</span><span class="sxs-lookup"><span data-stu-id="25d61-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="25d61-124">Standard ordretype er satt til Produksjon, Bestilling eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="25d61-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="25d61-125">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="25d61-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="25d61-126">Velg varen og deretter i Handlingsrute i kategorien **Plan** klikker du **Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="25d61-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="25d61-127">I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.</span><span class="sxs-lookup"><span data-stu-id="25d61-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Behov for site- og lagerdekning, lager obligatorisk](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="25d61-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="25d61-129">Additional resources</span></span>
--------

[<span data-ttu-id="25d61-130">Hovedplanlegging og multisite-funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="25d61-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="25d61-131">Hovedplanlegging – område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="25d61-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="25d61-132">Hovedplanlegging – område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="25d61-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="25d61-133">Hovedplanlegging – område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="25d61-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="25d61-134">Hovedplanlegging – hvordan stykklisteversjon fastsettes</span><span class="sxs-lookup"><span data-stu-id="25d61-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




