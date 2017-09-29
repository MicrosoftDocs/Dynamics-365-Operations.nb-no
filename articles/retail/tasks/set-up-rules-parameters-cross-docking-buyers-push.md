--- 
title: " Definere regler og parametere for direkteoverføring og sentralt innkjøp"
description: "Denne prosedyren beskriver fremgangsmåten for å opprette etterfyllingsregler."
author: josaw1
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1ff41a18be066b6f32c5172bda38c389e7f34128
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="d3634-103"> Definere regler og parametere for direkteoverføring og sentralt innkjøp</span><span class="sxs-lookup"><span data-stu-id="d3634-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d3634-104">Denne prosedyren beskriver fremgangsmåten for å opprette etterfyllingsregler.</span><span class="sxs-lookup"><span data-stu-id="d3634-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="d3634-105">Etterfyllingsregler kan brukes til å kontrollere hvordan produkter distribueres til butikkene når du bruker direkteoverføring og sentralt innkjøp.</span><span class="sxs-lookup"><span data-stu-id="d3634-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="d3634-106">Etterfyllingsregler kan angis for butikker eller butikkgrupper.</span><span class="sxs-lookup"><span data-stu-id="d3634-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="d3634-107">Vekten som er definert for hver linje i en regel, styrer hvordan antallene av produkter blir fordelt mellom butikkene når etterfyllingsregler brukes som distribusjonsmetode i direkteoverføring eller sentralt innkjøp.</span><span class="sxs-lookup"><span data-stu-id="d3634-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="d3634-108">Denne prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="d3634-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d3634-109">Gå til Etterfyllingsregler.</span><span class="sxs-lookup"><span data-stu-id="d3634-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="d3634-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d3634-110">Click New.</span></span>
3. <span data-ttu-id="d3634-111">Skriv inn en verdi i feltet Etterfyllingsregel.</span><span class="sxs-lookup"><span data-stu-id="d3634-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="d3634-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d3634-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d3634-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d3634-113">Click Save.</span></span>
6. <span data-ttu-id="d3634-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="d3634-114">Click Add.</span></span>
7. <span data-ttu-id="d3634-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d3634-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d3634-116">Du kan velge Etterfyllingshierarki eller Kanal for typen.</span><span class="sxs-lookup"><span data-stu-id="d3634-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="d3634-117">Verdien angir om valget i Navn blir et hierarki av kanaler eller en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="d3634-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="d3634-118">La det for eksempel stå som Etterfyllingshierarki..</span><span class="sxs-lookup"><span data-stu-id="d3634-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="d3634-119">Velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3634-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="d3634-120">Standardvektverdien fylles ut fra vekten som er definert i lageret.</span><span class="sxs-lookup"><span data-stu-id="d3634-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="d3634-121">Vekten kan brukes til etterfyllingsregelen eller du kan angi en ny vekt i Vekt-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3634-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="d3634-122">Angi et tall i Vekt-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3634-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="d3634-123">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="d3634-123">Click Add.</span></span>
11. <span data-ttu-id="d3634-124">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d3634-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="d3634-125">Velg Kanal i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3634-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="d3634-126">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3634-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="d3634-127">Angi et tall i Vekt-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3634-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="d3634-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d3634-128">Click Save.</span></span>


