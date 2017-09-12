--- 
title: Opprette Kanban-regel ved hjelp av en hendelse for Kanban-linje
description: "Denne fremgangsmåten oppretter en Kanban-regel ved å bruke hendelsesinnstillingen for Kanban-linjen for å utløse trekk fra en prosessaktivitet."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9ef7b8e920d22cbc4f96676e68a263f2da7f232c
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="3a9aa-103">Opprette Kanban-regel ved hjelp av en hendelse for Kanban-linje</span><span class="sxs-lookup"><span data-stu-id="3a9aa-103">Create a kanban rule using a kanban line event</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a9aa-104">Denne fremgangsmåten oppretter en Kanban-regel ved å bruke hendelsesinnstillingen for Kanban-linjen for å utløse trekk fra en prosessaktivitet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="3a9aa-105">Kanban-regelen blir utløst av en kanban-prosessaktivitet, med et antall like eller større enn 25 hver.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="3a9aa-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="3a9aa-107">Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="3a9aa-108">Opprette en Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="3a9aa-108">Create a kanban rule</span></span>
1. <span data-ttu-id="3a9aa-109">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="3a9aa-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-110">Click New.</span></span>
3. <span data-ttu-id="3a9aa-111">Velg Hendelse i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="3a9aa-112">Dette genererer Kanbaner direkte fra behovet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="3a9aa-113">Den brukes til å definere regler som definerer et bestillingsproduktscenario.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="3a9aa-114">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="3a9aa-115">Angi eller velg SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="3a9aa-116">Den første aktiviteten i en Kanban-regel er en prosessaktivitet i produksjonsflyten.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="3a9aa-117">Når du velger aktiviteten, blir gyldighetsdatoene for aktiviteten kopiert til gyldighetsdatoene for Kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="3a9aa-118">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-118">Expand the Details section.</span></span>
6. <span data-ttu-id="3a9aa-119">Skriv L0001 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="3a9aa-120">Utvid delen Hendelser.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-120">Expand the Events section.</span></span>
8. <span data-ttu-id="3a9aa-121">Velg Automatisk i hendelsesfeltet Kanban-linje.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="3a9aa-122">Dette genererer hendelses-Kanbaner ved behov.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="3a9aa-123">Dette feltet brukes for å konfigurere Kanban-regler som etterfyller materiale som kreves for en etterfølgende prosessaktivitet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="3a9aa-124">Når du velger Automatisk, opprettes hendelses-Kanbaner med behovet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="3a9aa-125">Denne innstillingen anbefales hvis du har tenkt å utføre produksjon på samme dag.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="3a9aa-126">Sett Minimumsantall for hendelse til 25.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="3a9aa-127">Hendelses-Kanbaner genereres når behovsantallet er lik eller større enn dette feltet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="3a9aa-128">Dette er nyttig hvis du vil produsere et ordreantall som er mindre enn dette feltet på en maskin og flere enn dette feltet på en annen maskin.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="3a9aa-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="3a9aa-130">Opprette salgsordre og utløse Kanban-kjede</span><span class="sxs-lookup"><span data-stu-id="3a9aa-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="3a9aa-131">Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="3a9aa-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-132">Click New.</span></span>
3. <span data-ttu-id="3a9aa-133">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="3a9aa-134">Velg kundekontoen USA-003, Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="3a9aa-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-135">Click OK.</span></span>
5. <span data-ttu-id="3a9aa-136">Skriv inn L0001 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="3a9aa-137">L0001 er varen du opprettet Kanban-regelen for.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="3a9aa-138">Sett verdien for Antall til 27.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="3a9aa-139">Siden 27 er høyere enn minimumsantallet 25 i Kanban-regelen, utløser dette en hendelses-Kanban.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="3a9aa-140">Skriv inn 1 i feltet Område.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="3a9aa-141">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="3a9aa-142">Velg lager 13.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="3a9aa-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="3a9aa-144">Vise Kanban som er generert av Kanban-regelen</span><span class="sxs-lookup"><span data-stu-id="3a9aa-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="3a9aa-145">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="3a9aa-146">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3a9aa-147">Vis delen Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="3a9aa-148">Legg merke til at en Kanban for 27 ble opprettet for å behandle aktiviteten basert på den opprettede Kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="3a9aa-149">Dette er det siste trinnet.</span><span class="sxs-lookup"><span data-stu-id="3a9aa-149">This is the last step.</span></span>  


