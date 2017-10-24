--- 
title: Definere attributtbasert prissetting for konfigurerbare produkter
description: Denne prosedyren viser hvordan du setter opp attributtbasert prising.
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 88402bef6fd5dad38a74795cd31a4046085d6db7
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="8c17d-103">Definere attributtbasert prissetting for konfigurerbare produkter</span><span class="sxs-lookup"><span data-stu-id="8c17d-103">Set up attribute-based pricing for configurable products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c17d-104">Denne prosedyren viser hvordan du setter opp attributtbasert prising.</span><span class="sxs-lookup"><span data-stu-id="8c17d-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="8c17d-105">Det er en forutsetning at du har en produktkonfigurasjonsmodell som har én eller flere komponenter og attributter.</span><span class="sxs-lookup"><span data-stu-id="8c17d-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="8c17d-106">Dette eksemplet bruker produktmodellen for High-end-høyttaler i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="8c17d-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="8c17d-107">Produktsjefen bruker vanligvis denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8c17d-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="8c17d-108">Opprette en ny prismodell</span><span class="sxs-lookup"><span data-stu-id="8c17d-108">Create a new price model</span></span>
1. <span data-ttu-id="8c17d-109">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="8c17d-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="8c17d-110">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="8c17d-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="8c17d-111">I listen velger du linjen med High-end-høyttaler, men ikke klikk koblingen for navnet.</span><span class="sxs-lookup"><span data-stu-id="8c17d-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="8c17d-112">Klikk Modell i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8c17d-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="8c17d-113">Klikk Prismodeller.</span><span class="sxs-lookup"><span data-stu-id="8c17d-113">Click Price models.</span></span>
6. <span data-ttu-id="8c17d-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8c17d-114">Click New.</span></span>
7. <span data-ttu-id="8c17d-115">Skriv inn en verdi i feltet Prismodellnavn.</span><span class="sxs-lookup"><span data-stu-id="8c17d-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="8c17d-116">Bruk et navn som gjør det enkelt å identifisere modellen.</span><span class="sxs-lookup"><span data-stu-id="8c17d-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="8c17d-117">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8c17d-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="8c17d-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8c17d-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="8c17d-119">Legge til priselementer</span><span class="sxs-lookup"><span data-stu-id="8c17d-119">Add price elements</span></span>
1. <span data-ttu-id="8c17d-120">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="8c17d-120">Click Edit.</span></span>
    * <span data-ttu-id="8c17d-121">Hver komponent i en produktmodell kan ha et basispriselement og et hvilket som helst antall prisuttrykksregler.</span><span class="sxs-lookup"><span data-stu-id="8c17d-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="8c17d-122">Du kan også legge til priser i ulike valutaer.</span><span class="sxs-lookup"><span data-stu-id="8c17d-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="8c17d-123">Skriv inn en verdi i feltet Basisprisuttrykk.</span><span class="sxs-lookup"><span data-stu-id="8c17d-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="8c17d-124">Skriv for eksempel 100.</span><span class="sxs-lookup"><span data-stu-id="8c17d-124">For example, type 100.</span></span>   <span data-ttu-id="8c17d-125">Et basisprisuttrykk kan være en numerisk verdi, eller det kan bestå av den aritmetiske beregningen som omfatter ett eller flere attributter.</span><span class="sxs-lookup"><span data-stu-id="8c17d-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="8c17d-126">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8c17d-126">Click Add.</span></span>
4. <span data-ttu-id="8c17d-127">I Navn-feltet skriver du inn Rosewood.</span><span class="sxs-lookup"><span data-stu-id="8c17d-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="8c17d-128">Prisuttrykksnavnet identifiserer hva priselementet representerer.</span><span class="sxs-lookup"><span data-stu-id="8c17d-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="8c17d-129">I dette eksemplet oppretter vi et priselement for alternativet høyttalerkabinett med Rosewood-finish.</span><span class="sxs-lookup"><span data-stu-id="8c17d-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="8c17d-130">Klikk Rediger betingelse.</span><span class="sxs-lookup"><span data-stu-id="8c17d-130">Click Edit condition.</span></span>
    * <span data-ttu-id="8c17d-131">En prisbetingelse bidrar til å garantere at prisuttrykkselementet er inkludert i salgsprisen bare hvis det finnes en bestemt kombinasjon av attributter.</span><span class="sxs-lookup"><span data-stu-id="8c17d-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="8c17d-132">I ConstraintBody-feltet skriver du inn CabinetFinish=="Rosewood".</span><span class="sxs-lookup"><span data-stu-id="8c17d-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="8c17d-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8c17d-133">Click OK.</span></span>
8. <span data-ttu-id="8c17d-134">Skriv inn en verdi i feltet Uttrykk.</span><span class="sxs-lookup"><span data-stu-id="8c17d-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="8c17d-135">Skriv for eksempel 50.</span><span class="sxs-lookup"><span data-stu-id="8c17d-135">For example, type 50.</span></span>  
9. <span data-ttu-id="8c17d-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8c17d-136">Close the page.</span></span>
10. <span data-ttu-id="8c17d-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8c17d-137">Close the page.</span></span>


