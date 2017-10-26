---
title: Lagerlokasjoner
description: "Lagerlokasjoner brukes med grunnleggende lageraktiviteter (WMS I) til å angi hvor varene er lagret, og der varer hentes fra i et WMS I-lager."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 6d40069b4116d38f25a12340df0d939afa2866e7
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="inventory-locations"></a><span data-ttu-id="3eb59-103">Lagerlokasjoner</span><span class="sxs-lookup"><span data-stu-id="3eb59-103">Inventory locations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3eb59-104">Lagerlokasjoner brukes med grunnleggende lageraktiviteter (WMS I) til å angi hvor varene er lagret, og der varer hentes fra i et WMS I-lager.</span><span class="sxs-lookup"><span data-stu-id="3eb59-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="3eb59-105">Dette emnet gjelder funksjoner i beholdningstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="3eb59-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="3eb59-106">Det gjelder ikke for funksjoner i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="3eb59-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="3eb59-107">Termen lokasjon brukes om et sted der varer lagres og hentes fra.</span><span class="sxs-lookup"><span data-stu-id="3eb59-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="3eb59-108">For hver lokasjon kan stedet der varen legges inn, også angis.</span><span class="sxs-lookup"><span data-stu-id="3eb59-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="3eb59-109">De er som standard like.</span><span class="sxs-lookup"><span data-stu-id="3eb59-109">By default, they are the same.</span></span> <span data-ttu-id="3eb59-110">Varer legges vanligvis inn og hentes fra den samme siden av en lokasjon, men ikke alltid.</span><span class="sxs-lookup"><span data-stu-id="3eb59-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="3eb59-111">Varer som for eksempel er lagret på lagringsreoler legges inn fra én gang, og hentes fra en annen.</span><span class="sxs-lookup"><span data-stu-id="3eb59-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="3eb59-112">De viktigste inndataene angis ved et lokasjonsnavn som vanligvis bestemmes av lokasjonens koordinater: lager, gang, reol, hylle og boks..</span><span class="sxs-lookup"><span data-stu-id="3eb59-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="3eb59-113">Dette navnet eller denne IDen kan angis manuelt, eller genereres fra lokasjonskoordinatene, for eksempel 01-02-03-4 for gang 1, reol 2, hylle 3, posisjon 4 på Lagerlokasjoner-siden.</span><span class="sxs-lookup"><span data-stu-id="3eb59-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="3eb59-114">Lokasjonsegenskaper</span><span class="sxs-lookup"><span data-stu-id="3eb59-114">Location properties</span></span>

<span data-ttu-id="3eb59-115">En lokasjon har følgende kjennetegn:</span><span class="sxs-lookup"><span data-stu-id="3eb59-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="3eb59-116">Størrelse (høyde, bredde, dybde og dermed volum)</span><span class="sxs-lookup"><span data-stu-id="3eb59-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="3eb59-117">Lager, gang, reol, hylle og boksposisjon</span><span class="sxs-lookup"><span data-stu-id="3eb59-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="3eb59-118">Lokasjonstype (bulklokasjon, plukklokasjon, mottakssone, utleveringsport, produksjonsinnleveringssted, inspeksjonslokasjon eller kanban-supermarked)</span><span class="sxs-lookup"><span data-stu-id="3eb59-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="3eb59-119">Du kan bruke kontrolltekst i online-systemer til å kontrollere at operatøren har valgt riktig lokasjon for en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="3eb59-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="3eb59-120">Denne kontrollteksten kan opprettes manuelt eller det brukes som standardtekst.</span><span class="sxs-lookup"><span data-stu-id="3eb59-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="3eb59-121">Sorteringskoder</span><span class="sxs-lookup"><span data-stu-id="3eb59-121">Sort codes</span></span>
<span data-ttu-id="3eb59-122">Bruk sorteringskoder for å optimalisere håndteringen av plukklinjer, som beskriver informasjonen som kreves for plukking av varer fra lager, inkludert plukkordren.</span><span class="sxs-lookup"><span data-stu-id="3eb59-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="3eb59-123">Sorteringskoder kan angis etter gangen og andre koordinater, eller tilordnes manuelt for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="3eb59-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="3eb59-124">Blokkerte lokasjoner</span><span class="sxs-lookup"><span data-stu-id="3eb59-124">Blocked locations</span></span>
<span data-ttu-id="3eb59-125">Noen ganger vil du kanskje angi at en lokasjon er blokkert for en tidsperiode, for eksempel ved reparasjon.</span><span class="sxs-lookup"><span data-stu-id="3eb59-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="3eb59-126">Andre ganger vil du kanskje angi at du vil blokkere bare innleveringen eller utleveringen.</span><span class="sxs-lookup"><span data-stu-id="3eb59-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="3eb59-127">Trestruktur</span><span class="sxs-lookup"><span data-stu-id="3eb59-127">Tree structure</span></span>

<span data-ttu-id="3eb59-128">På Lagerlokasjoner-siden kan du vise lageroppsettet i en trestruktur basert på koordinatene for lagerlokasjoner, i et definert visningsformat.</span><span class="sxs-lookup"><span data-stu-id="3eb59-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="3eb59-129">Vedlikeholde lagerlokasjoner via lagerskjemaet</span><span class="sxs-lookup"><span data-stu-id="3eb59-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="3eb59-130">Det er mulig å kopiere lokasjoner fra ett lager til et annet og opprette lokasjoner via en veiviser.</span><span class="sxs-lookup"><span data-stu-id="3eb59-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="3eb59-131">Før du kjører veiviseren, må du kontrollere at du har definert navnene på standardlokasjon på Lager-siden.</span><span class="sxs-lookup"><span data-stu-id="3eb59-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="see-also"></a><span data-ttu-id="3eb59-132">Se også</span><span class="sxs-lookup"><span data-stu-id="3eb59-132">See also</span></span>
--------

[<span data-ttu-id="3eb59-133">Opprette et nytt oppsett for lager (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3eb59-133">Create a new warehouse layout (Task guide)</span></span>](tasks/create-new-warehouse-layout.md)

