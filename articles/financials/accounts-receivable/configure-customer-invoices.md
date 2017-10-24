---
title: Opprette en kundefaktura
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="a6aa5-102">Opprette en kundefaktura</span><span class="sxs-lookup"><span data-stu-id="a6aa5-102">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a6aa5-103">En **kundefaktura for en salgsordre** er en regning som er knyttet til et salg, og som en organisasjon gir til en kunde.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-103">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="a6aa5-104">Denne typen kundefaktura opprettes basert på en salgsordre, som inneholder ordrelinjer og varenumre.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-104">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="a6aa5-105">Varenumrene er spesifisert og postert i finans.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-105">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="a6aa5-106">Underfinansjournaloppføringer er ikke tilgjengelig for en kundefaktura for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-106">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="a6aa5-107">Hvis du vil ha mer informasjon, kan du se [Opprette salgsordrefakturaer](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="a6aa5-107">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="a6aa5-108">En **fritekstfaktura** er ikke relatert til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-108">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="a6aa5-109">Den inneholder ordrelinjer som omfatter finanskontoer, fritekstbeskrivelser og et salgsbeløp som du angir.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-109">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="a6aa5-110">Du kan ikke legge inn et varenummer i denne fakturatypen.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-110">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="a6aa5-111">Du må legge inn riktige mva-opplysninger.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-111">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="a6aa5-112">En hovedkonto for salg er angitt i hver fakturalinje, som du kan distribuere til flere finanskontoer ved å klikke **Fordel beløp** på siden **Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-112">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="a6aa5-113">I tillegg posteres kundesaldoen til samlekontoen fra posteringsprofilen som brukes for fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-113">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="a6aa5-114">Du finner mer informasjon under: </span><span class="sxs-lookup"><span data-stu-id="a6aa5-114">For more information see:</span></span>

[<span data-ttu-id="a6aa5-115">Opprette en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="a6aa5-115">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="a6aa5-116">Opprette en mal for fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="a6aa5-116">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="a6aa5-117">Tilordne en mal for fritekstfaktura til en kunde</span><span class="sxs-lookup"><span data-stu-id="a6aa5-117">Assign a free text invoice tempate to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="a6aa5-118">Generere og postere gjentakende fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="a6aa5-118">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="a6aa5-119">En **proformafaktura** er en faktura som er klargjort som et estimat av de faktiske fakturabeløpene før fakturaen posteres.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-119">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="a6aa5-120">Du kan skrive ut en proformafaktura for en kundefaktura for en salgsordre eller for en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-120">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="a6aa5-121">Postere og skrive ut individuelle kundefakturaer som er basert på salgsordrer</span><span class="sxs-lookup"><span data-stu-id="a6aa5-121">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="a6aa5-122">Bruk denne fremgangsmåten til å opprette en faktura som er basert på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-122">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="a6aa5-123">Du kan gjøre dette hvis du beslutter å fakturere kunden før du leverer varene eller tjenestene.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-123">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="a6aa5-124">Når du posterer en faktura, oppdateres **Fakturarest**-antallet for hver vare med totalantallet som er fakturert fra den valgte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-124">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="a6aa5-125">Hvis både **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på salgsorden er 0 (null), endres statusen for salgsorden til **Fakturert**.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-125">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="a6aa5-126">Hvis **Fakturarest**-antallet ikke er 0 (null), endres ikke statusen for salgsordren, og flere fakturaer kan registreres på den.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-126">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="a6aa5-127">Du kan vise statusen for salgsordrene på listesiden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-127">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="a6aa5-128">Bruk listesiden **Åpne kundefakturaer** til å vise fakturaene du har postert.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-128">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="a6aa5-129">Postere og skrive ut individuelle kundefakturaer som er basert på følgesedler og datoen</span><span class="sxs-lookup"><span data-stu-id="a6aa5-129">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="a6aa5-130">Bruk denne fremgangsmåten når én eller flere følgesedler er postert for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-130">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="a6aa5-131">Kundefakturaen er basert på disse følgesedlene og gjenspeiler antallet i dem.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-131">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="a6aa5-132">Finansinformasjonen for fakturaen er basert på informasjonen du angir når du posterer fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-132">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="a6aa5-133">Du kan opprette en kundefaktura som er basert på følgeseddellinjevarene som er levert til nå, selv om ikke alle varene i en bestemt salgsordre er levert ennå.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-133">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="a6aa5-134">Du kan for eksempel gjøre dette hvis den juridiske enheten din sender ut én faktura per kunde per måned som dekker alle forsendelser du sender i løpet av den måneden.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-134">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="a6aa5-135">Hver følgeseddel representerer en delvis eller komplett forsendelse av varene i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-135">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="a6aa5-136">Når du posterer fakturaen, oppdateres **Fakturarest**-antallet for hver vare med totalantallet som er levert for de valgte følgesedlene.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-136">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="a6aa5-137">Hvis både **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på salgsorden er 0 (null), endres statusen for salgsorden til **Fakturert**.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-137">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="a6aa5-138">Hvis **Fakturarest**-antallet ikke er 0 (null), endres ikke statusen for salgsordren, og flere fakturaer kan registreres på den.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-138">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="a6aa5-139">Lagertransaksjoner oppdateres med fakturanummeret, og statusen i **Linjestatus**-feltet på salgsordren endres til **Fakturert**.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-139">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="a6aa5-140">Vis statusen for salgsordrene på listesiden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-140">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="a6aa5-141">Konsolidere salgsordrer eller følgesedler for postering</span><span class="sxs-lookup"><span data-stu-id="a6aa5-141">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="a6aa5-142">Bruk denne fremgangsmåten når én eller flere salgsordrer er klare til fakturering, og du vil konsolidere dem i én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-142">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="a6aa5-143">Du kan velge flere fakturaer på **Salgsordre**-listesiden og deretter bruke **Generer fakturaer** for å konsolidere dem.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-143">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="a6aa5-144">På siden **Postering av faktura** kan du endre innstillingen **Samleordre** for å summere etter ordrenummer (der det finnes flere følgesedler for én enkelt ordre) eller etter fakturakonto (der det er flere salgsordrer for én enkelt fakturakonto).</span><span class="sxs-lookup"><span data-stu-id="a6aa5-144">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="a6aa5-145">Bruk knappen **Ordne** for å konsolidere salgsordrer til enkeltfakturaer basert på **Samleordre**-innstillingene.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-145">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="a6aa5-146">Tilleggsinnstillinger som endrer posteringsvirkemåten</span><span class="sxs-lookup"><span data-stu-id="a6aa5-146">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="a6aa5-147">Følgende felt endrer virkemåten for posteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-147">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6aa5-148">Felt</span><span class="sxs-lookup"><span data-stu-id="a6aa5-148">Field</span></span></th>
<th><span data-ttu-id="a6aa5-149">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a6aa5-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a6aa5-150">Antall</span><span class="sxs-lookup"><span data-stu-id="a6aa5-150">Quantity</span></span></td>
<td><span data-ttu-id="a6aa5-151">Velg antallsinformasjonen som dokumentposteringen skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-151">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="a6aa5-152">Alternativene som er tilgjengelige, varierer avhengig av typen dokument du posterer, for eksempel en følgeseddel eller en faktura.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-152">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="a6aa5-153"><strong>Lever nå</strong> – Velg alle antall som er angitt i feltet <strong>Lever nå</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-153"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="a6aa5-154">Bruk dette alternativet til å bekrefte eller levere en delordre.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-154">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="a6aa5-155"><strong>Plukket</strong> – Velg alle antall som er plukket.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-155"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="a6aa5-156"><strong>Alle</strong> – Velg alle antall på salgsordren som ennå ikke er oppdatert med den gjeldende dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-156"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="a6aa5-157"><strong>Følgeseddel</strong> – Velg alle antall som er blitt oppdatert av en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-157"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="a6aa5-158"><strong>Plukket antall og ikke-lagerførte produkter</strong> – Velg alle antall som er plukket og alle produktantall som ikke er lagerført.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-158"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aa5-159">Posterer</span><span class="sxs-lookup"><span data-stu-id="a6aa5-159">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="a6aa5-160">Velg dette alternativet for å journalføre salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-160">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="a6aa5-161">Fjern merket for å skrive ut en proformasalgsordre.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-161">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="a6aa5-162"><strong>Obs!</strong> Hvis du har gjort en avtale for en betalingsplan, blir ikke betalingsplanen vist på proformasalgsordren.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-162"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="a6aa5-163">Betalingsplaner vises bare på faktiske salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-163">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aa5-164">Senere valg</span><span class="sxs-lookup"><span data-stu-id="a6aa5-164">Late selection</span></span></td>
<td><span data-ttu-id="a6aa5-165">Velg dette alternativet hvis du vil bruke spørringen senere.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-165">Select this option to apply the selected query later.</span></span> <span data-ttu-id="a6aa5-166">Dette alternativet brukes for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-166">This option is used for batch jobs.</span></span> <span data-ttu-id="a6aa5-167">Spørringen kjøres når den satsvise jobben kjøres.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-167">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aa5-168">Reduser antall</span><span class="sxs-lookup"><span data-stu-id="a6aa5-168">Reduce quantity</span></span></td>
<td><span data-ttu-id="a6aa5-169">Velg dette alternativet for å automatisk redusere det leverte antallet når dokumentet posteres, slik at det leverte antallet er lik det tilgjengelige lageret.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-169">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aa5-170">Skriv ut</span><span class="sxs-lookup"><span data-stu-id="a6aa5-170">Print</span></span></td>
<td><span data-ttu-id="a6aa5-171">Velg når dokumenter skal skrives ut:</span><span class="sxs-lookup"><span data-stu-id="a6aa5-171">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="a6aa5-172"><strong>Gjeldende</strong> – Skriv ut dokumenter etter at hver faktura er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-172"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="a6aa5-173"><strong>Etter</strong> – Skriv ut dokumenter når alle fakturaene er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-173"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="a6aa5-174">
<strong>Obs!</strong> <strong>Skriv ut</strong>-feltet er bare tilgjengelig hvis du velger <strong>Skriv ut faktura</strong>, <strong>Skriv ut bekreftelse</strong>, <strong>Skriv ut plukkliste</strong> eller <strong>Skriv ut følgeseddel</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-174">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="a6aa5-175">På siden <strong>Skjemasortering</strong> definerer du at informasjonen skal sorteres etter fakturakonto i systemet.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-175">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="a6aa5-176">Du kan deretter velge <strong>Etter</strong> for å skrive ut dokumentene i et parti som sorteres etter fakturakonto.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-176">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="a6aa5-177">Hvis ikke skrives dokumentene ut før behandlingen er fullført, og dokumentene sorteres ikke i rekkefølgen som er angitt på siden <strong>Skjemasortering</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-177">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aa5-178">Skriv ut faktura</span><span class="sxs-lookup"><span data-stu-id="a6aa5-178">Print invoice</span></span></td>
<td><span data-ttu-id="a6aa5-179">Merk av i denne boksen for å skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-179">Select this option to print the invoice.</span></span> <span data-ttu-id="a6aa5-180">Hvis dette alternativet er deaktivert, kan du postere en faktura uten å skrive ut den.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-180">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aa5-181">Send e-post</span><span class="sxs-lookup"><span data-stu-id="a6aa5-181">Send e-mail</span></span></td>
<td><span data-ttu-id="a6aa5-182">Velg dette alternativet for å sende fakturaen for en salgsordre til kunden som et e-postvedlegg når fakturaen er postert.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-182">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="a6aa5-183">Vedlegg sendes som PDF- og XML-filer.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-183">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="a6aa5-184">Dette alternativet er bare tilgjengelig hvis du velger alternativet <strong>Aktiver CFD (elektroniske fakturaer)</strong> på siden <strong>Parametere for elektroniske fakturaer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-184">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="a6aa5-185"><strong>Obs!</strong> (MEX) Denne kontrollen er bare tilgjengelig for juridiske enheter med primæradresse i Mexico.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-185"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aa5-186">Bruk utskriftsbehandlingsmål</span><span class="sxs-lookup"><span data-stu-id="a6aa5-186">Use print management destination</span></span></td>
<td><span data-ttu-id="a6aa5-187">Velg dette alternativet for å bruke utskriftsinnstillingene som er angitt for transaksjonen, dokumentet eller modulen på siden <strong>Oppsett for utskriftsbehandling</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-187">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aa5-188">Kontroller kredittgrense</span><span class="sxs-lookup"><span data-stu-id="a6aa5-188">Check credit limit</span></span></td>
<td><span data-ttu-id="a6aa5-189">Velg informasjonen som skal analyseres når en kredittgrensekontroll utføres.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-189">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="a6aa5-190"><strong>Ingen</strong> - Det er ingen krav til kontroll av kredittgrense.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-190"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="a6aa5-191"><strong>Saldo</strong> - Kredittgrensen kontrolleres mot kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-191"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="a6aa5-192"><strong>Saldo + følgeseddel eller produktkvittering</strong> – Kredittgrensen kontrolleres mot kundesaldoen og leveranser.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-192"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="a6aa5-193"><strong>Saldo+Alt</strong> - Kredittgrensen kontrolleres mot kundesaldoen, leveranser og åpne ordrer.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-193"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aa5-194">Kreditrettelse</span><span class="sxs-lookup"><span data-stu-id="a6aa5-194">Credit correction</span></span></td>
<td><span data-ttu-id="a6aa5-195">Velg dette alternativet for å vise kreditnotaen som debet i bilagstransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-195">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aa5-196">Kreditrestantall</span><span class="sxs-lookup"><span data-stu-id="a6aa5-196">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="a6aa5-197">Hvis du posterer en kreditnota, velger du dette alternativet for å beholde det resterende antallet på ordren.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-197">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="a6aa5-198">Hvis dette alternativet ikke er valgt, settes det gjenstående antallet til 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a6aa5-198">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aa5-199">Samleoppdatering for</span><span class="sxs-lookup"><span data-stu-id="a6aa5-199">Summary update for</span></span></td>
<td><span data-ttu-id="a6aa5-200">Velg hvordan flere salgsordrer skal summeres:</span><span class="sxs-lookup"><span data-stu-id="a6aa5-200">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="a6aa5-201"><strong>Ingen</strong> – Ikke oppsummer salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-201"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="a6aa5-202">En egen faktura opprettes eksempelvis for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-202">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="a6aa5-203"><strong>Fakturakonto</strong> – Oppsummer alle valgte ordrer i henhold til kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-203"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="a6aa5-204"><strong>Ordre</strong> – Summer et valgt intervall av ordrer, i én angitt ordre.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-204"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="a6aa5-205">Ordrene oppsummeres i henhold til kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-205">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="a6aa5-206">Hvis du velger dette alternativet, må du velge en verdi i feltet <strong>Salgsordre</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-206">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="a6aa5-207"><strong>Automatisk oppsummering</strong> – Hvis samleoppdateringer er angitt på siden <strong>Samleoppdatering</strong>, oppsummeres alle valgte ordrer basert på kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-207"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="a6aa5-208">Hvis det ikke er angitt samleoppdateringer, posteres ordren separat.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-208">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="a6aa5-209"><strong>Følgeseddel</strong> – Summer et valgt intervall av ordrer i én faktura per følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-209"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="a6aa5-210">Dette alternativet er bare tilgjengelig hvis <strong>Følgeseddel</strong> er valgt i <strong>Antall</strong>-feltet.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-210">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






