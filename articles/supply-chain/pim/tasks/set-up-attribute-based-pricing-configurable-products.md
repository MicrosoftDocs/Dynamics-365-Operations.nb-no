---
title: Definere attributtbasert prissetting for konfigurerbare produkter
description: Dette emnet forklarer hvordan du setter opp attributtbasert prising.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 534e9c9332c107afebd814cf2090ecbdf0ec6459
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914705"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="1986a-103">Definere attributtbasert prissetting for konfigurerbare produkter</span><span class="sxs-lookup"><span data-stu-id="1986a-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1986a-104">Dette emnet forklarer hvordan du setter opp attributtbasert prising.</span><span class="sxs-lookup"><span data-stu-id="1986a-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="1986a-105">Det er en forutsetning at du har en produktkonfigurasjonsmodell som har én eller flere komponenter og attributter.</span><span class="sxs-lookup"><span data-stu-id="1986a-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="1986a-106">Dette eksemplet bruker produktmodellen for High-end-høyttaler i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="1986a-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="1986a-107">Produktsjefen bruker vanligvis denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="1986a-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="1986a-108">Opprette en ny prismodell</span><span class="sxs-lookup"><span data-stu-id="1986a-108">Create a new price model</span></span>
1. <span data-ttu-id="1986a-109">Velg **Definisjon av produktvariantmodell** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="1986a-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="1986a-110">Velg **Produktkonfigurasjonsmodeller** i **koblinger**-delen.</span><span class="sxs-lookup"><span data-stu-id="1986a-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="1986a-111">I listen velger du linjen med **High-end-høyttaler**, men ikke velg koblingen for navnet.</span><span class="sxs-lookup"><span data-stu-id="1986a-111">In the list, select the **High End Speaker** line, but don’t select the link for the name.</span></span>
4. <span data-ttu-id="1986a-112">Velg **Modell** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1986a-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="1986a-113">Velg **Prismodeller**.</span><span class="sxs-lookup"><span data-stu-id="1986a-113">Select **Price models**.</span></span>
6. <span data-ttu-id="1986a-114">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1986a-114">Select **New**.</span></span>
7. <span data-ttu-id="1986a-115">Skriv inn en verdi i feltet **Prismodellnavn**.</span><span class="sxs-lookup"><span data-stu-id="1986a-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="1986a-116">Bruk et navn som gjør det enkelt å identifisere modellen.</span><span class="sxs-lookup"><span data-stu-id="1986a-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="1986a-117">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1986a-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="1986a-118">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1986a-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="1986a-119">Legge til priselementer</span><span class="sxs-lookup"><span data-stu-id="1986a-119">Add price elements</span></span>
1. <span data-ttu-id="1986a-120">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="1986a-120">Select **Edit**.</span></span> <span data-ttu-id="1986a-121">Hver komponent i en produktmodell kan ha et basispriselement og et hvilket som helst antall prisuttrykksregler.</span><span class="sxs-lookup"><span data-stu-id="1986a-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="1986a-122">Du kan også legge til priser i ulike valutaer.</span><span class="sxs-lookup"><span data-stu-id="1986a-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="1986a-123">Skriv inn en verdi i feltet **Basisprisuttrykk**.</span><span class="sxs-lookup"><span data-stu-id="1986a-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="1986a-124">Skriv for eksempel 100.</span><span class="sxs-lookup"><span data-stu-id="1986a-124">For example, type 100.</span></span> <span data-ttu-id="1986a-125">Et basisprisuttrykk kan være en numerisk verdi, eller det kan bestå av den aritmetiske beregningen som omfatter ett eller flere attributter.</span><span class="sxs-lookup"><span data-stu-id="1986a-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="1986a-126">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="1986a-126">Select **Add**.</span></span>
4. <span data-ttu-id="1986a-127">I **Navn**-feltet skriver du inn `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="1986a-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="1986a-128">Prisuttrykksnavnet identifiserer hva priselementet representerer.</span><span class="sxs-lookup"><span data-stu-id="1986a-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="1986a-129">I dette eksemplet oppretter vi et priselement for alternativet høyttalerkabinett med Rosewood-finish.</span><span class="sxs-lookup"><span data-stu-id="1986a-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="1986a-130">Velg **Rediger betingelse**.</span><span class="sxs-lookup"><span data-stu-id="1986a-130">Select **Edit condition**.</span></span> <span data-ttu-id="1986a-131">En prisbetingelse bidrar til å garantere at prisuttrykkselementet er inkludert i salgsprisen bare hvis det finnes en bestemt kombinasjon av attributter.</span><span class="sxs-lookup"><span data-stu-id="1986a-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="1986a-132">I feltet **ConstraintBody** angir du `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="1986a-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="1986a-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1986a-133">Select **OK**.</span></span>
8. <span data-ttu-id="1986a-134">Skriv inn en verdi i feltet **Uttrykk**.</span><span class="sxs-lookup"><span data-stu-id="1986a-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="1986a-135">Skriv for eksempel `50`.</span><span class="sxs-lookup"><span data-stu-id="1986a-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="1986a-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1986a-136">Close the page.</span></span>

