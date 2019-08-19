---
title: Planlegge laster og leveringer ved hjelp av arbeidsområdet for lastplanlegging
description: Dette emnet viser hvordan du bruker arbeidsområdet for lastplanlegging til å opprette en last for en salgsordre.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5e20eef8aa748bb64c6c14dd7e1d92ccf6592e0
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/10/2019
ms.locfileid: "1739071"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="fd8b4-103">Planlegge laster og leveringer ved hjelp av arbeidsområdet for lastplanlegging</span><span class="sxs-lookup"><span data-stu-id="fd8b4-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd8b4-104">Dette emnet viser hvordan du bruker arbeidsområdet for lastplanlegging til å opprette en last for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="fd8b4-105">Som en forutsetning skal vi først opprette salgsordren.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="fd8b4-106">Denne prosedyren er en del av det daglige arbeidet for transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="fd8b4-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="fd8b4-108">Opprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="fd8b4-108">Create a sales order</span></span>
1. <span data-ttu-id="fd8b4-109">Gå til **Navigasjonsrute > Moduler > Kunder > Ordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="fd8b4-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-110">Select **New**.</span></span>
3. <span data-ttu-id="fd8b4-111">Klikk på rullegardinknappen i **Kundekonto**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fd8b4-112">Velg konto **US-004**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="fd8b4-113">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-113">Select **OK**.</span></span>
6. <span data-ttu-id="fd8b4-114">Klikk på rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fd8b4-115">Velg vare **A0001**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-115">Select item **A0001**.</span></span> <span data-ttu-id="fd8b4-116">**A0001** er aktivert for transportstyring.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="fd8b4-117">Klikk på rullegardinknappen i feltet **Område** for å velge et element.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="fd8b4-118">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="fd8b4-119">I **Lager**-feltet skriver du inn 24 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="fd8b4-120">Dette lageret er aktivert for transportstyring og avansert lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="fd8b4-121">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-121">Select **Save**.</span></span>
12. <span data-ttu-id="fd8b4-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="fd8b4-123">Opprette en ny last</span><span class="sxs-lookup"><span data-stu-id="fd8b4-123">Create a new load</span></span>
1. <span data-ttu-id="fd8b4-124">Gå til **Navigasjonsrute > Moduler > Transportatstyring > Planlegging > Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="fd8b4-125">Velg kategorien **Salgslinjer**. Nå vil du bygge belastningen for salgsordren som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="fd8b4-126">Belastninger kan bygges basert på tilbud og etterspørsel fra bestillinger, salgsordrer og overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="fd8b4-127">Velg **Forsyning og behov** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="fd8b4-128">Velg **Til ny belastning**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-128">Select **To new load**.</span></span>
5. <span data-ttu-id="fd8b4-129">Klikk rullegardinknappen i feltet **Lastmal-ID** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="fd8b4-130">Lastmalen angir maksimale mål for vekt og volum for hele belastningen.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="fd8b4-131">Lastmalen kan for eksempel representere størrelsen på en container eller lastebil.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="fd8b4-132">Velg en vare.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-132">Select an item.</span></span>
6. <span data-ttu-id="fd8b4-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="fd8b4-134">Vurdere og rute lasten</span><span class="sxs-lookup"><span data-stu-id="fd8b4-134">Rate and route the load</span></span>
1. <span data-ttu-id="fd8b4-135">Velg **Vurdering og ruting**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="fd8b4-136">Velg **Arbeidsområde for vurderingsrute**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="fd8b4-137">Velg **Vurder butikk**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="fd8b4-138">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="fd8b4-139">Velg **Tilordne**.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-139">Select **Assign**.</span></span>
6. <span data-ttu-id="fd8b4-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fd8b4-140">Close the page.</span></span>

