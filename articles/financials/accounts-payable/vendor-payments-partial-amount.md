---
title: "Leverandørbetalinger for et delbeløp"
description: "Du kan eventuelt opprette en betaling til en leverandør som er mindre enn beløpet i en faktura. Denne artikkelen beskriver de ulike alternativene for håndtering av dette. Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aeef806980665c523f10b373f7662ecf509a8172
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="bf6a1-105">Leverandørbetalinger for et delbeløp</span><span class="sxs-lookup"><span data-stu-id="bf6a1-105">Vendor payments for a partial amount</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bf6a1-106">Du kan eventuelt opprette en betaling til en leverandør som er mindre enn beløpet i en faktura.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-106">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="bf6a1-107">Denne artikkelen beskriver de ulike alternativene for håndtering av dette.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="bf6a1-108">Hvilke alternativer som er tilgjengelige, avhenger av dine forretningsbehov og konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-108">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="bf6a1-109">Kontantrabattbeløp</span><span class="sxs-lookup"><span data-stu-id="bf6a1-109">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="bf6a1-110">En leverandør kan tilby deg en kontantrabatt for å betale en faktura før forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-110">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="bf6a1-111">Du kan for eksempel registrere en faktura for 100,00 som angir en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-111">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="bf6a1-112">Forfallsdatoen er om 30 dager.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-112">The due date terms are 30 days.</span></span> <span data-ttu-id="bf6a1-113">Hvis et betalingsforslag bruker kontantrabatten som et kriterium for å velge en faktura, og hvis forslaget kjøres på eller før kontantrabattdatoen, velges fakturaen for betaling, og betalingen opprettes for 98,00.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-113">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="bf6a1-114">En kontantrabatt kan også brukes for en engangsbetaling som ble opprettet manuelt.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-114">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="bf6a1-115">Delbetalinger med kontantrabatter</span><span class="sxs-lookup"><span data-stu-id="bf6a1-115">Partial payments with cash discounts</span></span>
<span data-ttu-id="bf6a1-116">Når du foretar en delbetaling, kan det hende at du har tenkt å lage en ekstra delbetaling for å utligne fullt ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-116">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="bf6a1-117">Hvis tar en kontantrabatt for en delbetaling, må du angi alternativet <strong>Beregn kontantrabatter for delvise betalinger **til**Ja</strong> på siden <strong>Leverandørparametere</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-117">To take a cash discount for a partial payment, you must set the <strong>Calculate cash discounts for partial payments **option to **Yes</strong> on the <strong>Account payable parameters</strong> page.</span></span> 

<span data-ttu-id="bf6a1-118">Du får for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager etter at den utstedes.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-118">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="bf6a1-119">Det posteres en faktura på 100,00.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-119">An invoice is posted for 100.00.</span></span> <span data-ttu-id="bf6a1-120">Hvis du foretar en betaling på 49,00 innen 10 dager, angir du et debetbeløp i 49,00 i en betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-120">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="bf6a1-121">Når du utligner delbetalingen delvis på siden **Utlign åpne transaksjoner**, vises **1,00** i feltet **Kontantrabattbeløp som skal brukes**.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-121">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="bf6a1-122">Hvis du angir en delbetaling og lar det fullstendige fakturabeløpet stå i feltet **Beløp som skal utlignes**, beregnes feltet **Kontantrabattbeløp som skal brukes** automatisk på nytt når du posterer transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-122">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="bf6a1-123">Kreditnotaer med kontantrabatter</span><span class="sxs-lookup"><span data-stu-id="bf6a1-123">Credit notes with cash discounts</span></span>
<span data-ttu-id="bf6a1-124">Du kan returnere noen av elementene på en faktura og motta en kreditnota.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-124">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="bf6a1-125">Hvis en kontantrabatt ble brukt på den opprinnelige fakturaen, kan du trekke fra verdien av rabatten og få en refundering for riktig beløp.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-125">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="bf6a1-126">Hvis alternativet <strong>Beregn kontantrabatter for kreditnotaer **er satt til **Ja</strong> på siden <strong>Leverandørparametere</strong>, beregnes rabatten automatisk for kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-126">If the <strong>Calculate cash discounts for credit notes **option is set to **Yes</strong> on the <strong>Accounts payable parameters</strong> page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="bf6a1-127">Du får for eksempel en kontantrabatt på 2 prosent hvis fakturaen er betalt innen 10 dager etter at den utstedes.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-127">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="bf6a1-128">Det posteres en faktura på 100,00.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-128">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="bf6a1-129">Hvis du returnerer varene og mottar en kreditnota, kan du angi kreditnotaen for hele beløpet i den opprinnelige fakturaen 100,00, sammen med 2 prosent kontantrabatt, som også er definert i kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-129">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="bf6a1-130">Når du viser kreditnotaen på siden **Utlign åpne transaksjoner**, vises **98,00** i feltet **Beløp som skal utlignes**, og **-2,00** vises i feltet **Kontantrabattbeløp**.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-130">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="bf6a1-131">Rabattbeløpet posteres til en kontantrabattkonto.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-131">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="bf6a1-132">Overbetalings-/underbetalingsbeløp</span><span class="sxs-lookup"><span data-stu-id="bf6a1-132">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="bf6a1-133">Du kan foreta en delbetaling der beløpet som fremdeles skal utlignes, er svært lite.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-133">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="bf6a1-134">Anta for eksempel at leverandørfakturaen gjelder 1 000,00, og du betaler 999,90.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-134">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="bf6a1-135">Hvis det gjenstående beløpet er mindre enn beløpet som er angitt for overbetalinger eller underbetalinger på siden **Leverandørparametere**, posteres differansen automatisk til en finanskonto for overbetaling/underbetaling.</span><span class="sxs-lookup"><span data-stu-id="bf6a1-135">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="bf6a1-136">Hvis du vil ha mer informasjon, kan du se [Oversikt over leverandørbetaling](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bf6a1-136">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>

