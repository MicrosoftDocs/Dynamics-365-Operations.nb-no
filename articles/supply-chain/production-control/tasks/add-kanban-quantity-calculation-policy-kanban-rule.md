--- 
title: Legge til en policy for beregning av Kanban-antall i en Kanban-regel
description: "Denne prosedyren fokuserer på å opprette en policy for Kanban-antallsberegning og legge den til i en kanban-regel for å optimalisere kanban-størrelse og -antall."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6a947d4a5302c6ed1848396d50cfbfcb78aabf97
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="ef84d-103">Legge til en policy for beregning av Kanban-antall i en Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="ef84d-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef84d-104">Denne prosedyren fokuserer på å opprette en policy for Kanban-antallsberegning og legge den til i en kanban-regel for å optimalisere kanban-størrelse og -antall.</span><span class="sxs-lookup"><span data-stu-id="ef84d-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="ef84d-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ef84d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ef84d-106">Denne fremgangsmåten er ment for verdistrømsbehandling.</span><span class="sxs-lookup"><span data-stu-id="ef84d-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="ef84d-107">Denne prosedyren er en forutsetning for oppretting av prosedyren Beregne forslag til Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ef84d-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="ef84d-108">Opprett en policy for Kanban-antallsberegning</span><span class="sxs-lookup"><span data-stu-id="ef84d-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="ef84d-109">Gå til Produksjonskontroll > Periodiske oppgaver > Kanban-antallsberegning > Policyer for Kanban-antallsberegning.</span><span class="sxs-lookup"><span data-stu-id="ef84d-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="ef84d-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ef84d-110">Click New.</span></span>
3. <span data-ttu-id="ef84d-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef84d-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ef84d-112">Skriv for eksempel inn Høyttaler2016.</span><span class="sxs-lookup"><span data-stu-id="ef84d-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="ef84d-113">Klikk rullegardinknappen i feltet Hovedplan for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef84d-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ef84d-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ef84d-115">Velg Statisk plan for å beregne behov.</span><span class="sxs-lookup"><span data-stu-id="ef84d-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="ef84d-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ef84d-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ef84d-117">Click Save.</span></span>
8. <span data-ttu-id="ef84d-118">Angi 1 i feltet Minste Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ef84d-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="ef84d-119">Dette er det ekstra antallet Kanbaner som er tatt med i Kanban-antallsberegningen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="ef84d-120">Angi Sikkerhetsfaktor til 1.</span><span class="sxs-lookup"><span data-stu-id="ef84d-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="ef84d-121">Dette er faktoren som brukes til å beregne tilleggsantall for sikkerhetslager.</span><span class="sxs-lookup"><span data-stu-id="ef84d-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="ef84d-122">Angi 30 i Dager foran-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef84d-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="ef84d-123">Dette er antall dager bakover fra beregningsdatoen for Kanban-antall som behov er inkludert i behovsberegningen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="ef84d-124">Angi 30 i Dager etter-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef84d-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="ef84d-125">Dette er antall dager fremover fra beregningsdatoen for Kanban-antall som behov er inkludert i behovsberegningen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="ef84d-126">Formelen som brukes i beregningen, vises med de faktiske verdiene.</span><span class="sxs-lookup"><span data-stu-id="ef84d-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="ef84d-127">Eksempel: Kanban-antall = ((gjennomsnittlig daglig behov x leveringstid x 2.00) / produktantall per håndteringsenhet) + 1</span><span class="sxs-lookup"><span data-stu-id="ef84d-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="ef84d-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ef84d-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="ef84d-129">Legg til Kanban-beregningspolicyen i en Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="ef84d-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="ef84d-130">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="ef84d-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="ef84d-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ef84d-132">Velg kanban-regel 000020 for denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ef84d-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="ef84d-133">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ef84d-134">Aktiver utvidelsen av delen Policyer for Kanban-antallsberegning.</span><span class="sxs-lookup"><span data-stu-id="ef84d-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="ef84d-135">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ef84d-135">Click Add.</span></span>
    * <span data-ttu-id="ef84d-136">Legg til policyen for Kanban-antallsberegning som du nettopp opprettet i den forrige delaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="ef84d-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="ef84d-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="ef84d-138">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef84d-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ef84d-139">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef84d-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef84d-140">Velg policyen Speaker2016 som du nettopp opprettet i den forrige delaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="ef84d-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  


