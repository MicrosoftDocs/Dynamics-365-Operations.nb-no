---
title: Amortisere konstante kostnader for en produsert vare
description: "De konstante kostnadene til en produsert vare viser oppstillingstider for operasjonene og komponentene som har et konstant antall eller et konstant svinnbeløp."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8c72cf675d99f78c03ae2f2fef53b51fbf4bd8b
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="95beb-103">Amortisere konstante kostnader for en produsert vare</span><span class="sxs-lookup"><span data-stu-id="95beb-103">Amortize constant costs for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="95beb-104">De konstante kostnadene til en produsert vare viser oppstillingstider for operasjonene og komponentene som har et konstant antall eller et konstant svinnbeløp.</span><span class="sxs-lookup"><span data-stu-id="95beb-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="95beb-105">Konseptet med en kostnadspartistørrelse brukes til nedbetaling av disse konstante kostnadene i de beregnede kostnadene til en produsert vare.</span><span class="sxs-lookup"><span data-stu-id="95beb-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="95beb-106">Dette konseptet har flere synonymer, for eksempel regnskapspartistørrelse.</span><span class="sxs-lookup"><span data-stu-id="95beb-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="95beb-107">Konseptet med nedbetaling av konstante kostnader har også flere synonymer, for eksempel proporsjonale konstante kostnader.</span><span class="sxs-lookup"><span data-stu-id="95beb-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>
<span data-ttu-id="95beb-108">Kostnadspartistørrelsesantallet for en produsert vare brukes i en stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="95beb-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="95beb-109">Antallet avhenger av hvordan du starter og utfører stykklisteberegningen, slik det illustreres nedenfor:</span><span class="sxs-lookup"><span data-stu-id="95beb-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>
-   <span data-ttu-id="95beb-110">Standard beregningsantall i en vares stykklisteberegning − Varens standard bestillingsantall for lager fungerer som standardverdi for kostnadspartistørrelsen til varen, men standardverdien kan være et større antall for å gjenspeile varens bestillingsmultiplumsantall.</span><span class="sxs-lookup"><span data-stu-id="95beb-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="95beb-111">Varens standard bestillingsantall og multiplum kan defineres innenfor standardinnstillingene for bestilling eller stedsbestemte bestillingsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="95beb-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="95beb-112">Angitt beregningsantall i en vares stykklisteberegning − Det angitte beregningsantallet fungerer som kostnadspartistørrelsen til varen.</span><span class="sxs-lookup"><span data-stu-id="95beb-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="95beb-113">Beregningsantallet er i utgangspunktet varens standard bestillingsantall, men kan overstyres manuelt.</span><span class="sxs-lookup"><span data-stu-id="95beb-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="95beb-114">Det angitte beregningsantallet representerer kostnadspartistørrelsen for den angitte varen, og for produserte komponenter som har stykklistelinjetypen produksjon.</span><span class="sxs-lookup"><span data-stu-id="95beb-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="95beb-115">Dette er fordi det antas at komponenten vil bli produsert i et eksakt antall.</span><span class="sxs-lookup"><span data-stu-id="95beb-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="95beb-116">Kostnadspartistørrelsen for andre produserte komponenter med stykklistelinjetypevarer viser deres standard bestillingsantall.</span><span class="sxs-lookup"><span data-stu-id="95beb-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="95beb-117">Angitt beregningsantall for produksjon-etter-ordre i en vares stykklisteberegning − Det angitte beregningsantallet fungerer som kostnadspartistørrelsen for varen og de produserte komponentene når stykklisteberegninger bruker en produksjon-etter-ordre-nedbrytingsmodus.</span><span class="sxs-lookup"><span data-stu-id="95beb-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="95beb-118">Det antas at komponenten vil bli produsert i et eksakt antall, på samme måte som en produsert komponent i en stykklistelinjetypeproduksjon.</span><span class="sxs-lookup"><span data-stu-id="95beb-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="95beb-119">Angitt beregningsantall i en ordrespesifikk stykklisteberegning − En ordrespesifikk stykklisteberegning kan utføres for en linjevare på en salgsordre, et salgstilbud eller en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="95beb-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="95beb-120">Det angitte beregningsantallet bruker som standard antallet på linjen der varen opprinnelig kommer fra, men standardantallet kan overstyres.</span><span class="sxs-lookup"><span data-stu-id="95beb-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="95beb-121">Du kan velge om den ordrespesifikke stykklisteberegningen skal bruke modusen produksjon-etter-ordre eller nedbryting på flere nivåer.</span><span class="sxs-lookup"><span data-stu-id="95beb-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="95beb-122">Det beregnede beløpet for nedbetaling av en produsert vares konstante kostnader, kalles tillegg.</span><span class="sxs-lookup"><span data-stu-id="95beb-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>






