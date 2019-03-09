---
title: Hovedplanlegging for område- og lagerdekning, lager obligatorisk
description: Dette emnet beskriver hvordan en vare som har en dekningsdimensjon planlegges. Lager er en obligatorisk dimensjon.
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f61c142fff73fdeeca573cca3f54e654511af1e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "328338"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="c39bd-104">Hovedplanlegging for område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c39bd-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c39bd-105">Dette emnet beskriver hvordan en vare som har en dekningsdimensjon planlegges.</span><span class="sxs-lookup"><span data-stu-id="c39bd-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="c39bd-106">Lager er en obligatorisk dimensjon.</span><span class="sxs-lookup"><span data-stu-id="c39bd-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="c39bd-107">Dette hovedplanleggingsscenariet omfatter følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="c39bd-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="c39bd-108">Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="c39bd-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="c39bd-109">Denne innstillingen kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="c39bd-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="c39bd-110">Lagerdimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="c39bd-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="c39bd-111">Sitedimensjonen er angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="c39bd-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="c39bd-112">Andre dimensjoner kan også være angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="c39bd-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="c39bd-113">De berøres imidlertid ikke av multisite-funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="c39bd-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="c39bd-114">Lagerdimensjonen er ikke angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="c39bd-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="c39bd-115">Derfor samles tilbud og etterspørsel etter område, og kanskje også andre dekningsplanlagte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="c39bd-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="c39bd-116">Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår.</span><span class="sxs-lookup"><span data-stu-id="c39bd-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="c39bd-117">Parameterne det refereres til i grafikken, og plasseringene, er følgende:</span><span class="sxs-lookup"><span data-stu-id="c39bd-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="c39bd-118">Varedekning er definert for varen.</span><span class="sxs-lookup"><span data-stu-id="c39bd-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="c39bd-119">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="c39bd-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c39bd-120">Velg varen, og klikk deretter **Plan &gt; Varedekning**.</span><span class="sxs-lookup"><span data-stu-id="c39bd-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="c39bd-121">Påfyllingsrelasjoner er definert for lageret.</span><span class="sxs-lookup"><span data-stu-id="c39bd-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="c39bd-122">Klikk **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c39bd-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="c39bd-123">På **Hovedplanlegging**-fanen kan du se feltgruppen **Hovedlager**.</span><span class="sxs-lookup"><span data-stu-id="c39bd-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="c39bd-124">Standard ordretype er satt til Produksjon, Bestilling eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="c39bd-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="c39bd-125">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="c39bd-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c39bd-126">Velg varen, og klikk deretter **Plan &gt; Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="c39bd-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="c39bd-127">I **Standard ordreinnstillinger**-skjemaet kan du se **Standard ordretype**.</span><span class="sxs-lookup"><span data-stu-id="c39bd-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Behov for sitedekning, lager obligatorisk](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="c39bd-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c39bd-129">Additional resources</span></span>
--------

[<span data-ttu-id="c39bd-130">Hovedplanlegging og multisite-funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="c39bd-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="c39bd-131">Hovedplanlegging – område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c39bd-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c39bd-132">Hovedplanlegging – område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c39bd-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c39bd-133">Hovedplanlegging – område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c39bd-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c39bd-134">Hovedplanlegging – hvordan stykklisteversjon fastsettes</span><span class="sxs-lookup"><span data-stu-id="c39bd-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



