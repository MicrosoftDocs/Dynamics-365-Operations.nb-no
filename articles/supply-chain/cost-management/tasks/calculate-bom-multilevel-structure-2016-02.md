--- 
title: "Beregne en stykkliste ved hjelp av en struktur med flere nivåer (bare februar 2016)"
description: "Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på flere nivåer som er basert på kostarket."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16c2cacaf70df5455c3ed49b8dcb5756e89f8cb8
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a><span data-ttu-id="ea97d-103">Beregne en stykkliste ved hjelp av en struktur med flere nivåer (bare februar 2016)</span><span class="sxs-lookup"><span data-stu-id="ea97d-103">Calculate a BOM by using a multilevel structure (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea97d-104">Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på flere nivåer som er basert på kostarket.</span><span class="sxs-lookup"><span data-stu-id="ea97d-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="ea97d-105">Det er den sjuende oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="ea97d-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="ea97d-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="ea97d-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="ea97d-107">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="ea97d-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ea97d-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ea97d-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ea97d-109">Velg produkt BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ea97d-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="ea97d-110">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ea97d-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="ea97d-111">Klikk Varepris.</span><span class="sxs-lookup"><span data-stu-id="ea97d-111">Click Item price.</span></span>
5. <span data-ttu-id="ea97d-112">Klikk Beregn varekostnad.</span><span class="sxs-lookup"><span data-stu-id="ea97d-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="ea97d-113">Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="ea97d-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="ea97d-114">Angi eller velg en verdi i Etterkalkuleringsversjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="ea97d-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="ea97d-115">Velg Etterkalkuleringsversjon 20, fordi den planlagte kostnadstypen og nedbrytingsmodusen er Flere nivåer.</span><span class="sxs-lookup"><span data-stu-id="ea97d-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="ea97d-116">Modusen Nedbryting på flere nivåer gjelder for planlagte kostnader og simuleringer.</span><span class="sxs-lookup"><span data-stu-id="ea97d-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="ea97d-117">Den brukes ikke for standardkostnad.</span><span class="sxs-lookup"><span data-stu-id="ea97d-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="ea97d-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ea97d-118">Click OK.</span></span>
8. <span data-ttu-id="ea97d-119">Klikk Vis beregningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="ea97d-119">Click View calculation details.</span></span>
    * <span data-ttu-id="ea97d-120">Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="ea97d-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="ea97d-121">I dette tilfellet ser du hvordan BOM_2 er beregnet ved å ta hensyn til råvaren, prosessen og administrasjonskostnadene med totalt 29,40 i stedet for standardkostnad på 10 som ble aktivert i den første oppgaveveiledningen i denne serien.</span><span class="sxs-lookup"><span data-stu-id="ea97d-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="ea97d-122">Klikk kategorien Kostark.</span><span class="sxs-lookup"><span data-stu-id="ea97d-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="ea97d-123">Går vi til kategorien Kostark, er totaler per kostgruppe forskjellige sammenlignet med beregningen utført i den forrige oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="ea97d-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="ea97d-124">Velg Flere i Nivå-feltet.</span><span class="sxs-lookup"><span data-stu-id="ea97d-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="ea97d-125">Når du velger Flere, klassifiseres kostnadene i henhold til sammensetningen av BOM_2, der 10 er avledet fra M1-kostnadsgruppen (ITEM_C), og 15,60 er avledet fra produksjonen der kostgruppen er L2.</span><span class="sxs-lookup"><span data-stu-id="ea97d-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="ea97d-126">Indirekte kostnader varierer også.</span><span class="sxs-lookup"><span data-stu-id="ea97d-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="ea97d-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ea97d-127">Close the page.</span></span>
12. <span data-ttu-id="ea97d-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ea97d-128">Close the page.</span></span>


