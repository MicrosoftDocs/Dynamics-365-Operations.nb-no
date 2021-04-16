---
title: Starte en produksjonsordre
description: Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be1c389bc4193ef080dbeb1639b69acf466ef0de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831872"
---
# <a name="start-a-production-order"></a><span data-ttu-id="96cb3-103">Starte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="96cb3-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96cb3-104">Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor.</span><span class="sxs-lookup"><span data-stu-id="96cb3-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="96cb3-105">Tid og materialforbruk blir rapportert i denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="96cb3-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="96cb3-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="96cb3-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="96cb3-107">Dette er den femte fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="96cb3-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="96cb3-108">Starte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="96cb3-108">Start a production order</span></span>
1. <span data-ttu-id="96cb3-109">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="96cb3-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="96cb3-110">Velg en produksjonsordre med statusen Frigitt.</span><span class="sxs-lookup"><span data-stu-id="96cb3-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="96cb3-111">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="96cb3-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="96cb3-112">Klikk på Start.</span><span class="sxs-lookup"><span data-stu-id="96cb3-112">Click Start.</span></span>
    * <span data-ttu-id="96cb3-113">På denne siden kan du bekrefte starten på produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="96cb3-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="96cb3-114">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="96cb3-114">Click the General tab.</span></span>
5. <span data-ttu-id="96cb3-115">I Fra oper.</span><span class="sxs-lookup"><span data-stu-id="96cb3-115">In the From Oper.</span></span> <span data-ttu-id="96cb3-116">Nei.</span><span class="sxs-lookup"><span data-stu-id="96cb3-116">No.</span></span> <span data-ttu-id="96cb3-117">-feltet skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="96cb3-117">field, enter '10'.</span></span>
6. <span data-ttu-id="96cb3-118">Velg "Alltid" i feltet Automatisk ruteforbruk.</span><span class="sxs-lookup"><span data-stu-id="96cb3-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="96cb3-119">Merk av for Poster rutekort nå.</span><span class="sxs-lookup"><span data-stu-id="96cb3-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="96cb3-120">Velg "Alltid" i feltet Automatisk stykklisteforbruk.</span><span class="sxs-lookup"><span data-stu-id="96cb3-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="96cb3-121">Klikk på avmerkingsboksen Poster plukkliste nå.</span><span class="sxs-lookup"><span data-stu-id="96cb3-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="96cb3-122">Klikk på avmerkingsboksen Skriv ut plukkliste.</span><span class="sxs-lookup"><span data-stu-id="96cb3-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="96cb3-123">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="96cb3-123">Click OK.</span></span>
    * <span data-ttu-id="96cb3-124">Dette er den utskrevne plukklisten som viser materialene som ble brukt for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="96cb3-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="96cb3-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="96cb3-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="96cb3-126">Validere plukklisten</span><span class="sxs-lookup"><span data-stu-id="96cb3-126">Validate the picking list</span></span>
1. <span data-ttu-id="96cb3-127">Klikk på Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="96cb3-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="96cb3-128">Klikk på Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="96cb3-128">Click Picking list.</span></span>
3. <span data-ttu-id="96cb3-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="96cb3-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="96cb3-130">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="96cb3-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="96cb3-131">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="96cb3-131">Click Edit.</span></span>
6. <span data-ttu-id="96cb3-132">Skriv inn et tall i Forbruk-feltet.</span><span class="sxs-lookup"><span data-stu-id="96cb3-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="96cb3-133">Klikk på Poster.</span><span class="sxs-lookup"><span data-stu-id="96cb3-133">Click Post.</span></span>
8. <span data-ttu-id="96cb3-134">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="96cb3-134">Click OK.</span></span>
    * <span data-ttu-id="96cb3-135">I plukklistejournalen posteres materialene som forbrukes av produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="96cb3-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="96cb3-136">Før du posterer journalen, kan du gjøre justeringer hvis det er forskjell mellom det estimerte antallet og det faktiske forbrukte antallet.</span><span class="sxs-lookup"><span data-stu-id="96cb3-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="96cb3-137">Klikk på fanen GridPanel.</span><span class="sxs-lookup"><span data-stu-id="96cb3-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="96cb3-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="96cb3-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="96cb3-139">Verifisere rutekortjournalen</span><span class="sxs-lookup"><span data-stu-id="96cb3-139">Verify the route card journal</span></span>
1. <span data-ttu-id="96cb3-140">Klikk på Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="96cb3-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="96cb3-141">Klikk på Rutekort.</span><span class="sxs-lookup"><span data-stu-id="96cb3-141">Click Route card.</span></span>
3. <span data-ttu-id="96cb3-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="96cb3-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="96cb3-143">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="96cb3-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="96cb3-144">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="96cb3-144">Click Edit.</span></span>
6. <span data-ttu-id="96cb3-145">Angi et tall i feltet Timer.</span><span class="sxs-lookup"><span data-stu-id="96cb3-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="96cb3-146">Klikk på Poster.</span><span class="sxs-lookup"><span data-stu-id="96cb3-146">Click Post.</span></span>
8. <span data-ttu-id="96cb3-147">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="96cb3-147">Click OK.</span></span>
    * <span data-ttu-id="96cb3-148">Tiden som brukes på de enkelte operasjonene er registrert i rutekortjournalen.</span><span class="sxs-lookup"><span data-stu-id="96cb3-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="96cb3-149">Antall korrekte og feil kan også rapporteres.</span><span class="sxs-lookup"><span data-stu-id="96cb3-149">Good and error quantity can also be reported.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]