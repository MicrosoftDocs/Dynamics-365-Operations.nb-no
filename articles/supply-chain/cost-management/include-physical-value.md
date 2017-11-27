---
title: Ta med fysisk verdi
description: "Du bruker avmerkingsboksen Ta med fysisk verdi i hurtigkategorien Lagermodell på Varemodellgrupper-siden til å angi om fysisk oppdaterte transaksjoner skal tas med i beregningen av løpende gjennomsnittlig kostpris for en vare."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ea8fe31588dd0768e0651c9e1e332212a00cde2
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="include-physical-value"></a><span data-ttu-id="70d2a-103">Ta med fysisk verdi</span><span class="sxs-lookup"><span data-stu-id="70d2a-103">Include physical value</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="70d2a-104">Du bruker avmerkingsboksen Ta med fysisk verdi i hurtigkategorien Lagermodell på Varemodellgrupper-siden til å angi om fysisk oppdaterte transaksjoner skal tas med i beregningen av løpende gjennomsnittlig kostpris for en vare.</span><span class="sxs-lookup"><span data-stu-id="70d2a-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="70d2a-105">Avmerkingsboksen **Ta med fysisk verdi** har følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="70d2a-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="70d2a-106">Verdi</span><span class="sxs-lookup"><span data-stu-id="70d2a-106">Value</span></span>    | <span data-ttu-id="70d2a-107">Resultat</span><span class="sxs-lookup"><span data-stu-id="70d2a-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70d2a-108">Valgt</span><span class="sxs-lookup"><span data-stu-id="70d2a-108">Selected</span></span> | <span data-ttu-id="70d2a-109">Både fysisk oppdaterte transaksjoner og økonomisk oppdaterte transaksjoner brukes til å beregne løpende gjennomsnittlig kostpris.</span><span class="sxs-lookup"><span data-stu-id="70d2a-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="70d2a-110">Avstem</span><span class="sxs-lookup"><span data-stu-id="70d2a-110">Cleared</span></span>  | <span data-ttu-id="70d2a-111">Bare økonomisk oppdaterte transaksjoner brukes til å beregne løpende gjennomsnittlig kostpris.</span><span class="sxs-lookup"><span data-stu-id="70d2a-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="70d2a-112">Avmerkingsboksen har litt forskjellige effekter, avhengig av hvilken lagermodell du bruker.</span><span class="sxs-lookup"><span data-stu-id="70d2a-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="70d2a-113">Hvis du merrker av for **Ta med fysisk verdi** når du bruker lagermodellen FIFO (først inn, først ut), LIFO (sist inn, først ut) eller LIFO-dato, vil en lagerlukking også medføre justeringer i fysisk oppdaterte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="70d2a-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="70d2a-114">Hvis du ikke merker merket av for **Ta med fysisk verdi** når du bruker disse lagermodellene, vil lagerlukking med bare utligne transaksjoner som er økonomisk oppdatert.</span><span class="sxs-lookup"><span data-stu-id="70d2a-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="70d2a-115">Når du bruker lagermodellene med avveid gjennomsnitt eller avveid gjennomsnittsdato, vil lagerlukking bare utligne økonomisk oppdaterte transaksjoner, uansett om du merker av for **Ta med fysisk verdi** eller ikke.</span><span class="sxs-lookup"><span data-stu-id="70d2a-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="70d2a-116">**Eksempel 1** Du har merket av for **Ta med fysisk verdi** og mottar følgende bestillinger:</span><span class="sxs-lookup"><span data-stu-id="70d2a-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="70d2a-117">En bestilling av et antall på 2 og en kostpris på USD 10,00 har en oppdatert følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="70d2a-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="70d2a-118">En bestilling av et antall på 3 og en kostpris på USD 12,00 har en oppdatert faktura.</span><span class="sxs-lookup"><span data-stu-id="70d2a-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="70d2a-119">I dette tilfellet, vil løpende gjennomsnittlig kostpris være USD 11,20, fordi både fysisk og økonomisk oppdaterte transaksjoner brukes til å beregne kostprisen.</span><span class="sxs-lookup"><span data-stu-id="70d2a-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="70d2a-120">**Eksempel 2** Du har ikke merket av for **Ta med fysisk verdi**, og kostprisen i vareoppsettet er USD 10,00.</span><span class="sxs-lookup"><span data-stu-id="70d2a-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="70d2a-121">Du mottar en bestilling av et antall på 20 og en kostpris på USD 12,00 med en oppdatert følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="70d2a-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="70d2a-122">Når en salgsordre posteres, er det posterte kostbeløpet USD 10,00, fordi løpende gjennomsnittlig kostpris ikke omfatter fysisk posterte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="70d2a-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="70d2a-123">**Merk:** For sammenligning: Hvis du merker av for **Ta med fysisk verdi** for denne varen, når en salgsordre posteres, blir det posterte kostnadsbeløpet USD 12,00.</span><span class="sxs-lookup"><span data-stu-id="70d2a-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>




