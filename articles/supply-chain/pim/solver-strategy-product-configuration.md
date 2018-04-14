---
title: "Problemløserstrategi for produktkonfigurasjon"
description: "Dette emnet beskriver hvordan du kan bruke problemløserstrategien til å forbedre ytelsen til produktkonfigurasjon."
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 468e2c5ce2915bf346ade20159e24fb98fcd4336
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="65e1c-103">Problemløserstrategi for produktkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="65e1c-103">Solver strategy for product configuration</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="65e1c-104">Dette emnet beskriver hvordan du kan bruke problemløserstrategien til å forbedre ytelsen til produktkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="65e1c-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="65e1c-105">Konseptet med problemløserstrategier ble først innført i Kumulativ oppdatering 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="65e1c-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="65e1c-106">Det ble utvidet i Kumulativ oppdatering 8 (CU8) for Microsoft Dynamics AX 2012 R3 og Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span><span class="sxs-lookup"><span data-stu-id="65e1c-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="65e1c-107">Problemløserstrategikonseptet består nå av følgende strategier:</span><span class="sxs-lookup"><span data-stu-id="65e1c-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="65e1c-108">Standard</span><span class="sxs-lookup"><span data-stu-id="65e1c-108">Default</span></span>
- <span data-ttu-id="65e1c-109">Små domener først</span><span class="sxs-lookup"><span data-stu-id="65e1c-109">Minimal domains first</span></span>
- <span data-ttu-id="65e1c-110">Ovenfra og nedover</span><span class="sxs-lookup"><span data-stu-id="65e1c-110">Top-down</span></span>
- <span data-ttu-id="65e1c-111">Z3</span><span class="sxs-lookup"><span data-stu-id="65e1c-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="65e1c-112">Problemløserstrategi</span><span class="sxs-lookup"><span data-stu-id="65e1c-112">Solver strategy</span></span> 

<span data-ttu-id="65e1c-113">En produktkonfigurasjonsmodell kan formuleres som et [begrensningsbasert problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span><span class="sxs-lookup"><span data-stu-id="65e1c-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="65e1c-114">Microsoft Solver Foundation (MSF) inneholder to typer problemløserstrategier for å løse CSP-er som kan brukes fra produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="65e1c-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="65e1c-115">Disse problemløserstrategiene er avhengige av [heuristikk](https://techterms.com/definition/heuristic), som brukes til å bestemme rekkefølgen som variablene i CSP-er blir vurdert når problemet løses.</span><span class="sxs-lookup"><span data-stu-id="65e1c-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="65e1c-116">Heuristikk kan ha stor innvirkning på ytelsen når et problem eller en klasse med problemer løses.</span><span class="sxs-lookup"><span data-stu-id="65e1c-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="65e1c-117">I Finance and Operations bestemmer problemløserstrategien for produktkonfigurasjonsmodeller hvilken problemløser som brukes med heuristikk.</span><span class="sxs-lookup"><span data-stu-id="65e1c-117">In Finance and Operations, the solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="65e1c-118">Strategien **Standard**, **Små domener først** og **Ovenfra og nedover** bruker de to problemløserne fra MSF, mens **Z3**-strategien bruker Z3-problemløseren.</span><span class="sxs-lookup"><span data-stu-id="65e1c-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="65e1c-119">Studier av kundeimplementering har vist at en endring i problemløserstrategien for en produktkonfigurasjonsmodell kan redusere svartiden fra minutter til millisekunder.</span><span class="sxs-lookup"><span data-stu-id="65e1c-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="65e1c-120">Derfor er det verdt å prøve forskjellige problemløserstrategier for å finne den mest effektive strategien for produktkonfigurasjonsmodellen din.</span><span class="sxs-lookup"><span data-stu-id="65e1c-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="65e1c-121">Endre innstillingene for problemløserstrategien</span><span class="sxs-lookup"><span data-stu-id="65e1c-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="65e1c-122">Du kan endre problemløserstrategien på siden **Produktkonfigurasjonsmodeller** i handlingsruten ved å velge **Modellegenskaper**.</span><span class="sxs-lookup"><span data-stu-id="65e1c-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="65e1c-123">Deretter i **Rediger modelldetaljene**-dialogboksen velger du en problemløserstrategi.</span><span class="sxs-lookup"><span data-stu-id="65e1c-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="65e1c-124">[![Endre problemløserstrategien](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="65e1c-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="65e1c-125">Det er for øyeblikket ingen logikk som automatisk oppdager hvilken problemløserstrategi som vil være den mest effektive strategien for restriksjonsbasert produktkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="65e1c-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="65e1c-126">Du må derfor prøve ut en og en problemløserstrategi.</span><span class="sxs-lookup"><span data-stu-id="65e1c-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="65e1c-127">Følgende tabell inneholder anbefalinger om problemløserstrategien som skal brukes i ulike scenarier.</span><span class="sxs-lookup"><span data-stu-id="65e1c-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="65e1c-128">Problemløserstrategi</span><span class="sxs-lookup"><span data-stu-id="65e1c-128">Solver strategy</span></span>      | <span data-ttu-id="65e1c-129">Bruk strategien i dette scenariet</span><span class="sxs-lookup"><span data-stu-id="65e1c-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="65e1c-130">Standard</span><span class="sxs-lookup"><span data-stu-id="65e1c-130">Default</span></span>              | <span data-ttu-id="65e1c-131">**Standard**-strategien er optimalisert til å løse modeller som bruker tabellbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="65e1c-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="65e1c-132">Kundeimplementeringsstudier har vist at denne strategien er den mest effektive strategien i scenarier der tabellbegrensninger brukes mye.</span><span class="sxs-lookup"><span data-stu-id="65e1c-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="65e1c-133">Små domener først</span><span class="sxs-lookup"><span data-stu-id="65e1c-133">Minimal domain first</span></span> | <span data-ttu-id="65e1c-134">**Små domener først**- og **Ovenfra og nedover**-strategien henger nøye sammen.</span><span class="sxs-lookup"><span data-stu-id="65e1c-134">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="65e1c-135">Kundeimplementeringsstudier har vist at **Ovenfra og nedover**-strategien, som ble introdusert i CU8, overgår **Små domener først**-strategien.</span><span class="sxs-lookup"><span data-stu-id="65e1c-135">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="65e1c-136">Men **Små domener først**-strategien bevares i produktet for bakoverkompatibilitet.</span><span class="sxs-lookup"><span data-stu-id="65e1c-136">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="65e1c-137">Begge disse problemløserstrategiene har vist seg å være mer effektive på å løse modeller som inneholder flere aritmetiske uttrykk der det ikke brukes tabellbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="65e1c-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="65e1c-138">I noen tilfeller kan imidlertid **Standard**-strategien overgå disse to strategiene.</span><span class="sxs-lookup"><span data-stu-id="65e1c-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="65e1c-139">Derfor må du huske å forsøke hver strategi.</span><span class="sxs-lookup"><span data-stu-id="65e1c-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="65e1c-140">Ovenfra og nedover</span><span class="sxs-lookup"><span data-stu-id="65e1c-140">Top-down</span></span>             | <span data-ttu-id="65e1c-141">**Små domener først**- og **Ovenfra og nedover**-strategien henger nøye sammen.</span><span class="sxs-lookup"><span data-stu-id="65e1c-141">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="65e1c-142">Kundeimplementeringsstudier har vist at **Ovenfra og nedover**-strategien, som ble introdusert i CU8, overgår **Små domener først**-strategien.</span><span class="sxs-lookup"><span data-stu-id="65e1c-142">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="65e1c-143">Men **Små domener først**-strategien bevares i produktet for bakoverkompatibilitet.</span><span class="sxs-lookup"><span data-stu-id="65e1c-143">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="65e1c-144">Begge disse problemløserstrategiene har vist seg å være mer effektive på å løse modeller som inneholder flere aritmetiske uttrykk der det ikke brukes tabellbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="65e1c-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="65e1c-145">I noen tilfeller kan imidlertid **Standard**-strategien overgå disse to strategiene.</span><span class="sxs-lookup"><span data-stu-id="65e1c-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="65e1c-146">Derfor må du huske å forsøke hver strategi.</span><span class="sxs-lookup"><span data-stu-id="65e1c-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="65e1c-147">Z3</span><span class="sxs-lookup"><span data-stu-id="65e1c-147">Z3</span></span>                   | <span data-ttu-id="65e1c-148">Vi anbefaler at du bruker **Z3**-strategien som standard problemløserstrategi.</span><span class="sxs-lookup"><span data-stu-id="65e1c-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="65e1c-149">Hvis du er bekymret for ytelse og skalerbarhet, kan du evaluere de andre strategiene.</span><span class="sxs-lookup"><span data-stu-id="65e1c-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="65e1c-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="65e1c-150">Additional resources</span></span>

[<span data-ttu-id="65e1c-151">Bygge produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="65e1c-151">Build product configuration model</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="65e1c-152">Heuristikk</span><span class="sxs-lookup"><span data-stu-id="65e1c-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="65e1c-153">Begrensningsbasert problem</span><span class="sxs-lookup"><span data-stu-id="65e1c-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)

