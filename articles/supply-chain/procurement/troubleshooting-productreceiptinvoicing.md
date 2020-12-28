---
title: Feilsøke mottakssedler og fakturering
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med mottakssedler og fakturering.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434833"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="84908-103">Feilsøke mottakssedler og fakturering</span><span class="sxs-lookup"><span data-stu-id="84908-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="84908-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med mottakssedler og fakturering.</span><span class="sxs-lookup"><span data-stu-id="84908-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="84908-105">Jeg kan ikke postere mer enn én faktura for en bestillingslinje som har kategoribaserte varer.</span><span class="sxs-lookup"><span data-stu-id="84908-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="84908-106">Et antall er obligatorisk hvis du vil postere fakturaer.</span><span class="sxs-lookup"><span data-stu-id="84908-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="84908-107">Hvis hele antallet av en linje er fakturert bare for et delvis beløp, kan du fakturere restbeløpet på en annen faktura.</span><span class="sxs-lookup"><span data-stu-id="84908-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="84908-108">Jeg får feilmeldingen "Objektreferanse er ikke angitt" under bestillingsbekreftelsen, eller unntaket "Målet forårsaket et unntak under aktivering" oppstår ved postering av leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="84908-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="84908-109">Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.</span><span class="sxs-lookup"><span data-stu-id="84908-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="84908-110">Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**.</span><span class="sxs-lookup"><span data-stu-id="84908-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="84908-111">Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="84908-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="84908-112">Jeg får ikke til å konsolidere flere produktkvitteringer til én bestilling.</span><span class="sxs-lookup"><span data-stu-id="84908-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="84908-113">Du kan ikke konsolidere flere produktkvitteringer i én enkelt bestilling hvis de ulike produktkvitteringslinjene har forskjellige regnskapsdatoer.</span><span class="sxs-lookup"><span data-stu-id="84908-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="84908-114">I tidligere versjoner av Microsoft Dynamics 365 Supply Chain Management var konsolidering tillatt i denne situasjonen.</span><span class="sxs-lookup"><span data-stu-id="84908-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="84908-115">Dette er imidlertid utsatt for feil.</span><span class="sxs-lookup"><span data-stu-id="84908-115">However, the practice is prone to error.</span></span> <span data-ttu-id="84908-116">Regnskapsdatoen på bestillingslinjene som opprettes, må ikke være forskjellige fra regnskapsdatoen på produktkvitteringslinjene som disse bestillingslinjene ble opprettet fra.</span><span class="sxs-lookup"><span data-stu-id="84908-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="84908-117">(Regnskapsdatoen i bestillingslinjene samsvarer med regnskapsdatoen i bestillingshodet.) Derfor er ikke konsolideringen av flere produktkvitteringer i én enkelt bestillinger tillatt.</span><span class="sxs-lookup"><span data-stu-id="84908-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="84908-118">Regnskapsdatoen brukes for eksempel for budsjettreservasjoner og disposisjoner.</span><span class="sxs-lookup"><span data-stu-id="84908-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="84908-119">Derfor bør den holdes i løpet av overgangen fra produktkvittering til bestilling.</span><span class="sxs-lookup"><span data-stu-id="84908-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="84908-120">Når produktkvitteringer annulleres, kan transaksjoner posteres til en suspendert finanskonto.</span><span class="sxs-lookup"><span data-stu-id="84908-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="84908-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="84908-121">Issue description</span></span>

<span data-ttu-id="84908-122">Hvis en produktkvittering avlyses, tillater systemet at transaksjoner posteres til utestengte finanskontoer, selv om hovedkontoene er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="84908-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="84908-123">Reprodusere problemet</span><span class="sxs-lookup"><span data-stu-id="84908-123">Reproduce the issue</span></span>

<span data-ttu-id="84908-124">Følgende prosedyre viser én måte å reprodusere problemet på.</span><span class="sxs-lookup"><span data-stu-id="84908-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="84908-125">På siden for **Leverandørparametere**, i kategorien **Generelt**, må du kontrollere at alternativet **Poster produktkvittering i finans** er satt til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="84908-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="84908-126">Opprett en bestilling, og legg til en ordrelinje som har et antall på *1000* for et produkt.</span><span class="sxs-lookup"><span data-stu-id="84908-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="84908-127">Bekreft bestillingen.</span><span class="sxs-lookup"><span data-stu-id="84908-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="84908-128">Poster produktkvitteringen, og sjekk bilagene.</span><span class="sxs-lookup"><span data-stu-id="84908-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="84908-129">Stopp de aktuelle hovedkontoene, *200140* og *140200*.</span><span class="sxs-lookup"><span data-stu-id="84908-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="84908-130">Avbryt den posterte produktkvitteringen.</span><span class="sxs-lookup"><span data-stu-id="84908-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="84908-131">Legg merke til at transaksjoner kan posteres til de suspenderte finanskontoene.</span><span class="sxs-lookup"><span data-stu-id="84908-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="84908-132">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="84908-132">Issue resolution</span></span>

<span data-ttu-id="84908-133">Transaksjoner kan posteres til de suspenderte finanskontoene når produktkvitteringer avbrytes, fordi denne virkemåten sørger for riktige posteringer.</span><span class="sxs-lookup"><span data-stu-id="84908-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="84908-134">Et bilagsnummer for produktkvitteringen forbrukes selv om det ikke genereres et økonomisk bilag under produktkvitteringen.</span><span class="sxs-lookup"><span data-stu-id="84908-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="84908-135">Hvis alternativet **Gjeldsavsetning på produktkvittering** er satt til *Nei* for varemodellgruppen, vil ingen posteringer til økonomimodulen forekomme.</span><span class="sxs-lookup"><span data-stu-id="84908-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="84908-136">En fysisk hendelse vil imidlertid bli registrert for regnskapsformål i en underfinans, og denne hendelsen krever et bilagsnummer.</span><span class="sxs-lookup"><span data-stu-id="84908-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="84908-137">Dette bilagsnummeret er bilagsnummeret som det refereres til i lagertransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="84908-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="84908-138">Vi anbefaler at du setter alternativet **Gjeldsavsetning på produktkvittering** til *Ja*, som beskrevet i følgende blogginnlegg: [Poster tilleggskostnader på tidspunktet for produktkvitteringen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="84908-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="84908-139">Innstillingen Postere i belastningskonto i finans er ikke aktivert.</span><span class="sxs-lookup"><span data-stu-id="84908-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="84908-140">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="84908-140">Issue description</span></span>

<span data-ttu-id="84908-141">Dette problemet oppstår når en bestilling faktureres hvis alternativet **Postere i belastningskonto i finans** er satt til *Ja* i kategorien **Faktura** på siden **Leverandørparametere**.</span><span class="sxs-lookup"><span data-stu-id="84908-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="84908-142">Reprodusere problemet</span><span class="sxs-lookup"><span data-stu-id="84908-142">Reproduce the issue</span></span>

<span data-ttu-id="84908-143">Følgende prosedyre viser én måte å reprodusere problemet på.</span><span class="sxs-lookup"><span data-stu-id="84908-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="84908-144">Gå til **Leverandører \> Oppsett \> Leverandørparametere**.</span><span class="sxs-lookup"><span data-stu-id="84908-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="84908-145">I kategorien **Faktura** setter du alternativet **Postere i belastningskonto i finans** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="84908-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="84908-146">Gå til **Lagerstyring \> Oppsett \> Postering \> Postering**.</span><span class="sxs-lookup"><span data-stu-id="84908-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="84908-147">I kategorien **Bestilling** må du kontrollere at du har slettet alle linjene i innkjøpsutgiften for produktet.</span><span class="sxs-lookup"><span data-stu-id="84908-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="84908-148">Gå til **Leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="84908-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="84908-149">Opprett en bestilling.</span><span class="sxs-lookup"><span data-stu-id="84908-149">Create a purchase order.</span></span> <span data-ttu-id="84908-150">I feltet **Leverandørkonto** velger du *1001 Acme-kontorutstyr*.</span><span class="sxs-lookup"><span data-stu-id="84908-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="84908-151">Legg til en bestillingslinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="84908-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="84908-152">**Varenummer:** *D0011 laserprojektor*</span><span class="sxs-lookup"><span data-stu-id="84908-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="84908-153">**Område:** *1*</span><span class="sxs-lookup"><span data-stu-id="84908-153">**Site:** *1*</span></span>
    - <span data-ttu-id="84908-154">**Lager:** *11*</span><span class="sxs-lookup"><span data-stu-id="84908-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="84908-155">**Antall:** *4*</span><span class="sxs-lookup"><span data-stu-id="84908-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="84908-156">I handlingsruten i kategorien **Bestilling** i gruppen **Handling** velger du **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="84908-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="84908-157">I handlingsruten i kategorien **Motta** i gruppen **Generer** velger du **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="84908-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="84908-158">I dialogboksen **Poster mottaksseddel**, i feltet **Produktkvittering**, angir du et vilkårlig nummer og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="84908-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="84908-159">I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="84908-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="84908-160">I **Nummer**-feltet angir du et tilfeldig nummer som fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="84908-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="84908-161">Oppdater samsvarsstatusen, og poster.</span><span class="sxs-lookup"><span data-stu-id="84908-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="84908-162">Legg merke til at du nå får følgende feilmelding når du genererer en faktura fra en bestilling: "Kontonummeret for transaksjonstypen Innkjøpsutgift for produkt finnes ikke".</span><span class="sxs-lookup"><span data-stu-id="84908-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="84908-163">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="84908-163">Issue resolution</span></span>

<span data-ttu-id="84908-164">Dette avhenger av parameterinnstillingene for fakturaer og fakturagrupper.</span><span class="sxs-lookup"><span data-stu-id="84908-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="84908-165">Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Regnskap for innkjøpstillegg og lageravvik](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="84908-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
