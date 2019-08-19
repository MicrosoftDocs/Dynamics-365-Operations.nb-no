---
title: Kostnadselementdimensjoner
description: Som en av de viktige søylene i kostnadsregnskap, brukes kostnadelementdimensjoner til å kategorisere og spore hvor kostnadene flyter til.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 037d4971fe0a5a9d08f0ed20d2482b8feb9aa4f2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841615"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="957a2-103">Kostnadselementdimensjoner</span><span class="sxs-lookup"><span data-stu-id="957a2-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="957a2-104">Som en av de viktige søylene i kostnadsregnskap, brukes kostnadelementdimensjoner til å kategorisere og spore hvor kostnadene flyter til.</span><span class="sxs-lookup"><span data-stu-id="957a2-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="957a2-105">Et kostnadselement tilsvarer et kostnadsrelevant element i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="957a2-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="957a2-106">I utgangspunktet kan det være en hvilken som helst type element på laveste nivå i et firma der kostnadene kan flyte til.</span><span class="sxs-lookup"><span data-stu-id="957a2-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="957a2-107">Kostnadselementene som konsept strekker seg fra finanskontoer til alle kostnadsrelevante ressurser.</span><span class="sxs-lookup"><span data-stu-id="957a2-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="957a2-108">Kostnadsregnskap støtter for øyeblikket finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="957a2-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="957a2-109">To typer kostnadselementer</span><span class="sxs-lookup"><span data-stu-id="957a2-109">Two types of cost elements</span></span>
<span data-ttu-id="957a2-110">Det finnes to typer kostnadselementer: primære kostnadselementer og sekundære kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="957a2-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="957a2-111">I tabellen nedenfor beskrives forskjellen mellom de to typene.</span><span class="sxs-lookup"><span data-stu-id="957a2-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="957a2-112"><strong>Primære kostnadselementer</strong></span><span class="sxs-lookup"><span data-stu-id="957a2-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="957a2-113"><strong>Sekundærkostnadselementer</strong></span><span class="sxs-lookup"><span data-stu-id="957a2-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="957a2-114">De primære kostnadselementer representerer kostflyten fra finansbokføring til kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="957a2-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="957a2-115">Kostnadselementstrukturen tilsvarer kontostrukturen for resultat i økonomimodulen, der en kostnadselement kan tilsvare en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="957a2-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="957a2-116">Ikke alle hovedkontoer vil nødvendigvis vises som kostnadselementer avhengig av forretningsbehovene.</span><span class="sxs-lookup"><span data-stu-id="957a2-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="957a2-117">Eksempler på primære kostnadselementer:</span><span class="sxs-lookup"><span data-stu-id="957a2-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="957a2-118">Solgte varers kost (COG-er)</span><span class="sxs-lookup"><span data-stu-id="957a2-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="957a2-119">Indirekte materialkostnader</span><span class="sxs-lookup"><span data-stu-id="957a2-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="957a2-120">Personalkostnader</span><span class="sxs-lookup"><span data-stu-id="957a2-120">Personnel costs</span></span></li>
<li><span data-ttu-id="957a2-121">Energikostnader</span><span class="sxs-lookup"><span data-stu-id="957a2-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="957a2-122">Sekundære kostnadselementer representerer kostflyten internt fordi disse kostnadene opprettes og brukes bare i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="957a2-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="957a2-123">De brukes til å sikre at kilden til kostnadene kan spores.</span><span class="sxs-lookup"><span data-stu-id="957a2-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="957a2-124">Disse kostnadselementene brukes i kostnadsfordelinger og beregninger for indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="957a2-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="957a2-125">Eksempler på sekundære kostnadselementer:</span><span class="sxs-lookup"><span data-stu-id="957a2-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="957a2-126">Produksjonskostnader</span><span class="sxs-lookup"><span data-stu-id="957a2-126">Production costs</span></span></li>
<li><span data-ttu-id="957a2-127">Produksjon, materiale og administrasjonskostnader for markedsføring</span><span class="sxs-lookup"><span data-stu-id="957a2-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="957a2-128">Kostnadselementdimensjoner og medlemmer av kostnadselementdimensjonen</span><span class="sxs-lookup"><span data-stu-id="957a2-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="957a2-129">Kostnadselementer kalles *kostnadselementdimensjoner* .</span><span class="sxs-lookup"><span data-stu-id="957a2-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="957a2-130">De enkelte dimensjonsverdiene kalles *medlemmer av kostnadselementdimensjon*.</span><span class="sxs-lookup"><span data-stu-id="957a2-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="957a2-131">Du har for eksempel en amerikansk kontoplanstruktur (COA) som er grunnlaget for den lovbestemte rapporteringen.</span><span class="sxs-lookup"><span data-stu-id="957a2-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="957a2-132">Denne kontoplanen brukes som kostnadselementdimensjon.</span><span class="sxs-lookup"><span data-stu-id="957a2-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="957a2-133">Kontoene, som er primært kostnadselementer, representeres som medlemmer av kostnadselementdimensjon i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="957a2-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="957a2-134">Følgende skjermbilde viser et eksempel på hovedkontoer som kostnadselementdimensjonen med de faktiske hovedkontoene som medlemmene av kostnadselementdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="957a2-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="957a2-135">[![kostnad-element-dimensjoner](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="957a2-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="957a2-136">Importere medlemmer av kostnadselementdimensjon gjennom datakoblinger</span><span class="sxs-lookup"><span data-stu-id="957a2-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="957a2-137">For å forenkle oppsettet av medlemmene av kostnadselementdimensjoner i kostnadsregnskap, kan du bruke datakoblinger som er forhåndsbygget eller bygge dine egne for å hente de primære kostnadselementer fra ett eller flere kildesystemer.</span><span class="sxs-lookup"><span data-stu-id="957a2-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="957a2-138">Informasjon om implementering</span><span class="sxs-lookup"><span data-stu-id="957a2-138">Implementation considerations</span></span>
<span data-ttu-id="957a2-139">Når kostnadselementer representerer det laveste nivået av kostnadsdetaljer, må du kontrollere at alle kostnadselementer som er nødvendig for å lage lederrapporteringen er tatt med når du implementerer kostnadselementstrukturen.</span><span class="sxs-lookup"><span data-stu-id="957a2-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="957a2-140">Det kan være vanskelig å finne et passende antall kostnadselementer for kostnadskontroll.</span><span class="sxs-lookup"><span data-stu-id="957a2-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="957a2-141">Når du har tusenvis av kostnadselementer, kan det være vanskelig å styre hvert kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="957a2-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="957a2-142">Du kan eventuelt gruppere kostnadselementer og styre kostnadskontroll på et aggregert nivå.</span><span class="sxs-lookup"><span data-stu-id="957a2-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>



