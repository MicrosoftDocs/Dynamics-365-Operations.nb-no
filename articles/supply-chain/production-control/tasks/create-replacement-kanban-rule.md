---
title: Opprette en ny Kanban-regel
description: Denne prosedyren fokuserer på å erstatte en eksisterende kanban-regel med en ny kanban-regel på en bestemt dato.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d68087afd1a0c9b675e4ac1ef2118e6aab5213d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998659"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="1a26a-103">Opprette en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="1a26a-103">Create a replacement kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a26a-104">Denne prosedyren fokuserer på å erstatte en eksisterende kanban-regel med en ny kanban-regel på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="1a26a-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="1a26a-105">Dette er nyttig når endringer i reglene for produksjonsflyt eller etterfylling må koordineres og planlegges.</span><span class="sxs-lookup"><span data-stu-id="1a26a-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="1a26a-106">USMF-demodatafirmaet brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="1a26a-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="1a26a-107">Denne fremgangsmåten er ment for prosessingeniøren eller verdistrømlederen når de klargjør produksjon for en endret produksjonsflyt eller en ny etterfyllingsregel.</span><span class="sxs-lookup"><span data-stu-id="1a26a-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="1a26a-108">Denne oppgaven kanban-regel 000022 med en ny regel og øker det maksimale antallet fra 48-100 for den nye regelen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="1a26a-109">Velge en kanban-regel å erstatte</span><span class="sxs-lookup"><span data-stu-id="1a26a-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="1a26a-110">Gå til Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="1a26a-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="1a26a-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1a26a-112">Velg Kanban-regel 000022.</span><span class="sxs-lookup"><span data-stu-id="1a26a-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="1a26a-113">Opprette en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="1a26a-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="1a26a-114">Klikk på Erstatt Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="1a26a-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="1a26a-115">Angi dato og klokkeslett i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="1a26a-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="1a26a-116">Velg en dato i fremtiden, for eksempel én uke fra nå.</span><span class="sxs-lookup"><span data-stu-id="1a26a-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="1a26a-117">Dette er datoen og klokkeslettet da den nye kanban-regelen blir aktiv og erstatter den gamle kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="1a26a-118">Hvis kanban-regelen endrer banen i produksjonsflyten, kan du velge en annen aktivitet.</span><span class="sxs-lookup"><span data-stu-id="1a26a-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="1a26a-119">I denne fremgangsmåten beholder vi aktiviteten uendret.</span><span class="sxs-lookup"><span data-stu-id="1a26a-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="1a26a-120">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="1a26a-120">Click OK.</span></span>
    * <span data-ttu-id="1a26a-121">Legg merke til at det opprettes en ny kanban-regel som erstatter kanban-regel 000022.</span><span class="sxs-lookup"><span data-stu-id="1a26a-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="1a26a-122">Gyldighetsdatoen angis i henhold til datoen som velges når du erstatter kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="1a26a-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1a26a-124">Velg den erstattede kanban-regelen 000022.</span><span class="sxs-lookup"><span data-stu-id="1a26a-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="1a26a-125">Legg merke til at den erstattede kanban-regelen har samme dato som utløpsdatoen fordi dette er datoen den utløper.</span><span class="sxs-lookup"><span data-stu-id="1a26a-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="1a26a-126">Velg rad 1 i listen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="1a26a-127">Velg den nye kanban-regelen øverst i listen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="1a26a-128">Dette er Kanban-regelen med det høyeste kanban-regelnummeret.</span><span class="sxs-lookup"><span data-stu-id="1a26a-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="1a26a-129">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1a26a-130">Klikk på kanban-regelnummeret for å åpne kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="1a26a-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="1a26a-131">Endre maksimalt antall for den nye kanban-regelen</span><span class="sxs-lookup"><span data-stu-id="1a26a-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="1a26a-132">Sett Maksimalt antall til 100.</span><span class="sxs-lookup"><span data-stu-id="1a26a-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="1a26a-133">Vis hurtigfanen Antall hvis du vil vise Maksimalt antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="1a26a-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="1a26a-134">Hvis du endrer det maksimale antallet til 100, kan opptil 100 Kanbaner behandles.</span><span class="sxs-lookup"><span data-stu-id="1a26a-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="1a26a-135">Dette er det siste trinnet i oppgaven.</span><span class="sxs-lookup"><span data-stu-id="1a26a-135">This is the last step in this task.</span></span>  

