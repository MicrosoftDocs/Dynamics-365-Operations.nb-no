---
title: Definere vurderingsstandarder
description: Denne fremgangsmåten viser hvordan du setter opp en vurderingsstandard.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808996"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="f6fb8-103">Definere vurderingsstandarder</span><span class="sxs-lookup"><span data-stu-id="f6fb8-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6fb8-104">Denne fremgangsmåten viser hvordan du setter opp en vurderingsstandard.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="f6fb8-105">Logistikklederen setter vanligvis opp vurderingsstandardene, avhengig av kontraktene som er signert med transportørene.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="f6fb8-106">I dette scenarioet definerer du en vurderingsstandard for en flytransportør.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="f6fb8-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="f6fb8-108">Definere pausestandard</span><span class="sxs-lookup"><span data-stu-id="f6fb8-108">Set up break master</span></span>

1. <span data-ttu-id="f6fb8-109">Gå til **Transportstyring > Oppsett > Vurdering > Pausestandard**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="f6fb8-110">Pausestandarder brukes til å definere prissettingsstrukturen og dens bruddpunkter.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="f6fb8-111">Prissettingsstrukturen bruker fordelte priser som er basert på fysiske dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="f6fb8-112">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-112">Select **New**.</span></span>
1. <span data-ttu-id="f6fb8-113">Angi en verdi i feltet **Pausestandard**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="f6fb8-114">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="f6fb8-115">I **Datatype**-feltet velger du datatypen.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="f6fb8-116">I **Sammenligning**-feltet angir du den typen sammenligning som er forespurt (ved hjelp av operatorer).</span><span class="sxs-lookup"><span data-stu-id="f6fb8-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="f6fb8-117">I **Pauseenhet**-feltet angir du pauseenheten.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="f6fb8-118">I **Detaljer**-delen oppretter du så mange pauser som nødvendig for prissettingsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="f6fb8-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="f6fb8-120">Definer vurderingsstandard</span><span class="sxs-lookup"><span data-stu-id="f6fb8-120">Set up rate master</span></span>

1. <span data-ttu-id="f6fb8-121">Gå til **Transportstyring > Oppsett > Vurdering > Vurderingsstandard**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="f6fb8-122">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-122">Select **New**.</span></span>
1. <span data-ttu-id="f6fb8-123">Skriv inn en verdi i **Vurderingsstandard**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="f6fb8-124">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="f6fb8-125">Velg rullegardinknappen i feltet **ID for metadata for vurdering** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="f6fb8-126">ID-en for metadata for vurdering bestemmer dataene som kreves for vurderingsstandarden fordi den definerer metadataene forventet av transportstyringsmotoren som bruker denne vurderingsstandarden.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="f6fb8-127">I dette eksemplet velger du alternativet P2P.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-127">For this example, select the P2P option.</span></span> <span data-ttu-id="f6fb8-128">Dette er allerede definert i demodataene.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="f6fb8-129">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="f6fb8-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="f6fb8-131">Konfigurer satsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="f6fb8-131">Set up rate base</span></span>

1. <span data-ttu-id="f6fb8-132">Velg **Satsgrunnlag**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="f6fb8-133">Satsgrunnlaget bestemmer satsen for transportøren, og kan brukes til å definere en tariffstruktur ettersom den strukturerer satsene i bruddpunktene definert i pausestandarden.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="f6fb8-134">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-134">Select **New**.</span></span>
3. <span data-ttu-id="f6fb8-135">Skriv inn en verdi i **Satsgrunnlag**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="f6fb8-136">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="f6fb8-137">Velg rullegardinknappen i feltet **Pausestandard** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f6fb8-138">Pausestandarder brukes til å definere prissettingsstrukturen og dens bruddpunkter.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="f6fb8-139">Prissettingsstrukturen bruker fordelte priser som er basert på fysiske dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="f6fb8-140">I dette eksemplet bruker du vekt.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-140">For this example, use weight.</span></span> <span data-ttu-id="f6fb8-141">Dette er allerede definert i demodataene.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="f6fb8-142">Velg koblingen i den uthevede raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="f6fb8-143">Vis delen **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="f6fb8-144">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-144">Select **New**.</span></span>
10. <span data-ttu-id="f6fb8-145">Skriv inn 30301 i feltet **Fra-postnummer for levering**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="f6fb8-146">Skriv inn 30318 i feltet **Til-postnummer for levering**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="f6fb8-147">Skriv inn USA i feltet **Land/område for levering**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="f6fb8-148">I feltet **<1,00 kg** skriver du inn 100.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="f6fb8-149">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 1 pund.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="f6fb8-150">I feltet **<5,00 kg** skriver du inn 300.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="f6fb8-151">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 5 pund.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="f6fb8-152">I feltet **<20,00 kg** skriver du inn 500.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="f6fb8-153">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 20 pund.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="f6fb8-154">I feltet **<100,00 kg** skriver du inn 1000.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="f6fb8-155">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 100 pund.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="f6fb8-156">I feltet **<1.000,00 kg** skriver du inn 3000.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="f6fb8-157">Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 1000 pund.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="f6fb8-158">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-158">Select **Save**.</span></span>
19. <span data-ttu-id="f6fb8-159">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="f6fb8-160">Tilordne satsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="f6fb8-160">Assign rate base</span></span>

1. <span data-ttu-id="f6fb8-161">Vis delen **Tilordninger av satsgrunnlag**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="f6fb8-162">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-162">Select **New**.</span></span>
    * <span data-ttu-id="f6fb8-163">Du kan ha flere tilordninger av satsgrunnlag for hver vurderingsstandard.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="f6fb8-164">Dette gjør det mulig å opprette flere forskjellige prispunkter for hver transportør avhengig av mål, tjenester eller andre satsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="f6fb8-165">I denne fremgangsmåten vil du bare opprette én tilordning av satsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="f6fb8-166">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f6fb8-167">Velg rullegardinknappen i feltet **Satsgrunnlag** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f6fb8-168">Velg koblingen i den uthevede raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="f6fb8-169">Velg rullegardinknappen i feltet **Tjeneste** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f6fb8-170">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f6fb8-171">Velg koblingen i den uthevede raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="f6fb8-172">I feltet **Postnummer for henting** skriver du inn 98052.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="f6fb8-173">Angi hvilket postnummer denne tilordningen av satsgrunnlag skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="f6fb8-174">I feltet **Land/område for henting** skriver du inn USA.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="f6fb8-175">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f6fb8-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]