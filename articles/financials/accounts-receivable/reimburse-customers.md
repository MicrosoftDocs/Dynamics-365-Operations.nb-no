---
title: Refundere kunder
description: Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe. Hvis en kunde har en kreditsaldo, kan du refundere kunden for saldobeløpet.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97982dec140ed440682ae507f40557670ebccd3e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836645"
---
# <a name="reimburse-customers"></a><span data-ttu-id="ed5b2-104">Refundere kunder</span><span class="sxs-lookup"><span data-stu-id="ed5b2-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed5b2-105">Denne artikkelen beskriver hvordan du oppretter refusjonstransaksjoner for en kundegruppe.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="ed5b2-106">Hvis en kunde har en kreditsaldo, kan du refundere kunden for saldobeløpet.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="ed5b2-107">Tabellen nedenfor viser forutsetninger som må være på plass før du starter.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="ed5b2-108">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="ed5b2-108">Prerequisite</span></span>                                                            | <span data-ttu-id="ed5b2-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ed5b2-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5b2-110">Angi det minste refusjonsbeløpet for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="ed5b2-111">Angi det minste beløpet som kan refunderes for kunders overbetaling, i **Minimumsrefusjon**-feltet i **Generelt**-området på **Kundeparametere**-siden.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="ed5b2-112">Valgfritt: Legg til en leverandørkonto i hver kunde som kan refunderes.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="ed5b2-113">Velg leverandørkontoen for kunden i **Leverandørkonto**-feltet i hurtigfanen **Diverse detaljer** på **Kunder**-siden.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="ed5b2-114">Når du oppretter refusjonstransaksjoner, opprettes en leverandørfaktura for beløpet i kreditsaldoen.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="ed5b2-115">Refusjonsprosessen fjerner kreditsaldoen for kundekontoen og oppretter en forfalt saldo for leverandørkontoen som tilsvarer kunden.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="ed5b2-116">Kjør **Refusjon**-prosessen i Kunder.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="ed5b2-117">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="ed5b2-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="ed5b2-118">Klikk **Velg**, og angi kundekontoene i spørringen for å refundere bestemte kundekontoer.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="ed5b2-119">Klikk **OK** for å refundere alle kundekontoer.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="ed5b2-120">Kreditbeløpene overføres til leverandørkontoene til kundene og behandles som ordinære betalinger.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="ed5b2-121">Hvis en kunde ikke har en leverandørkonto, opprettes det automatisk en engangsleverandørkonto for kunden.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="ed5b2-122">Hvis du vil vise refusjonstransaksjonene som ble opprettet, bruker du **Refusjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="ed5b2-123">Opprett en betaling for leverandørfakturaer som ble opprettet av refusjonsprosessen, i Leverandører.</span><span class="sxs-lookup"><span data-stu-id="ed5b2-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>




