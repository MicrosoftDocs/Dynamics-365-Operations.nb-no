---
title: Leveringsalternativer
description: Salgsordretakere kan bruke siden Leveringsalternativer til å søke etter alternativer for ordrefullføring.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 783307ea5cc764f4a04d069dfd7d614a4f63dd2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229261"
---
# <a name="delivery-alternatives"></a><span data-ttu-id="f7c00-103">Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="f7c00-103">Delivery alternatives</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7c00-104">Salgsordretakere kan bruke siden **Leveringsalternativer** til å søke etter alternativer for ordrefullføring.</span><span class="sxs-lookup"><span data-stu-id="f7c00-104">Sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="f7c00-105">Det nye oppsettet på siden **Leveringsalternativer** gir en oversikt over alle alternativer.</span><span class="sxs-lookup"><span data-stu-id="f7c00-105">The **Delivery alternatives** page layout gives an overview of all alternative options.</span></span> <span data-ttu-id="f7c00-106">Den lar også ordretakere se utenfor gjeldende firma for fullføringsmuligheter.</span><span class="sxs-lookup"><span data-stu-id="f7c00-106">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="f7c00-107">De kan nå vise både konserninterne muligheter og muligheter fra eksterne leverandører.</span><span class="sxs-lookup"><span data-stu-id="f7c00-107">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="f7c00-108">Salgsordretakere kan vise en intelligent liste med leveringsalternativer ved å sortere alternativene etter leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="f7c00-108">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="f7c00-109">I tillegg bidrar parametere til enklere administrasjon av foreslåtte leveringer.</span><span class="sxs-lookup"><span data-stu-id="f7c00-109">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="f7c00-110">Siden transporttid kan påvirke leveringsdatoer, kan salgsordretakere utforske de forskjellige transportvalgene som transportører tilbyr.</span><span class="sxs-lookup"><span data-stu-id="f7c00-110">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="f7c00-111">Siden det vises detaljert informasjon for hver forslag, kan salgsordretakere ta informerte avgjørelser direkte fra siden **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="f7c00-111">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="f7c00-112">Åpne siden Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="f7c00-112">Open the Delivery alternatives page</span></span>

<span data-ttu-id="f7c00-113">Du kan åpne siden **Leveringsalternativer** fra salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-113">You can open the **Delivery alternatives** page from the sales order line.</span></span>

1. <span data-ttu-id="f7c00-114">Velg **Produkter og forsyning \> Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="f7c00-114">Select **Products and supply \> Delivery alternatives**.</span></span>
1. <span data-ttu-id="f7c00-115">Velg **Linjedetaljer \> Levering \> Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="f7c00-115">Select **Line details \> Delivery \> Delivery alternatives.**</span></span>

<span data-ttu-id="f7c00-116">Du kan også åpne siden **Leveringsalternativer** ved å åpne arbeidsområdet **Salgsordrebehandling og -spørring**, og deretter velge **Ordrer og favoritter \> Forsinkede ordrelinjer \> Leveringsalternativer** **Obs!** Du kan bare åpne siden **Leveringsalternativer** hvis begge følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="f7c00-116">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then selecting **Orders and favorites \> Delayed order lines \> Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

- <span data-ttu-id="f7c00-117">All obligatorisk informasjon for salgslinje er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="f7c00-117">All mandatory sales line information is filled in.</span></span>
- <span data-ttu-id="f7c00-118">Feltet **Leveringsdatokontroll** er satt til en annen verdi enn **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="f7c00-118">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="f7c00-119">Metoder for leveringsdatokontroll</span><span class="sxs-lookup"><span data-stu-id="f7c00-119">Delivery date control methods</span></span>

<span data-ttu-id="f7c00-120">Metoden for leveringsdatokontroll avgjør hvordan systemet oppretter leveringsdatoer, hvordan leveringsalternativer beregnes og hvilken informasjon som vises.</span><span class="sxs-lookup"><span data-stu-id="f7c00-120">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="f7c00-121">Legg merke til at leveringsdatokontroll tar hensyn til kalendere.</span><span class="sxs-lookup"><span data-stu-id="f7c00-121">Note that delivery date control takes calendars into consideration.</span></span> <span data-ttu-id="f7c00-122">Kalenderne nedenfor kan derfor påvirke den foreslåtte mottaksdatoen: lagerkalender, transportkalender, leverandørkalender og kundekalender.</span><span class="sxs-lookup"><span data-stu-id="f7c00-122">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="f7c00-123">Tabellen nedenfor beskriver alle metodene for leveringsdatokontroll.</span><span class="sxs-lookup"><span data-stu-id="f7c00-123">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7c00-124"><strong>Metode</strong></span><span class="sxs-lookup"><span data-stu-id="f7c00-124"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="f7c00-125"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="f7c00-125"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7c00-126"><strong>None</strong></span><span class="sxs-lookup"><span data-stu-id="f7c00-126"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="f7c00-127">Leveringsalternativer for salgslinjer støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="f7c00-127">Delivery alternatives for sales lines aren't supported.</span></span> <span data-ttu-id="f7c00-128">Dette alternativet deaktiverer leveringsdatokontroll.</span><span class="sxs-lookup"><span data-stu-id="f7c00-128">This option turns off delivery date control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7c00-129"><strong>Salgsleveringstid</strong></span><span class="sxs-lookup"><span data-stu-id="f7c00-129"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="f7c00-130">Leveringsalternativer beregnes basert på den forhåndsdefinerte salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="f7c00-130">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="f7c00-131">Transportdagene beregnes basert på leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="f7c00-131">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="f7c00-132">Leveringsalternativer omfatter lagre som har lagerbeholdning og forsynings-/behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="f7c00-132">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7c00-133"><strong>ATP</strong></span><span class="sxs-lookup"><span data-stu-id="f7c00-133"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="f7c00-134">Leveringsalternativer beregnes basert på tilgjengelig for ordre-logikk (ATP).</span><span class="sxs-lookup"><span data-stu-id="f7c00-134">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="f7c00-135">Det tas hensyn til gjeldende tilgjengelighet og forventet fremtidig tilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="f7c00-135">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="f7c00-136">Transportdagene beregnes basert på leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="f7c00-136">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="f7c00-137">Leveringsalternativer omfatter lagre som har lagerbeholdning og forsynings-/behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="f7c00-137">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7c00-138"><strong>ATP + Avgang-margin</strong></span><span class="sxs-lookup"><span data-stu-id="f7c00-138"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="f7c00-139">Leveringsalternativer beregnes som for ATP-metoden, men antall sikkerhetsdager er inkludert i beregningen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-139">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7c00-140"><strong>CTP</strong></span><span class="sxs-lookup"><span data-stu-id="f7c00-140"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="f7c00-141">Leveringsalternativer beregnes basert på leveringskapasitetlogikk (CTP).</span><span class="sxs-lookup"><span data-stu-id="f7c00-141">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="f7c00-142">MRP-nedbryting brukes til å bestemme tilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="f7c00-142">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="f7c00-143">Legg merke til CTP forskyver minimumleveringsdatoer til salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="f7c00-143">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="f7c00-144">Transportdagene beregnes basert på leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="f7c00-144">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="f7c00-145">Leveringsalternativer inkluderer forslag for følgende lagre:</span><span class="sxs-lookup"><span data-stu-id="f7c00-145">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="f7c00-146">Gjeldende lager</span><span class="sxs-lookup"><span data-stu-id="f7c00-146">Current warehouse</span></span></li>
<li><span data-ttu-id="f7c00-147">Standardlager</span><span class="sxs-lookup"><span data-stu-id="f7c00-147">Default warehouse</span></span></li>
<li><span data-ttu-id="f7c00-148">Alle lagre som har tilgjengelig lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="f7c00-148">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="f7c00-149">Alle lagre som har forsyningsordrer</span><span class="sxs-lookup"><span data-stu-id="f7c00-149">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="f7c00-150">Alle lagre som har aktive stykklisteversjoner</span><span class="sxs-lookup"><span data-stu-id="f7c00-150">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="f7c00-151">Vise informasjon om leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="f7c00-151">View information about delivery alternatives</span></span>

<span data-ttu-id="f7c00-152">Dette avsnittet inneholder informasjon om leveringsalternativer som er tilgjengelige i hver hurtigfane på siden **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="f7c00-152">This section describes the information about delivery alternatives that is available on each FastTab of the **Delivery alternatives** page.</span></span>

### <a name="the-product-fasttab"></a><span data-ttu-id="f7c00-153">Hurtigfanen Produkt</span><span class="sxs-lookup"><span data-stu-id="f7c00-153">The Product FastTab</span></span>

<span data-ttu-id="f7c00-154">Denne hurtigfanen viser et sammendrag av produktet og detaljene om den gjeldende salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-154">This FastTab shows a summary of the product and details of the current sales line.</span></span>

### <a name="the-delivery-alternatives-fasttab"></a><span data-ttu-id="f7c00-155">Åpne hurtigfanen Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="f7c00-155">The Delivery alternatives FastTab</span></span>

<span data-ttu-id="f7c00-156">Denne hurtigfanen viser en liste over leveringsalternativer som er sortert etter mottaksdato.</span><span class="sxs-lookup"><span data-stu-id="f7c00-156">This FastTab shows a list of delivery alternatives that is sorted by receipt date.</span></span> <span data-ttu-id="f7c00-157">Over listen kan du velge hvilke alternativer du vil basere forslagene på.</span><span class="sxs-lookup"><span data-stu-id="f7c00-157">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="f7c00-158">Du kan også velge leveringsmåten, som bestemmer transportdagene.</span><span class="sxs-lookup"><span data-stu-id="f7c00-158">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="f7c00-159">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f7c00-159">The following options are available:</span></span>

- <span data-ttu-id="f7c00-160">**Ta med andre produktvarianter** – Dette alternativet er tilgjengelig for produkter som har produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="f7c00-160">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="f7c00-161">Det inneholder leveringsalternativer for andre varianter av produktet.</span><span class="sxs-lookup"><span data-stu-id="f7c00-161">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="f7c00-162">Dette alternativet er ikke tilgjengelig for CTP.</span><span class="sxs-lookup"><span data-stu-id="f7c00-162">This option isn't available for CTP.</span></span>
- <span data-ttu-id="f7c00-163">**Inkluder delvis antall** – Som standard inkluderbare forslag som oppfyller hele antallet for salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-163">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="f7c00-164">Velg dette alternativet for å inkludere forslag som bare delvis oppfyller ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-164">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="f7c00-165">Dette alternativet er nyttig når kunden ber om en tidligere leveringsdato og godtar dellevering.</span><span class="sxs-lookup"><span data-stu-id="f7c00-165">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
- <span data-ttu-id="f7c00-166">**Ta med senere datoer** – Som standard vise bare forslag som er bedre (tidligere) enn gjeldende datoer på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-166">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="f7c00-167">Velg dette alternativet for å inkludere senere datoer.</span><span class="sxs-lookup"><span data-stu-id="f7c00-167">Select this option to include later dates.</span></span> <span data-ttu-id="f7c00-168">Dette alternativet kan være nyttig i situasjoner der andre parametere enn datoen har prioritet.</span><span class="sxs-lookup"><span data-stu-id="f7c00-168">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="f7c00-169">En bestemt leverandør eller lager kan for eksempel være foretrukket.</span><span class="sxs-lookup"><span data-stu-id="f7c00-169">For example, a specific vendor or warehouse might be preferred.</span></span>
- <span data-ttu-id="f7c00-170">**Leveringsmåte** – Velg den foretrukne leveringsmåten for å optimalisere transporttiden og kostnadene.</span><span class="sxs-lookup"><span data-stu-id="f7c00-170">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="f7c00-171">Virkningen på foreslåtte leveringsalternativer vises umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="f7c00-171">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="f7c00-172">Derfor er det enklere å sammenligne alternativene.</span><span class="sxs-lookup"><span data-stu-id="f7c00-172">Therefore, it's easy to compare the alternatives.</span></span>
- <span data-ttu-id="f7c00-173">**Inkluder innkjøp** – Når innkjøp er valgt, vil foreslåtte leveringsalternativer inkludere alternativer for å produsere fra eksterne leverandører og andre firmaer i organisasjonen (konsernintern).</span><span class="sxs-lookup"><span data-stu-id="f7c00-173">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="f7c00-174">Alternativet **Inkluder innkjøp** støttes for leveringsdatokontroll for ATP og ATP + Avgang-margin.</span><span class="sxs-lookup"><span data-stu-id="f7c00-174">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="f7c00-175">Innkjøpsalternativer fra standard kjøpsleverandør for produktet og alle godkjente leverandører for produktet, er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f7c00-175">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
- <span data-ttu-id="f7c00-176">Beregningen er basert på leveringstiden for innkjøp for eksterne leverandører.</span><span class="sxs-lookup"><span data-stu-id="f7c00-176">For external vendors, the calculation is based on the purchase lead time.</span></span>
- <span data-ttu-id="f7c00-177">For konserninterne tar beregningen hensyn til hva som er tilgjengelig fra leverandørfirmaet, basert på leveringsdatokontroll i leverandørfirmaet.</span><span class="sxs-lookup"><span data-stu-id="f7c00-177">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
- <span data-ttu-id="f7c00-178">**Leveringstype** (Relevant for innkjøp)</span><span class="sxs-lookup"><span data-stu-id="f7c00-178">**Delivery type** (Relevant for procurement)</span></span>
  - <span data-ttu-id="f7c00-179">**Lager** – Produkter sendes fra leverandørlageret til området/lageret på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-179">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="f7c00-180">De sendes deretter fra dette lageret til kunden.</span><span class="sxs-lookup"><span data-stu-id="f7c00-180">They are then shipped from that warehouse to the customer.</span></span>
  - <span data-ttu-id="f7c00-181">**Direktelevering** – Produktene leveres direkte fra leverandørlageret til kunden.</span><span class="sxs-lookup"><span data-stu-id="f7c00-181">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="the-availability-information-fasttab"></a><span data-ttu-id="f7c00-182">Hurtigfanen Tilgjengelighetsinformasjon</span><span class="sxs-lookup"><span data-stu-id="f7c00-182">The Availability information FastTab</span></span>

<span data-ttu-id="f7c00-183">Informasjon i denne hurtigfanen er knyttet til leveringsalternativlinjen som er valgt.</span><span class="sxs-lookup"><span data-stu-id="f7c00-183">Information on this FastTab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="f7c00-184">Følgende informasjon vises, avhengig av leveringsdatokontrollen for salgslinjen:</span><span class="sxs-lookup"><span data-stu-id="f7c00-184">The following information is shown, depending on the delivery date control for the sales line:</span></span>

- <span data-ttu-id="f7c00-185">**Salgsleveringstid**</span><span class="sxs-lookup"><span data-stu-id="f7c00-185">**Sales lead time**</span></span>
  - <span data-ttu-id="f7c00-186">**Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="f7c00-186">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="f7c00-187">**Parametere** – Viser lagerenheten og salgsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="f7c00-187">**Parameters** - Show the inventory unit and sales lead time.</span></span>

- <span data-ttu-id="f7c00-188">**ATP og ATP + Avgang-margin**</span><span class="sxs-lookup"><span data-stu-id="f7c00-188">**ATP and ATP + Issue margin**</span></span>
  - <span data-ttu-id="f7c00-189">**Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="f7c00-189">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="f7c00-190">**Parametere** – Viser lagerenheten og salgsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="f7c00-190">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="f7c00-191">**Fremtidig tilgjengelighet** – Viser en grafisk fremstilling av gjeldende og fremtidig tilgjengelighet for det valgte området og lageret under **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="f7c00-191">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="f7c00-192">Du kan velge diagramkolonnene for å vise mer detaljert informasjon om fremtidig tilgjengelighet for produktet.</span><span class="sxs-lookup"><span data-stu-id="f7c00-192">You can select the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="f7c00-193">Glidebryteren viser en liste over relevante behovs- og forsyningsordrer i ATP-horisonten.</span><span class="sxs-lookup"><span data-stu-id="f7c00-193">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

- <span data-ttu-id="f7c00-194">**CTP**</span><span class="sxs-lookup"><span data-stu-id="f7c00-194">**CTP**</span></span>
  - <span data-ttu-id="f7c00-195">**Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="f7c00-195">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="f7c00-196">**Parametere** – Viser lagerenheten og salgsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="f7c00-196">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="f7c00-197">**Nedbryting** – Viser en forsyningsnedbryting av valgt leveringsalternativ.</span><span class="sxs-lookup"><span data-stu-id="f7c00-197">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="f7c00-198">Du kan bruke **Oppsett** til å endre feltene og lagerdimensjonene som vises i nedbrytingen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-198">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="the-impact-of-selected-alternative-fasttab"></a><span data-ttu-id="f7c00-199">Hurtigfanen Innvirkning av valgt alternativ</span><span class="sxs-lookup"><span data-stu-id="f7c00-199">The Impact of selected alternative FastTab</span></span>

<span data-ttu-id="f7c00-200">Denne hurtigfanen uthever effekten av det valgte leveringsalternativet.</span><span class="sxs-lookup"><span data-stu-id="f7c00-200">This FastTab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="f7c00-201">Hvis du velger **OK**, oppdateres salgslinjen med de uthevede verdiene i VALGT-kolonnene.</span><span class="sxs-lookup"><span data-stu-id="f7c00-201">If you select **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="f7c00-202">Legg merke til at hvis antallet på det valgte leveringsalternativet er mindre enn antall på salgslinjen, opprettes en leveringsplan og ordrelinjen deles inn i to linjer: én linje for det valgte antallet og én linje for det restantallet.</span><span class="sxs-lookup"><span data-stu-id="f7c00-202">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="f7c00-203">Du kan også oppdatere den kommersielle linjen, slik at den samsvarer med planlinjene og påvirker prissettingen.</span><span class="sxs-lookup"><span data-stu-id="f7c00-203">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7c00-204">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f7c00-204">Additional resources</span></span>

[<span data-ttu-id="f7c00-205">Ordrebekreftelse</span><span class="sxs-lookup"><span data-stu-id="f7c00-205">Order promising</span></span>](delivery-dates-available-promise-calculations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]