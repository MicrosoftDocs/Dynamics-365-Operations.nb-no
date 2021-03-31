---
title: Opprette en kundefaktura
description: En **kundefaktura for en salgsordre** er en regning som er knyttet til et salg, og som en organisasjon gir til en kunde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff988fff23611805c2849a63c2aaba74fc255d4c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217584"
---
# <a name="create-a-customer-invoice"></a><span data-ttu-id="19dea-103">Opprette en kundefaktura</span><span class="sxs-lookup"><span data-stu-id="19dea-103">Create a customer invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19dea-104">En **kundefaktura for en salgsordre** er en regning som er knyttet til et salg, og som en organisasjon gir til en kunde.</span><span class="sxs-lookup"><span data-stu-id="19dea-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="19dea-105">Denne typen kundefaktura opprettes basert på en salgsordre, som inneholder ordrelinjer og varenumre.</span><span class="sxs-lookup"><span data-stu-id="19dea-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="19dea-106">Varenumrene er spesifisert og postert i finans.</span><span class="sxs-lookup"><span data-stu-id="19dea-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="19dea-107">Underfinansjournaloppføringer er ikke tilgjengelig for en kundefaktura for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="19dea-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="19dea-108">Hvis du vil ha mer informasjon, kan du se [Opprette salgsordrefakturaer](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="19dea-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="19dea-109">En **fritekstfaktura** er ikke relatert til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="19dea-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="19dea-110">Den inneholder ordrelinjer som omfatter finanskontoer, fritekstbeskrivelser og et salgsbeløp som du angir.</span><span class="sxs-lookup"><span data-stu-id="19dea-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="19dea-111">Du kan ikke legge inn et varenummer i denne fakturatypen.</span><span class="sxs-lookup"><span data-stu-id="19dea-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="19dea-112">Du må legge inn riktige mva-opplysninger.</span><span class="sxs-lookup"><span data-stu-id="19dea-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="19dea-113">En hovedkonto for salg er angitt i hver fakturalinje, som du kan distribuere til flere finanskontoer ved å klikke **Fordel beløp** på siden **Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="19dea-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="19dea-114">I tillegg posteres kundesaldoen til samlekontoen fra posteringsprofilen som brukes for fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="19dea-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="19dea-115">Du finner mer informasjon under: </span><span class="sxs-lookup"><span data-stu-id="19dea-115">For more information see:</span></span>

[<span data-ttu-id="19dea-116">Opprett fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="19dea-116">Create free text invoices</span></span>](../accounts-receivable/create-free-text-invoice-new.md)

[<span data-ttu-id="19dea-117">Opprette en mal for fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="19dea-117">Create a free text invoice template</span></span>](../accounts-receivable/create-free-text-invoice-template-new.md)

[<span data-ttu-id="19dea-118">Tilordne mal for fritekstfaktura til en kunde</span><span class="sxs-lookup"><span data-stu-id="19dea-118">Assign free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="19dea-119">Generere og postere gjentakende fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="19dea-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="19dea-120">En **proformafaktura** er en faktura som er klargjort som et estimat av de faktiske fakturabeløpene før fakturaen posteres.</span><span class="sxs-lookup"><span data-stu-id="19dea-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="19dea-121">Du kan skrive ut en proformafaktura for en kundefaktura for en salgsordre eller for en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="19dea-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="19dea-122">Postere og skrive ut individuelle kundefakturaer som er basert på salgsordrer</span><span class="sxs-lookup"><span data-stu-id="19dea-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="19dea-123">Bruk denne fremgangsmåten til å opprette en faktura som er basert på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="19dea-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="19dea-124">Du kan gjøre dette hvis du beslutter å fakturere kunden før du leverer varene eller tjenestene.</span><span class="sxs-lookup"><span data-stu-id="19dea-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="19dea-125">Når du posterer en faktura, oppdateres **Fakturarest**-antallet for hver vare med totalantallet som er fakturert fra den valgte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="19dea-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="19dea-126">Hvis både **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på salgsorden er 0 (null), endres statusen for salgsorden til **Fakturert**.</span><span class="sxs-lookup"><span data-stu-id="19dea-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="19dea-127">Hvis **Fakturarest**-antallet ikke er 0 (null), endres ikke statusen for salgsordren, og flere fakturaer kan registreres på den.</span><span class="sxs-lookup"><span data-stu-id="19dea-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="19dea-128">Du kan vise statusen for salgsordrene på listesiden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="19dea-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="19dea-129">Bruk listesiden **Åpne kundefakturaer** til å vise fakturaene du har postert.</span><span class="sxs-lookup"><span data-stu-id="19dea-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="19dea-130">Postere og skrive ut individuelle kundefakturaer som er basert på følgesedler og datoen</span><span class="sxs-lookup"><span data-stu-id="19dea-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="19dea-131">Bruk denne fremgangsmåten når én eller flere følgesedler er postert for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="19dea-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="19dea-132">Kundefakturaen er basert på disse følgesedlene og gjenspeiler antallet i dem.</span><span class="sxs-lookup"><span data-stu-id="19dea-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="19dea-133">Finansinformasjonen for fakturaen er basert på informasjonen du angir når du posterer fakturaen.</span><span class="sxs-lookup"><span data-stu-id="19dea-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="19dea-134">Du kan opprette en kundefaktura som er basert på følgeseddellinjevarene som er levert til nå, selv om ikke alle varene i en bestemt salgsordre er levert ennå.</span><span class="sxs-lookup"><span data-stu-id="19dea-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="19dea-135">Du kan for eksempel gjøre dette hvis den juridiske enheten din sender ut én faktura per kunde per måned som dekker alle forsendelser du sender i løpet av den måneden.</span><span class="sxs-lookup"><span data-stu-id="19dea-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="19dea-136">Hver følgeseddel representerer en delvis eller komplett forsendelse av varene i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="19dea-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="19dea-137">Når du posterer fakturaen, oppdateres **Fakturarest**-antallet for hver vare med totalantallet som er levert for de valgte følgesedlene.</span><span class="sxs-lookup"><span data-stu-id="19dea-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="19dea-138">Hvis både **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på salgsorden er 0 (null), endres statusen for salgsorden til **Fakturert**.</span><span class="sxs-lookup"><span data-stu-id="19dea-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="19dea-139">Hvis **Fakturarest**-antallet ikke er 0 (null), endres ikke statusen for salgsordren, og flere fakturaer kan registreres på den.</span><span class="sxs-lookup"><span data-stu-id="19dea-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="19dea-140">Lagertransaksjoner oppdateres med fakturanummeret, og statusen i **Linjestatus**-feltet på salgsordren endres til **Fakturert**.</span><span class="sxs-lookup"><span data-stu-id="19dea-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="19dea-141">Vis statusen for salgsordrene på listesiden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="19dea-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="19dea-142">Konsolidere salgsordrer eller følgesedler for postering</span><span class="sxs-lookup"><span data-stu-id="19dea-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="19dea-143">Bruk denne fremgangsmåten når én eller flere salgsordrer er klare til fakturering, og du vil konsolidere dem i én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="19dea-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="19dea-144">Du kan velge flere fakturaer på **Salgsordre**-listesiden og deretter bruke **Generer fakturaer** for å konsolidere dem.</span><span class="sxs-lookup"><span data-stu-id="19dea-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="19dea-145">På siden **Postering av faktura** kan du endre innstillingen **Samleordre** for å summere etter ordrenummer (der det finnes flere følgesedler for én enkelt ordre) eller etter fakturakonto (der det er flere salgsordrer for én enkelt fakturakonto).</span><span class="sxs-lookup"><span data-stu-id="19dea-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="19dea-146">Bruk knappen **Ordne** for å konsolidere salgsordrer til enkeltfakturaer basert på **Samleordre**-innstillingene.</span><span class="sxs-lookup"><span data-stu-id="19dea-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="19dea-147">Tilleggsinnstillinger som endrer posteringsvirkemåten</span><span class="sxs-lookup"><span data-stu-id="19dea-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="19dea-148">Følgende felt endrer virkemåten for posteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="19dea-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19dea-149">Felt</span><span class="sxs-lookup"><span data-stu-id="19dea-149">Field</span></span></th>
<th><span data-ttu-id="19dea-150">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="19dea-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19dea-151">Antall</span><span class="sxs-lookup"><span data-stu-id="19dea-151">Quantity</span></span></td>
<td><span data-ttu-id="19dea-152">Velg antallsinformasjonen som dokumentposteringen skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="19dea-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="19dea-153">Alternativene som er tilgjengelige, varierer avhengig av typen dokument du posterer, for eksempel en følgeseddel eller en faktura.</span><span class="sxs-lookup"><span data-stu-id="19dea-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="19dea-154"><strong>Lever nå</strong> – Velg alle antall som er angitt i feltet <strong>Lever nå</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="19dea-155">Bruk dette alternativet til å bekrefte eller levere en delordre.</span><span class="sxs-lookup"><span data-stu-id="19dea-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="19dea-156"><strong>Plukket</strong> – Velg alle antall som er plukket.</span><span class="sxs-lookup"><span data-stu-id="19dea-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="19dea-157"><strong>Alle</strong> – Velg alle antall på salgsordren som ennå ikke er oppdatert med den gjeldende dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="19dea-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="19dea-158"><strong>Følgeseddel</strong> – Velg alle antall som er blitt oppdatert av en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="19dea-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="19dea-159"><strong>Plukket antall og ikke-lagerførte produkter</strong> – Velg alle antall som er plukket og alle produktantall som ikke er lagerført.</span><span class="sxs-lookup"><span data-stu-id="19dea-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dea-160">Posterer</span><span class="sxs-lookup"><span data-stu-id="19dea-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="19dea-161">Velg dette alternativet for å journalføre salgsordren.</span><span class="sxs-lookup"><span data-stu-id="19dea-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="19dea-162">Fjern merket for å skrive ut en proformasalgsordre.</span><span class="sxs-lookup"><span data-stu-id="19dea-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="19dea-163"><strong>Obs!</strong> Hvis du har gjort en avtale for en betalingsplan, blir ikke betalingsplanen vist på proformasalgsordren.</span><span class="sxs-lookup"><span data-stu-id="19dea-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="19dea-164">Betalingsplaner vises bare på faktiske salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="19dea-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dea-165">Senere valg</span><span class="sxs-lookup"><span data-stu-id="19dea-165">Late selection</span></span></td>
<td><span data-ttu-id="19dea-166">Velg dette alternativet hvis du vil bruke spørringen senere.</span><span class="sxs-lookup"><span data-stu-id="19dea-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="19dea-167">Dette alternativet brukes for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="19dea-167">This option is used for batch jobs.</span></span> <span data-ttu-id="19dea-168">Spørringen kjøres når den satsvise jobben kjøres.</span><span class="sxs-lookup"><span data-stu-id="19dea-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dea-169">Reduser antall</span><span class="sxs-lookup"><span data-stu-id="19dea-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="19dea-170">Velg dette alternativet for å automatisk redusere det leverte antallet når dokumentet posteres, slik at det leverte antallet er lik det tilgjengelige lageret.</span><span class="sxs-lookup"><span data-stu-id="19dea-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dea-171">Skriv ut</span><span class="sxs-lookup"><span data-stu-id="19dea-171">Print</span></span></td>
<td><span data-ttu-id="19dea-172">Velg når dokumenter skal skrives ut:</span><span class="sxs-lookup"><span data-stu-id="19dea-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="19dea-173"><strong>Gjeldende</strong> – Skriv ut dokumenter etter at hver faktura er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="19dea-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="19dea-174"><strong>Etter</strong> – Skriv ut dokumenter når alle fakturaene er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="19dea-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="19dea-175">
<strong>Obs!</strong> <strong>Skriv ut</strong>-feltet er bare tilgjengelig hvis du velger <strong>Skriv ut faktura</strong>, <strong>Skriv ut bekreftelse</strong>, <strong>Skriv ut plukkliste</strong> eller <strong>Skriv ut følgeseddel</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="19dea-176">På siden <strong>Skjemasortering</strong> definerer du at informasjonen skal sorteres etter fakturakonto i systemet.</span><span class="sxs-lookup"><span data-stu-id="19dea-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="19dea-177">Du kan deretter velge <strong>Etter</strong> for å skrive ut dokumentene i en bunke som sorteres etter fakturakonto.</span><span class="sxs-lookup"><span data-stu-id="19dea-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="19dea-178">Hvis ikke skrives dokumentene ut før behandlingen er fullført, og dokumentene sorteres ikke i rekkefølgen som er angitt på siden <strong>Skjemasortering</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dea-179">Skriv ut faktura</span><span class="sxs-lookup"><span data-stu-id="19dea-179">Print invoice</span></span></td>
<td><span data-ttu-id="19dea-180">Merk av i denne boksen for å skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="19dea-180">Select this option to print the invoice.</span></span> <span data-ttu-id="19dea-181">Hvis dette alternativet er deaktivert, kan du postere en faktura uten å skrive ut den.</span><span class="sxs-lookup"><span data-stu-id="19dea-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dea-182">Send e-post</span><span class="sxs-lookup"><span data-stu-id="19dea-182">Send e-mail</span></span></td>
<td><span data-ttu-id="19dea-183">Velg dette alternativet for å sende fakturaen for en salgsordre til kunden som et e-postvedlegg når fakturaen er postert.</span><span class="sxs-lookup"><span data-stu-id="19dea-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="19dea-184">Vedlegg sendes som PDF- og XML-filer.</span><span class="sxs-lookup"><span data-stu-id="19dea-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="19dea-185">Dette alternativet er bare tilgjengelig hvis du velger alternativet <strong>Aktiver CFD (elektroniske fakturaer)</strong> på siden <strong>Parametere for elektroniske fakturaer</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="19dea-186"><strong>Obs!</strong> (MEX) Denne kontrollen er bare tilgjengelig for juridiske enheter med primæradresse i Mexico.</span><span class="sxs-lookup"><span data-stu-id="19dea-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dea-187">Bruk utskriftsbehandlingsmål</span><span class="sxs-lookup"><span data-stu-id="19dea-187">Use print management destination</span></span></td>
<td><span data-ttu-id="19dea-188">Velg dette alternativet for å bruke utskriftsinnstillingene som er angitt for transaksjonen, dokumentet eller modulen på siden <strong>Oppsett for utskriftsbehandling</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dea-189">Kontroller kredittgrense</span><span class="sxs-lookup"><span data-stu-id="19dea-189">Check credit limit</span></span></td>
<td><span data-ttu-id="19dea-190">Velg informasjonen som skal analyseres når en kredittgrensekontroll utføres.</span><span class="sxs-lookup"><span data-stu-id="19dea-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="19dea-191"><strong>Ingen</strong> - Det er ingen krav til kontroll av kredittgrense.</span><span class="sxs-lookup"><span data-stu-id="19dea-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="19dea-192"><strong>Saldo</strong> - Kredittgrensen kontrolleres mot kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="19dea-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="19dea-193"><strong>Saldo + følgeseddel eller produktkvittering</strong> – Kredittgrensen kontrolleres mot kundesaldoen og leveranser.</span><span class="sxs-lookup"><span data-stu-id="19dea-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="19dea-194"><strong>Saldo+Alt</strong> - Kredittgrensen kontrolleres mot kundesaldoen, leveranser og åpne ordrer.</span><span class="sxs-lookup"><span data-stu-id="19dea-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dea-195">Kreditrettelse</span><span class="sxs-lookup"><span data-stu-id="19dea-195">Credit correction</span></span></td>
<td><span data-ttu-id="19dea-196">Velg dette alternativet for å vise kreditnotaen som debet i bilagstransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="19dea-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dea-197">Kreditrestantall</span><span class="sxs-lookup"><span data-stu-id="19dea-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="19dea-198">Hvis du posterer en kreditnota, velger du dette alternativet for å beholde det resterende antallet på ordren.</span><span class="sxs-lookup"><span data-stu-id="19dea-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="19dea-199">Hvis dette alternativet ikke er valgt, settes det gjenstående antallet til 0 (null).</span><span class="sxs-lookup"><span data-stu-id="19dea-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dea-200">Samleoppdatering for</span><span class="sxs-lookup"><span data-stu-id="19dea-200">Summary update for</span></span></td>
<td><span data-ttu-id="19dea-201">Velg hvordan flere salgsordrer skal summeres:</span><span class="sxs-lookup"><span data-stu-id="19dea-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="19dea-202"><strong>Ingen</strong> – Ikke oppsummer salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="19dea-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="19dea-203">En egen faktura opprettes eksempelvis for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="19dea-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="19dea-204"><strong>Fakturakonto</strong> – Oppsummer alle valgte ordrer i henhold til kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="19dea-205"><strong>Ordre</strong> – Summer et valgt intervall av ordrer, i én angitt ordre.</span><span class="sxs-lookup"><span data-stu-id="19dea-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="19dea-206">Ordrene oppsummeres i henhold til kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="19dea-207">Hvis du velger dette alternativet, må du velge en verdi i feltet <strong>Salgsordre</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="19dea-208"><strong>Automatisk oppsummering</strong> – Hvis samleoppdateringer er angitt på siden <strong>Samleoppdatering</strong>, oppsummeres alle valgte ordrer basert på kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="19dea-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="19dea-209">Hvis det ikke er angitt samleoppdateringer, posteres ordren separat.</span><span class="sxs-lookup"><span data-stu-id="19dea-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="19dea-210"><strong>Følgeseddel</strong> – Summer et valgt intervall av ordrer i én faktura per følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="19dea-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="19dea-211">Dette alternativet er bare tilgjengelig hvis <strong>Følgeseddel</strong> er valgt i <strong>Antall</strong>-feltet.</span><span class="sxs-lookup"><span data-stu-id="19dea-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]