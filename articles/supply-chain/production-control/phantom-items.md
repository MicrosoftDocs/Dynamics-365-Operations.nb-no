---
title: Fantomvarer
description: Dette emnet beskriver detaljer hvordan linjetype Fantom kan brukes for linjene i en stykkliste (BOM) og en formel i Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: 
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---

# <a name="phantom-items"></a><span data-ttu-id="635e8-103">Fantomvarer</span><span class="sxs-lookup"><span data-stu-id="635e8-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="635e8-104">Dette emnet beskriver detaljer hvordan linjetype Fantom kan brukes for linjene i en stykkliste (BOM) og en formel.</span><span class="sxs-lookup"><span data-stu-id="635e8-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="635e8-105">I illustrasjonen nedenfor (a) er stykklisten for produkt H og der F og G, og (b) er rutearket for produkt H-og del F.</span><span class="sxs-lookup"><span data-stu-id="635e8-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Produkt H og del F](media/product-H-part-F.png)


<span data-ttu-id="635e8-107">Denne illustrasjonen viser et eksempel på en stykklistestruktur i to nivåer.</span><span class="sxs-lookup"><span data-stu-id="635e8-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="635e8-108">Det ferdige produktet H representerer et produkt i en maskinmontering.</span><span class="sxs-lookup"><span data-stu-id="635e8-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="635e8-109">Maskinmonteringen består av to deler, en elektrisk enhet (F) med to materialer (A og B) og en gruppe med emballasje (G) som også har to materialer (C og D).</span><span class="sxs-lookup"><span data-stu-id="635e8-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="635e8-110">Et annet materiale (E) brukes under den generelle monteringen av maskinen.</span><span class="sxs-lookup"><span data-stu-id="635e8-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Produkt H og del F](media/product-H-part-B.png)

<span data-ttu-id="635e8-112">Den forrige illustrasjonen representerer konstruksjonsstykklisten for produkt H. Denne strukturen gir god oversikt over delene og komponentene i den generelle maskinmonteringen.</span><span class="sxs-lookup"><span data-stu-id="635e8-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="635e8-113">Men selv om produktdesignere kanskje vil se stykklisten representert på denne måten, representerer denne strukturen kanskje ikke riktig måten maskinen bygges i butikken.</span><span class="sxs-lookup"><span data-stu-id="635e8-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="635e8-114">Konstruksjonsstykklisten i den forrige illustrasjonen angir for eksempel at den elektriske enheten F er montert som en egen del i en egen arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="635e8-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="635e8-115">I butikken kan det kanskje være mer optimalt å montere den elektriske enheten som en del av den generelle maskinmonteringen, ikke som en egen arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="635e8-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="635e8-116">Denne konstruksjonsstykklisten angir også at del G er en egen del.</span><span class="sxs-lookup"><span data-stu-id="635e8-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="635e8-117">I denne strukturen representerer imidlertid ikke del G en fysisk del, men en samling av emballasje.</span><span class="sxs-lookup"><span data-stu-id="635e8-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="635e8-118">Derfor, selv om en konstruksjonsstykkliste gir mye for pengene for utformingen av et produkt og vedlikehold av denne utformingen, er det kanskje ikke den mest logiske måten å støtte produksjonsprosessen av produktet.</span><span class="sxs-lookup"><span data-stu-id="635e8-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="635e8-119">En produksjonstykkliste representerer derimot den beste måten å bygge et produkt på.</span><span class="sxs-lookup"><span data-stu-id="635e8-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="635e8-120">Illustrasjonen nedenfor viser hvordan den forrige konstruksjonsstykklisten er gått over i en produksjonsstykkliste.</span><span class="sxs-lookup"><span data-stu-id="635e8-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="635e8-121">I denne illustrasjonen (a) er stykklisten for produkt H, og b er rutearket for produkt H.</span><span class="sxs-lookup"><span data-stu-id="635e8-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="635e8-122">I denne strukturen kan du se at del F og G ikke er nevnt, og materialene som disse delene består av, har blitt forhøyet til det neste stykklistenivået.</span><span class="sxs-lookup"><span data-stu-id="635e8-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="635e8-123">I motsetning til konstruksjonsstykklisten, som har to operasjonsark, har produksjonsstykklisten bare ett ark operasjonsark.</span><span class="sxs-lookup"><span data-stu-id="635e8-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="635e8-124">Emballasjeoperasjonen som var koblet til en del G, er også forhøyet og er nå en del av operasjonsarket for produkt H. Montering av elektriske enheten er den første operasjonen.</span><span class="sxs-lookup"><span data-stu-id="635e8-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="635e8-125">Denne rekkefølgen kan være lur, fordi denne enheten brukes i den neste operasjonen, som er maskinmonteringen.</span><span class="sxs-lookup"><span data-stu-id="635e8-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="635e8-126">Den siste operasjon er emballasjeoperasjonen, som bruker to emballasjematerialer (C og D).</span><span class="sxs-lookup"><span data-stu-id="635e8-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="635e8-127">I Microsoft Dynamics 365 for Finance and Operations aktiveres overgangen mellom konstruksjonsstykklisten og produksjonsstykklisten gjennom stykklistelinjetypen Fantom.</span><span class="sxs-lookup"><span data-stu-id="635e8-127">In Microsoft Dynamics 365 for Finance and Operations, the transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="635e8-128">Som begrepet "fantom" hentyder, er del F og G forsvunnet under overgangen mellom de to stykklistetypene.</span><span class="sxs-lookup"><span data-stu-id="635e8-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="635e8-129">I dette eksemplet brukes linjetypen Fantom på stykklistelinjene for del F og G i konstruksjonsstykklisten.</span><span class="sxs-lookup"><span data-stu-id="635e8-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="635e8-130">Når det opprettes en produksjons- eller partiordre, kopieres konstruksjonsstykklisten til produksjons- eller partiordren.</span><span class="sxs-lookup"><span data-stu-id="635e8-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="635e8-131">Deretter, når ordren er beregnet, oppstår overgangen fra konstruksjonsstykklisten til produksjonsstykklisten, som vist i illustrasjonene ovenfor.</span><span class="sxs-lookup"><span data-stu-id="635e8-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="635e8-132">Fra operasjonsarket i den andre illustrasjonen er emballasjemateriale C og D inndata for operasjonen.</span><span class="sxs-lookup"><span data-stu-id="635e8-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="635e8-133">Stykklistestrukturer på flere nivåer for fantom</span><span class="sxs-lookup"><span data-stu-id="635e8-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="635e8-134">Linjetype Fantom kan brukes i stykklistestrukturer på flere nivåer, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="635e8-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="635e8-135">I denne illustrasjonen (a) er stykklisten for produkt G, og (b) er rutearket for del E og F og produkt G.</span><span class="sxs-lookup"><span data-stu-id="635e8-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Produkt G og del F med ruteark](media/product-G-route-sheet-G.png)


<span data-ttu-id="635e8-137">Illustrasjonen nedenfor viser den resulterende produksjonsstykklisten og rutearket hvis stykklistelinjene for dele E og F er konfigurert slik at linjetypen er Fantom.</span><span class="sxs-lookup"><span data-stu-id="635e8-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="635e8-138">I denne illustrasjonen (a) er stykklisten for produkt G, og (b) er rutearket for produkt G.</span><span class="sxs-lookup"><span data-stu-id="635e8-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Produkt G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="635e8-140">Fantom og rutenettverk</span><span class="sxs-lookup"><span data-stu-id="635e8-140">Phantom and route network</span></span>
<span data-ttu-id="635e8-141">Fantomstykklister kan også brukes for en stykkliste som har et rutenettverk.</span><span class="sxs-lookup"><span data-stu-id="635e8-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="635e8-142">I et rutenettverk kjøres én eller flere operasjoner parallelt.</span><span class="sxs-lookup"><span data-stu-id="635e8-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="635e8-143">Illustrasjonen nedenfor viser et eksempel på et rutenettverk som brukes i en stykkliste med flere nivåer.</span><span class="sxs-lookup"><span data-stu-id="635e8-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="635e8-144">I denne illustrasjonen (a) er stykklisten for produkt G og del F, og (b) er rutearket for produkt G og del F, som har et rutenettverk.</span><span class="sxs-lookup"><span data-stu-id="635e8-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Produkt G og del F](media/product-G-part-F.png)


<span data-ttu-id="635e8-146">I illustrasjonen nedenfor (a) er stykklisten for produkt G og del F, og (b) er rutearket for produkt G-og del F.</span><span class="sxs-lookup"><span data-stu-id="635e8-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Produkt G og del F med ruteark](media/product-G-part-F-with-route-sheet.png)

