---
title: Fordele hodegebyrer til samsvarende salgslinjer
description: Dette emnet beskriver flere funksjoner for beregning og bruk av automatiske tillegg for handelskanalordrer ved å bruke funksjonen for avanserte automatiske gebyrer.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 048885cac7a316e144b2df072da405d74096203f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414518"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="35c0c-103">Fordele hodegebyrer til samsvarende salgslinjer</span><span class="sxs-lookup"><span data-stu-id="35c0c-103">Prorate header charges to matching sales lines</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="35c0c-104">Dette emnet beskriver funksjonen for å gruppere automatiske gebyrer på hodenivå og fordele dem proporsjonalt til handelslinjer.</span><span class="sxs-lookup"><span data-stu-id="35c0c-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to commerce sales lines.</span></span> <span data-ttu-id="35c0c-105">Denne funksjonen er tilgjengelig for transaksjoner som opprettes ved salgsstedet (POS) i Retail-versjon 10.0.1 og salg som er opprettet i et telefonsenter i Retail-versjon 10.0.2.</span><span class="sxs-lookup"><span data-stu-id="35c0c-105">This functionality is available for transactions that are created at the point of sale (POS) in Retail version 10.0.1 and sales that are created in a call center in Retail version 10.0.2.</span></span>

<span data-ttu-id="35c0c-106">Denne funksjonen er tilgjengelig bare hvis funksjonen [avanserte automatiske tillegg](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) er aktivert ved hjelp av alternativet på **Handelsparametere**-siden.</span><span class="sxs-lookup"><span data-stu-id="35c0c-106">This functionality is available only if the [advanced auto-charges](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Commerce parameters** page.</span></span> <span data-ttu-id="35c0c-107">I tillegg kan utvidet beregningsmetode for automatiske gebyrer bare brukes på salgsordrer som er opprettet ved hjelp av handelskanaler (salgsstedet, et telefonsenter og e-handelsplattformen til Dynamics).</span><span class="sxs-lookup"><span data-stu-id="35c0c-107">Additionally, the enhanced calculation method for auto-charges can be applied only to sales orders that are created through commerce channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="35c0c-108">Den nye funksjonaliteten gir organisasjoner større fleksibilitet i måten automatiske gebyrer på hodenivå beregnes og brukes på salgstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="35c0c-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to sales transactions.</span></span>

<span data-ttu-id="35c0c-109">I versjoner av appen som er eldre enn versjon 10.0.1, beregnes automatiske gebyrer på hodenivå som har en bestemt leveringsmåte bare når det er samsvar med leveringsmåten som er definert i salgsordrehodet.</span><span class="sxs-lookup"><span data-stu-id="35c0c-109">In versions of the app earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="35c0c-110">For eksempel er automatiske gebyrer på hodenivå definert for leveringsmåten **99** og leveringsmåten **11**.</span><span class="sxs-lookup"><span data-stu-id="35c0c-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="35c0c-111">Det opprettes en salgsordre, og leveringsmåten **99** er definert i ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="35c0c-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="35c0c-112">Men noen av linjene for salg er satt opp slik at de er sendt ved hjelp av leveringsmåten **11**.</span><span class="sxs-lookup"><span data-stu-id="35c0c-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="35c0c-113">I dette tilfellet er det bare gebyrer på hodenivå som er knyttet til leveringsmåten **99**, som blir tatt hensyn til og brukt på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="35c0c-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="35c0c-114">I Commerce har gebyrer på hodenivå en tilleggsfunksjon som lar deg definere en [konfigurasjon av fordelt tillegg](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) som er basert på ordreverdien.</span><span class="sxs-lookup"><span data-stu-id="35c0c-114">In Commerce, the header-level charges have an additional feature that lets you define a [tiered charge configuration](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="35c0c-115">Hvis orderverdien er mellom USD 50,00 og USD 200,00, kan en organisasjon for eksempel belaste et fraktgebyr på USD 5,00.</span><span class="sxs-lookup"><span data-stu-id="35c0c-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="35c0c-116">Hvis orderverdien er mellom USD 200,01 og USD 500,00, kan imidlertid fraktkostnadene være USD 4,00.</span><span class="sxs-lookup"><span data-stu-id="35c0c-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="35c0c-117">Noen organisasjoner ønsker fordelene med beregningen av fordelte tillegg som følger med gebyrer på hodenivå.</span><span class="sxs-lookup"><span data-stu-id="35c0c-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="35c0c-118">I scenarioer med blandede leveringsmåter vil de også være sikre på at tilleggene som er beregnet, er basert på treff med leveringsmåten som er definert på hver salgslinje.</span><span class="sxs-lookup"><span data-stu-id="35c0c-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="35c0c-119">Du kan nå konfigurere automatiske gebyrer på hodenivå, slik at alle leveringsmåter på bestillingen medregnes når tillegg beregnes.</span><span class="sxs-lookup"><span data-stu-id="35c0c-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="35c0c-120">Denne funksjonen krever en mer sammensatt beregningslogikk for å beregne gebyrer på hodenivå.</span><span class="sxs-lookup"><span data-stu-id="35c0c-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="35c0c-121">Logikken grupperer alle varer som leveres ved hjelp av samme beregningsmodus for levering, og den behandler den gruppen som beregningsgruppen for varene ved beregning av automatiske gebyrer på hodenivå.</span><span class="sxs-lookup"><span data-stu-id="35c0c-121">The logic groups together all the items that are shipped using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="35c0c-122">For varer som har samme leveringsmåte, er automatiske gebyrer beregnet basert på den totale salgsverdien for varene.</span><span class="sxs-lookup"><span data-stu-id="35c0c-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="35c0c-123">På denne måten bestemmes riktig automatisk tillegg.</span><span class="sxs-lookup"><span data-stu-id="35c0c-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="35c0c-124">Etter at riktige gebyrer på hodenivå hentes fra salgslinjene som sendes ved hjelp av samme leveringsmåte, blir de beregnede kostnadene fordelt ned til salgslinjenivå.</span><span class="sxs-lookup"><span data-stu-id="35c0c-124">After the appropriate header-level charges are obtained for the sales lines that are shipped using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="35c0c-125">Fordi disse gebyrene er på linjenivå og ikke holdes på overskriftsnivå, lages en mer spesifikk kobling mellom varen og tilleggsverdien som ble beregnet for den.</span><span class="sxs-lookup"><span data-stu-id="35c0c-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="35c0c-126">Dette kan være nyttig i delvise returscenarier der en organisasjon vil refundere bare en del av tillegget i stedet for hele tillegget når bare noen varer returneres.</span><span class="sxs-lookup"><span data-stu-id="35c0c-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="35c0c-127">Scenarier</span><span class="sxs-lookup"><span data-stu-id="35c0c-127">Scenarios</span></span>

<span data-ttu-id="35c0c-128">Følgende to eksempelscenarier viser hvordan disse gebyrene er beregnet både når den nye funksjonaliteten brukes, og når den brukes ikke.</span><span class="sxs-lookup"><span data-stu-id="35c0c-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="35c0c-129">Scenario 1</span><span class="sxs-lookup"><span data-stu-id="35c0c-129">Scenario 1</span></span>

<span data-ttu-id="35c0c-130">Dette scenariet beskriver virkemåten når alternativet **Fordel til samsvarende salgslinjer** er **Nei** i det automatiske oppsettet.</span><span class="sxs-lookup"><span data-stu-id="35c0c-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="35c0c-131">(Virkemåten er lik virkemåten til gebyrer på hodenivå i appversjoner som er eldre enn versjon 10.0.1).</span><span class="sxs-lookup"><span data-stu-id="35c0c-131">(The behavior is equivalent to the behavior of header-level charges in app versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="35c0c-132">I dette scenarioet har organisasjonen definert gebyrer på hodenivå for relasjon for leveringsmåte **99** og relasjon for leveringsmåte **11**.</span><span class="sxs-lookup"><span data-stu-id="35c0c-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="35c0c-133">Ingen automatiske tillegg som er konfigurert for leveringsmåte **21**.</span><span class="sxs-lookup"><span data-stu-id="35c0c-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![Automatiske tillegg for leveringsmåte 99 når linjesamsvarsfordeling er slått av](media/99_disabled.png)

![Automatiske tillegg for leveringsmåte 11 når linjesamsvarsfordeling er slått av](media/11_disabled.png)

<span data-ttu-id="35c0c-136">Det opprettes en salgsordre i telefonsenteret, og leveringsmåten settes til **99**.</span><span class="sxs-lookup"><span data-stu-id="35c0c-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="35c0c-137">Denne rekkefølgen inneholder fem elementer.</span><span class="sxs-lookup"><span data-stu-id="35c0c-137">This order contains five items.</span></span> <span data-ttu-id="35c0c-138">To ordrelinjer er konfigurert for å bruke leveringsmåten **99**, to linjer er konfigurert til å bruke leveringsmåten **11**, og én linje er konfigurert for å bruke leveringsmåten **21**, som vist i eksempelet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="35c0c-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="35c0c-139">Artikkel</span><span class="sxs-lookup"><span data-stu-id="35c0c-139">Item</span></span>  | <span data-ttu-id="35c0c-140">Linjeantall</span><span class="sxs-lookup"><span data-stu-id="35c0c-140">Line quantity</span></span> | <span data-ttu-id="35c0c-141">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="35c0c-141">Delivery mode</span></span> | <span data-ttu-id="35c0c-142">Pris per enhet</span><span class="sxs-lookup"><span data-stu-id="35c0c-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="35c0c-143">81331</span><span class="sxs-lookup"><span data-stu-id="35c0c-143">81331</span></span> | <span data-ttu-id="35c0c-144">1</span><span class="sxs-lookup"><span data-stu-id="35c0c-144">1</span></span>             | <span data-ttu-id="35c0c-145">11</span><span class="sxs-lookup"><span data-stu-id="35c0c-145">11</span></span>            | <span data-ttu-id="35c0c-146">USD 10</span><span class="sxs-lookup"><span data-stu-id="35c0c-146">$10</span></span>            |
| <span data-ttu-id="35c0c-147">81332</span><span class="sxs-lookup"><span data-stu-id="35c0c-147">81332</span></span> | <span data-ttu-id="35c0c-148">1</span><span class="sxs-lookup"><span data-stu-id="35c0c-148">1</span></span>             | <span data-ttu-id="35c0c-149">99</span><span class="sxs-lookup"><span data-stu-id="35c0c-149">99</span></span>            | <span data-ttu-id="35c0c-150">USD 50</span><span class="sxs-lookup"><span data-stu-id="35c0c-150">$50</span></span>            |
| <span data-ttu-id="35c0c-151">81333</span><span class="sxs-lookup"><span data-stu-id="35c0c-151">81333</span></span> | <span data-ttu-id="35c0c-152">2</span><span class="sxs-lookup"><span data-stu-id="35c0c-152">2</span></span>             | <span data-ttu-id="35c0c-153">11</span><span class="sxs-lookup"><span data-stu-id="35c0c-153">11</span></span>            | <span data-ttu-id="35c0c-154">USD 30</span><span class="sxs-lookup"><span data-stu-id="35c0c-154">$30</span></span>            |
| <span data-ttu-id="35c0c-155">81334</span><span class="sxs-lookup"><span data-stu-id="35c0c-155">81334</span></span> | <span data-ttu-id="35c0c-156">3</span><span class="sxs-lookup"><span data-stu-id="35c0c-156">3</span></span>             | <span data-ttu-id="35c0c-157">99</span><span class="sxs-lookup"><span data-stu-id="35c0c-157">99</span></span>            | <span data-ttu-id="35c0c-158">USD 10</span><span class="sxs-lookup"><span data-stu-id="35c0c-158">$10</span></span>            |
| <span data-ttu-id="35c0c-159">81334</span><span class="sxs-lookup"><span data-stu-id="35c0c-159">81334</span></span> | <span data-ttu-id="35c0c-160">3</span><span class="sxs-lookup"><span data-stu-id="35c0c-160">3</span></span>             | <span data-ttu-id="35c0c-161">21</span><span class="sxs-lookup"><span data-stu-id="35c0c-161">21</span></span>            | <span data-ttu-id="35c0c-162">USD 5</span><span class="sxs-lookup"><span data-stu-id="35c0c-162">$5</span></span>             |

<span data-ttu-id="35c0c-163">I dette scenarioet evalueres hele ordren mot tabellen for automatisk tillegg for leveringsmåten **99**.</span><span class="sxs-lookup"><span data-stu-id="35c0c-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="35c0c-164">Hele totalen for alle salgslinjer brukes til å finne et samsvarende nivå i konfigurasjonen for automatisk tillegg, og dette tillegget brukes på ordrehodenivå.</span><span class="sxs-lookup"><span data-stu-id="35c0c-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="35c0c-165">I dette eksemplet er ordretotalen USD 165,00, og frakttillegget på USD 15,00 brukes på ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="35c0c-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="35c0c-166">Automatiske tillegg som er konfigurert for leveringsmåten **11**, er aldri referert til eller brukt.</span><span class="sxs-lookup"><span data-stu-id="35c0c-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="35c0c-167">I dette scenarioet, hvis en kunde returnerer noen av varene i ordren, og hvis [tilleggskoden er konfigurert slik at den blir refundert](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), blir totalt hodenivåtillegg systematisk brukt til refunderingen, selv om bare noen av varene returneres.</span><span class="sxs-lookup"><span data-stu-id="35c0c-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="35c0c-168">Scenario 2</span><span class="sxs-lookup"><span data-stu-id="35c0c-168">Scenario 2</span></span>

<span data-ttu-id="35c0c-169">I dette scenarioet defineres gebyrer på hodenivå for relasjon for leveringsmåte **99** og relasjon for leveringsmåte **11**.</span><span class="sxs-lookup"><span data-stu-id="35c0c-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="35c0c-170">Men alternativet **Fordel til samsvarende salgslinjer** settes til **Ja** for disse tabellene for automatisk tillegg.</span><span class="sxs-lookup"><span data-stu-id="35c0c-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![Automatiske tillegg for leveringsmåte 99 når linjesamsvarsfordeling er slått på](media/99_enabled.png)

![Automatiske tillegg for leveringsmåte 11 når linjesamsvarsfordeling er slått på](media/11_enabled.png)

<span data-ttu-id="35c0c-173">Dette scenarioet bruker den samme salgsordren som har fem linjer.</span><span class="sxs-lookup"><span data-stu-id="35c0c-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="35c0c-174">Leveringsmåte på ordrehodet er satt til **99**, men leveringsmåten for hver vare i salgsordren konfigureres som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="35c0c-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="35c0c-175">Artikkel</span><span class="sxs-lookup"><span data-stu-id="35c0c-175">Item</span></span>  | <span data-ttu-id="35c0c-176">Linjeantall</span><span class="sxs-lookup"><span data-stu-id="35c0c-176">Line quantity</span></span> | <span data-ttu-id="35c0c-177">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="35c0c-177">Delivery mode</span></span> | <span data-ttu-id="35c0c-178">Pris per enhet</span><span class="sxs-lookup"><span data-stu-id="35c0c-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="35c0c-179">81331</span><span class="sxs-lookup"><span data-stu-id="35c0c-179">81331</span></span> | <span data-ttu-id="35c0c-180">1</span><span class="sxs-lookup"><span data-stu-id="35c0c-180">1</span></span>             | <span data-ttu-id="35c0c-181">11</span><span class="sxs-lookup"><span data-stu-id="35c0c-181">11</span></span>            | <span data-ttu-id="35c0c-182">USD 10</span><span class="sxs-lookup"><span data-stu-id="35c0c-182">$10</span></span>            |
| <span data-ttu-id="35c0c-183">81332</span><span class="sxs-lookup"><span data-stu-id="35c0c-183">81332</span></span> | <span data-ttu-id="35c0c-184">1</span><span class="sxs-lookup"><span data-stu-id="35c0c-184">1</span></span>             | <span data-ttu-id="35c0c-185">99</span><span class="sxs-lookup"><span data-stu-id="35c0c-185">99</span></span>            | <span data-ttu-id="35c0c-186">USD 50</span><span class="sxs-lookup"><span data-stu-id="35c0c-186">$50</span></span>            |
| <span data-ttu-id="35c0c-187">81333</span><span class="sxs-lookup"><span data-stu-id="35c0c-187">81333</span></span> | <span data-ttu-id="35c0c-188">2</span><span class="sxs-lookup"><span data-stu-id="35c0c-188">2</span></span>             | <span data-ttu-id="35c0c-189">11</span><span class="sxs-lookup"><span data-stu-id="35c0c-189">11</span></span>            | <span data-ttu-id="35c0c-190">USD 30</span><span class="sxs-lookup"><span data-stu-id="35c0c-190">$30</span></span>            |
| <span data-ttu-id="35c0c-191">81334</span><span class="sxs-lookup"><span data-stu-id="35c0c-191">81334</span></span> | <span data-ttu-id="35c0c-192">3</span><span class="sxs-lookup"><span data-stu-id="35c0c-192">3</span></span>             | <span data-ttu-id="35c0c-193">99</span><span class="sxs-lookup"><span data-stu-id="35c0c-193">99</span></span>            | <span data-ttu-id="35c0c-194">USD 10</span><span class="sxs-lookup"><span data-stu-id="35c0c-194">$10</span></span>            |
| <span data-ttu-id="35c0c-195">81334</span><span class="sxs-lookup"><span data-stu-id="35c0c-195">81334</span></span> | <span data-ttu-id="35c0c-196">3</span><span class="sxs-lookup"><span data-stu-id="35c0c-196">3</span></span>             | <span data-ttu-id="35c0c-197">21</span><span class="sxs-lookup"><span data-stu-id="35c0c-197">21</span></span>            | <span data-ttu-id="35c0c-198">USD 5</span><span class="sxs-lookup"><span data-stu-id="35c0c-198">$5</span></span>             |

<span data-ttu-id="35c0c-199">Fordi automatisk tillegg-konfigurasjonen er satt til å fordele til samsvarende salgslinjer, utfører systemet følgende beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="35c0c-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="35c0c-200">Alle varer som har samme leveringsmåte, grupperes sammen, og systemet beregner den totale produktverdien av varene i gruppen.</span><span class="sxs-lookup"><span data-stu-id="35c0c-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="35c0c-201">**Leveringsmodus 11**</span><span class="sxs-lookup"><span data-stu-id="35c0c-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="35c0c-202">Vare 81331, antall 1 = USD 10</span><span class="sxs-lookup"><span data-stu-id="35c0c-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="35c0c-203">Vare 81333, antall 2 = USD 60 netto (USD 30 per enhet)</span><span class="sxs-lookup"><span data-stu-id="35c0c-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="35c0c-204">**Total verdi av produktet for leveringsmåten 11 = USD 70**</span><span class="sxs-lookup"><span data-stu-id="35c0c-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="35c0c-205">**Leveringsmodus 99**</span><span class="sxs-lookup"><span data-stu-id="35c0c-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="35c0c-206">Vare 81332, antall 1 = USD 50</span><span class="sxs-lookup"><span data-stu-id="35c0c-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="35c0c-207">Vare 81334, antall 3 = USD 30 netto</span><span class="sxs-lookup"><span data-stu-id="35c0c-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="35c0c-208">**Total verdi av produktet for leveringsmåten 99 = USD 80**</span><span class="sxs-lookup"><span data-stu-id="35c0c-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="35c0c-209">**Leveringsmodus 21**</span><span class="sxs-lookup"><span data-stu-id="35c0c-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="35c0c-210">Vare 81334, antall 3 = USD 15 netto</span><span class="sxs-lookup"><span data-stu-id="35c0c-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="35c0c-211">**Total verdi av produktet for leveringsmåten 21 = USD 15**</span><span class="sxs-lookup"><span data-stu-id="35c0c-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="35c0c-212">Systemet søker etter konfigurasjonen for automatiske gebyrer på hodenivå som samsvarer med kunde- og leveringsmåteinnstillingene for hver varegruppe.</span><span class="sxs-lookup"><span data-stu-id="35c0c-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="35c0c-213">Hvis konfigurasjonen blir funnet, leter systemet i den fordelte konfigurasjonen for å finne tillegget som skal brukes, basert på total produktverdi av varer i leveringsmåtegruppen.</span><span class="sxs-lookup"><span data-stu-id="35c0c-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="35c0c-214">**Leveringsmodus 11**</span><span class="sxs-lookup"><span data-stu-id="35c0c-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="35c0c-215">Total produktverdi = USD 70</span><span class="sxs-lookup"><span data-stu-id="35c0c-215">Total product value = $70</span></span>
    - <span data-ttu-id="35c0c-216">**Gebyrverdi = USD 7**</span><span class="sxs-lookup"><span data-stu-id="35c0c-216">**Charge value = $7**</span></span>

    <span data-ttu-id="35c0c-217">**Leveringsmodus 99**</span><span class="sxs-lookup"><span data-stu-id="35c0c-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="35c0c-218">Total produktverdi = USD 80</span><span class="sxs-lookup"><span data-stu-id="35c0c-218">Total product value = $80</span></span>
    - <span data-ttu-id="35c0c-219">**Gebyrverdi = USD 15**</span><span class="sxs-lookup"><span data-stu-id="35c0c-219">**Charge value = $15**</span></span>

    <span data-ttu-id="35c0c-220">**Leveringsmodus 21**</span><span class="sxs-lookup"><span data-stu-id="35c0c-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="35c0c-221">Total produktverdi = USD 15</span><span class="sxs-lookup"><span data-stu-id="35c0c-221">Total product value = $15</span></span>
    - <span data-ttu-id="35c0c-222">**Gebyrverdi = USD 0** (ingen automatiske gebyrer er konfigurert for denne kombinasjonen av kunde og leveringsmåte.)</span><span class="sxs-lookup"><span data-stu-id="35c0c-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![Leveringsmodus 11-gebyrer faller innenfor det merkede laget](media/step2mode11.png)

    ![Leveringsmodus 99-gebyrer faller innenfor det merkede laget](media/step2mode99.png)

3. <span data-ttu-id="35c0c-225">Systemet beregner gebyrverdien som skal brukes på hver linje, basert på fordelingslogikk som vurderer den proporsjonale verdien av linjen i forhold til gruppens totale produktverdi.</span><span class="sxs-lookup"><span data-stu-id="35c0c-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="35c0c-226">**Leveringsmodus 11**</span><span class="sxs-lookup"><span data-stu-id="35c0c-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="35c0c-227">Gebyrverdi = USD 7</span><span class="sxs-lookup"><span data-stu-id="35c0c-227">Charge value = $7</span></span>
    - <span data-ttu-id="35c0c-228">Gruppeproduktverdi = USD 70</span><span class="sxs-lookup"><span data-stu-id="35c0c-228">Group product value = $70</span></span>
    - <span data-ttu-id="35c0c-229">Linje 1-verdi = USD 10 (= 14,2857 % av gruppeverdien)</span><span class="sxs-lookup"><span data-stu-id="35c0c-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="35c0c-230">Linje 3-verdi = USD 60 (= 85,7143 % av gruppeverdien)</span><span class="sxs-lookup"><span data-stu-id="35c0c-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="35c0c-231">**Linjetillegg for linje 1 = USD 1**</span><span class="sxs-lookup"><span data-stu-id="35c0c-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="35c0c-232">**Linjetillegg for linje 3 = USD 6**</span><span class="sxs-lookup"><span data-stu-id="35c0c-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="35c0c-233">**Leveringsmodus 99**</span><span class="sxs-lookup"><span data-stu-id="35c0c-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="35c0c-234">Gebyrverdi = USD 15</span><span class="sxs-lookup"><span data-stu-id="35c0c-234">Charge value = $15</span></span>
    - <span data-ttu-id="35c0c-235">Gruppeproduktverdi = USD 80</span><span class="sxs-lookup"><span data-stu-id="35c0c-235">Group product value = $80</span></span>
    - <span data-ttu-id="35c0c-236">Linje 2-verdi = USD 50 (= 62,5 % av gruppeverdien)</span><span class="sxs-lookup"><span data-stu-id="35c0c-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="35c0c-237">Linje 4-verdi = USD 30 (= 37,5 % av gruppeverdien)</span><span class="sxs-lookup"><span data-stu-id="35c0c-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="35c0c-238">**Linjetillegg for linje 2 = USD 9,38**</span><span class="sxs-lookup"><span data-stu-id="35c0c-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="35c0c-239">**Linjetillegg for linje 4 = USD 5,62**</span><span class="sxs-lookup"><span data-stu-id="35c0c-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="35c0c-240">**Leveringsmodus 21**</span><span class="sxs-lookup"><span data-stu-id="35c0c-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="35c0c-241">Gebyrverdi = USD 0</span><span class="sxs-lookup"><span data-stu-id="35c0c-241">Charge value = $0</span></span>
    - <span data-ttu-id="35c0c-242">Gruppeproduktverdi = USD 15</span><span class="sxs-lookup"><span data-stu-id="35c0c-242">Group product value = $15</span></span>
    - <span data-ttu-id="35c0c-243">Linje 5-verdi = USD 15 (= 100 % av gruppeverdien)</span><span class="sxs-lookup"><span data-stu-id="35c0c-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="35c0c-244">**Linjetillegg for linje 5 = USD 0**</span><span class="sxs-lookup"><span data-stu-id="35c0c-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="35c0c-245">Derfor, i dette eksempelet, tilordnes varen 81334 et fraktgebyr på USD 5,62.</span><span class="sxs-lookup"><span data-stu-id="35c0c-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="35c0c-246">Du kan vise disse gebyrene på siden **Vedlikehold tillegg** for salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="35c0c-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="35c0c-247">Illustrasjonen nedenfor viser hvordan denne siden ser ut for varen 81334.</span><span class="sxs-lookup"><span data-stu-id="35c0c-247">The following illustration shows what this page looks like for item 81334.</span></span>

![Fordelte tillegg på salgslinje for varen 81334](media/proratedlinecharge.png)

<span data-ttu-id="35c0c-249">Når denne beregningsmåten brukes i en delvis retur-scenario, hvis tilleggskoden er refunderbar, vil bare delen av tillegget som er tilordnet til denne linjen, refunderes når varen returneres.</span><span class="sxs-lookup"><span data-stu-id="35c0c-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35c0c-250">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="35c0c-250">Additional resources</span></span>

[<span data-ttu-id="35c0c-251">Avanserte automatiske tillegg for omnikanal</span><span class="sxs-lookup"><span data-stu-id="35c0c-251">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="35c0c-252">Aktivere og konfigurere automatiske avregninger etter kanal</span><span class="sxs-lookup"><span data-stu-id="35c0c-252">Enable and configure auto charges by channel</span></span>](auto-charges-by-channel.md)
