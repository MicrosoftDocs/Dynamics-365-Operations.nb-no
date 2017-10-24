---
title: Fysiske og finansielle oppdateringer
description: "Dette emnet gir en oversikt over hvilke typer transaksjoner som øker eller reduserer lagerantallet."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 01121e7330efe00daa84ca274e4e94bb324175bb
ms.contentlocale: nb-no
ms.lasthandoff: 10/13/2017

---

# <a name="physical-and-financial-updates"></a><span data-ttu-id="a04a1-103">Fysiske og finansielle oppdateringer</span><span class="sxs-lookup"><span data-stu-id="a04a1-103">Physical and financial updates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a04a1-104">Dette emnet gir en oversikt over hvilke typer transaksjoner som øker eller reduserer lagerantallet.</span><span class="sxs-lookup"><span data-stu-id="a04a1-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="a04a1-105">Lagertransaksjoner kan oppdateres fysisk og finansielt i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a04a1-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a04a1-106">Noen typer fysiske og finansielle transaksjoner øker lagerantallet, mens andre reduserer antallet.</span><span class="sxs-lookup"><span data-stu-id="a04a1-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="a04a1-107">Fysiske økninger</span><span class="sxs-lookup"><span data-stu-id="a04a1-107">Physical increases</span></span>
<span data-ttu-id="a04a1-108">Når en fysisk transaksjon blir postert, er statusen til transaksjonsposten **Mottatt**.</span><span class="sxs-lookup"><span data-stu-id="a04a1-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="a04a1-109">Følgende transaksjoner regnes som fysisk økning:</span><span class="sxs-lookup"><span data-stu-id="a04a1-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="a04a1-110">Bestillingsmottak</span><span class="sxs-lookup"><span data-stu-id="a04a1-110">Purchase order receipt</span></span>
-   <span data-ttu-id="a04a1-111">Retur av følgeseddel for salgsordre</span><span class="sxs-lookup"><span data-stu-id="a04a1-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="a04a1-112">Rapportere en produksjonsordre som avsluttet</span><span class="sxs-lookup"><span data-stu-id="a04a1-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="a04a1-113">Etter produkt på en produksjonsordreplukkliste</span><span class="sxs-lookup"><span data-stu-id="a04a1-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="a04a1-114">Finansiell økning</span><span class="sxs-lookup"><span data-stu-id="a04a1-114">Financial increases</span></span>
<span data-ttu-id="a04a1-115">Når en finansiell tilgangstransaksjon blir postert, blir statusen til transaksjonsposten som øker antallet, satt til **Kjøpt**.</span><span class="sxs-lookup"><span data-stu-id="a04a1-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="a04a1-116">Følgende transaksjoner regnes som finansiell økning:</span><span class="sxs-lookup"><span data-stu-id="a04a1-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="a04a1-117">Leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="a04a1-117">Vendor invoice</span></span>
-   <span data-ttu-id="a04a1-118">Salgsordrefaktura for en retur</span><span class="sxs-lookup"><span data-stu-id="a04a1-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="a04a1-119">Produksjonsordrekostnad</span><span class="sxs-lookup"><span data-stu-id="a04a1-119">Production order costing</span></span>
-   <span data-ttu-id="a04a1-120">Lagerjournaler med positivt antall, for eksempel bevegelse, resultat, opptelling, stykklister og overføring</span><span class="sxs-lookup"><span data-stu-id="a04a1-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="a04a1-121">Transaksjoner som øker antallet</span><span class="sxs-lookup"><span data-stu-id="a04a1-121">Transactions that increase quantity</span></span>
<span data-ttu-id="a04a1-122">Transaksjoner som øker antallet posteres til løpende gjennomsnittlig kostpris.</span><span class="sxs-lookup"><span data-stu-id="a04a1-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="a04a1-123">Finance and Operations beregner en løpende gjennomsnittlig kostpris basert på kostnaden til hver av disse transaksjonene for hver lagerdimensjon som spores økonomisk.</span><span class="sxs-lookup"><span data-stu-id="a04a1-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="a04a1-124">Hvis du vil ha informasjon om løpende gjennomsnittlige kostpriser, se [Løpende gjennomsnittlig kostpris](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="a04a1-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="a04a1-125">Transaksjoner som reduserer antallet</span><span class="sxs-lookup"><span data-stu-id="a04a1-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="a04a1-126">Finance and Operations bruker beregnet løpende gjennomsnitt for kostpris når det posteres en transaksjon som reduserer antallet, uavhengig av lagermodellen som er tilknyttet den beholdningen.</span><span class="sxs-lookup"><span data-stu-id="a04a1-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="a04a1-127">Transaksjonen som reduserer antallet, må ikke tidligere ha vært knyttet til en annen transaksjon før postering.</span><span class="sxs-lookup"><span data-stu-id="a04a1-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="a04a1-128">Hvis den fysiske lagerbeholdningen blir negativ, bruker Finance and Operations lagerkosten som er definert for varen på **Vare**-siden.</span><span class="sxs-lookup"><span data-stu-id="a04a1-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="a04a1-129">**Obs!** Hvis multisite-funksjonalitet er aktivert, blir denne kostnaden i stedet den definerte lagerkostnaden som defineres for et område på siden **Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a04a1-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="a04a1-130">Fysisk avgang i forhold til økonomiske avganger</span><span class="sxs-lookup"><span data-stu-id="a04a1-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="a04a1-131">Når en fysisk avgangstransaksjon blir postert, er statusen til transaksjonsposten **Fratrukket**.</span><span class="sxs-lookup"><span data-stu-id="a04a1-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="a04a1-132">Følgende transaksjoner regnes som fysisk avgang:</span><span class="sxs-lookup"><span data-stu-id="a04a1-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="a04a1-133">Plukklistejournal for produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="a04a1-133">Production order picking list journal</span></span>
-   <span data-ttu-id="a04a1-134">Følgeseddel for salgsordre</span><span class="sxs-lookup"><span data-stu-id="a04a1-134">Sales order packing slip</span></span>
-   <span data-ttu-id="a04a1-135">Følgeseddel for bestillingsretur</span><span class="sxs-lookup"><span data-stu-id="a04a1-135">Purchase order packing slip return</span></span>

<span data-ttu-id="a04a1-136">Når en økonomisk transaksjon blir postert, er statusen til transaksjonsposten **Solgt**.</span><span class="sxs-lookup"><span data-stu-id="a04a1-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="a04a1-137">Følgende transaksjoner regnes som økonomiske avganger:</span><span class="sxs-lookup"><span data-stu-id="a04a1-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="a04a1-138">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="a04a1-138">Ending a production order</span></span>
-   <span data-ttu-id="a04a1-139">Salgsordrefaktura</span><span class="sxs-lookup"><span data-stu-id="a04a1-139">Sales order invoice</span></span>
-   <span data-ttu-id="a04a1-140">Leverandørfakturaretur</span><span class="sxs-lookup"><span data-stu-id="a04a1-140">Vendor invoice return</span></span>
-   <span data-ttu-id="a04a1-141">Lagerjournaler med negativt antall, for eksempel bevegelse, resultat, opptelling, stykklister og overføring</span><span class="sxs-lookup"><span data-stu-id="a04a1-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="a04a1-142">Transaksjoner som reduserer antallet posteres til løpende gjennomsnittlig kostpris.</span><span class="sxs-lookup"><span data-stu-id="a04a1-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="a04a1-143">Prosedyren for lagerlukking er derfor nødvendig for å utligne avgangstransaksjoner mot tilgangstransaksjoner på grunnlag av lagermodellen som er tilordnet hver vare.</span><span class="sxs-lookup"><span data-stu-id="a04a1-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>




