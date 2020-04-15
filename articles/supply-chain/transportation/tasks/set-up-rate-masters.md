---
title: Definere vurderingsstandarder
description: Denne fremgangsmåten viser hvordan du setter opp en vurderingsstandard.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aaceb78029408dcea67d0382fd1fc05e550d02a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146198"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="e0398-103">Definere vurderingsstandarder</span><span class="sxs-lookup"><span data-stu-id="e0398-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0398-104">Denne fremgangsmåten viser hvordan du setter opp en vurderingsstandard.</span><span class="sxs-lookup"><span data-stu-id="e0398-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="e0398-105">Logistikklederen setter vanligvis opp vurderingsstandardene, avhengig av kontraktene som er signert med transportørene.</span><span class="sxs-lookup"><span data-stu-id="e0398-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="e0398-106">I dette scenarioet definerer du en vurderingsstandard for en flytransportør.</span><span class="sxs-lookup"><span data-stu-id="e0398-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="e0398-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e0398-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="e0398-108">Definer vurderingsstandard</span><span class="sxs-lookup"><span data-stu-id="e0398-108">Set up rate master</span></span>
1. <span data-ttu-id="e0398-109">Gå til Transportstyring > Oppsett > Vurdering > Vurderingsstandard.</span><span class="sxs-lookup"><span data-stu-id="e0398-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="e0398-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e0398-110">Click New.</span></span>
3. <span data-ttu-id="e0398-111">Skriv inn en verdi i Vurderingsstandard-feltet.</span><span class="sxs-lookup"><span data-stu-id="e0398-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="e0398-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="e0398-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e0398-113">Klikk rullegardinknappen i feltet ID for metadata for vurdering for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e0398-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e0398-114">ID-en for metadata for vurdering bestemmer dataene som kreves for vurderingsstandarden fordi den definerer metadataene forventet av TMS-motoren som bruker denne vurderingsstandarden.</span><span class="sxs-lookup"><span data-stu-id="e0398-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="e0398-115">I dette eksemplet velger du alternativet P2P</span><span class="sxs-lookup"><span data-stu-id="e0398-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="e0398-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e0398-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0398-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e0398-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="e0398-118">Konfigurer satsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="e0398-118">Set up rate base</span></span>
1. <span data-ttu-id="e0398-119">Klikk Satsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e0398-119">Click Rate base.</span></span>
    * <span data-ttu-id="e0398-120">Satsgrunnlaget bestemmer satsen for transportøren, og kan brukes til å definere en tariffstruktur ettersom den strukturerer satsene i bruddpunktene definert i pausestandarden.</span><span class="sxs-lookup"><span data-stu-id="e0398-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="e0398-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e0398-121">Click New.</span></span>
3. <span data-ttu-id="e0398-122">Skriv inn en verdi i Satsgrunnlag-feltet.</span><span class="sxs-lookup"><span data-stu-id="e0398-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="e0398-123">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="e0398-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e0398-124">Klikk rullegardinknappen i feltet Pausestandard for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e0398-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e0398-125">Pausestandarder brukes til å definere prissettingsstrukturen og dens bruddpunkter.</span><span class="sxs-lookup"><span data-stu-id="e0398-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="e0398-126">Prissettingsstrukturen bruker fordelte priser som er basert på fysiske dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="e0398-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="e0398-127">I dette eksemplet bruker du vekt</span><span class="sxs-lookup"><span data-stu-id="e0398-127">For this example, use weight</span></span>
7. <span data-ttu-id="e0398-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e0398-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0398-129">Aktiver/deaktiver utvidelsen av delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="e0398-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="e0398-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e0398-130">Click New.</span></span>
10. <span data-ttu-id="e0398-131">Skriv inn 30301 i feltet Fra-postnummer for levering.</span><span class="sxs-lookup"><span data-stu-id="e0398-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="e0398-132">Skriv inn 30318 i feltet Til-postnummer for levering.</span><span class="sxs-lookup"><span data-stu-id="e0398-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="e0398-133">Skriv inn USA i feltet Land/område for levering.</span><span class="sxs-lookup"><span data-stu-id="e0398-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="e0398-134">I feltet <1,00 kg skriver du inn 100.</span><span class="sxs-lookup"><span data-stu-id="e0398-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="e0398-135">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 1 pund.</span><span class="sxs-lookup"><span data-stu-id="e0398-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="e0398-136">I feltet <5,00 kg skriver du inn 300.</span><span class="sxs-lookup"><span data-stu-id="e0398-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="e0398-137">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 5 pund.</span><span class="sxs-lookup"><span data-stu-id="e0398-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="e0398-138">I feltet <20,00 kg skriver du inn 500.</span><span class="sxs-lookup"><span data-stu-id="e0398-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="e0398-139">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 20 pund.</span><span class="sxs-lookup"><span data-stu-id="e0398-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="e0398-140">I feltet <100,00 kg skriver du inn 1000.</span><span class="sxs-lookup"><span data-stu-id="e0398-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="e0398-141">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 100 pund.</span><span class="sxs-lookup"><span data-stu-id="e0398-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="e0398-142">I feltet <1.000,00 kg skriver du inn 3000.</span><span class="sxs-lookup"><span data-stu-id="e0398-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="e0398-143">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 1000 pund.</span><span class="sxs-lookup"><span data-stu-id="e0398-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="e0398-144">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e0398-144">Click Save.</span></span>
19. <span data-ttu-id="e0398-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e0398-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="e0398-146">Tilordne satsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="e0398-146">Assign rate base</span></span>
1. <span data-ttu-id="e0398-147">Aktiver/deaktiver utvidelsen av delen Tilordninger av satsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e0398-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="e0398-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e0398-148">Click New.</span></span>
    * <span data-ttu-id="e0398-149">Du kan ha flere tilordninger av satsgrunnlag for hver vurderingsstandard.</span><span class="sxs-lookup"><span data-stu-id="e0398-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="e0398-150">Dette gjør det mulig å opprette flere forskjellige prispunkter for hver transportør avhengig av mål, tjenester eller andre satsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e0398-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="e0398-151">I denne fremgangsmåten vil du bare opprette én tilordning av satsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e0398-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="e0398-152">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="e0398-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e0398-153">Klikk rullegardinknappen i feltet Satsgrunnlag for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e0398-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e0398-154">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e0398-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e0398-155">Klikk rullegardinknappen i feltet Service for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e0398-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e0398-156">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e0398-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e0398-157">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e0398-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e0398-158">I feltet Postnummer for henting skriver du inn 98052.</span><span class="sxs-lookup"><span data-stu-id="e0398-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="e0398-159">Angi hvilket postnummer denne tilordningen av satsgrunnlag skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="e0398-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="e0398-160">I feltet Land/område for henting skriver du inn USA.</span><span class="sxs-lookup"><span data-stu-id="e0398-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="e0398-161">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e0398-161">Click Save.</span></span>

