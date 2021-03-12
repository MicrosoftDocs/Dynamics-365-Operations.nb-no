---
title: Beregne en stykkliste ved hjelp av en struktur med flere nivåer (februar 2016)
description: Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på flere nivåer som er basert på kostarket.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f07bab0bab5553764982b44d9b135b4baa8310f9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987610"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="40f34-103">Beregne en stykkliste ved hjelp av en struktur med flere nivåer (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="40f34-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40f34-104">Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på flere nivåer som er basert på kostarket.</span><span class="sxs-lookup"><span data-stu-id="40f34-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="40f34-105">Det er den sjuende oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="40f34-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="40f34-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="40f34-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="40f34-107">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="40f34-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="40f34-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="40f34-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="40f34-109">Velg produkt BOM_1.</span><span class="sxs-lookup"><span data-stu-id="40f34-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="40f34-110">Klikk på Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="40f34-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="40f34-111">Klikk på Varepris.</span><span class="sxs-lookup"><span data-stu-id="40f34-111">Click Item price.</span></span>
5. <span data-ttu-id="40f34-112">Klikk på Beregn varekostnad.</span><span class="sxs-lookup"><span data-stu-id="40f34-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="40f34-113">Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="40f34-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="40f34-114">Angi eller velg en verdi i Etterkalkuleringsversjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="40f34-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="40f34-115">Velg Etterkalkuleringsversjon 20, fordi den planlagte kostnadstypen og nedbrytingsmodusen er Flere nivåer.</span><span class="sxs-lookup"><span data-stu-id="40f34-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="40f34-116">Modusen Nedbryting på flere nivåer gjelder for planlagte kostnader og simuleringer.</span><span class="sxs-lookup"><span data-stu-id="40f34-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="40f34-117">Den brukes ikke for standardkostnad.</span><span class="sxs-lookup"><span data-stu-id="40f34-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="40f34-118">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="40f34-118">Click OK.</span></span>
8. <span data-ttu-id="40f34-119">Klikk på Vis beregningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="40f34-119">Click View calculation details.</span></span>
    * <span data-ttu-id="40f34-120">Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="40f34-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="40f34-121">I dette tilfellet ser du hvordan BOM_2 er beregnet ved å ta hensyn til råvaren, prosessen og administrasjonskostnadene med totalt 29,40 i stedet for standardkostnad på 10 som ble aktivert i den første oppgaveveiledningen i denne serien.</span><span class="sxs-lookup"><span data-stu-id="40f34-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="40f34-122">Klikk på fanen Kostark.</span><span class="sxs-lookup"><span data-stu-id="40f34-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="40f34-123">Går vi til fanen Kostark, er totaler per kostgruppe forskjellige sammenlignet med beregningen utført i den forrige oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="40f34-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="40f34-124">Velg Flere i Nivå-feltet.</span><span class="sxs-lookup"><span data-stu-id="40f34-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="40f34-125">Når du velger Flere, klassifiseres kostnadene i henhold til sammensetningen av BOM_2, der 10 er avledet fra M1-kostnadsgruppen (ITEM_C), og 15,60 er avledet fra produksjonen der kostgruppen er L2.</span><span class="sxs-lookup"><span data-stu-id="40f34-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="40f34-126">Indirekte kostnader varierer også.</span><span class="sxs-lookup"><span data-stu-id="40f34-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="40f34-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="40f34-127">Close the page.</span></span>
12. <span data-ttu-id="40f34-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="40f34-128">Close the page.</span></span>

