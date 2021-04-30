---
title: Feilsøking i forbindelse med priser, rabatter og avtaler
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med priser, rabatter og avtaler.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2ccc1d52b83f9319af1c6336c1876c795c70028a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908525"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="5f57c-103">Feilsøking i forbindelse med priser, rabatter og avtaler</span><span class="sxs-lookup"><span data-stu-id="5f57c-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="5f57c-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med priser, rabatter og avtaler.</span><span class="sxs-lookup"><span data-stu-id="5f57c-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="5f57c-105">Jeg kan ikke koble en kjøpsavtale til en bestillingslinje etter at bestillingen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="5f57c-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="5f57c-106">En kjøpsavtale må knyttes til en bestilling når bestillingen opprettes.</span><span class="sxs-lookup"><span data-stu-id="5f57c-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="5f57c-107">Hvis ikke kan ikke bestillingslinjer knyttes til kjøpsavtalelinjer.</span><span class="sxs-lookup"><span data-stu-id="5f57c-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="5f57c-108">Hvilken kontroll utløser meldingen "Oppdater priser og rabatter som er angitt manuelt eller eksternt dokument"?</span><span class="sxs-lookup"><span data-stu-id="5f57c-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="5f57c-109">Når du endrer leveringsdatoen, kan du få en melding om å oppdatere priser og rabatter som er angitt manuelt, eller eksternt dokument.</span><span class="sxs-lookup"><span data-stu-id="5f57c-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="5f57c-110">Du får denne meldingen fordi hvis leveringsdatoen endres, kan en annen handels- eller salgsavtale utløses og føre til en prisendring.</span><span class="sxs-lookup"><span data-stu-id="5f57c-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="5f57c-111">En endring i forsendelsesdatoen kan også ha innvirkning på lagerplanene og annen relatert informasjon.</span><span class="sxs-lookup"><span data-stu-id="5f57c-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="5f57c-112">Meldingen utløses når en av datoene eller en annen parameter endres.</span><span class="sxs-lookup"><span data-stu-id="5f57c-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="5f57c-113">Formålet med meldingen er å sørge for at du kjenner til prisendringer som kan forekomme på grunn av endringene.</span><span class="sxs-lookup"><span data-stu-id="5f57c-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="5f57c-114">Meldingen er anmodningen om evaluering av forretningsavtale (TAE).</span><span class="sxs-lookup"><span data-stu-id="5f57c-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="5f57c-115">Hvis du vil ha en fullstendig beskrivelse, se [Evalueringspolicyer for forretningsavtale](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="5f57c-115">For a full description, see [Trade agreement evaluation policies](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="5f57c-116">En bestillingskvittering omfatter ikke alle gebyrer.</span><span class="sxs-lookup"><span data-stu-id="5f57c-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="5f57c-117">Reprodusere problemet</span><span class="sxs-lookup"><span data-stu-id="5f57c-117">Reproduce the issue</span></span>

<span data-ttu-id="5f57c-118">Følgende prosedyre viser én måte å reprodusere problemet på.</span><span class="sxs-lookup"><span data-stu-id="5f57c-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="5f57c-119">På siden for **Parametere for innkjøp og leverandører**, i fanen **Levering**, må du kontrollere at alternativet for **Generer tillegg på produktkvittering** er satt til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="5f57c-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="5f57c-120">Opprette en bestilling som inkluderer tillegg.</span><span class="sxs-lookup"><span data-stu-id="5f57c-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="5f57c-121">Bekreft bestillingen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="5f57c-122">Motta bestillingen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="5f57c-123">Se på det kvitteringstotalen, og sammenlign den med forventet totalbeløp.</span><span class="sxs-lookup"><span data-stu-id="5f57c-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="5f57c-124">Legg merke til at ikke alle gebyrene er inkludert i bestillingskvitteringen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5f57c-125">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="5f57c-125">Issue resolution</span></span>

<span data-ttu-id="5f57c-126">Oppløsningen avhenger av hvordan tilleggene er definert.</span><span class="sxs-lookup"><span data-stu-id="5f57c-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="5f57c-127">Hvis du vil ha informasjon om hvordan du definerer tillegg for å oppfylle dine behov, kan du se følgende blogginnlegg: [Poster tilleggskostnader på tidspunktet for produktkvitteringen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="5f57c-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="5f57c-128">Forretningsavtalepriser og -rabatter blir ikke tatt i bruk på salgs- eller bestillingslinjer som er importert via databehandling.</span><span class="sxs-lookup"><span data-stu-id="5f57c-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5f57c-129">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5f57c-129">Issue description</span></span>

<span data-ttu-id="5f57c-130">Forretningsavtaler som gjelder salgs- eller bestillingslinjer, brukes ikke på linjer som er importert via databehandling.</span><span class="sxs-lookup"><span data-stu-id="5f57c-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="5f57c-131">De samme forretningsavtalene brukes imidlertid på salgs- eller bestillingslinjer som opprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="5f57c-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="5f57c-132">Årsak til problemet</span><span class="sxs-lookup"><span data-stu-id="5f57c-132">Reason for the issue</span></span>

<span data-ttu-id="5f57c-133">Hvis innkjøpsordrelinjer som er importert via databehandling, allerede inkluderer prisinformasjon, blir ikke forretningsavtalen evaluert på nytt for disse linjene.</span><span class="sxs-lookup"><span data-stu-id="5f57c-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="5f57c-134">Hvis for eksempel **Linjerabatt i prosent** eller noen av pris- og rabattverdiene er angitt for en linje, vil det ikke bli slått opp forretningsavtaler for denne linjen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="5f57c-135">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="5f57c-135">Issue workaround</span></span>

<span data-ttu-id="5f57c-136">Denne virkemåten er forventet og er lik for både salgsordrer og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="5f57c-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="5f57c-137">For å unngå dette kan du importere bestillingslinjene uten å angi prisinformasjon.</span><span class="sxs-lookup"><span data-stu-id="5f57c-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="5f57c-138">Forretningsavtalene blir deretter brukt, og bestillingslinjene blir oppdatert basert på de definerte forretningsavtalene.</span><span class="sxs-lookup"><span data-stu-id="5f57c-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="5f57c-139">En leverandørrabatt blir ikke akkumulert basert på fakturaer.</span><span class="sxs-lookup"><span data-stu-id="5f57c-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5f57c-140">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5f57c-140">Issue description</span></span>

<span data-ttu-id="5f57c-141">Hvis fakturaer som er postert, har forskjellige forfallsdatoer, blir ikke disse fakturaene gjenspeilet i leverandørrabatter som genereres fra dem.</span><span class="sxs-lookup"><span data-stu-id="5f57c-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5f57c-142">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="5f57c-142">Issue resolution</span></span>

<span data-ttu-id="5f57c-143">Som standard tas ikke forfallsdatoen med når leverandørrabatten beregnes.</span><span class="sxs-lookup"><span data-stu-id="5f57c-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="5f57c-144">Vurder å tilpasse systemet slik at forfallsdatoen og forbindelsen til fakturaen er mer synlig med hensyn til den faktiske leverandørrabatten.</span><span class="sxs-lookup"><span data-stu-id="5f57c-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="5f57c-145">Enhetspriser på bestillinger beregnes ikke basert på enhetsomregningen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5f57c-146">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5f57c-146">Issue description</span></span>

<span data-ttu-id="5f57c-147">Når en enhet endres på en bestilling, beregnes ikke forretningsavtalepriser på nytt i henhold til enhetsomregningsdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="5f57c-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5f57c-148">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="5f57c-148">Issue resolution</span></span>

<span data-ttu-id="5f57c-149">Prisene hentes alltid fra forretningsavtaler (eller andre prisinnstillinger i systemet, for eksempel salgsavtaler eller varepriser), og de angis for en enhet.</span><span class="sxs-lookup"><span data-stu-id="5f57c-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="5f57c-150">Hvis enheten endres på en ordrelinje, søker systemet etter en pris for den nye enheten og bruker denne prisen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="5f57c-151">Hvis det ikke finnes en pris for enheten, bruker ikke systemet en pris.</span><span class="sxs-lookup"><span data-stu-id="5f57c-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="5f57c-152">Enhetskonverteringen kan ikke brukes til å omberegne prisen til en annen enhet.</span><span class="sxs-lookup"><span data-stu-id="5f57c-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="5f57c-153">I teorien kan det hende at prisen for en boks på ti ikke er lik ti ganger prisen på en boks.</span><span class="sxs-lookup"><span data-stu-id="5f57c-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="5f57c-154">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="5f57c-154">Issue workaround</span></span>

<span data-ttu-id="5f57c-155">En måte å omgå dette problemet på, er å kontrollere at det finnes forretningsavtaler for de enhetene du forventer vil bli brukt på ordrelinjer for varen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="5f57c-156">Det oppstår problemer med valutaomregning med forretningsavtaler.</span><span class="sxs-lookup"><span data-stu-id="5f57c-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="5f57c-157">Forretningsavtale priser blir ikke omberegnet i henhold til valutaen når valutaen er forskjellig i en bestilling.</span><span class="sxs-lookup"><span data-stu-id="5f57c-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="5f57c-158">Med funksjonen *Generisk valuta* kan du definere priser og rabatter i bare én valuta.</span><span class="sxs-lookup"><span data-stu-id="5f57c-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="5f57c-159">Du kan deretter konvertere til andre valutaer etter behov.</span><span class="sxs-lookup"><span data-stu-id="5f57c-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="5f57c-160">Etter at konverteringen er utført, kan funksjonen også bruke smart avrunding automatisk.</span><span class="sxs-lookup"><span data-stu-id="5f57c-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="5f57c-161">Når jeg åpner kjøpsavtalesiden i en linjevisningsmodus, kan jeg ikke tilpasse siden ved å legge til Prisenhet-feltet i oversikten over linjen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="5f57c-162">Enkelte delte felt i avtalerammeverket kan ikke inkluderes i personlige tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="5f57c-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="5f57c-163">Denne begrensningen oppstår på grunn av datamodellen som er implementert.</span><span class="sxs-lookup"><span data-stu-id="5f57c-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="5f57c-164">Derfor kan du ikke tilpasse **Prisenhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5f57c-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="5f57c-165">Maksimumsgrensen fra en kjøpsavtale er ikke gyldig på en innkjøpsrekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="5f57c-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5f57c-166">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5f57c-166">Issue description</span></span>

<span data-ttu-id="5f57c-167">Når en innkjøpsrekvisisjon er koblet til en kjøpsavtale, gjelder ikke maksimumsgrensen fra kjøpsavtalen i innkjøpsrekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="5f57c-168">Standard prisinformasjon angis på riktig måte, men mer enn maksimumsgrensen fra kjøpsavtalen kan bestilles i innkjøpsrekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5f57c-169">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="5f57c-169">Issue resolution</span></span>

<span data-ttu-id="5f57c-170">Denne virkemåten er forventet.</span><span class="sxs-lookup"><span data-stu-id="5f57c-170">This behavior is expected.</span></span> <span data-ttu-id="5f57c-171">Fordi rekvisisjoner ikke alltid er godkjent, skal det ikke reserveres et antall eller et beløp på kjøpsavtalen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="5f57c-172">Derfor oppfyller du ikke maksimumsgrensen fra kjøpsavtalen.</span><span class="sxs-lookup"><span data-stu-id="5f57c-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="5f57c-173">Forretningsavtaler kan opprettes fra avviste tilbudsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="5f57c-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="5f57c-174">Derfor kan ikke systemet hindre at det opprettes forretningsavtalejournaler hvis tilbudsforespørselslinjen ikke er godtatt.</span><span class="sxs-lookup"><span data-stu-id="5f57c-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="5f57c-175">Du kan opprette forretningsavtaler for et hvilket som helst svar på en tilbudsforespørsel, uansett om de ble godtatt eller avvist.</span><span class="sxs-lookup"><span data-stu-id="5f57c-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="5f57c-176">Hvis du vil ha mer informasjon, se [Oversikt over tilbudsforespørsler](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="5f57c-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]