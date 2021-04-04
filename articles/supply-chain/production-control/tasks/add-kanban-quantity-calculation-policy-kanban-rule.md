---
title: Legge til en policy for beregning av Kanban-antall i en Kanban-regel
description: Denne prosedyren fokuserer på å opprette en policy for Kanban-antallsberegning og legge den til i en kanban-regel for å optimalisere kanban-størrelse og -antall.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a32753701c9e06c46ed9b2a9c4b0329f62f15597
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255475"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="49e36-103">Legge til en policy for beregning av Kanban-antall i en Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="49e36-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49e36-104">Denne prosedyren fokuserer på å opprette en policy for Kanban-antallsberegning og legge den til i en kanban-regel for å optimalisere kanban-størrelse og -antall.</span><span class="sxs-lookup"><span data-stu-id="49e36-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="49e36-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="49e36-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="49e36-106">Denne fremgangsmåten er ment for verdistrømsbehandling.</span><span class="sxs-lookup"><span data-stu-id="49e36-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="49e36-107">Denne prosedyren er en forutsetning for oppretting av prosedyren Beregne forslag til Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="49e36-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="49e36-108">Opprett en policy for Kanban-antallsberegning</span><span class="sxs-lookup"><span data-stu-id="49e36-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="49e36-109">Gå til Produksjonskontroll > Periodiske oppgaver > Kanban-antallsberegning > Policyer for Kanban-antallsberegning.</span><span class="sxs-lookup"><span data-stu-id="49e36-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="49e36-110">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="49e36-110">Click New.</span></span>
3. <span data-ttu-id="49e36-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="49e36-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="49e36-112">Skriv for eksempel inn Høyttaler2016.</span><span class="sxs-lookup"><span data-stu-id="49e36-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="49e36-113">Klikk på rullegardinknappen i feltet Hovedplan for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="49e36-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="49e36-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="49e36-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49e36-115">Velg Statisk plan for å beregne behov.</span><span class="sxs-lookup"><span data-stu-id="49e36-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="49e36-116">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="49e36-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="49e36-117">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="49e36-117">Click Save.</span></span>
8. <span data-ttu-id="49e36-118">Angi 1 i feltet Minste Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="49e36-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="49e36-119">Dette er det ekstra antallet Kanbaner som er tatt med i Kanban-antallsberegningen.</span><span class="sxs-lookup"><span data-stu-id="49e36-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="49e36-120">Angi Sikkerhetsfaktor til 1.</span><span class="sxs-lookup"><span data-stu-id="49e36-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="49e36-121">Dette er faktoren som brukes til å beregne tilleggsantall for sikkerhetslager.</span><span class="sxs-lookup"><span data-stu-id="49e36-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="49e36-122">Angi 30 i Dager foran-feltet.</span><span class="sxs-lookup"><span data-stu-id="49e36-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="49e36-123">Dette er antall dager bakover fra beregningsdatoen for Kanban-antall som behov er inkludert i behovsberegningen.</span><span class="sxs-lookup"><span data-stu-id="49e36-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="49e36-124">Angi 30 i Dager etter-feltet.</span><span class="sxs-lookup"><span data-stu-id="49e36-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="49e36-125">Dette er antall dager fremover fra beregningsdatoen for Kanban-antall som behov er inkludert i behovsberegningen.</span><span class="sxs-lookup"><span data-stu-id="49e36-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="49e36-126">Formelen som brukes i beregningen, vises med de faktiske verdiene.</span><span class="sxs-lookup"><span data-stu-id="49e36-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="49e36-127">Eksempel: Kanban-antall = ((gjennomsnittlig daglig behov x leveringstid x 2.00) / produktantall per håndteringsenhet) + 1</span><span class="sxs-lookup"><span data-stu-id="49e36-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="49e36-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="49e36-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="49e36-129">Legg til Kanban-beregningspolicyen i en Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="49e36-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="49e36-130">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="49e36-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="49e36-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="49e36-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49e36-132">Velg kanban-regel 000020 for denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="49e36-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="49e36-133">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="49e36-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="49e36-134">Aktiver utvidelsen av delen Policyer for Kanban-antallsberegning.</span><span class="sxs-lookup"><span data-stu-id="49e36-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="49e36-135">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="49e36-135">Click Add.</span></span>
    * <span data-ttu-id="49e36-136">Legg til policyen for Kanban-antallsberegning som du nettopp opprettet i den forrige delaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="49e36-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="49e36-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="49e36-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="49e36-138">Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="49e36-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="49e36-139">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="49e36-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="49e36-140">Velg policyen Speaker2016 som du nettopp opprettet i den forrige delaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="49e36-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]