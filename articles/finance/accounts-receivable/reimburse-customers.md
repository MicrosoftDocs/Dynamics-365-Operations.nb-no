---
title: Refundere kunder
description: Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe. Hvis en kunde har en kreditsaldo, kan du refundere kunden for saldobeløpet.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd8b32e04743fdde3cc339e1535f8ae58c518aed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816298"
---
# <a name="reimburse-customers"></a><span data-ttu-id="a6648-104">Refundere kunder</span><span class="sxs-lookup"><span data-stu-id="a6648-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6648-105">Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe.</span><span class="sxs-lookup"><span data-stu-id="a6648-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="a6648-106">Hvis en kunde har en kreditsaldo, kan du refundere kunden for saldobeløpet.</span><span class="sxs-lookup"><span data-stu-id="a6648-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="a6648-107">Tabellen nedenfor viser forutsetninger som må være på plass før du starter.</span><span class="sxs-lookup"><span data-stu-id="a6648-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="a6648-108">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="a6648-108">Prerequisite</span></span>                                                            | <span data-ttu-id="a6648-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a6648-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="a6648-110">Angi det minste refusjonsbeløpet for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="a6648-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="a6648-111">Angi det minste beløpet som kan refunderes for kunders overbetaling, i **Minimumsrefusjon**-feltet i **Generelt**-området på **Kundeparametere**-siden.</span><span class="sxs-lookup"><span data-stu-id="a6648-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="a6648-112">Valgfritt: Legg til en leverandørkonto i hver kunde som kan refunderes.</span><span class="sxs-lookup"><span data-stu-id="a6648-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="a6648-113">Velg leverandørkontoen for kunden i **Leverandørkonto**-feltet i hurtigfanen **Diverse detaljer** på **Kunder**-siden.</span><span class="sxs-lookup"><span data-stu-id="a6648-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="a6648-114">Når du oppretter refusjonstransaksjoner, opprettes en leverandørfaktura for beløpet i kreditsaldoen.</span><span class="sxs-lookup"><span data-stu-id="a6648-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="a6648-115">Refusjonsprosessen fjerner kreditsaldoen for kundekontoen og oppretter en forfalt saldo for leverandørkontoen som tilsvarer kunden.</span><span class="sxs-lookup"><span data-stu-id="a6648-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="a6648-116">I Kunder kjører du **Refusjon**-prosessen (**Kunder \> Periodiske oppgaver \> Refusjon**).</span><span class="sxs-lookup"><span data-stu-id="a6648-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="a6648-117">Hvis du vil gruppere alle transaksjoner, uansett finansdimensjoner, setter du **Summer kunde** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a6648-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="a6648-118">Hvis du bare vil gruppere transaksjoner som har like finansdimensjoner, setter du alternativet til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="a6648-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="a6648-119">Velg **Ta med kunder med utestående debettransaksjoner** for å velge kunder som har ikke-utlignede debetbeløp.</span><span class="sxs-lookup"><span data-stu-id="a6648-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="a6648-120">Hvis du vil refundere bestemte kundekontoer, går du til hurtigfanen **Poster som skal inkluderes** og velger **Filter**, og deretter angir du kundekontoene i spørringen.</span><span class="sxs-lookup"><span data-stu-id="a6648-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="a6648-121">Kreditbeløpene overføres til leverandørkontoene til kundene og behandles som ordinære betalinger.</span><span class="sxs-lookup"><span data-stu-id="a6648-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="a6648-122">Hvis en kunde ikke har en leverandørkonto, opprettes det automatisk en engangsleverandørkonto for kunden.</span><span class="sxs-lookup"><span data-stu-id="a6648-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="a6648-123">Hvis du vil vise refusjonstransaksjonene som ble opprettet, bruker du **Refusjon**-rapporten (**Kunder \> Forespørsler og rapporter \> Refusjon-rapporten**).</span><span class="sxs-lookup"><span data-stu-id="a6648-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="a6648-124">Opprett en betaling for leverandørfakturaer som ble opprettet av refusjonsprosessen, i Leverandører.</span><span class="sxs-lookup"><span data-stu-id="a6648-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="a6648-125">Du finner mer informasjon om hvordan du betaler leverandører, i [Oversikt over leverandørbetaling](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="a6648-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]