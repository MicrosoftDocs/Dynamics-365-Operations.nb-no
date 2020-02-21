---
title: Kostnadskonfigurasjon for behandling av distribuert ordre (DOM)
description: Dette emnet beskriver kostnadskonfigurasjon for DOM-funksjonaliteten i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004234"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="a3cd0-103">Kostnadskonfigurasjon for behandling av distribuert ordre (DOM)</span><span class="sxs-lookup"><span data-stu-id="a3cd0-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3cd0-104">Organisasjoner vurderer flere kostnadskomponenter for å fastslå hvilken lokasjon som er best å oppfylle ordrer fra.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="a3cd0-105">Noen av disse kostnadskomponentene er knyttet til frakt, håndtering og emballasje.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="a3cd0-106">En kombinasjon av disse kostnadene beregnes for å bestemme oppfyllingslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="a3cd0-107">Da den første gjentakelsen av behandling av distribuert ordre (DOM) i Dynamics 365 Commerce optimaliserte tilordningen av ordrer til oppfyllingslokasjoner, ble det bare tatt hensyn til avstand.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="a3cd0-108">Selv om avstand kan korreleres med kostnad, er det ikke det samme som kostnad.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="a3cd0-109">En leveranse til neste dag koster for eksempel mer enn tredagers leveranse eller sjudagers leveranse med samme avstand.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="a3cd0-110">Med funksjonen for kostnadskonfigurasjon kan forhandlere definere og konfigurere ytterligere kostnadskomponenter som skal beregnes og tas hensyn til når den beste lokasjonen for oppfylling av ordrelinjer fastsettes.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="a3cd0-111">Når kostnadskomponenter er konfigurert, bruker DOM-problemløseren bare disse kostnadsdefinisjonene for å fastslå den beste lokasjonen for ordreoppfyllelse.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="a3cd0-112">Den tar ikke hensyn til avstandskomponenten som kostnad.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="a3cd0-113">Men hvis ingen kostnadskomponenter er konfigurert, bruker DOM-problemløseren avstandskomponenten som kostnad for å fastslå den beste lokasjonen for ordreoppfyllelse.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="a3cd0-114">Konfigurere kostnadskomponenter</span><span class="sxs-lookup"><span data-stu-id="a3cd0-114">Set up cost components</span></span>

<span data-ttu-id="a3cd0-115">Du kan definere to hovedtyper av kostnadskomponenter i systemet: **Forsendelse** og **Annet**.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="a3cd0-116">Begge kostnadskomponenttypene støtter flere beregningsgrunnlag, som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a3cd0-117">Type kostnadskomponent</span><span class="sxs-lookup"><span data-stu-id="a3cd0-117">Cost component type</span></span></th>
<th><span data-ttu-id="a3cd0-118">Beregningsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="a3cd0-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a3cd0-119">Forsendelse</span><span class="sxs-lookup"><span data-stu-id="a3cd0-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a3cd0-120">Enkel</span><span class="sxs-lookup"><span data-stu-id="a3cd0-120">Simple</span></span></li>
<li><span data-ttu-id="a3cd0-121">Trinnvis</span><span class="sxs-lookup"><span data-stu-id="a3cd0-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cd0-122">Annet</span><span class="sxs-lookup"><span data-stu-id="a3cd0-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a3cd0-123">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="a3cd0-123">Sales order</span></span></li>
<li><span data-ttu-id="a3cd0-124">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="a3cd0-124">Sales line</span></span></li>
<li><span data-ttu-id="a3cd0-125">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="a3cd0-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="a3cd0-126">Kostnadskomponenttypen Forsendelse</span><span class="sxs-lookup"><span data-stu-id="a3cd0-126">Shipping cost component type</span></span>

<span data-ttu-id="a3cd0-127">Denne delen forklarer hvordan du definerer hver kombinasjon av kostnadskomponenttypen **Forsendelse** og beregningsgrunnlaget for forsendelseskostnader.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="a3cd0-128">Den inneholder også informasjon om hvordan DOM-problemløseren bruker ulike kombinasjoner.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="a3cd0-129">Type kostnadskomponent = Forsendelse og beregningsgrunnlag = Enkel</span><span class="sxs-lookup"><span data-stu-id="a3cd0-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="a3cd0-130">Hvis en kombinasjon av kostnadskomponenttypen **Forsendelse** og beregningsgrunnlaget **Enkel** brukes, er forsendelseskostnaden for en leveringsmåte basert på enten en fast kostnad eller avstand.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="a3cd0-131">Du må definere følgende felt for denne kombinasjonen:</span><span class="sxs-lookup"><span data-stu-id="a3cd0-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="a3cd0-132">**Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="a3cd0-133">**Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="a3cd0-134">**Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="a3cd0-135">Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="a3cd0-136">**Aktiv** – Angi om kostnadsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="a3cd0-137">DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="a3cd0-138">**Firma** – Angi den juridiske enheten som kostnadsfaktoren er konfigurert for.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="a3cd0-139">Alle linjer i beregningskriteriene må være for samme juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="a3cd0-140">**Leveringsmåter** – Angir leveringsmåtene som kostnaden er konfigurert for.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="a3cd0-141">**Beregningstype** – Angi hvordan kostnaden skal beregnes for en bestemt leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="a3cd0-142">To beregningstyper støttes:</span><span class="sxs-lookup"><span data-stu-id="a3cd0-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="a3cd0-143">**Fast** – En fast kostnad brukes for leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="a3cd0-144">Hvis du velger denne beregningstypen, definerer **Kostnad**-feltet den faste kostnaden.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="a3cd0-145">**Per avstandsenhet** – Kostnaden for leveringsmåten beregnes som kostverdien som angis i **Kostnad**-feltet, multiplisert med avstanden mellom leveringsadressen og lokasjonene.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="a3cd0-146">**Kostnad** – Angi kostverdien som brukes sammen med **Beregningstype**-feltet, for å beregne kostnaden for en leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="a3cd0-147">Type kostnadskomponent = Forsendelse og beregningsgrunnlag = Trinnvis</span><span class="sxs-lookup"><span data-stu-id="a3cd0-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="a3cd0-148">Hvis en kombinasjon av kostnadskomponenttypen **Forsendelse** og beregningsgrunnlaget **Trinnvis** brukes, er forsendelseskostnaden for en leveringsmåte basert på enten en fast kostnad eller avstand.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="a3cd0-149">I denne kombinasjonen er avstanden imidlertid basert på et trinnvist avstandsområde.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="a3cd0-150">Du må definere følgende felt for denne kombinasjonen:</span><span class="sxs-lookup"><span data-stu-id="a3cd0-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="a3cd0-151">**Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="a3cd0-152">**Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="a3cd0-153">**Standardkostnad** – Angi kostnaden som skal brukes for en leveringsmåte hvis avstanden mellom leveringsadressen og lokasjonen ikke er innenfor noen av de trinnvise avstandene for leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="a3cd0-154">**Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="a3cd0-155">Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="a3cd0-156">**Aktiv** – Angi om kostnadsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="a3cd0-157">DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="a3cd0-158">**Firma** – Angi den juridiske enheten som kostnadsfaktoren er konfigurert for.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="a3cd0-159">Alle linjer i beregningskriteriene må være for samme juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="a3cd0-160">**Leveringsmåter** – Angir leveringsmåtene som kostnaden er konfigurert for.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="a3cd0-161">**Avstandstype** – Angi om definisjonen av trinnvis avstand er luftavstand eller veiavstand.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="a3cd0-162">**Avstandsenheter** – Angi enheten som den trinnvise avstanden måles i.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="a3cd0-163">**Avstand fra** – Angi startområdet for den trinnvise avstanden.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="a3cd0-164">**Avstand til** – Angi sluttområdet for den trinnvise avstanden.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="a3cd0-165">**Beregningstype** – Angi hvordan kostnaden skal beregnes for en bestemt leveringsmåte og trinnvis avstand.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="a3cd0-166">To beregningstyper støttes:</span><span class="sxs-lookup"><span data-stu-id="a3cd0-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="a3cd0-167">**Fast** – En fast kostnad brukes for leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="a3cd0-168">Hvis du velger denne beregningstypen, definerer **Kostnad**-feltet den faste kostnaden.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="a3cd0-169">**Per avstandsenhet** – Kostnaden for leveringsmåten og trinnvis avstand beregnes som kostverdien som angis i **Kostnad**-feltet, multiplisert med avstanden mellom leveringsadressen og lokasjonene.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="a3cd0-170">**Kostnad** – Angi kostverdien som brukes sammen med **Beregningstype**-feltet, for å beregne kostnaden for en leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="a3cd0-171">Når du definerer trinnvise avstander, validerer systemet at det ikke er noen avstander som mangler eller overlapper.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="a3cd0-172">Avstandstypen som brukes for en leveringsmåte, må være den samme for alle trinnvise avstander.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="a3cd0-173">Kostnadskomponenttypen Annet</span><span class="sxs-lookup"><span data-stu-id="a3cd0-173">Other cost component type</span></span>

<span data-ttu-id="a3cd0-174">Denne delen forklarer hvordan du definerer hver kombinasjon av kostnadskomponenttypen **Annet** og en annen kostnadstype for kostnader som ikke er forsendelseskostnader.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="a3cd0-175">Den inneholder også informasjon om hvordan DOM-problemløseren bruker ulike kombinasjoner.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="a3cd0-176">Kostnadskomponenttype = Annet og andre kostnadstyper = Salgsordre</span><span class="sxs-lookup"><span data-stu-id="a3cd0-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="a3cd0-177">En kombinasjon av kostnadskomponenttypen **Annet** og den andre kostnadstypen **Salgsordre** brukes til å definere kostnader på salgsordrenivå som ikke er forsendelseskostnader.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="a3cd0-178">Du må definere følgende felt for denne kombinasjonen:</span><span class="sxs-lookup"><span data-stu-id="a3cd0-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="a3cd0-179">**Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="a3cd0-180">**Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="a3cd0-181">**Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="a3cd0-182">Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="a3cd0-183">**Aktiv** – Angi om kostnadsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="a3cd0-184">DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="a3cd0-185">**Kostnad** – Angi kostverdien for en kostnad på salgsordrenivå som ikke er forsendelseskostnad.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="a3cd0-186">Kostnadskomponenttype = Annet og andre kostnadstyper = Salgslinje</span><span class="sxs-lookup"><span data-stu-id="a3cd0-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="a3cd0-187">En kombinasjon av kostnadskomponenttypen **Annet** og den andre kostnadstypen **Salgslinje** brukes til å definere kostnader på salgsordrelinjenivå som ikke er forsendelseskostnader.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="a3cd0-188">Du må definere følgende felt for denne kombinasjonen:</span><span class="sxs-lookup"><span data-stu-id="a3cd0-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="a3cd0-189">**Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="a3cd0-190">**Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="a3cd0-191">**Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="a3cd0-192">Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="a3cd0-193">**Aktiv** – Angi om kostnadsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="a3cd0-194">DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="a3cd0-195">**Kostnad** – Angi kostverdien for en kostnad på salgsordrelinjenivå som ikke er forsendelseskostnad.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="a3cd0-196">Kostnadskomponenttype = Annet og andre kostnadstyper = Lokasjon</span><span class="sxs-lookup"><span data-stu-id="a3cd0-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="a3cd0-197">En kombinasjon av kostnadskomponenttypen **Annet** og den andre kostnadstypen **Lokasjon** brukes til å definere kostnader for en gruppe lokasjoner eller en enkelt lokasjon som ikke er forsendelseskostnader.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="a3cd0-198">Du må definere følgende felt for denne kombinasjonen:</span><span class="sxs-lookup"><span data-stu-id="a3cd0-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="a3cd0-199">**Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="a3cd0-200">**Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="a3cd0-201">**Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="a3cd0-202">Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="a3cd0-203">**Aktiv** – Angi om kostnadsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="a3cd0-204">DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="a3cd0-205">**Oppfyllelsesgruppe** – Angi gruppen med lokasjoner som kostnadene som ikke er forsendelseskostnader, defineres for.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="a3cd0-206">**Oppfyllelseslokasjon** – Angi lokasjonen som kostnadene som ikke er forsendelseskostnader, defineres for.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3cd0-207">Du kan ikke angi en oppfyllelsesgruppe og en oppfyllelseslokasjon på samme linje for lokasjonsbaserte beregningskriterier.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="a3cd0-208">**Kostnad** – Angi kostverdien for en kostnad som ikke er forsendelseskostnad, på oppfyllelsesgruppenivå eller oppfyllelseslokasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3cd0-209">Hvis DOM skal ta hensyn til disse kostnadene under kjøring, må du legge til kostnadsfaktoren i den relevante oppfyllelsesprofilen.</span><span class="sxs-lookup"><span data-stu-id="a3cd0-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
