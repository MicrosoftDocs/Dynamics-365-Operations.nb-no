---
title: Opprette en operasjonsressurs
description: En operasjonsressurs utfører aktivitetene for et prosjekt eller en produksjonsprosess.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 514b0b27065b4318891a84f364b39e8e378d6a4a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255091"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="0aa53-103">Opprette en operasjonsressurs</span><span class="sxs-lookup"><span data-stu-id="0aa53-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0aa53-104">En operasjonsressurs utfører aktivitetene for et prosjekt eller en produksjonsprosess.</span><span class="sxs-lookup"><span data-stu-id="0aa53-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="0aa53-105">Denne prosedyren viser hvordan du definerer en operasjonsressurs.</span><span class="sxs-lookup"><span data-stu-id="0aa53-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="0aa53-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="0aa53-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="0aa53-107">Gå til Ressurser.</span><span class="sxs-lookup"><span data-stu-id="0aa53-107">Go to Resources.</span></span>
2. <span data-ttu-id="0aa53-108">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="0aa53-108">Click New.</span></span>
3. <span data-ttu-id="0aa53-109">Skriv inn en verdi i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="0aa53-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0aa53-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="0aa53-111">Definere parametere for kapasitet og forbruk</span><span class="sxs-lookup"><span data-stu-id="0aa53-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="0aa53-112">Utvid delen Operasjon.</span><span class="sxs-lookup"><span data-stu-id="0aa53-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="0aa53-113">Angi et nummer i Svinnprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="0aa53-114">Angi eller velg en verdi i Oppsettkategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="0aa53-115">Angi kostkategorien som definerer hvordan du kan ta hensyn til kostnadene for oppsett.</span><span class="sxs-lookup"><span data-stu-id="0aa53-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="0aa53-116">Angi eller velg en verdi i Kjøretid-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="0aa53-117">Angi kostkategorien som definerer hvordan du kan ta hensyn til kostnadene for operasjonstid.</span><span class="sxs-lookup"><span data-stu-id="0aa53-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="0aa53-118">Angi eller velg en verdi i Antallskategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="0aa53-119">Angi kostkategorien som definerer hvordan du kan ta hensyn til ressurskostnadene basert på produsert antall.</span><span class="sxs-lookup"><span data-stu-id="0aa53-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="0aa53-120">Velg et alternativ i Kapasitetsenhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="0aa53-121">Angi enheten som skal brukes til å uttrykke kapasitet for operasjonsressursen.</span><span class="sxs-lookup"><span data-stu-id="0aa53-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="0aa53-122">Angi et tall i Kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="0aa53-123">Angi et tall i Effektivitetsprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="0aa53-124">Angi effektiviteten som du forventer fra operasjonsressursen.</span><span class="sxs-lookup"><span data-stu-id="0aa53-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="0aa53-125">Effektivitetsprosenten justerer produksjonen for operasjonsressursen, og påvirker tiden som er reservert for ressursen.</span><span class="sxs-lookup"><span data-stu-id="0aa53-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="0aa53-126">Angi et tall i prosentfeltet for grovplanlegging.</span><span class="sxs-lookup"><span data-stu-id="0aa53-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="0aa53-127">Angi maksimumsprosenten av kapasiteten til operasjonsressursen du vil bruke til grovplanlegging.</span><span class="sxs-lookup"><span data-stu-id="0aa53-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="0aa53-128">Velg Ja i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="0aa53-129">Sett dette alternativet til Ja hvis operasjonsressursen skal planlegges på grunnlag av faktisk kapasitet som er tilgjengelig, og hvis eksisterende kapasitetsreservasjoner skal anses.</span><span class="sxs-lookup"><span data-stu-id="0aa53-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="0aa53-130">Hvis dette alternativet er satt til Nei, antas operasjonsressursen å ha ubegrenset kapasitet, og ressursen kan være overbestilt.</span><span class="sxs-lookup"><span data-stu-id="0aa53-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="0aa53-131">Velg Ja i Flaskehalsressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="0aa53-132">Definere arbeidstider</span><span class="sxs-lookup"><span data-stu-id="0aa53-132">Define working times</span></span>
1. <span data-ttu-id="0aa53-133">Utvid seksjonen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="0aa53-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="0aa53-134">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="0aa53-134">Click Add.</span></span>
3. <span data-ttu-id="0aa53-135">Angi eller velg en verdi i Kalender-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="0aa53-136">Angi arbeidstidskalenderen som definerer kapasiteten (i timer) for ressursen.</span><span class="sxs-lookup"><span data-stu-id="0aa53-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="0aa53-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0aa53-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0aa53-138">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0aa53-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="0aa53-139">Definere ressursfunksjoner</span><span class="sxs-lookup"><span data-stu-id="0aa53-139">Define resource capabilities</span></span>
1. <span data-ttu-id="0aa53-140">Vis delen Muligheter.</span><span class="sxs-lookup"><span data-stu-id="0aa53-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="0aa53-141">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="0aa53-141">Click Add.</span></span>
    * <span data-ttu-id="0aa53-142">En funksjon er muligheten for en operasjonsressurs til å utføre en bestemt aktivitet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="0aa53-143">Planleggingsmotoren tildeler ressurser ved å sammenligne ressurskravene for hver aktivitet med egenskapene til de tilgjengelige operasjonsressursene.</span><span class="sxs-lookup"><span data-stu-id="0aa53-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="0aa53-144">Angi eller velg en verdi i Funksjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="0aa53-145">Angi et nummer i Nivå-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="0aa53-146">Angi ferdighetsnivået som ressursen behandler muligheten med.</span><span class="sxs-lookup"><span data-stu-id="0aa53-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="0aa53-147">Angi et tall i Prioritet-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="0aa53-148">Angi prioriteten for operasjonsressursen med hensyn til kapasiteten.</span><span class="sxs-lookup"><span data-stu-id="0aa53-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="0aa53-149">Når du planlegger etter prioritet, velges først operasjonsressursen med den høyeste prioriteten (lavest numerisk verdi).</span><span class="sxs-lookup"><span data-stu-id="0aa53-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="0aa53-150">Tilordne ressurs til ressursgruppe</span><span class="sxs-lookup"><span data-stu-id="0aa53-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="0aa53-151">Utvid seksjonen Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="0aa53-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="0aa53-152">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="0aa53-152">Click Add.</span></span>
    * <span data-ttu-id="0aa53-153">Ressursgruppen definerer området, produksjonsenheten og lagerkonteksten for operasjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="0aa53-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="0aa53-154">Operasjonsressursen kan bare planlegges når tilordnet til en ressursgruppe, og bare på området der ressursgruppen finnes.</span><span class="sxs-lookup"><span data-stu-id="0aa53-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="0aa53-155">Angi eller velg en verdi i Ressursgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="0aa53-156">Angi eller velg en verdi i Innleveringssted-feltet.</span><span class="sxs-lookup"><span data-stu-id="0aa53-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="0aa53-157">Angi lagerlokasjonen der operasjonsressursen forbruker materialer.</span><span class="sxs-lookup"><span data-stu-id="0aa53-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]