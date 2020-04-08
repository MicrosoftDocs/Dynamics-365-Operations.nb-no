---
title: Opprette en operasjonsressurs
description: En operasjonsressurs utfører aktivitetene for et prosjekt eller en produksjonsprosess.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c4836b6f51f0be5afbdb55838dde27b3aaec5c1
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146980"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="bd676-103">Opprette en operasjonsressurs</span><span class="sxs-lookup"><span data-stu-id="bd676-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd676-104">En operasjonsressurs utfører aktivitetene for et prosjekt eller en produksjonsprosess.</span><span class="sxs-lookup"><span data-stu-id="bd676-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="bd676-105">Denne prosedyren viser hvordan du definerer en operasjonsressurs.</span><span class="sxs-lookup"><span data-stu-id="bd676-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="bd676-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="bd676-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="bd676-107">Gå til Ressurser.</span><span class="sxs-lookup"><span data-stu-id="bd676-107">Go to Resources.</span></span>
2. <span data-ttu-id="bd676-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bd676-108">Click New.</span></span>
3. <span data-ttu-id="bd676-109">Skriv inn en verdi i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="bd676-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="bd676-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="bd676-111">Definere parametere for kapasitet og forbruk</span><span class="sxs-lookup"><span data-stu-id="bd676-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="bd676-112">Utvid delen Operasjon.</span><span class="sxs-lookup"><span data-stu-id="bd676-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="bd676-113">Angi et nummer i Svinnprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="bd676-114">Angi eller velg en verdi i Oppsettkategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="bd676-115">Angi kostkategorien som definerer hvordan du kan ta hensyn til kostnadene for oppsett.</span><span class="sxs-lookup"><span data-stu-id="bd676-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="bd676-116">Angi eller velg en verdi i Kjøretid-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="bd676-117">Angi kostkategorien som definerer hvordan du kan ta hensyn til kostnadene for operasjonstid.</span><span class="sxs-lookup"><span data-stu-id="bd676-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="bd676-118">Angi eller velg en verdi i Antallskategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="bd676-119">Angi kostkategorien som definerer hvordan du kan ta hensyn til ressurskostnadene basert på produsert antall.</span><span class="sxs-lookup"><span data-stu-id="bd676-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="bd676-120">Velg et alternativ i Kapasitetsenhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="bd676-121">Angi enheten som skal brukes til å uttrykke kapasitet for operasjonsressursen.</span><span class="sxs-lookup"><span data-stu-id="bd676-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="bd676-122">Angi et tall i Kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="bd676-123">Angi et tall i Effektivitetsprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="bd676-124">Angi effektiviteten som du forventer fra operasjonsressursen.</span><span class="sxs-lookup"><span data-stu-id="bd676-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="bd676-125">Effektivitetsprosenten justerer produksjonen for operasjonsressursen, og påvirker tiden som er reservert for ressursen.</span><span class="sxs-lookup"><span data-stu-id="bd676-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="bd676-126">Angi et tall i prosentfeltet for grovplanlegging.</span><span class="sxs-lookup"><span data-stu-id="bd676-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="bd676-127">Angi maksimumsprosenten av kapasiteten til operasjonsressursen du vil bruke til grovplanlegging.</span><span class="sxs-lookup"><span data-stu-id="bd676-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="bd676-128">Velg Ja i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="bd676-129">Sett dette alternativet til Ja hvis operasjonsressursen skal planlegges på grunnlag av faktisk kapasitet som er tilgjengelig, og hvis eksisterende kapasitetsreservasjoner skal anses.</span><span class="sxs-lookup"><span data-stu-id="bd676-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="bd676-130">Hvis dette alternativet er satt til Nei, antas operasjonsressursen å ha ubegrenset kapasitet, og ressursen kan være overbestilt.</span><span class="sxs-lookup"><span data-stu-id="bd676-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="bd676-131">Velg Ja i Flaskehalsressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="bd676-132">Definere arbeidstider</span><span class="sxs-lookup"><span data-stu-id="bd676-132">Define working times</span></span>
1. <span data-ttu-id="bd676-133">Utvid seksjonen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="bd676-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="bd676-134">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd676-134">Click Add.</span></span>
3. <span data-ttu-id="bd676-135">Angi eller velg en verdi i Kalender-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="bd676-136">Angi arbeidstidskalenderen som definerer kapasiteten (i timer) for ressursen.</span><span class="sxs-lookup"><span data-stu-id="bd676-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="bd676-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bd676-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bd676-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bd676-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="bd676-139">Definere ressursfunksjoner</span><span class="sxs-lookup"><span data-stu-id="bd676-139">Define resource capabilities</span></span>
1. <span data-ttu-id="bd676-140">Vis delen Muligheter.</span><span class="sxs-lookup"><span data-stu-id="bd676-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="bd676-141">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd676-141">Click Add.</span></span>
    * <span data-ttu-id="bd676-142">En funksjon er muligheten for en operasjonsressurs til å utføre en bestemt aktivitet.</span><span class="sxs-lookup"><span data-stu-id="bd676-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="bd676-143">Planleggingsmotoren tildeler ressurser ved å sammenligne ressurskravene for hver aktivitet med egenskapene til de tilgjengelige operasjonsressursene.</span><span class="sxs-lookup"><span data-stu-id="bd676-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="bd676-144">Angi eller velg en verdi i Funksjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="bd676-145">Angi et nummer i Nivå-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="bd676-146">Angi ferdighetsnivået som ressursen behandler muligheten med.</span><span class="sxs-lookup"><span data-stu-id="bd676-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="bd676-147">Angi et tall i Prioritet-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="bd676-148">Angi prioriteten for operasjonsressursen med hensyn til kapasiteten.</span><span class="sxs-lookup"><span data-stu-id="bd676-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="bd676-149">Når du planlegger etter prioritet, velges først operasjonsressursen med den høyeste prioriteten (lavest numerisk verdi).</span><span class="sxs-lookup"><span data-stu-id="bd676-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="bd676-150">Tilordne ressurs til ressursgruppe</span><span class="sxs-lookup"><span data-stu-id="bd676-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="bd676-151">Utvid seksjonen Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="bd676-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="bd676-152">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd676-152">Click Add.</span></span>
    * <span data-ttu-id="bd676-153">Ressursgruppen definerer området, produksjonsenheten og lagerkonteksten for operasjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="bd676-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="bd676-154">Operasjonsressursen kan bare planlegges når tilordnet til en ressursgruppe, og bare på området der ressursgruppen finnes.</span><span class="sxs-lookup"><span data-stu-id="bd676-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="bd676-155">Angi eller velg en verdi i Ressursgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="bd676-156">Angi eller velg en verdi i Innleveringssted-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd676-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="bd676-157">Angi lagerlokasjonen der operasjonsressursen forbruker materialer.</span><span class="sxs-lookup"><span data-stu-id="bd676-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

