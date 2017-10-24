--- 
title: Starte en produksjonsordre
description: "Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor."
author: johanhoffmann
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
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33558053d33d9fe4a2ecb3576da569b2c441db80
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="start-a-production-order"></a><span data-ttu-id="652ea-103">Starte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="652ea-103">Start a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="652ea-104">Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor.</span><span class="sxs-lookup"><span data-stu-id="652ea-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="652ea-105">Tid og materialforbruk blir rapportert i denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="652ea-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="652ea-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="652ea-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="652ea-107">Dette er den femte fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="652ea-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="652ea-108">Starte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="652ea-108">Start a production order</span></span>
1. <span data-ttu-id="652ea-109">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="652ea-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="652ea-110">Velg en produksjonsordre med statusen Frigitt.</span><span class="sxs-lookup"><span data-stu-id="652ea-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="652ea-111">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="652ea-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="652ea-112">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="652ea-112">Click Start.</span></span>
    * <span data-ttu-id="652ea-113">På denne siden kan du bekrefte starten på produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="652ea-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="652ea-114">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="652ea-114">Click the General tab.</span></span>
5. <span data-ttu-id="652ea-115">I Fra oper.</span><span class="sxs-lookup"><span data-stu-id="652ea-115">In the From Oper.</span></span> <span data-ttu-id="652ea-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="652ea-116">No.</span></span> <span data-ttu-id="652ea-117">-feltet skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="652ea-117">field, enter '10'.</span></span>
6. <span data-ttu-id="652ea-118">Velg "Alltid" i feltet Automatisk ruteforbruk.</span><span class="sxs-lookup"><span data-stu-id="652ea-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="652ea-119">Merk av for Poster rutekort nå.</span><span class="sxs-lookup"><span data-stu-id="652ea-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="652ea-120">Velg "Alltid" i feltet Automatisk stykklisteforbruk.</span><span class="sxs-lookup"><span data-stu-id="652ea-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="652ea-121">Klikk avmerkingsboksen Poster plukkliste nå.</span><span class="sxs-lookup"><span data-stu-id="652ea-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="652ea-122">Klikk avmerkingsboksen Skriv ut plukkliste.</span><span class="sxs-lookup"><span data-stu-id="652ea-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="652ea-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="652ea-123">Click OK.</span></span>
    * <span data-ttu-id="652ea-124">Dette er den utskrevne plukklisten som viser materialene som ble brukt for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="652ea-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="652ea-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="652ea-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="652ea-126">Validere plukklisten</span><span class="sxs-lookup"><span data-stu-id="652ea-126">Validate the picking list</span></span>
1. <span data-ttu-id="652ea-127">Klikk Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="652ea-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="652ea-128">Klikk Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="652ea-128">Click Picking list.</span></span>
3. <span data-ttu-id="652ea-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="652ea-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="652ea-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="652ea-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="652ea-131">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="652ea-131">Click Edit.</span></span>
6. <span data-ttu-id="652ea-132">Skriv inn et tall i Forbruk-feltet.</span><span class="sxs-lookup"><span data-stu-id="652ea-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="652ea-133">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="652ea-133">Click Post.</span></span>
8. <span data-ttu-id="652ea-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="652ea-134">Click OK.</span></span>
    * <span data-ttu-id="652ea-135">I plukklistejournalen posteres materialene som forbrukes av produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="652ea-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="652ea-136">Før du posterer journalen, kan du gjøre justeringer hvis det er forskjell mellom det estimerte antallet og det faktiske forbrukte antallet.</span><span class="sxs-lookup"><span data-stu-id="652ea-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="652ea-137">Klikk kategorien GridPanel.</span><span class="sxs-lookup"><span data-stu-id="652ea-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="652ea-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="652ea-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="652ea-139">Verifisere rutekortjournalen</span><span class="sxs-lookup"><span data-stu-id="652ea-139">Verify the route card journal</span></span>
1. <span data-ttu-id="652ea-140">Klikk Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="652ea-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="652ea-141">Klikk Rutekort.</span><span class="sxs-lookup"><span data-stu-id="652ea-141">Click Route card.</span></span>
3. <span data-ttu-id="652ea-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="652ea-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="652ea-143">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="652ea-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="652ea-144">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="652ea-144">Click Edit.</span></span>
6. <span data-ttu-id="652ea-145">Angi et tall i feltet Timer.</span><span class="sxs-lookup"><span data-stu-id="652ea-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="652ea-146">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="652ea-146">Click Post.</span></span>
8. <span data-ttu-id="652ea-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="652ea-147">Click OK.</span></span>
    * <span data-ttu-id="652ea-148">Tiden som brukes på de enkelte operasjonene er registrert i rutekortjournalen.</span><span class="sxs-lookup"><span data-stu-id="652ea-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="652ea-149">Antall korrekte og feil kan også rapporteres.</span><span class="sxs-lookup"><span data-stu-id="652ea-149">Good and error quantity can also be reported.</span></span>  


