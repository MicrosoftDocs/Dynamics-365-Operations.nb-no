---
title: Spore glidende gjennomsnitt av kostpris per lagerdimensjon
description: "En lagerdimensjonsgruppe er knyttet til hver lagervare. Det glidende gjennomsnittet av kostprisen for en vare beregnes derfor på grunnlag av et utvalg av lagerdimensjoner som spores økonomisk."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bb2a3a193585944810c5dfac1eb3c019e074008f
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="5b889-104">Spore glidende gjennomsnitt av kostpris per lagerdimensjon</span><span class="sxs-lookup"><span data-stu-id="5b889-104">Tracking running average cost per inventory dimension</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="5b889-105">En lagerdimensjonsgruppe er knyttet til hver lagervare.</span><span class="sxs-lookup"><span data-stu-id="5b889-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="5b889-106">Det glidende gjennomsnittet av kostprisen for en vare beregnes derfor på grunnlag av et utvalg av lagerdimensjoner som spores økonomisk.</span><span class="sxs-lookup"><span data-stu-id="5b889-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="5b889-107">Det finnes tre typer lagerdimensjoner: produkt, lagring og sporing.</span><span class="sxs-lookup"><span data-stu-id="5b889-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="5b889-108">Produktdimensjonene inkluderer konfigurasjon, størrelse og farge.</span><span class="sxs-lookup"><span data-stu-id="5b889-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="5b889-109">Produktdimensjoner spores alltid økonomisk.</span><span class="sxs-lookup"><span data-stu-id="5b889-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="5b889-110">Lagrings- og sporingsdimensjoner omfatter område, lager, sted, lagerstatus, nummerskilt, partinummer og serienummer.</span><span class="sxs-lookup"><span data-stu-id="5b889-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="5b889-111">Du kan bestemme hvilke lagrings- og sporingsdimensjoner som spores økonomisk.</span><span class="sxs-lookup"><span data-stu-id="5b889-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="5b889-112">**Eksempel 1**</span><span class="sxs-lookup"><span data-stu-id="5b889-112">**Example 1**</span></span> 

<span data-ttu-id="5b889-113">Hvis lagerdimensjonsgruppen som er knyttet til varen, spores økonomisk etter lager, vil det glidende gjennomsnittet av kostprisen beregnes for hvert lager.</span><span class="sxs-lookup"><span data-stu-id="5b889-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="5b889-114">Følgende bestillinger er fakturert:</span><span class="sxs-lookup"><span data-stu-id="5b889-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="5b889-115">En bestilling av et antall på 2 til en kostpris på USD 10,00 er fakturert for lageret HL.</span><span class="sxs-lookup"><span data-stu-id="5b889-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="5b889-116">En bestilling av et antall på 3 til en kostpris på USD 12,00 er fakturert for lageret HL.</span><span class="sxs-lookup"><span data-stu-id="5b889-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="5b889-117">En bestilling av et antall på 5 til en kostpris på USD 15,00 er fakturert for lageret ML.</span><span class="sxs-lookup"><span data-stu-id="5b889-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="5b889-118">Løpende gjennomsnittlig kostpris for lageret HL er USD 11,20, og den løpende gjennomsnittlige kostprisen for lageret ML er USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="5b889-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="5b889-119">En salgsordrefaktura posteres for lageret HL.</span><span class="sxs-lookup"><span data-stu-id="5b889-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="5b889-120">Verdien av lageret og kostnader for solgte varer (før lagerlukking kjøres og uten merking) er USD 11,20.</span><span class="sxs-lookup"><span data-stu-id="5b889-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="5b889-121">En ny salgsordrefaktura posteres for lageret HL.</span><span class="sxs-lookup"><span data-stu-id="5b889-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="5b889-122">Verdien av lageret og kostnader for solgte varer (før lagerlukking kjøres og uten merking) er USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="5b889-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="5b889-123">**Eksempel 2** Hvis lagringsdimensjonsgruppen som er knyttet til varen, spores økonomisk etter lager og sporingsdimensjonsgruppen spores økonomisk etter partinummer, blir det glidende gjennomsnittet av kostprisen beregnet for hvert parti.</span><span class="sxs-lookup"><span data-stu-id="5b889-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="5b889-124">**Obs!** Vi anbefaler at du alltid viser kostprisen for alle økonomiske dimensjoner som spores.</span><span class="sxs-lookup"><span data-stu-id="5b889-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="5b889-125">Følgende bestillinger er fakturert:</span><span class="sxs-lookup"><span data-stu-id="5b889-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="5b889-126">En bestilling av et antall på 2 til en kostpris på USD 10,00 er fakturert for lageret HL og partiet AAA.</span><span class="sxs-lookup"><span data-stu-id="5b889-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="5b889-127">En bestilling av et antall på 3 til en kostpris på USD 12,00 er fakturert for lageret HL og partiet AAA.</span><span class="sxs-lookup"><span data-stu-id="5b889-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="5b889-128">En bestilling av et antall på 2 til en kostpris på USD 15,00 er fakturert for lageret HL og partiet BBB.</span><span class="sxs-lookup"><span data-stu-id="5b889-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="5b889-129">Løpende gjennomsnittlig kostpris for lageret HL og parti AAA er USD 11,20, og den løpende gjennomsnittlige kostprisen for lageret ML og parti BBB er USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="5b889-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




