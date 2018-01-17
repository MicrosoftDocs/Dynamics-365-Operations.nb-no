---
title: Leveringsalternativer
description: "Salgsordretakere kan bruke siden Leveringsalternativer til å søke etter alternativer for ordrefullføring."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 4d59db5a8909cca2ee958a928345e57f4c2abaa2
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---

# <a name="delivery-alternatives"></a><span data-ttu-id="a37c8-103">Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="a37c8-103">Delivery alternatives</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a37c8-104">Salgsordretakere kan bruke siden Leveringsalternativer til å søke etter alternativer for ordrefullføring.</span><span class="sxs-lookup"><span data-stu-id="a37c8-104">Sales order takers can use the Delivery alternatives page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="a37c8-105">I Microsoft Dynamics 365 for Operations versjon 1611 (november 2016),kan salgsordretakere bruke siden **Leveringsalternativer** til å finne alternativer for ordrefullføring.</span><span class="sxs-lookup"><span data-stu-id="a37c8-105">In Microsoft Dynamics 365 for Operations version 1611 (November 2016), sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span> <span data-ttu-id="a37c8-106">Det nye sideoppsettet gir bedre oversikt over alle alternativer.</span><span class="sxs-lookup"><span data-stu-id="a37c8-106">The redesigned page layout gives a better overview of all alternative options.</span></span> <span data-ttu-id="a37c8-107">Den lar også ordretakere se utenfor gjeldende firma for fullføringsmuligheter.</span><span class="sxs-lookup"><span data-stu-id="a37c8-107">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="a37c8-108">De kan nå vise både konserninterne muligheter og muligheter fra eksterne leverandører.</span><span class="sxs-lookup"><span data-stu-id="a37c8-108">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="a37c8-109">Salgsordretakere kan vise en intelligent liste med leveringsalternativer ved å sortere alternativene etter leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="a37c8-109">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="a37c8-110">I tillegg bidrar parametere til enklere administrasjon av foreslåtte leveringer.</span><span class="sxs-lookup"><span data-stu-id="a37c8-110">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="a37c8-111">Siden transporttid kan påvirke leveringsdatoer, kan salgsordretakere utforske de forskjellige transportvalgene som transportører tilbyr.</span><span class="sxs-lookup"><span data-stu-id="a37c8-111">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="a37c8-112">Siden det vises detaljert informasjon for hver forslag, kan salgsordretakere ta informerte avgjørelser direkte fra siden **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="a37c8-112">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="a37c8-113">Åpne siden Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="a37c8-113">Open the Delivery alternatives page</span></span>
<span data-ttu-id="a37c8-114">Du kan åpne siden **Leverings****alternativer** fra salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a37c8-114">You can open the **Delivery** **alternatives** page from the sales order line.</span></span>

1.  <span data-ttu-id="a37c8-115">Klikk på **Produkter og forsyning** &gt; **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="a37c8-115">Click **Products and supply** &gt; **Delivery alternatives**.</span></span>
2.  <span data-ttu-id="a37c8-116">Klikk på **Linjedetaljer** &gt; **Levering** &gt; **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="a37c8-116">Click **Line details** &gt; **Delivery** &gt; **Delivery alternatives.**</span></span>

<span data-ttu-id="a37c8-117">Du kan også åpne siden **Leveringsalternativer** ved å åpne arbeidsområdet **Salgsordrebehandling og -spørring**, og deretter klikke på **Ordrer og favoritter** &gt; **Forsinkede ordrelinjer** &gt; **Leveringsalternativer** **Obs!** Du kan bare åpne siden **Leveringsalternativer** hvis begge følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="a37c8-117">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then clicking **Orders and favorites** &gt; **Delayed order lines** &gt; **Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

-   <span data-ttu-id="a37c8-118">All obligatorisk informasjon for salgslinje er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="a37c8-118">All mandatory sales line information is filled in.</span></span>
-   <span data-ttu-id="a37c8-119">Feltet **Leveringsdatokontroll** er satt til en annen verdi enn **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="a37c8-119">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="a37c8-120">Metoder for leveringsdatokontroll</span><span class="sxs-lookup"><span data-stu-id="a37c8-120">Delivery date control methods</span></span>
<span data-ttu-id="a37c8-121">Metoden for leveringsdatokontroll avgjør hvordan systemet oppretter leveringsdatoer, hvordan leveringsalternativer beregnes og hvilken informasjon som vises.</span><span class="sxs-lookup"><span data-stu-id="a37c8-121">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="a37c8-122">Legg merke til at leveringsdatokontroll tar hensyn til kalendere.</span><span class="sxs-lookup"><span data-stu-id="a37c8-122">Note that delivery data control takes calendars into consideration.</span></span> <span data-ttu-id="a37c8-123">Kalenderne nedenfor kan derfor påvirke den foreslåtte mottaksdatoen: lagerkalender, transportkalender, leverandørkalender og kundekalender.</span><span class="sxs-lookup"><span data-stu-id="a37c8-123">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="a37c8-124">Tabellen nedenfor beskriver alle metodene for leveringsdatokontroll.</span><span class="sxs-lookup"><span data-stu-id="a37c8-124">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a37c8-125"><strong>Metode</strong></span><span class="sxs-lookup"><span data-stu-id="a37c8-125"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="a37c8-126"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="a37c8-126"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a37c8-127"><strong>Ingen</strong></span><span class="sxs-lookup"><span data-stu-id="a37c8-127"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a37c8-128">Leveringsalternativer for salgslinjer støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="a37c8-128">Delivery alternatives for sales lines aren't supported.</span></span> <span data-ttu-id="a37c8-129">Dette alternativet deaktiverer leveringsdatokontroll.</span><span class="sxs-lookup"><span data-stu-id="a37c8-129">This option turns off delivery data control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a37c8-130"><strong>Salgsleveringstid</strong></span><span class="sxs-lookup"><span data-stu-id="a37c8-130"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a37c8-131">Leveringsalternativer beregnes basert på den forhåndsdefinerte salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="a37c8-131">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="a37c8-132">Transportdagene beregnes basert på leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="a37c8-132">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="a37c8-133">Leveringsalternativer omfatter lagre som har lagerbeholdning og forsynings-/behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="a37c8-133">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a37c8-134"><strong>ATP</strong></span><span class="sxs-lookup"><span data-stu-id="a37c8-134"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a37c8-135">Leveringsalternativer beregnes basert på tilgjengelig for ordre-logikk (ATP).</span><span class="sxs-lookup"><span data-stu-id="a37c8-135">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="a37c8-136">Det tas hensyn til gjeldende tilgjengelighet og forventet fremtidig tilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="a37c8-136">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="a37c8-137">Transportdagene beregnes basert på leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="a37c8-137">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="a37c8-138">Leveringsalternativer omfatter lagre som har lagerbeholdning og forsynings-/behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="a37c8-138">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a37c8-139"><strong>ATP + Avgang-margin</strong></span><span class="sxs-lookup"><span data-stu-id="a37c8-139"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a37c8-140">Leveringsalternativer beregnes som for ATP-metoden, men antall sikkerhetsdager er inkludert i beregningen.</span><span class="sxs-lookup"><span data-stu-id="a37c8-140">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a37c8-141"><strong>CTP</strong></span><span class="sxs-lookup"><span data-stu-id="a37c8-141"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a37c8-142">Leveringsalternativer beregnes basert på leveringskapasitetlogikk (CTP).</span><span class="sxs-lookup"><span data-stu-id="a37c8-142">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="a37c8-143">MRP-nedbryting brukes til å bestemme tilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="a37c8-143">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="a37c8-144">Legg merke til CTP forskyver minimumleveringsdatoer til salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="a37c8-144">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="a37c8-145">Transportdagene beregnes basert på leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="a37c8-145">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="a37c8-146">Leveringsalternativer inkluderer forslag for følgende lagre:</span><span class="sxs-lookup"><span data-stu-id="a37c8-146">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="a37c8-147">Gjeldende lager</span><span class="sxs-lookup"><span data-stu-id="a37c8-147">Current warehouse</span></span></li>
<li><span data-ttu-id="a37c8-148">Standardlager</span><span class="sxs-lookup"><span data-stu-id="a37c8-148">Default warehouse</span></span></li>
<li><span data-ttu-id="a37c8-149">Alle lagre som har tilgjengelig lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="a37c8-149">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="a37c8-150">Alle lagre som har forsyningsordrer</span><span class="sxs-lookup"><span data-stu-id="a37c8-150">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="a37c8-151">Alle lagre som har aktive stykklisteversjoner</span><span class="sxs-lookup"><span data-stu-id="a37c8-151">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="a37c8-152">Vise informasjon om leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="a37c8-152">View information about delivery alternatives</span></span>
<span data-ttu-id="a37c8-153">Dette avsnittet inneholder informasjon om leveringsalternativer som er tilgjengelige i hver kategori på siden **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="a37c8-153">This section describes the information about delivery alternatives that is available on each tab of the **Delivery alternatives** page.</span></span>

### <a name="products"></a><span data-ttu-id="a37c8-154">Produkter</span><span class="sxs-lookup"><span data-stu-id="a37c8-154">Products</span></span>

<span data-ttu-id="a37c8-155">Denne kategorien viser et sammendrag av produktet og detaljer om den gjeldende salgslinje.</span><span class="sxs-lookup"><span data-stu-id="a37c8-155">This tab shows a summary of the product and details of the current sales line.</span></span>

### <a name="delivery-alternatives"></a><span data-ttu-id="a37c8-156">Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="a37c8-156">Delivery alternatives</span></span>

<span data-ttu-id="a37c8-157">Denne kategorien viser en liste med leveringsalternativer som er sortert etter mottaksdata.</span><span class="sxs-lookup"><span data-stu-id="a37c8-157">This tab shows a list of delivery alternatives that is sorted by receipt data.</span></span> <span data-ttu-id="a37c8-158">Over listen kan du velge hvilke alternativer du vil basere forslagene på.</span><span class="sxs-lookup"><span data-stu-id="a37c8-158">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="a37c8-159">Du kan også velge leveringsmåten, som bestemmer transportdagene.</span><span class="sxs-lookup"><span data-stu-id="a37c8-159">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="a37c8-160">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="a37c8-160">The following options are available:</span></span>

-   <span data-ttu-id="a37c8-161">**Ta med andre produktvarianter** – Dette alternativet er tilgjengelig for produkter som har produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="a37c8-161">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="a37c8-162">Det inneholder leveringsalternativer for andre varianter av produktet.</span><span class="sxs-lookup"><span data-stu-id="a37c8-162">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="a37c8-163">Dette alternativet er ikke tilgjengelig for CTP.</span><span class="sxs-lookup"><span data-stu-id="a37c8-163">This option isn't available for CTP.</span></span>
-   <span data-ttu-id="a37c8-164">**Inkluder delvis antall** – Som standard inkluderbare forslag som oppfyller hele antallet for salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a37c8-164">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="a37c8-165">Velg dette alternativet for å inkludere forslag som bare delvis oppfyller ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a37c8-165">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="a37c8-166">Dette alternativet er nyttig når kunden ber om en tidligere leveringsdato og godtar dellevering.</span><span class="sxs-lookup"><span data-stu-id="a37c8-166">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
-   <span data-ttu-id="a37c8-167">**Ta med senere datoer** – Som standard vise bare forslag som er bedre (tidligere) enn gjeldende datoer på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a37c8-167">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="a37c8-168">Velg dette alternativet for å inkludere senere datoer.</span><span class="sxs-lookup"><span data-stu-id="a37c8-168">Select this option to include later dates.</span></span> <span data-ttu-id="a37c8-169">Dette alternativet kan være nyttig i situasjoner der andre parametere enn datoen har prioritet.</span><span class="sxs-lookup"><span data-stu-id="a37c8-169">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="a37c8-170">En bestemt leverandør eller lager kan for eksempel være foretrukket.</span><span class="sxs-lookup"><span data-stu-id="a37c8-170">For example, a specific vendor or warehouse might be preferred.</span></span>
-   <span data-ttu-id="a37c8-171">**Leveringsmåte** – Velg den foretrukne leveringsmåten for å optimalisere transporttiden og kostnadene.</span><span class="sxs-lookup"><span data-stu-id="a37c8-171">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="a37c8-172">Virkningen på foreslåtte leveringsalternativer vises umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="a37c8-172">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="a37c8-173">Derfor er det enklere å sammenligne alternativene.</span><span class="sxs-lookup"><span data-stu-id="a37c8-173">Therefore, it's easy to compare the alternatives.</span></span>
-   <span data-ttu-id="a37c8-174">**Inkluder innkjøp** – Når innkjøp er valgt, vil foreslåtte leveringsalternativer inkludere alternativer for å produsere fra eksterne leverandører og andre firmaer i organisasjonen (konsernintern).</span><span class="sxs-lookup"><span data-stu-id="a37c8-174">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="a37c8-175">Alternativet **Inkluder innkjøp** støttes for leveringsdatokontroll for ATP og ATP + Avgang-margin.</span><span class="sxs-lookup"><span data-stu-id="a37c8-175">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="a37c8-176">Innkjøpsalternativer fra standard kjøpsleverandør for produktet og alle godkjente leverandører for produktet, er inkludert.</span><span class="sxs-lookup"><span data-stu-id="a37c8-176">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
-   <span data-ttu-id="a37c8-177">Beregningen er basert på leveringstiden for innkjøp for eksterne leverandører.</span><span class="sxs-lookup"><span data-stu-id="a37c8-177">For external vendors, the calculation is based on the purchase lead time.</span></span>
-   <span data-ttu-id="a37c8-178">For konserninterne tar beregningen hensyn til hva som er tilgjengelig fra leverandørfirmaet, basert på leveringsdatokontroll i leverandørfirmaet.</span><span class="sxs-lookup"><span data-stu-id="a37c8-178">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
-   <span data-ttu-id="a37c8-179">**Leveringstype** (Relevant for innkjøp)</span><span class="sxs-lookup"><span data-stu-id="a37c8-179">**Delivery type** (Relevant for procurement)</span></span>
    -   <span data-ttu-id="a37c8-180">**Lager** – Produkter sendes fra leverandørlageret til området/lageret på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a37c8-180">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="a37c8-181">De sendes deretter fra dette lageret til kunden.</span><span class="sxs-lookup"><span data-stu-id="a37c8-181">They are then shipped from that warehouse to the customer.</span></span>
    -   <span data-ttu-id="a37c8-182">**Direktelevering** – Produktene leveres direkte fra leverandørlageret til kunden.</span><span class="sxs-lookup"><span data-stu-id="a37c8-182">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="availability-information"></a><span data-ttu-id="a37c8-183">Tilgjengelighetsinformasjon</span><span class="sxs-lookup"><span data-stu-id="a37c8-183">Availability information</span></span>

<span data-ttu-id="a37c8-184">Informasjon i denne kategorien er knyttet til leveringsalternativlinjen som er valgt.</span><span class="sxs-lookup"><span data-stu-id="a37c8-184">Information on this tab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="a37c8-185">Følgende informasjon vises, avhengig av leveringsdatokontrollen for salgslinjen:</span><span class="sxs-lookup"><span data-stu-id="a37c8-185">The following information is shown, depending on the delivery date control for the sales line:</span></span>

-   <span data-ttu-id="a37c8-186">**Salgsleveringstid**</span><span class="sxs-lookup"><span data-stu-id="a37c8-186">**Sales lead time**</span></span>
    -   <span data-ttu-id="a37c8-187">**Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="a37c8-187">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="a37c8-188">**Parametere** – Viser lagerenheten og salgsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="a37c8-188">**Parameters** - Show the inventory unit and sales lead time.</span></span>

-   <span data-ttu-id="a37c8-189">**ATP og ATP + Avgang-margin**</span><span class="sxs-lookup"><span data-stu-id="a37c8-189">**ATP and ATP + Issue margin**</span></span>
    -   <span data-ttu-id="a37c8-190">**Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="a37c8-190">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="a37c8-191">**Parametere** – Viser lagerenheten og salgsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="a37c8-191">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="a37c8-192">**Fremtidig tilgjengelighet** – Viser en grafisk fremstilling av gjeldende og fremtidig tilgjengelighet for det valgte området og lageret under **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="a37c8-192">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="a37c8-193">Du kan klikke diagramkolonnene for å vise mer detaljert informasjon om fremtidig tilgjengelighet for produktet.</span><span class="sxs-lookup"><span data-stu-id="a37c8-193">You can click the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="a37c8-194">Glidebryteren viser en liste over relevante behovs- og forsyningsordrer i ATP-horisonten.</span><span class="sxs-lookup"><span data-stu-id="a37c8-194">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

-   <span data-ttu-id="a37c8-195">**CTP**</span><span class="sxs-lookup"><span data-stu-id="a37c8-195">**CTP**</span></span>
    -   <span data-ttu-id="a37c8-196">**Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="a37c8-196">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="a37c8-197">**Parametere** – Viser lagerenheten og salgsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="a37c8-197">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="a37c8-198">**Nedbryting** – Viser en forsyningsnedbryting av valgt leveringsalternativ.</span><span class="sxs-lookup"><span data-stu-id="a37c8-198">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="a37c8-199">Du kan bruke **Oppsett** til å endre feltene og lagerdimensjonene som vises i nedbrytingen.</span><span class="sxs-lookup"><span data-stu-id="a37c8-199">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="impact-of-selected-alternative"></a><span data-ttu-id="a37c8-200">Innvirkning av valgt alternativ</span><span class="sxs-lookup"><span data-stu-id="a37c8-200">Impact of selected alternative</span></span>

<span data-ttu-id="a37c8-201">Denne kategorien uthever effekten av det valgte leveringsalternativet.</span><span class="sxs-lookup"><span data-stu-id="a37c8-201">This tab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="a37c8-202">Hvis du klikker på **OK**, oppdateres salgslinjen med de uthevede verdiene i VALGT-kolonnene.</span><span class="sxs-lookup"><span data-stu-id="a37c8-202">If you click **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="a37c8-203">Legg merke til at hvis antallet på det valgte leveringsalternativet er mindre enn antall på salgslinjen, opprettes en leveringsplan og ordrelinjen deles inn i to linjer: én linje for det valgte antallet og én linje for det restantallet.</span><span class="sxs-lookup"><span data-stu-id="a37c8-203">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="a37c8-204">Du kan også oppdatere den kommersielle linjen, slik at den samsvarer med planlinjene og påvirker prissettingen.</span><span class="sxs-lookup"><span data-stu-id="a37c8-204">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

<a name="see-also"></a><span data-ttu-id="a37c8-205">Se også</span><span class="sxs-lookup"><span data-stu-id="a37c8-205">See also</span></span>
--------

[<span data-ttu-id="a37c8-206">Ordrebekreftelse</span><span class="sxs-lookup"><span data-stu-id="a37c8-206">Order promising</span></span>](delivery-dates-available-promise-calculations.md)





