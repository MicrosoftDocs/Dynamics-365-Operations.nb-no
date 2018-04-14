---
title: Kostnadsobjektdimensjoner
description: "Når du analyserer kostnader, kan du bruke kostnadelementdimensjoner til å bestemme hvor kostnader flyter til. Du bruker kostnadsobjektdimensjoner brukes til å bestemme hvor du skal tildele kostnader. Dette emnet gir informasjon om kostnadsobjektdimensjoner."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a6c93252f95e3c07e1929d70467f6aa8d43af593
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="cost-object-dimensions"></a><span data-ttu-id="41645-105">Kostnadsobjektdimensjoner</span><span class="sxs-lookup"><span data-stu-id="41645-105">Cost object dimensions</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="41645-106">Når du analyserer kostnader, kan du bruke kostnadelementdimensjoner til å bestemme hvor kostnader flyter til.</span><span class="sxs-lookup"><span data-stu-id="41645-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="41645-107">Du bruker kostnadsobjektdimensjoner brukes til å bestemme hvor du skal tildele kostnader.</span><span class="sxs-lookup"><span data-stu-id="41645-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="41645-108">Dette emnet gir informasjon om kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="41645-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="41645-109">Et kostnadsobjekt kan være en hvilken som helst type objekt du vil beregne, fordele kostnader til eller måle direkte.</span><span class="sxs-lookup"><span data-stu-id="41645-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="41645-110">Vanlige kostnadsobjekter omfatter produkter, prosjekter, ressurser, avdelinger, kostsentre og geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="41645-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="41645-111">Ledelsen bruker kostnadsobjekter til å kvantifisere kostnader og utføre fortjenesteanalyse.</span><span class="sxs-lookup"><span data-stu-id="41645-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="41645-112">Kostnadsobjektdimensjoner og medlemmer av kostnadsobjektdimensjon</span><span class="sxs-lookup"><span data-stu-id="41645-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="41645-113">Kostobjekter kalles også *kostnadsobjektdimensjoner*.</span><span class="sxs-lookup"><span data-stu-id="41645-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="41645-114">Etter at du har bestemt deg for hvilken enhet kostnadsobjektdimensjonen skal referere til, må du angi de individuelle dimensjonsverdiene eller importere dem til kostnadsregnskapet fra andre kildesystemer.</span><span class="sxs-lookup"><span data-stu-id="41645-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="41645-115">Disse individuelle dimensjonsverdiene kalles *medlemmer av kostnadsobjektdimensjon*.</span><span class="sxs-lookup"><span data-stu-id="41645-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="41645-116">Du vil for eksempel bruke finansdimensjonen som heter Kostsenter som kostnadsobjektdimensjon.</span><span class="sxs-lookup"><span data-stu-id="41645-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="41645-117">Hvis du vil se hvordan kostnader flyter for individuelle kostsentre, må du importere medlemmene av kostnadsobjektdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="41645-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="41645-118">I så fall er medlemmene av kostnadsobjektdimensjonen de faktiske kostsentrene, for eksempel salg, produksjon, administrasjon og geografiske steder.</span><span class="sxs-lookup"><span data-stu-id="41645-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="41645-119">Skjermbildet nedenfor viser et eksempel på kostsentre som kostnadsobjektdimensjonen med de faktiske kostsentrene som medlemmene av kostnadsobjektdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="41645-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="41645-120">[![kostnad-objekt-dimensjoner](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="41645-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="41645-121">Importere medlemmer av kostnadsobjektdimensjon gjennom datakoblinger</span><span class="sxs-lookup"><span data-stu-id="41645-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="41645-122">Hvis du vil gjøre import av medlemmer av kostnadsobjektdimensjon enklere, kan du bruke datakoblinger til å hente verdiene fra enhetene som du vil bruke som kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="41645-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="41645-123">Du kan bruke det forhåndsbygde datakoblingene eller egendefinerte koblinger som du bygger.</span><span class="sxs-lookup"><span data-stu-id="41645-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>




