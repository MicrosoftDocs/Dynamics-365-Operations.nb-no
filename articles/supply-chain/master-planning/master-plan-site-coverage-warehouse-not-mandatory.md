---
title: Hovedplanlegging for områdedekning, lager ikke obligatorisk
description: Dette emnet beskriver hvordan en vare som har et områdedimensjonssett for dekning planlegges.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40ea467b9dcac20e163f8b6e6f91b238d40278f7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833527"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="d8aca-103">Hovedplanlegging for områdedekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="d8aca-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8aca-104">Dette emnet beskriver hvordan en vare som har et områdedimensjonssett for dekning planlegges.</span><span class="sxs-lookup"><span data-stu-id="d8aca-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="d8aca-105">Dette hovedplanleggingsscenariet omfatter følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="d8aca-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="d8aca-106">Områdedimensjonen er satt til obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="d8aca-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="d8aca-107">Lagerdimensjonen er ikke satt til obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d8aca-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="d8aca-108">Lageret kan være kjent, men det brukes ikke i hovedplanleggingsberegningen.</span><span class="sxs-lookup"><span data-stu-id="d8aca-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="d8aca-109">Sitedimensjonen er angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d8aca-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="d8aca-110">Lagerdimensjonen er ikke angitt for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d8aca-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="d8aca-111">Derfor samles tilbud og etterspørsel etter område, og kanskje også andre dekningsplanlagte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d8aca-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="d8aca-112">Grafikken nedenfor illustrerer hvordan hovedplanlegging pågår.</span><span class="sxs-lookup"><span data-stu-id="d8aca-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="d8aca-113">Parameterne det refereres til i grafikken, og plasseringene, er følgende:</span><span class="sxs-lookup"><span data-stu-id="d8aca-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="d8aca-114">Varedekning er definert for varen.</span><span class="sxs-lookup"><span data-stu-id="d8aca-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="d8aca-115">Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="d8aca-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d8aca-116">Velg varen, og klikk deretter **Plan &gt; Varedekning**.</span><span class="sxs-lookup"><span data-stu-id="d8aca-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="d8aca-117">Påfyllingsrelasjoner er definert for lageret.</span><span class="sxs-lookup"><span data-stu-id="d8aca-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="d8aca-118">Klikk på **Lagerstyring &gt; Oppsett &gt; Lageroppdeling &gt; Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d8aca-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d8aca-119">På **Hovedplanlegging**-fanen kan du se feltgruppen **Hovedlager**.</span><span class="sxs-lookup"><span data-stu-id="d8aca-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="d8aca-120">Standard ordretype er satt til Produksjon, Bestilling eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="d8aca-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="d8aca-121">Klikk på **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="d8aca-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d8aca-122">Velg varen, og klikk deretter **Plan &gt; Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d8aca-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="d8aca-123">I **Standard ordreinnstillinger**-skjemaet kan du se feltet **Standard ordretype**.</span><span class="sxs-lookup"><span data-stu-id="d8aca-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Behov for sitedekning, lager ikke obligatorisk    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="d8aca-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d8aca-125">Additional resources</span></span>
--------

[<span data-ttu-id="d8aca-126">Oversikt over hovedplanlegging og multisite-funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="d8aca-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="d8aca-127">Hovedplanlegging for område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="d8aca-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d8aca-128">Hovedplanlegging for områdedekning, obligatorisk lager</span><span class="sxs-lookup"><span data-stu-id="d8aca-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d8aca-129">Hovedplanlegging for områdedekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="d8aca-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d8aca-130">Fastslå stykklisteversjonen</span><span class="sxs-lookup"><span data-stu-id="d8aca-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]