---
title: Forberede vedlikehold av standard kostpris for produserte varer
description: Dette emnet beskriver fremgangsmåten for å forberede vedlikehold av kostnader for produserte varer.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6944782ac236a3f414b1cadfb12b0f0d8c1115b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821519"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="93511-103">Forberede vedlikehold av standard kostpris for produserte varer</span><span class="sxs-lookup"><span data-stu-id="93511-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93511-104">Dette emnet beskriver fremgangsmåten for å forberede vedlikehold av kostnader for produserte varer.</span><span class="sxs-lookup"><span data-stu-id="93511-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="93511-105">Fremgangsmåten for produserte varierer litt fra trinnene for innkjøpte varer.</span><span class="sxs-lookup"><span data-stu-id="93511-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="93511-106">Reglene som tilordnes produserte varer kan påvirke kostnadsberegningene for de overordnede produserte varene.</span><span class="sxs-lookup"><span data-stu-id="93511-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="93511-107">Når du skal forberede vedlikehold av kostpris for produserte varer, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="93511-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="93511-108">Tilordne en varemodellgruppe til den produserte varen.</span><span class="sxs-lookup"><span data-stu-id="93511-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="93511-109">Varemodellgruppen identifiserer at standard kostpris brukes.</span><span class="sxs-lookup"><span data-stu-id="93511-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="93511-110">Tilordne en varegruppe til den produserte varen.</span><span class="sxs-lookup"><span data-stu-id="93511-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="93511-111">Varegruppen inneholder finanskontoer som gjelder for den produserte varen.</span><span class="sxs-lookup"><span data-stu-id="93511-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="93511-112">Finanskontoen for en produsert vare som har en lagermodell med standard kostpris, omfatter flere produksjonsprisavvik, kostnadsendringsavvik og lagerkostnadsrevalueringen.</span><span class="sxs-lookup"><span data-stu-id="93511-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="93511-113">Tilordne lagermåleenheten til varen.</span><span class="sxs-lookup"><span data-stu-id="93511-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="93511-114">Varens kost uttrykkes alltid i varens lagermåleenhet.</span><span class="sxs-lookup"><span data-stu-id="93511-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="93511-115">Ikke tilordne en kostgruppe til den produserte varer med mindre varen skal behandles som en innkjøpt vare.</span><span class="sxs-lookup"><span data-stu-id="93511-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="93511-116">Tilordne en stykklisteberegningsgruppe til den produserte varen.</span><span class="sxs-lookup"><span data-stu-id="93511-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="93511-117">Varens stykklisteberegningsgruppe definerer advarselsbetingelsene som gjelder.</span><span class="sxs-lookup"><span data-stu-id="93511-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="93511-118">Når en stykklisteberegning er fullført, kan dermed advarslene genereres om mulige kilder for beregningsfeil.</span><span class="sxs-lookup"><span data-stu-id="93511-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="93511-119">En advarselsmelding kan for eksempel angi når en aktiv stykkliste eller rute ikke eksisterer.</span><span class="sxs-lookup"><span data-stu-id="93511-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="93511-120">Stykklisteberegningsgruppen inneholder en stopp nedbryting-regel som angir når en produsert vare skal behandles som en innkjøpt vare.</span><span class="sxs-lookup"><span data-stu-id="93511-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="93511-121">Hvis den produserte varen har konstantkostnader, tilordner du et standard ordreantall til den.</span><span class="sxs-lookup"><span data-stu-id="93511-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="93511-122">Standard ordreantall er en regnskapspartistørrelse for amortisering av konstante kostnader.</span><span class="sxs-lookup"><span data-stu-id="93511-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="93511-123">Eksempler på konstante kostnader omfatter oppstillingstid i ruteoperasjoner og en konstant komponentmengde i stykklisten.</span><span class="sxs-lookup"><span data-stu-id="93511-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="93511-124">Definer stykklisten for den produserte varen.</span><span class="sxs-lookup"><span data-stu-id="93511-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="93511-125">En eller flere stykklisteversjoner kan defineres for en produsert vare.</span><span class="sxs-lookup"><span data-stu-id="93511-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="93511-126">Kontroller at versjonene du vil ha, er markert som godkjent og aktive, og at de gjelder i det datointervallet du vil ha.</span><span class="sxs-lookup"><span data-stu-id="93511-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="93511-127">Stykklisteversjonen kan gjelde for hele firmaet eller bare for området.</span><span class="sxs-lookup"><span data-stu-id="93511-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="93511-128">Definer rutingen for den produserte varen.</span><span class="sxs-lookup"><span data-stu-id="93511-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="93511-129">En eller flere ruteversjoner kan defineres for en produsert vare.</span><span class="sxs-lookup"><span data-stu-id="93511-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="93511-130">Kontroller at versjonene du vil ha, er markert som godkjent og aktive, og at de gjelder i det datointervallet du vil ha.</span><span class="sxs-lookup"><span data-stu-id="93511-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="93511-131">Ruteversjonen kan bare gjelde for området.</span><span class="sxs-lookup"><span data-stu-id="93511-131">The route version must be site-specific.</span></span>

<span data-ttu-id="93511-132">Hvis du vil bruke rutinginformasjon til kostnadsformål, kreves det flere klargjøringstrinn.</span><span class="sxs-lookup"><span data-stu-id="93511-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="93511-133">Kostnadskategoriene som er tilordet ruteoperasjoner, må for eksempel korrigeres og fullføres.</span><span class="sxs-lookup"><span data-stu-id="93511-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="93511-134">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="93511-134">Related topics</span></span>
--------

[<span data-ttu-id="93511-135">Amortisere konstante kostnader for en produsert vare</span><span class="sxs-lookup"><span data-stu-id="93511-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="93511-136">Definere produkter som kan være produsert eller fremskaffet</span><span class="sxs-lookup"><span data-stu-id="93511-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]