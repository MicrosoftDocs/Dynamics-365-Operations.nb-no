---
title: Hovedplanlegging for områdedekning, lager ikke obligatorisk
description: Dette emnet beskriver hvordan en vare som har et områdedimensjonssett for dekning planlegges.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9475a7fbe40d7feb60c23e0d7164222469dffa75
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "353937"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="c29e2-103">Hovedplanlegging for områdedekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c29e2-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c29e2-104">Dette emnet beskriver hvordan en vare som har et områdedimensjonssett for dekning planlegges.</span><span class="sxs-lookup"><span data-stu-id="c29e2-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="c29e2-105">Dette hovedplanleggingsscenariet omfatter følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="c29e2-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="c29e2-106">Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="c29e2-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="c29e2-107">Lagerdimensjonen er ikke satt til obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c29e2-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="c29e2-108">Lageret kan være kjent, men det brukes ikke i hovedplanleggingsberegningen.</span><span class="sxs-lookup"><span data-stu-id="c29e2-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="c29e2-109">Sitedimensjonen er angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="c29e2-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="c29e2-110">Lagerdimensjonen er ikke angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="c29e2-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="c29e2-111">Derfor samles tilbud og etterspørsel etter område, og kanskje også andre dekningsplanlagte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="c29e2-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="c29e2-112">Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår.</span><span class="sxs-lookup"><span data-stu-id="c29e2-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="c29e2-113">Parameterne det refereres til i grafikken, og plasseringene, er følgende:</span><span class="sxs-lookup"><span data-stu-id="c29e2-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="c29e2-114">Varedekning er definert for varen.</span><span class="sxs-lookup"><span data-stu-id="c29e2-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="c29e2-115">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="c29e2-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c29e2-116">Velg varen, og klikk deretter **Plan &gt; Varedekning**.</span><span class="sxs-lookup"><span data-stu-id="c29e2-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="c29e2-117">Påfyllingsrelasjoner er definert for lageret.</span><span class="sxs-lookup"><span data-stu-id="c29e2-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="c29e2-118">Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c29e2-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="c29e2-119">På **Hovedplanlegging**-fanen kan du se feltgruppen **Hovedlager**.</span><span class="sxs-lookup"><span data-stu-id="c29e2-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="c29e2-120">Standard ordretype er satt til Produksjon, Bestilling eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="c29e2-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="c29e2-121">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="c29e2-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c29e2-122">Velg varen, og klikk deretter **Plan &gt; Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="c29e2-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="c29e2-123">I **Standard ordreinnstillinger**-skjemaet kan du se feltet **Standard ordretype**.</span><span class="sxs-lookup"><span data-stu-id="c29e2-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Behov for sitedekning, lager ikke obligatorisk    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="c29e2-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c29e2-125">Additional resources</span></span>
--------

[<span data-ttu-id="c29e2-126">Hovedplanlegging og multisite-funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="c29e2-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="c29e2-127">Hovedplanlegging – område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c29e2-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c29e2-128">Hovedplanlegging – område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c29e2-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c29e2-129">Hovedplanlegging – område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c29e2-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c29e2-130">Hovedplanlegging – hvordan stykklisteversjon fastsettes</span><span class="sxs-lookup"><span data-stu-id="c29e2-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



