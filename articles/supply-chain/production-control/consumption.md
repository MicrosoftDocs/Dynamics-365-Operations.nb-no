---
title: Beregne materialforbruk
description: Denne artikkelen inneholder informasjon om ulike alternativer som er knyttet til beregning av materialforbruk.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8defe5735726e877f37d8595a6aaa7c3d14d226b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="calculate-material-consumption"></a><span data-ttu-id="55b06-103">Beregne materialforbruk</span><span class="sxs-lookup"><span data-stu-id="55b06-103">Calculate material consumption</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="55b06-104">Denne artikkelen inneholder informasjon om ulike alternativer som er knyttet til beregning av materialforbruk.</span><span class="sxs-lookup"><span data-stu-id="55b06-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="55b06-105">Følgende alternativer som er knyttet til beregningen av materialforbruk, er tilgjengelige i fanen **Oppsett** og **Trinnforbruk** i hurtigfanen **Linjedetaljer** på **Stykkliste**-siden.</span><span class="sxs-lookup"><span data-stu-id="55b06-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="55b06-106">Variabelt og konstant forbruk</span><span class="sxs-lookup"><span data-stu-id="55b06-106">Variable and constant consumption</span></span>
<span data-ttu-id="55b06-107">I feltet **Forbruk er** kan du velge om forbruk skal beregnes som et konstant antall eller et variabelt antall.</span><span class="sxs-lookup"><span data-stu-id="55b06-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="55b06-108">Velg **Konstant** hvis et fast antall eller volum eller kreves for produksjonen, uansett antallet som produseres.</span><span class="sxs-lookup"><span data-stu-id="55b06-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="55b06-109">Velg **Variabel**, som er standardinnstillingen, hvis den nødvendige mengden materiale i ferdigvarene er proporsjonal med antall ferdigvarer som produseres.</span><span class="sxs-lookup"><span data-stu-id="55b06-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="55b06-110">Beregne forbruk med en formel</span><span class="sxs-lookup"><span data-stu-id="55b06-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="55b06-111">I **Formel**-feltet kan du definere forskjellige formler for beregning av materialforbruk.</span><span class="sxs-lookup"><span data-stu-id="55b06-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="55b06-112">Hvis du bruker standardverdien **Standard**, beregnes ikke forbruket av en formel.</span><span class="sxs-lookup"><span data-stu-id="55b06-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="55b06-113">Følgende formler fungerer sammen med feltet **Høyde**, **Bredde**, **Dybde**, **Tetthet** og **Konstant**:</span><span class="sxs-lookup"><span data-stu-id="55b06-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="55b06-114">Høyde \* Konstant</span><span class="sxs-lookup"><span data-stu-id="55b06-114">Height \* Constant</span></span>
-   <span data-ttu-id="55b06-115">Høyde \* Bredde \* Konstant</span><span class="sxs-lookup"><span data-stu-id="55b06-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="55b06-116">Høyde \* Bredde \* Dybde \* Konstant</span><span class="sxs-lookup"><span data-stu-id="55b06-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="55b06-117">(Høyde \* Bredde \* Dybde/Tetthet) \* Konstant</span><span class="sxs-lookup"><span data-stu-id="55b06-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="55b06-118">Avrunding opp og faktorer</span><span class="sxs-lookup"><span data-stu-id="55b06-118">Rounding up and multiples</span></span>
<span data-ttu-id="55b06-119">Sammen gjør feltet **Avrundes opp** og **Faktorer** det mulig å runde opp materialforbruksverdien.</span><span class="sxs-lookup"><span data-stu-id="55b06-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="55b06-120">Du kan for eksempel runde opp verdien i henhold til håndteringsenheten der råvarene plukkes for produksjon.</span><span class="sxs-lookup"><span data-stu-id="55b06-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="55b06-121">Følgende alternativer er tilgjengelige i **Avrundes opp**-feltet: **Antall**, **Mål** og **Forbruk**.</span><span class="sxs-lookup"><span data-stu-id="55b06-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="55b06-122">Antall</span><span class="sxs-lookup"><span data-stu-id="55b06-122">Quantity</span></span>

<span data-ttu-id="55b06-123">Hvis du velger **Antall** som avrundingsmåte, må antallet være et multiplumstall av det angitte antallet.</span><span class="sxs-lookup"><span data-stu-id="55b06-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="55b06-124">For eksempel hvis du må bruke hele tall, angir du **1** i **Faktorer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="55b06-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="55b06-125">Tall rundes deretter opp til et antall som kan deles med 1.</span><span class="sxs-lookup"><span data-stu-id="55b06-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="55b06-126">Mål</span><span class="sxs-lookup"><span data-stu-id="55b06-126">Measurement</span></span>

<span data-ttu-id="55b06-127">Vanligvis merker du av for **Mål** som avrundingsmåte når råvarene har bestemte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="55b06-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="55b06-128">Et metallrør på 2 meter kreves for eksempel for en ferdigvare, og metallrørene kommer i 4,5 meters lengder.</span><span class="sxs-lookup"><span data-stu-id="55b06-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="55b06-129">I dette tilfellet kan avrundingsmåten **Mål** brukes til å beregne hvor mange metallrør som kreves for å produsere et gitt antall enheter av ferdigvaren.</span><span class="sxs-lookup"><span data-stu-id="55b06-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="55b06-130">I dette eksemplet er **Formel**-feltet satt til **Høyde \* Konstant**.</span><span class="sxs-lookup"><span data-stu-id="55b06-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="55b06-131">**Høyde**-feltet er satt til **2** for å angi lengden på røret som kreves for den ferdige varen.</span><span class="sxs-lookup"><span data-stu-id="55b06-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="55b06-132">**Flere**-feltet settes til **4,5** for å angi at røret plukkes i lengder på 4,5 meter.</span><span class="sxs-lookup"><span data-stu-id="55b06-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="55b06-133">Her er beregningen:</span><span class="sxs-lookup"><span data-stu-id="55b06-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="55b06-134">Antallet som kreves for 10 stykker av ferdigvaren: 10 ÷ 2 = 5 stykker</span><span class="sxs-lookup"><span data-stu-id="55b06-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="55b06-135">Totalt forbruk: 4,5 x 5 = 22,5 meter med metallrør</span><span class="sxs-lookup"><span data-stu-id="55b06-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="55b06-136">Det forutsettes av 0,5 meter rør kasseres for hvert rør som forbrukes.</span><span class="sxs-lookup"><span data-stu-id="55b06-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="55b06-137">Forbruk</span><span class="sxs-lookup"><span data-stu-id="55b06-137">Consumption</span></span>

<span data-ttu-id="55b06-138">Vanligvis merker du av for **Forbruk** som avrundingsmåte når råvarer må plukkes i hele antall av en bestemt håndteringsenhet av produktet.</span><span class="sxs-lookup"><span data-stu-id="55b06-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="55b06-139">2 liter maling brukes for eksempel til å produsere en stykk ferdigvare, og malingen plukkes i 25 liters spann.</span><span class="sxs-lookup"><span data-stu-id="55b06-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="55b06-140">I dette tilfellet kan avrundingsmåten **Forbruk** brukes til å avrunde forbruk til hele tall for 25 liters spann.</span><span class="sxs-lookup"><span data-stu-id="55b06-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="55b06-141">Her er beregningen av hvor mye maling som kreves hvis det skal produseres 180 stykker av ferdigvaren:</span><span class="sxs-lookup"><span data-stu-id="55b06-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="55b06-142">Maling som kreves, unntatt svinn: 180 x 2 = 360 liter</span><span class="sxs-lookup"><span data-stu-id="55b06-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="55b06-143">Antall spann: 360 ÷ 25 = 14,4, som rundes opp til 15</span><span class="sxs-lookup"><span data-stu-id="55b06-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="55b06-144">Maling som kreves, inkludert svinn: 15 x 25 = 375 liter</span><span class="sxs-lookup"><span data-stu-id="55b06-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="55b06-145">Trinnforbruk</span><span class="sxs-lookup"><span data-stu-id="55b06-145">Step consumption</span></span>
<span data-ttu-id="55b06-146">Trinnforbruk brukes til å beregne konstant forbruk i antallsintervaller.</span><span class="sxs-lookup"><span data-stu-id="55b06-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="55b06-147">Hvis du velger **Timeforbruk** i feltet **Formel** i kategorien **Oppsett**, kan du legge til informasjon om trinnene i kategorien **Timeforbruk**. Den faste forbrukte mengden kan settes opp i intervaller av den produserte mengden.</span><span class="sxs-lookup"><span data-stu-id="55b06-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="55b06-148">For eksempel er trinnforbruk definert som i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="55b06-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="55b06-149">Fra serie</span><span class="sxs-lookup"><span data-stu-id="55b06-149">From series</span></span> | <span data-ttu-id="55b06-150">Antall</span><span class="sxs-lookup"><span data-stu-id="55b06-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="55b06-151">0,00</span><span class="sxs-lookup"><span data-stu-id="55b06-151">0.00</span></span>        | <span data-ttu-id="55b06-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="55b06-152">10.0000</span></span>  |
| <span data-ttu-id="55b06-153">100,00</span><span class="sxs-lookup"><span data-stu-id="55b06-153">100.00</span></span>      | <span data-ttu-id="55b06-154">20,0000</span><span class="sxs-lookup"><span data-stu-id="55b06-154">20.0000</span></span>  |
| <span data-ttu-id="55b06-155">200,00</span><span class="sxs-lookup"><span data-stu-id="55b06-155">200.00</span></span>      | <span data-ttu-id="55b06-156">40,0000</span><span class="sxs-lookup"><span data-stu-id="55b06-156">40.0000</span></span>  |

<span data-ttu-id="55b06-157">Stykklisteantallet er 1, og produksjonsantallet er 110.</span><span class="sxs-lookup"><span data-stu-id="55b06-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="55b06-158">Formelen for forbruket er av Fra serie (Antall) = Forbruk.</span><span class="sxs-lookup"><span data-stu-id="55b06-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="55b06-159">Ettersom produksjonsantallet er 110, kommer det inn under "Fra 100-serien."</span><span class="sxs-lookup"><span data-stu-id="55b06-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="55b06-160">Derfor er antallet 20.</span><span class="sxs-lookup"><span data-stu-id="55b06-160">Therefore, the quantity is 20.</span></span>




