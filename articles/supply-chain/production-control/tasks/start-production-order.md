---
title: Starte en produksjonsordre
description: Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e444f6c521c47964b9b9b864b62fb486102c2fc7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210393"
---
# <a name="start-a-production-order"></a><span data-ttu-id="3c756-103">Starte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="3c756-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3c756-104">Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor.</span><span class="sxs-lookup"><span data-stu-id="3c756-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="3c756-105">Tid og materialforbruk blir rapportert i denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="3c756-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="3c756-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3c756-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3c756-107">Dette er den femte fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="3c756-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="3c756-108">Starte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="3c756-108">Start a production order</span></span>
1. <span data-ttu-id="3c756-109">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="3c756-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="3c756-110">Velg en produksjonsordre med statusen Frigitt.</span><span class="sxs-lookup"><span data-stu-id="3c756-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="3c756-111">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3c756-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="3c756-112">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="3c756-112">Click Start.</span></span>
    * <span data-ttu-id="3c756-113">På denne siden kan du bekrefte starten på produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="3c756-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="3c756-114">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="3c756-114">Click the General tab.</span></span>
5. <span data-ttu-id="3c756-115">I Fra oper.</span><span class="sxs-lookup"><span data-stu-id="3c756-115">In the From Oper.</span></span> <span data-ttu-id="3c756-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="3c756-116">No.</span></span> <span data-ttu-id="3c756-117">-feltet skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="3c756-117">field, enter '10'.</span></span>
6. <span data-ttu-id="3c756-118">Velg "Alltid" i feltet Automatisk ruteforbruk.</span><span class="sxs-lookup"><span data-stu-id="3c756-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="3c756-119">Merk av for Poster rutekort nå.</span><span class="sxs-lookup"><span data-stu-id="3c756-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="3c756-120">Velg "Alltid" i feltet Automatisk stykklisteforbruk.</span><span class="sxs-lookup"><span data-stu-id="3c756-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="3c756-121">Klikk avmerkingsboksen Poster plukkliste nå.</span><span class="sxs-lookup"><span data-stu-id="3c756-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="3c756-122">Klikk avmerkingsboksen Skriv ut plukkliste.</span><span class="sxs-lookup"><span data-stu-id="3c756-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="3c756-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3c756-123">Click OK.</span></span>
    * <span data-ttu-id="3c756-124">Dette er den utskrevne plukklisten som viser materialene som ble brukt for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="3c756-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="3c756-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3c756-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="3c756-126">Validere plukklisten</span><span class="sxs-lookup"><span data-stu-id="3c756-126">Validate the picking list</span></span>
1. <span data-ttu-id="3c756-127">Klikk Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3c756-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="3c756-128">Klikk Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="3c756-128">Click Picking list.</span></span>
3. <span data-ttu-id="3c756-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3c756-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3c756-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3c756-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3c756-131">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="3c756-131">Click Edit.</span></span>
6. <span data-ttu-id="3c756-132">Skriv inn et tall i Forbruk-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c756-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="3c756-133">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="3c756-133">Click Post.</span></span>
8. <span data-ttu-id="3c756-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3c756-134">Click OK.</span></span>
    * <span data-ttu-id="3c756-135">I plukklistejournalen posteres materialene som forbrukes av produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="3c756-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="3c756-136">Før du posterer journalen, kan du gjøre justeringer hvis det er forskjell mellom det estimerte antallet og det faktiske forbrukte antallet.</span><span class="sxs-lookup"><span data-stu-id="3c756-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="3c756-137">Klikk kategorien GridPanel.</span><span class="sxs-lookup"><span data-stu-id="3c756-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="3c756-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3c756-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="3c756-139">Verifisere rutekortjournalen</span><span class="sxs-lookup"><span data-stu-id="3c756-139">Verify the route card journal</span></span>
1. <span data-ttu-id="3c756-140">Klikk Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3c756-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="3c756-141">Klikk Rutekort.</span><span class="sxs-lookup"><span data-stu-id="3c756-141">Click Route card.</span></span>
3. <span data-ttu-id="3c756-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3c756-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3c756-143">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3c756-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3c756-144">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="3c756-144">Click Edit.</span></span>
6. <span data-ttu-id="3c756-145">Angi et tall i feltet Timer.</span><span class="sxs-lookup"><span data-stu-id="3c756-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="3c756-146">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="3c756-146">Click Post.</span></span>
8. <span data-ttu-id="3c756-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3c756-147">Click OK.</span></span>
    * <span data-ttu-id="3c756-148">Tiden som brukes på de enkelte operasjonene er registrert i rutekortjournalen.</span><span class="sxs-lookup"><span data-stu-id="3c756-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="3c756-149">Antall korrekte og feil kan også rapporteres.</span><span class="sxs-lookup"><span data-stu-id="3c756-149">Good and error quantity can also be reported.</span></span>  
