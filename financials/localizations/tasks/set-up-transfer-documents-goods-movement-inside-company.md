--- 
title: "Definere overføringsdokumentene for varebevegelse i et selskap"
description: "Denne fremgangsmåten viser hvordan du oppretter overføringsdokumenter for flytting av varer i et selskap."
author: v-oloski
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2f10f627f33108b8750a1d71d24a99763178e2ef
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="ad794-103">Definere overføringsdokumentene for varebevegelse i et selskap</span><span class="sxs-lookup"><span data-stu-id="ad794-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad794-104">Denne fremgangsmåten viser hvordan du oppretter overføringsdokumenter for flytting av varer i et selskap.</span><span class="sxs-lookup"><span data-stu-id="ad794-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="ad794-105">Denne fremgangsmåten er bare tilgjengelig for juridiske enheter med hovedadresse i Litauen.</span><span class="sxs-lookup"><span data-stu-id="ad794-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="ad794-106">Prosedyren ble opprettet med demonstrasjonsdatafirmaet DEMF med en primæradresse i Litauen.</span><span class="sxs-lookup"><span data-stu-id="ad794-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="ad794-107">Før du kan fullføre denne prosedyren, må du fullføre fremgangsmåten Konfigurere overføringsdokumenter for flytting av varer i et selskap.</span><span class="sxs-lookup"><span data-stu-id="ad794-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="ad794-108">Denne prosedyren er ment for lagerregnskapsførere.</span><span class="sxs-lookup"><span data-stu-id="ad794-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="ad794-109">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="ad794-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="ad794-110">Opprett overføringsordre</span><span class="sxs-lookup"><span data-stu-id="ad794-110">Create a transfer order</span></span>
1. <span data-ttu-id="ad794-111">Gå til Lagerstyring > Innkommende ordrer > Overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="ad794-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="ad794-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ad794-112">Click New.</span></span>
3. <span data-ttu-id="ad794-113">Angi eller velg en verdi i feltet Fra lager.</span><span class="sxs-lookup"><span data-stu-id="ad794-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="ad794-114">Angi eller velg en verdi i feltet Til lager.</span><span class="sxs-lookup"><span data-stu-id="ad794-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="ad794-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ad794-115">Click Add.</span></span>
6. <span data-ttu-id="ad794-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ad794-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="ad794-117">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad794-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="ad794-118">Angi transportdetaljer for overføringsordren</span><span class="sxs-lookup"><span data-stu-id="ad794-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="ad794-119">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ad794-119">Click Save.</span></span>
2. <span data-ttu-id="ad794-120">Klikk Send i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ad794-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="ad794-121">Klikk Transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="ad794-121">Click Transportation details.</span></span>
4. <span data-ttu-id="ad794-122">Velg Ja i feltet Skriv ut transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="ad794-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="ad794-123">Angi eller velg en verdi i feltet Utstedte varer.</span><span class="sxs-lookup"><span data-stu-id="ad794-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="ad794-124">Skriv inn en verdi i feltet Pakke.</span><span class="sxs-lookup"><span data-stu-id="ad794-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="ad794-125">Skriv inn en verdi i feltet Risikonivå for lasten.</span><span class="sxs-lookup"><span data-stu-id="ad794-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="ad794-126">Angi eller velg en verdi i feltet Transportør.</span><span class="sxs-lookup"><span data-stu-id="ad794-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="ad794-127">Angi eller velg en verdi i feltet Modell.</span><span class="sxs-lookup"><span data-stu-id="ad794-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="ad794-128">Skriv inn en verdi i feltet Registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="ad794-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="ad794-129">Skriv inn en verdi i feltet Registreringsnummer for lastebil</span><span class="sxs-lookup"><span data-stu-id="ad794-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="ad794-130">Angi eller velg en verdi i feltet Sjåfør.</span><span class="sxs-lookup"><span data-stu-id="ad794-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="ad794-131">Skriv inn en verdi i feltet for sjåførnavn.</span><span class="sxs-lookup"><span data-stu-id="ad794-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="ad794-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ad794-132">Click Save.</span></span>
15. <span data-ttu-id="ad794-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ad794-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="ad794-134">Vise følgeseddelen for den uposterte overføringsordren</span><span class="sxs-lookup"><span data-stu-id="ad794-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="ad794-135">Klikk Følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="ad794-135">Click Packing slip.</span></span>
2. <span data-ttu-id="ad794-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ad794-136">Click OK.</span></span>
3. <span data-ttu-id="ad794-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ad794-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="ad794-138">Vise følgeseddelen for den posterte overføringsordren</span><span class="sxs-lookup"><span data-stu-id="ad794-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="ad794-139">Klikk Overføringsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ad794-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="ad794-140">Klikk Send i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ad794-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="ad794-141">Klikk Send overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="ad794-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="ad794-142">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="ad794-142">Click the General tab.</span></span>
5. <span data-ttu-id="ad794-143">Velg et alternativ i feltet Oppdater.</span><span class="sxs-lookup"><span data-stu-id="ad794-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="ad794-144">Klikk kategorien Oversikt.</span><span class="sxs-lookup"><span data-stu-id="ad794-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="ad794-145">Skriv inn en verdi i Følgeseddel-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad794-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="ad794-146">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ad794-146">Click OK.</span></span>
9. <span data-ttu-id="ad794-147">Klikk Send i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ad794-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="ad794-148">Klikk Følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="ad794-148">Click Packing slip.</span></span>
11. <span data-ttu-id="ad794-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ad794-149">Click OK.</span></span>


