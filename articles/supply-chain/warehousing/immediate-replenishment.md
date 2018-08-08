---
title: Umiddelbar etterfylling
description: "Dette emnet beskriver hvordan du kan bruke umiddelbar etterfylling for å etterfylle beholdningen når et lokasjonsdirektiv ikke kan tilordne beholdning."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: ab1f06951d5daceaf002b2cc23236dd818457985
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="immediate-replenishment"></a><span data-ttu-id="96fbf-103">Umiddelbar etterfylling</span><span class="sxs-lookup"><span data-stu-id="96fbf-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96fbf-104">Umiddelbar etterfylling lar deg etterfylle beholdning umiddelbart etter at en lokasjonsdirektivlinje ikke kan tilordne beholdning.</span><span class="sxs-lookup"><span data-stu-id="96fbf-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="96fbf-105">Etterfyllingen er basert på én linje i oppsettet av lokasjonsdirektivet.</span><span class="sxs-lookup"><span data-stu-id="96fbf-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="96fbf-106">Hvis lager ikke er tilgjengelig i måleenheten som er angitt av denne linjen, skjer etterfylling av denne målenheten umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="96fbf-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="96fbf-107">Umiddelbar etterfylling gir et alternativ til metoden der tildelingen av lager er basert på flere linjer i lokasjonsdirektivet, og der behovet er summert på slutten av tildelingen og etterfylles i måleenheten som er angitt av den siste linjen i lokasjonsdirektivet.</span><span class="sxs-lookup"><span data-stu-id="96fbf-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="96fbf-108">Fordelene ved å bruke umiddelbar etterfylling er at etterfylling kan begrenses av bestemte enheter, og antallet kan sendes til bestemte lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="96fbf-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="96fbf-109">Forretningsscenario</span><span class="sxs-lookup"><span data-stu-id="96fbf-109">Business scenario</span></span>

<span data-ttu-id="96fbf-110">Du har for eksempel et lager som har egne plukkeområder for målenheten "boks" og "enkelt".</span><span class="sxs-lookup"><span data-stu-id="96fbf-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="96fbf-111">Du vil optimalisere plukkeprosessen ved å plukke så mange bokser som mulig, og deretter plukke gjenværende antall som er mindre enn en boks, fra området "enkelt".</span><span class="sxs-lookup"><span data-stu-id="96fbf-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="96fbf-112">I dette tilfellet kan du bruke umiddelbar etterfylling.</span><span class="sxs-lookup"><span data-stu-id="96fbf-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="96fbf-113">I lokasjonsdirektivet kan du definere umiddelbar etterfylling for bokser slik at behovsetterfylling brukes så snart det er manko på bokser som kan plukkes for behovsantallet.</span><span class="sxs-lookup"><span data-stu-id="96fbf-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="96fbf-114">På denne måten kan du optimalisere plukkeprosessen slik at plukkingen inkluderer så mange bokser som mulig.</span><span class="sxs-lookup"><span data-stu-id="96fbf-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="96fbf-115">Umiddelbar etterfylling genererer etterfylling av boksene, og behovet sendes ikke videre slik at antallene plukkes i målenheten "enkelt.</span><span class="sxs-lookup"><span data-stu-id="96fbf-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="96fbf-116">Med andre ord så er det bare antallene som er ment å plukkes i "enkelt"-måleenheten (det vil si antall som er mindre enn en boks), som blir plukket fra "enkelt"-området.</span><span class="sxs-lookup"><span data-stu-id="96fbf-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="96fbf-117">Hvis det oppstår manko i "boks"-området, kan du plukke så mange bokser som mulig ut av det totale behovet.</span><span class="sxs-lookup"><span data-stu-id="96fbf-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="96fbf-118">De gjenstående antallene plukkes deretter fra området "enkelt".</span><span class="sxs-lookup"><span data-stu-id="96fbf-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="96fbf-119">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="96fbf-119">Where it applies</span></span>

<span data-ttu-id="96fbf-120">Umiddelbar etterfylling brukes under bølgeutførelse hvis tildelingen mislykkes for en lokasjonsdirektivlinje som en etterfyllingsmal er definert for.</span><span class="sxs-lookup"><span data-stu-id="96fbf-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="96fbf-121">Konfigurere umiddelbar etterfylling</span><span class="sxs-lookup"><span data-stu-id="96fbf-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="96fbf-122">Gå til **Lagerstyring** \> **Oppsett** \> **Lokasjonsdirektiver**, og deretter i **Linjer**-kategorien i **Mal for umiddelbar etterfylling**-listen velger du en etterfyllingsmal for bølgebehov.</span><span class="sxs-lookup"><span data-stu-id="96fbf-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="96fbf-123">Etterfyllingsmalen brukes hvis lokasjonsdirektivlinjen ikke kan tildele en angitt målenhet.</span><span class="sxs-lookup"><span data-stu-id="96fbf-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="96fbf-124">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="96fbf-124">Troubleshooting</span></span>

<span data-ttu-id="96fbf-125">Hvis umiddelbar etterfylling er valgt for en lokasjonsdirektivlinje, men ikke noe etterfyllingsarbeid genereres når du bruker maler for behovsetterfylling for denne lokasjonsdirektivlinjen, må to hovedårsaker undersøkes:</span><span class="sxs-lookup"><span data-stu-id="96fbf-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="96fbf-126">Kontroller at behovsetterfyllingsmalen som brukes, er konfigurert til å bruke de riktige lokasjonsmalene og arbeidsmalene for **Etterfylling**-typen.</span><span class="sxs-lookup"><span data-stu-id="96fbf-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="96fbf-127">Kontroller at det er stor nok lagerbeholdning på stedene der behovsetterfyllingsmalen søker etter lagerbeholdning for etterfylling.</span><span class="sxs-lookup"><span data-stu-id="96fbf-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>

