--- 
title: Beregne forslag til Kanban-antall
description: "Denne prosedyren fokuserer på å optimalisere kanban-størrelse og -antall for en bestemt Kanban-regel ved hjelp av Kanban-antallsberegningen."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 540dd32c5da5859ef5e69f55d6806eada90bc840
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="ccef4-103">Beregne forslag til Kanban-antall</span><span class="sxs-lookup"><span data-stu-id="ccef4-103">Calculate kanban quantity suggestions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ccef4-104">Denne prosedyren fokuserer på å optimalisere kanban-størrelse og -antall for en bestemt Kanban-regel ved hjelp av Kanban-antallsberegningen.</span><span class="sxs-lookup"><span data-stu-id="ccef4-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="ccef4-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ccef4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ccef4-106">Denne fremgangsmåten er ment for verdistrømsbehandling.</span><span class="sxs-lookup"><span data-stu-id="ccef4-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="ccef4-107">Det er en forutsetning at du har fullført prosedyren Legg til en ny policy for Kanban-antallsberegning i en Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="ccef4-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="ccef4-108">Opprett en beregning av Kanban-antall</span><span class="sxs-lookup"><span data-stu-id="ccef4-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="ccef4-109">Gå til Produksjonskontroll > Periodiske oppgaver > Kanban-antallsberegning > Beregn Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="ccef4-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ccef4-110">Click New.</span></span>
3. <span data-ttu-id="ccef4-111">I Navn-feltet skriver du inn Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="ccef4-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="ccef4-112">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ccef4-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ccef4-113">Velg policyen som du har opprettet i prosedyren Legg til en ny policy for Kanban-antallsberegning i en Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="ccef4-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="ccef4-114">For eksempel Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="ccef4-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="ccef4-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ccef4-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ccef4-116">I feltet Aktiveringsdato for regel setter du datoen og klokkeslettet til 2012-12-17T08:00:00.</span><span class="sxs-lookup"><span data-stu-id="ccef4-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="ccef4-117">Denne datoen fungerer som grunnlaget for å bestemme hvilke faste Kanban-regler som skal inngå i beregningen av Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="ccef4-118">I feltet Startdato for innfridd behovsperiode setter du datoen og klokkeslettet til 2012-11-17T09:00:00.</span><span class="sxs-lookup"><span data-stu-id="ccef4-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="ccef4-119">Fra-datoen for å inkludere transaksjoner for tidligere behov i beregning av Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="ccef4-120">I feltet Sluttdato for innfridd behovsperiode setter du datoen og klokkeslettet til 2012-12-17T07:59:59.</span><span class="sxs-lookup"><span data-stu-id="ccef4-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="ccef4-121">Til-datoen for å inkludere transaksjoner for tidligere behov i beregning av Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="ccef4-122">I feltet Startdato for behovsperiode setter du datoen og klokkeslettet til 2012-12-17T08:00:00.</span><span class="sxs-lookup"><span data-stu-id="ccef4-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="ccef4-123">Fra-datoen for å inkludere transaksjoner for nåværende behov i beregning av Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="ccef4-124">I feltet Sluttdato for behovsperiode setter du datoen og klokkeslettet til 2013-01-16T07:59:59.</span><span class="sxs-lookup"><span data-stu-id="ccef4-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="ccef4-125">Til-datoen for å inkludere transaksjoner for nåværende behov i beregning av Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="ccef4-126">Generer Kanban-antallsforslag</span><span class="sxs-lookup"><span data-stu-id="ccef4-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="ccef4-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ccef4-127">Click Save.</span></span>
2. <span data-ttu-id="ccef4-128">Klikk Generer.</span><span class="sxs-lookup"><span data-stu-id="ccef4-128">Click Generate.</span></span>
    * <span data-ttu-id="ccef4-129">Dette genererer en forslagslinje for kanban-antall for kanban-regelen 000020.</span><span class="sxs-lookup"><span data-stu-id="ccef4-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="ccef4-130">Kjør Kanban-antallsberegning</span><span class="sxs-lookup"><span data-stu-id="ccef4-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="ccef4-131">Klikk Beregn.</span><span class="sxs-lookup"><span data-stu-id="ccef4-131">Click Calculate.</span></span>
    * <span data-ttu-id="ccef4-132">Den beregner forslaget for kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="ccef4-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ccef4-133">Click OK.</span></span>
3. <span data-ttu-id="ccef4-134">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ccef4-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ccef4-135">Legg merke til at det foreslåtte kanban-antallet er 2.</span><span class="sxs-lookup"><span data-stu-id="ccef4-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="ccef4-136">Endre produktantallet og beregne på nytt</span><span class="sxs-lookup"><span data-stu-id="ccef4-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="ccef4-137">Sett Produktantall til 5.</span><span class="sxs-lookup"><span data-stu-id="ccef4-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="ccef4-138">Klikk Beregn.</span><span class="sxs-lookup"><span data-stu-id="ccef4-138">Click Calculate.</span></span>
3. <span data-ttu-id="ccef4-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ccef4-139">Click OK.</span></span>
    * <span data-ttu-id="ccef4-140">Legg merke til at med et kanban-antall på 5, endres forslaget til et kanban-antall på 4.</span><span class="sxs-lookup"><span data-stu-id="ccef4-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="ccef4-141">Dette skyldes det faktum at med et lavere produktantall trenger vi flere Kanbaner som skal dekke behovet.</span><span class="sxs-lookup"><span data-stu-id="ccef4-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="ccef4-142">Oppdater Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="ccef4-142">Update kanban rule</span></span>
1. <span data-ttu-id="ccef4-143">Angi dato og klokkeslett i feltet Ikrafttredelsesdato for regel.</span><span class="sxs-lookup"><span data-stu-id="ccef4-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="ccef4-144">Angi Aktiveringsdato for regel til en dato i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="ccef4-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="ccef4-145">For eksempel i dag + ett år.</span><span class="sxs-lookup"><span data-stu-id="ccef4-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="ccef4-146">Klikk Oppdater.</span><span class="sxs-lookup"><span data-stu-id="ccef4-146">Click Update.</span></span>
3. <span data-ttu-id="ccef4-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ccef4-147">Click OK.</span></span>
4. <span data-ttu-id="ccef4-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ccef4-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="ccef4-149">Valider endring i kanban-regel</span><span class="sxs-lookup"><span data-stu-id="ccef4-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="ccef4-150">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="ccef4-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="ccef4-151">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ccef4-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ccef4-152">Velg kanban-regelen som ble opprettet i den forrige underoppgaven.</span><span class="sxs-lookup"><span data-stu-id="ccef4-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="ccef4-153">Dette bør være den første kanban-regelen i listen sortert etter nummer.</span><span class="sxs-lookup"><span data-stu-id="ccef4-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="ccef4-154">Aktiver/deaktiver utvidelsen av delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="ccef4-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="ccef4-155">Legg merke til den gyldige datoen, som betyr at denne regelen ikke aktiveres før denne datoen.</span><span class="sxs-lookup"><span data-stu-id="ccef4-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="ccef4-156">Aktiver/deaktiver utvidelsen av delen Antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="ccef4-157">Legg merke til at dette er standardantallet som du angav i beregningen av kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="ccef4-158">Legg merke til dette er det faste kanban-antallet på 4 fra beregningen av kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ccef4-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="ccef4-159">Klikk kategorien ListPanel.</span><span class="sxs-lookup"><span data-stu-id="ccef4-159">Click the ListPanel tab.</span></span>


