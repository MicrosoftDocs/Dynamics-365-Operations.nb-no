--- 
title: "Planlegge laster og leveringer ved hjelp av arbeidsområdet for lastplanlegging"
description: "Denne fremgangsmåten viser hvordan du bruker arbeidsområdet for lastplanlegging til å opprette en last for en salgsordre."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3f08049ad8d670be808c3a51bb8735ac489eda94
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="8e844-103">Planlegge laster og leveringer ved hjelp av arbeidsområdet for lastplanlegging</span><span class="sxs-lookup"><span data-stu-id="8e844-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e844-104">Denne fremgangsmåten viser hvordan du bruker arbeidsområdet for lastplanlegging til å opprette en last for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="8e844-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="8e844-105">Som en forutsetning skal vi først opprette salgsordren.</span><span class="sxs-lookup"><span data-stu-id="8e844-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="8e844-106">Denne prosedyren er en del av det daglige arbeidet for transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="8e844-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="8e844-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8e844-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="8e844-108">Opprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="8e844-108">Create a sales order</span></span>
1. <span data-ttu-id="8e844-109">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="8e844-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="8e844-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8e844-110">Click New.</span></span>
3. <span data-ttu-id="8e844-111">Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8e844-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8e844-112">Velg konto US-004.</span><span class="sxs-lookup"><span data-stu-id="8e844-112">Select account US-004.</span></span>
5. <span data-ttu-id="8e844-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8e844-113">Click OK.</span></span>
6. <span data-ttu-id="8e844-114">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8e844-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8e844-115">Velg vare A0001.</span><span class="sxs-lookup"><span data-stu-id="8e844-115">Select item A0001.</span></span>
    * <span data-ttu-id="8e844-116">A0001 er aktivert for transportstyring.</span><span class="sxs-lookup"><span data-stu-id="8e844-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="8e844-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8e844-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8e844-118">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="8e844-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="8e844-119">Skriv inn 24 i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e844-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="8e844-120">I dette eksemplet velger du lager 24.</span><span class="sxs-lookup"><span data-stu-id="8e844-120">In this example select warehouse 24.</span></span> <span data-ttu-id="8e844-121">Dette lageret er aktivert for transportstyring og avansert lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="8e844-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="8e844-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8e844-122">Click Save.</span></span>
12. <span data-ttu-id="8e844-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e844-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="8e844-124">Opprette en ny last</span><span class="sxs-lookup"><span data-stu-id="8e844-124">Create a new load</span></span>
1. <span data-ttu-id="8e844-125">Gå til Transportstyring > Planlegging > Arbeidsområde for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="8e844-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="8e844-126">Klikk kategorien Salgslinjer.</span><span class="sxs-lookup"><span data-stu-id="8e844-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="8e844-127">Nå vil du bygge belastningen for salgsordren som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="8e844-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="8e844-128">Belastninger kan bygges basert på tilbud og etterspørsel fra bestillinger, salgsordrer og overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="8e844-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="8e844-129">Klikk Forsyning og behov i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8e844-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="8e844-130">Klikk Til ny belastning.</span><span class="sxs-lookup"><span data-stu-id="8e844-130">Click To new load.</span></span>
5. <span data-ttu-id="8e844-131">Klikk rullegardinknappen i feltet Lastmal-ID for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8e844-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8e844-132">Lastmalen angir maksimale mål for vekt og volum for hele belastningen.</span><span class="sxs-lookup"><span data-stu-id="8e844-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="8e844-133">Lastmalen kan for eksempel representere størrelsen på en container eller lastebil.</span><span class="sxs-lookup"><span data-stu-id="8e844-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="8e844-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8e844-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8e844-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8e844-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="8e844-136">Vurdere og rute lasten</span><span class="sxs-lookup"><span data-stu-id="8e844-136">Rate and route the load</span></span>
1. <span data-ttu-id="8e844-137">Klikk Vurdering og ruting.</span><span class="sxs-lookup"><span data-stu-id="8e844-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="8e844-138">Klikk Arbeidsområde for vurderingsrute.</span><span class="sxs-lookup"><span data-stu-id="8e844-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="8e844-139">Klikk Vurder butikk.</span><span class="sxs-lookup"><span data-stu-id="8e844-139">Click Rate shop.</span></span>
4. <span data-ttu-id="8e844-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8e844-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8e844-141">Velg Tilordne.</span><span class="sxs-lookup"><span data-stu-id="8e844-141">Click Assign.</span></span>
6. <span data-ttu-id="8e844-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e844-142">Close the page.</span></span>
7. <span data-ttu-id="8e844-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e844-143">Close the page.</span></span>


