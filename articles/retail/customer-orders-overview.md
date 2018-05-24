---
title: Oversikt over kundeordrer
description: "Dette emnet gir informasjon om kundeordrer i Moderne salgssted for detaljhandel (MPOS). Kundeordrer er også kjent som spesialbestillinger. Emnet inneholder en beskrivelse av relaterte parametere og flyter for transaksjonen."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f46cf7d4df4a8cb0ad1846882292965aa492239b
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="customer-orders-overview"></a><span data-ttu-id="f1c88-105">Oversikt over kundeordrer</span><span class="sxs-lookup"><span data-stu-id="f1c88-105">Customer orders overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1c88-106">Dette emnet gir informasjon om kundeordrer i Moderne salgssted for detaljhandel (MPOS).</span><span class="sxs-lookup"><span data-stu-id="f1c88-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="f1c88-107">Kundeordrer er også kjent som spesialbestillinger.</span><span class="sxs-lookup"><span data-stu-id="f1c88-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="f1c88-108">Emnet inneholder en beskrivelse av relaterte parametere og flyter for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1c88-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="f1c88-109">Omnikanal for detaljhandel gir mulighet for kundeordrer og spesialordrer, eller spesialordrer, for å møte ulike behov.</span><span class="sxs-lookup"><span data-stu-id="f1c88-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="f1c88-110">Her er noen vanlige scenarier:</span><span class="sxs-lookup"><span data-stu-id="f1c88-110">Here are some typical scenarios:</span></span>

-   <span data-ttu-id="f1c88-111">En kunde ønsker produkter som skal leveres til en bestemt adresse på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="f1c88-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
-   <span data-ttu-id="f1c88-112">En kunde ønsker å plukke opp produkter fra en butikk eller lokasjon som er forskjellig fra butikken eller plasseringen der kunden kjøpte disse produktene.</span><span class="sxs-lookup"><span data-stu-id="f1c88-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
-   <span data-ttu-id="f1c88-113">En kunde ønsker noen andre til å plukke opp produkter som kunden har kjøpt.</span><span class="sxs-lookup"><span data-stu-id="f1c88-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="f1c88-114">Forhandlere kan også bruke kundeordrer for å minimere tapt salg som ellers kan forårsakes av lagernedetid, fordi varene kan leveres eller hentes på et annet tidspunkt eller sted.</span><span class="sxs-lookup"><span data-stu-id="f1c88-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="f1c88-115">Definer kundeordrer</span><span class="sxs-lookup"><span data-stu-id="f1c88-115">Set up customer orders</span></span>
<span data-ttu-id="f1c88-116">Her er noen av parameterne som kan angis på siden **Parametere for detaljhandel** for å definere hvordan kundeordrer er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="f1c88-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

-   <span data-ttu-id="f1c88-117">**Standard innbetalingsprosent** – Angi beløpet som kunden må betale som et innskudd før en ordre kan bekreftes.</span><span class="sxs-lookup"><span data-stu-id="f1c88-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="f1c88-118">Standard innbetalingsbeløp beregnes som en prosentdel av ordreverdien.</span><span class="sxs-lookup"><span data-stu-id="f1c88-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="f1c88-119">Avhengig av rettigheter kan en butikkmedarbeider kanskje overstyre beløpet ved hjelp av **Overstyring av innbetaling**.</span><span class="sxs-lookup"><span data-stu-id="f1c88-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
-   <span data-ttu-id="f1c88-120">**Prosent for annulleringsgebyr** – Hvis et gebyr skal brukes når en kundebestilling annulleres, angir du beløpet for gebyret.</span><span class="sxs-lookup"><span data-stu-id="f1c88-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
-   <span data-ttu-id="f1c88-121">**Kode for annulleringsgebyr** – Hvis et gebyr skal brukes når en kundebestilling annulleres, vises dette gebyret under en gebyrkode i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="f1c88-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="f1c88-122">Bruk denne parameteren til å definere koden for annulleringsgebyr.</span><span class="sxs-lookup"><span data-stu-id="f1c88-122">Use this parameter to define the cancellation charge code.</span></span>
-   <span data-ttu-id="f1c88-123">**Kode for forsendelsesgebyr** – Forhandlere kan belaste en ekstra avgift for forsendelse av varer til en kunde.</span><span class="sxs-lookup"><span data-stu-id="f1c88-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="f1c88-124">Beløpet for forsendelsesgebyret vises under en gebyrkode i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="f1c88-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="f1c88-125">Bruk denne parameteren til å tilordne koden for forsendelsesgebyr til forsendelsegebyret på kundeordren.</span><span class="sxs-lookup"><span data-stu-id="f1c88-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
-   <span data-ttu-id="f1c88-126">**Refundering av forsendelseskostnader** – Angi om forsendelseskostnadene som er knyttet til en kundeordre, kan refunderes.</span><span class="sxs-lookup"><span data-stu-id="f1c88-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
-   <span data-ttu-id="f1c88-127">**Maksimumsbeløp uten godkjenning** – Hvis forsendelseskostnader kan refunderes, angir du maksimumsbeløpet for refundereringer av forsendelseskostnader på tvers av returordrer.</span><span class="sxs-lookup"><span data-stu-id="f1c88-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="f1c88-128">Hvis dette beløpet overstiges, er lederoverstyring nødvendig for å fortsette med refunderingen.</span><span class="sxs-lookup"><span data-stu-id="f1c88-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="f1c88-129">En refundering av forsendelseskostnader kan overskride beløpet som opprinnelig ble betalt, i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="f1c88-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>
    -   <span data-ttu-id="f1c88-130">Gebyrer brukes på nivået til salgsordrehodet, og når et antall av en produktserie returneres, kan ikke maksimal refundering av forsendelseskostnader som er tillatt for produktene og antallet, bestemmes på en måte som passer for alle detaljkunder.</span><span class="sxs-lookup"><span data-stu-id="f1c88-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    -   <span data-ttu-id="f1c88-131">Forsendelseskostnader påløpes for hver forekomst av levering.</span><span class="sxs-lookup"><span data-stu-id="f1c88-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="f1c88-132">Hvis en kunde returnerer varer flere ganger, og forhandlerens policy angir at forhandleren skal betale returgebyrene, blir returgebyrene større enn de faktiske forsendelseskostnadene.</span><span class="sxs-lookup"><span data-stu-id="f1c88-132">If a customer returns products multiple times, and the retailer’s policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="f1c88-133">Transaksjonsflyt for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="f1c88-133">Transaction flow for customer orders</span></span>
### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="f1c88-134">Opprett en kundeordre i moderne salgssted for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="f1c88-134">Create a customer order in Retail Modern POS</span></span>

1.  <span data-ttu-id="f1c88-135">Legg til en kunde i transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1c88-135">Add a customer to the transaction.</span></span>
2.  <span data-ttu-id="f1c88-136">Legg til produkter i handlevognen.</span><span class="sxs-lookup"><span data-stu-id="f1c88-136">Add products to the cart.</span></span>
3.  <span data-ttu-id="f1c88-137">Klikk **Opprett kundeordre**, og velg deretter ordretypen.</span><span class="sxs-lookup"><span data-stu-id="f1c88-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="f1c88-138">Ordretypen kan være enten **kundeordre** eller **tilbud**.</span><span class="sxs-lookup"><span data-stu-id="f1c88-138">The order type can be either **Customer order** or **Quote**.</span></span>
4.  <span data-ttu-id="f1c88-139">Klikk **Valgt for forsendelse** eller **Send alle** for å levere produktene til en adresse i kundekontoen, angi ønsket forsendelsesdato, og angi forsendelseskostnader.</span><span class="sxs-lookup"><span data-stu-id="f1c88-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5.  <span data-ttu-id="f1c88-140">Klikk **Valgt for plukking** eller **Plukk alle** for å velge produkter som plukkes fra det gjeldende lageret eller et annet lager på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="f1c88-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6.  <span data-ttu-id="f1c88-141">Samle innbetalingsbeløpet, hvis det kreves et depositum.</span><span class="sxs-lookup"><span data-stu-id="f1c88-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="f1c88-142">Rediger en eksisterende kundeordre</span><span class="sxs-lookup"><span data-stu-id="f1c88-142">Edit an existing customer order</span></span>

1.  <span data-ttu-id="f1c88-143">Klikk **Finn en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="f1c88-143">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="f1c88-144">Finn og velg ordren for å redigere.</span><span class="sxs-lookup"><span data-stu-id="f1c88-144">Find and select the order to edit.</span></span> <span data-ttu-id="f1c88-145">Klikk **Rediger** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="f1c88-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="f1c88-146">Hent en ordre</span><span class="sxs-lookup"><span data-stu-id="f1c88-146">Pick up an order</span></span>

1.  <span data-ttu-id="f1c88-147">Klikk **Finn en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="f1c88-147">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="f1c88-148">Velg ordren som skal hentes.</span><span class="sxs-lookup"><span data-stu-id="f1c88-148">Select the order to pick up.</span></span> <span data-ttu-id="f1c88-149">Klikk **Plukk og pakking** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="f1c88-149">At the bottom of the page, click **Picking and packing**.</span></span>
3.  <span data-ttu-id="f1c88-150">Klikk **Plukk**.</span><span class="sxs-lookup"><span data-stu-id="f1c88-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="f1c88-151">Annullere en ordre</span><span class="sxs-lookup"><span data-stu-id="f1c88-151">Cancel an order</span></span>

1.  <span data-ttu-id="f1c88-152">Klikk **Finn en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="f1c88-152">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="f1c88-153">Velg ordren som skal annulleres.</span><span class="sxs-lookup"><span data-stu-id="f1c88-153">Select the order to cancel.</span></span> <span data-ttu-id="f1c88-154">Klikk **Avbryt** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="f1c88-154">At the bottom of the page, click **Cancel**.</span></span>

#### <a name="create-a-return-order"></a><span data-ttu-id="f1c88-155">Opprette en returordre</span><span class="sxs-lookup"><span data-stu-id="f1c88-155">Create a return order</span></span>

1.  <span data-ttu-id="f1c88-156">Klikk **Finn en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="f1c88-156">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="f1c88-157">Velg ordren som skal returneres, velg fakturaen for ordren, og velg produktlinjen for varen som skal returneres.</span><span class="sxs-lookup"><span data-stu-id="f1c88-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3.  <span data-ttu-id="f1c88-158">Klikk **Returordre** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="f1c88-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="f1c88-159">Asynkron transaksjonsflyt for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="f1c88-159">Asynchronous transaction flow for customer orders</span></span>
<span data-ttu-id="f1c88-160">Kundeordrer kan opprettes fra salgssted-klienten i synkron eller asynkron modus.</span><span class="sxs-lookup"><span data-stu-id="f1c88-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="f1c88-161">La kundeordrer opprettes i asynkron modus</span><span class="sxs-lookup"><span data-stu-id="f1c88-161">Enable customer orders to be created in asynchronous mode</span></span>

1.  <span data-ttu-id="f1c88-162">Klikk **Retail** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofil** &gt; **Funksjonalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="f1c88-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2.  <span data-ttu-id="f1c88-163">På **Generelt**-hurtigfanen angir du **Opprett kundeordre i asynkron modus** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f1c88-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="f1c88-164">Når alternativet **Opprett kundeordre i asynkron modus** er satt til **Ja**, opprettes alltid kundeordrer i asynkron modus, selv om RTS er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f1c88-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="f1c88-165">Hvis du setter dette alternativet til **Nei**, opprettes alltid kundeordrer i synkron modus ved hjelp av RTS.</span><span class="sxs-lookup"><span data-stu-id="f1c88-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="f1c88-166">Når det opprettes kundeordrer i asynkron modus, hentes og settes de inn i Retail ved hentejobber (P-jobber).</span><span class="sxs-lookup"><span data-stu-id="f1c88-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="f1c88-167">De tilsvarende salgsordrene opprettes i Retail når **Synkroniser ordrer** kjøres manuelt eller via en satsvis prosess.</span><span class="sxs-lookup"><span data-stu-id="f1c88-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f1c88-168">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f1c88-168">Additional resources</span></span>
--------

[<span data-ttu-id="f1c88-169">Hybride kundeordrer</span><span class="sxs-lookup"><span data-stu-id="f1c88-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)




