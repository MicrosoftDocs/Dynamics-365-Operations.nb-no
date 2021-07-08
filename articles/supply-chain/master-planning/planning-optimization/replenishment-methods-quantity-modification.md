---
title: Etterfyllingsmetoder og antallsendring
description: Dette emnet inneholder informasjon om etterfyllingsmetoder i planleggingsoptimalisering. Det forklarer også hvordan flere bestillingsantall for et produkt påvirker resultatet.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261702"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="b2dd9-104">Etterfyllingsmetoder og antallsendring</span><span class="sxs-lookup"><span data-stu-id="b2dd9-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2dd9-105">Dette emnet inneholder informasjon om etterfyllingsmetoder i planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="b2dd9-106">Det forklarer også hvordan flere bestillingsantall for et produkt påvirker resultatet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="b2dd9-107">Etterfyllingsmetoder kalles også dekningsmetoder og metoder for justering av partistørrelse.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="b2dd9-108">Dekningskoder</span><span class="sxs-lookup"><span data-stu-id="b2dd9-108">Coverage codes</span></span>

<span data-ttu-id="b2dd9-109">Planleggingsoptimalisering kan konfigureres til å bruke forskjellige metoder for etterfylling.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="b2dd9-110">Etterfyllingsmetodene er teknikker som systemet bruker til å beregne behov for et produkt.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="b2dd9-111">Etterfyllingsmetoder defineres av dekningskoder som du kan definere på enten dekningsgruppen eller produktet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="b2dd9-112">Følgende dekningskoder kan brukes i planleggingsoptimalisering:</span><span class="sxs-lookup"><span data-stu-id="b2dd9-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="b2dd9-113">**Periode** – Etterfyllingsmetoden kombinerer alt behovet for en periode i én ordre for produktet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="b2dd9-114">Ordren vil bli planlagt for den første dagen i perioden, og antallet vil oppfylle nettobehovet i den etablerte perioden.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="b2dd9-115">Perioden begynner med det første behovet for produktet og dekker den definerte tidslengden.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="b2dd9-116">Neste periode starter med de neste behovene til produktet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="b2dd9-117">*Periode*-dekningskoden brukes ofte for ikke-forutsigbare lagertrekk, sesongprodukter eller produkter med høy kostnad.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="b2dd9-118">Illustrasjonen nedenfor viser et eksempel.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="b2dd9-119">![Eksempel på bruk av Periode-dekningskode](./media/coverage-code-period.png "Eksempel på bruk av Periode-dekningskode")</span><span class="sxs-lookup"><span data-stu-id="b2dd9-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="b2dd9-120">**Behov** – I etterfyllingsmetoden oppretter systemet et bestillingsforslag, en overføring eller en produksjonsordre per behov for produktet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="b2dd9-121">Denne metoden brukes for kostbare produkter som har uregelmessig etterspørsel.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="b2dd9-122">Dekningskoden *Behov* brukes ofte for konfigurerbare produkter eller bestillingsscenarier.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="b2dd9-123">Illustrasjonen nedenfor viser et eksempel.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="b2dd9-124">![Eksempel på bruk av Behov-dekningskode](./media/coverage-code-requirement.png "Eksempel på bruk av Behov-dekningskode")</span><span class="sxs-lookup"><span data-stu-id="b2dd9-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="b2dd9-125">**Min/maks**</span><span class="sxs-lookup"><span data-stu-id="b2dd9-125">**Min./Max.**</span></span> <span data-ttu-id="b2dd9-126">– Etterfyllingsmetoden er basert på lagernivået.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="b2dd9-127">Den definerer etterfyllingen av lager opptil et bestemt nivå når det forutsagte lagerbeholdningsnivået er under en bestemt terskel.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="b2dd9-128">Etterfyllingsantallet vil være differansen mellom maksimumsnivået og det forhåndsberegnede nivået.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="b2dd9-129">Dekningskoden *Min/maks*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-129">The *Min./Max.*</span></span> <span data-ttu-id="b2dd9-130">brukes ofte til forutsigbare lagertrekk, mest solgte produkter eller billigste produkter.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="b2dd9-131">Illustrasjonen nedenfor viser et eksempel.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="b2dd9-132">![Eksempel på bruk av Min/maks-dekningskode](./media/coverage-code-min-max.png "Eksempel på bruk av Min/maks-dekningskode")</span><span class="sxs-lookup"><span data-stu-id="b2dd9-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="b2dd9-133">**Manuell** – I etterfyllingsmetoden foreslår ikke systemet kjøps-, overførings- eller produksjonsordrer for produktet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="b2dd9-134">I stedet er det planleggeren for produktet som er ansvarlig for å opprette de nødvendige ordrene for etterfylling av produktet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="b2dd9-135">Den *manuelle* dekningskoden brukes ofte for produkter som systemgenererte planlagte bestillinger ikke er ønsket for.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="b2dd9-136">Virkningen av ordreantallet fra standardordreinnstillinger</span><span class="sxs-lookup"><span data-stu-id="b2dd9-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="b2dd9-137">På siden **Standard ordreinnstillinger** for et frigitt produkt kan du angi følgende antallsinnstillinger i hurtigkategoriene **Bestilling**, **Lager** og **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="b2dd9-138">(Hurtigkategorien **Lager** brukes for både overføringsordrer og produksjonsordrer.)</span><span class="sxs-lookup"><span data-stu-id="b2dd9-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="b2dd9-139">**Flere** – Planlagte bestillinger vil være et multiplum av dette antallet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="b2dd9-140">Hvis for eksempel **Flere**-feltet er satt til *5*, kan en ordre være på antallet på 5, 10, 15, 20 og så videre.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="b2dd9-141">**Minimumsordre** – Planlagte bestillinger vil ikke være mindre enn den angitte verdien.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="b2dd9-142">Hvis for eksempel feltet **Minimumsordre** er satt til *10*, opprettes det en planlagt bestilling for et antall på 10, selv om bare fire kreves for å tilfredsstille behovet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="b2dd9-143">**Maks. ordreantall** – Planlagte bestillinger vil ikke overstige den angitte verdien.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="b2dd9-144">Hvis behovet er mer enn **Maks. ordreantall**-verdien, blir det opprettet flere planlagte bestillinger for å dekke det.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="b2dd9-145">Hvis for eksempel feltet **Maks. bestillingsantall** er satt til *100*, og behovet er 450, vil det bli opprettet fire planlagte bestillinger for et antall på 100 og en planlagt bestilling på et antall på 50.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="b2dd9-146">Eksempler på etterfylling som bruker Min/maks.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="b2dd9-147">dekningskode</span><span class="sxs-lookup"><span data-stu-id="b2dd9-147">coverage code</span></span>

<span data-ttu-id="b2dd9-148">Hvis du ikke angir en verdi i **Flere**-feltet for et produkt på siden **Standard ordreinnstillinger**, og hvis du bruker etterfyllingsmetoden *Min/maks.*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="b2dd9-149">vil planleggingsoptimalisering etterfylle lageret opptil et bestemt nivå når det forutsagte lagerbeholdningsnivået er under en bestemt terskel.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="b2dd9-150">Hvis du definerer et multiplumsantall for et produkt, endrer etterfyllingsmetoden *Min/maks.*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="b2dd9-151">virkemåten og vurderer **Flere**-verdien.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="b2dd9-152">Med andre ord vil planleggingsoptimaliseringen etterfylle lageret opptil det definerte maksimumsnivået når det forutsagte lagernivået er mindre enn det definerte minimumsnivået.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="b2dd9-153">Etterfyllingsantallet må imidlertid være et multiplumsantall av **Flere**-verdien.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="b2dd9-154">Hvis etterfyllingsantallet (differansen mellom det maksimale nivået og det forutsagte beholdningsnivået) ikke er et multiplumsantall av det definerte multiplumsantallet, bruker planleggingsoptimalisering den første mulige verdien som, sammen med forventet beholdningsnivå, vil være under maksimumsnivået.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="b2dd9-155">Hvis summen er mindre enn minimumsnivået, bruker planleggingsoptimalisering den første verdien som, sammen med forventet lagerbeholdning, vil være over maksimumsnivået.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="b2dd9-156">Følgende delseksjoner gir noen eksempler som viser hvordan multiplumsordreantallet for et produkt påvirker resultatet av *Min/maks.*-</span><span class="sxs-lookup"><span data-stu-id="b2dd9-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="b2dd9-157">etterfyllingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="b2dd9-158">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b2dd9-158">Example 1</span></span>

<span data-ttu-id="b2dd9-159">Et produkt har følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="b2dd9-159">A product has the following configuration:</span></span>

- <span data-ttu-id="b2dd9-160">**Dekningskode:** *Min/maks.*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="b2dd9-161">**Minimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="b2dd9-162">**Maksimum:** *22*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="b2dd9-163">**Flere:** *0*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-163">**Multiple:** *0*</span></span>

<span data-ttu-id="b2dd9-164">Det er 10 stykker av lagerbeholdningen for produktet, og det er ingen annen etterspørsel eller forsyning.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="b2dd9-165">Når hovedplanleggingen kjøres, opprettes det en planlagt bestilling på 12 stykker for å etterfylle lageret til maksimumsantallet.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="b2dd9-166">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b2dd9-166">Example 2</span></span>

<span data-ttu-id="b2dd9-167">Et produkt har følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="b2dd9-167">A product has the following configuration:</span></span>

- <span data-ttu-id="b2dd9-168">**Dekningskode:** *Min/maks.*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="b2dd9-169">**Minimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="b2dd9-170">**Maksimum:** *22*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="b2dd9-171">**Flere:** *5*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-171">**Multiple:** *5*</span></span>

<span data-ttu-id="b2dd9-172">Det er 10 stykker av lagerbeholdningen for produktet, og det er ingen annen etterspørsel eller forsyning.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="b2dd9-173">Når hovedplanleggingen kjøres, opprettes det en planlagt bestilling på 10 stykker (fordi 15 stykker etterfylling pluss 10 stykker av lagerbeholdningen vil overskride maksimumsantallet).</span><span class="sxs-lookup"><span data-stu-id="b2dd9-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="b2dd9-174">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="b2dd9-174">Example 3</span></span>

<span data-ttu-id="b2dd9-175">Et produkt har følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="b2dd9-175">A product has the following configuration:</span></span>

- <span data-ttu-id="b2dd9-176">**Dekningskode:** *Min/maks.*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="b2dd9-177">**Minimum:** *21*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="b2dd9-178">**Maksimum:** *24*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="b2dd9-179">**Flere:** *5*</span><span class="sxs-lookup"><span data-stu-id="b2dd9-179">**Multiple:** *5*</span></span>

<span data-ttu-id="b2dd9-180">Det er 10 stykker av lagerbeholdningen for produktet, og det er ingen annen etterspørsel eller forsyning.</span><span class="sxs-lookup"><span data-stu-id="b2dd9-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="b2dd9-181">Når hovedplanleggingen kjøres, opprettes den planlagte bestillingen på 15 stykker (fordi 10 stykker etterfylling pluss 10 stykker av lagerbeholdningen vil være mindre enn minimumsantallet).</span><span class="sxs-lookup"><span data-stu-id="b2dd9-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
