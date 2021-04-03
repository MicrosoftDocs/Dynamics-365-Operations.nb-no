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
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b1cd11cc62f551e43a04b9a8cc17bf7a7e961ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255595"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="ed5b2-104">Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="ed5b2-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed5b2-105">Dette emnet beskriver hvordan en vare som har et område og lagre som dekningsdimensjoner planlegges.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="ed5b2-106">Lagerdimensjonen er ikke obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="ed5b2-107">Dette hovedplanleggingsscenarioet omfatter følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="ed5b2-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="ed5b2-108">Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="ed5b2-109">Denne innstillingen kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="ed5b2-110">Lagerdimensjonen er ikke satt til obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="ed5b2-111">Lageret kan være kjent, men det brukes ikke i hovedplanleggingsberegningen.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="ed5b2-112">Site- og lagerdimensjonene er angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="ed5b2-113">Andre dimensjoner kan også være angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="ed5b2-114">De berøres imidlertid ikke av multisite-funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="ed5b2-115">Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="ed5b2-116">Parameterne det refereres til i grafikken, og plasseringene, er følgende:</span><span class="sxs-lookup"><span data-stu-id="ed5b2-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="ed5b2-117">Lageret er satt til Manuell.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="ed5b2-118">Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="ed5b2-119">På **Hovedplanlegging**-hurtigfanen kan du se feltet **Manuelt**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="ed5b2-120">Varedekning er definert for varen.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="ed5b2-121">Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="ed5b2-122">Velg varen og deretter i Handlingsrute i fanen **Plan** klikker du **Varedekning**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="ed5b2-123">Påfyllingsrelasjoner er definert for lageret.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="ed5b2-124">Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="ed5b2-125">På **Hovedplanlegging**-hurtigfanen kan du se feltgruppen **Hovedlager**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="ed5b2-126">Standard ordretype er satt til Produksjon, Bestilling eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="ed5b2-127">Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="ed5b2-128">Velg varen og deretter i Handlingsrute i fanen **Plan** klikker du **Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="ed5b2-129">I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Behov for site og lager, ikke lager](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="ed5b2-131">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ed5b2-131">Additional resources</span></span>
--------

[<span data-ttu-id="ed5b2-132">Oversikt over hovedplanlegging og multisite-funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="ed5b2-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="ed5b2-133">Hovedplanlegging for områdedekning, obligatorisk lager</span><span class="sxs-lookup"><span data-stu-id="ed5b2-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ed5b2-134">Hovedplanlegging for område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="ed5b2-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ed5b2-135">Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="ed5b2-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="ed5b2-136">Fastslå stykklisteversjonen</span><span class="sxs-lookup"><span data-stu-id="ed5b2-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]