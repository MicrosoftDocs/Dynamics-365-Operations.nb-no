---
title: Oversikt over avsetninger
description: Denne artikkelen beskriver avsetninger og gir informasjon om hvordan du konfigurerer dem og opprette transaksjoner.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23c6a3402e4bc4a22d764017ba56554001300a67
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557388"
---
# <a name="accruals-overview"></a><span data-ttu-id="66b07-103">Oversikt over avsetninger</span><span class="sxs-lookup"><span data-stu-id="66b07-103">Accruals overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66b07-104">Denne artikkelen beskriver avsetninger og gir informasjon om hvordan du konfigurerer dem og opprette transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="66b07-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="66b07-105">Avsetninger brukes i avsetningsmetoden til å spore omsetning som gjenkjennes i perioden den er opptjent i, ikke når betaling mottas, og til å spore utgifter (kostnader) som gjenkjennes når de forekommer, ikke når betalingen foretas.</span><span class="sxs-lookup"><span data-stu-id="66b07-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="66b07-106">Avsetningsplaner</span><span class="sxs-lookup"><span data-stu-id="66b07-106">Accrual schemes</span></span>
<span data-ttu-id="66b07-107">Avsetningsplaner brukes til å definere utsatte inntekter og kostnader, og samme avsetningsplan kan brukes til både inntekter og kostnader.</span><span class="sxs-lookup"><span data-stu-id="66b07-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="66b07-108">Finansavsetninger omfordeler kostnadene eller inntektene på en journallinje slik at kostnadene og inntektene gjenkjennes i de riktige periodene.</span><span class="sxs-lookup"><span data-stu-id="66b07-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="66b07-109">På **Avsetningsplaner**-siden angir du debet- og kreditkontoer som skal brukes når avsetningsplanen brukes.</span><span class="sxs-lookup"><span data-stu-id="66b07-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="66b07-110">**Debet** – Hovedkontoen du definerer, erstatter debethovedkontoen på journalbilagslinjen.</span><span class="sxs-lookup"><span data-stu-id="66b07-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="66b07-111">Denne kontoen brukes også til tilbakeføring av henvisningen, basert på finansavsetningstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="66b07-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="66b07-112">**Kredit** – Hovedkontoen du definerer, erstatter kredithovedkontoen på journalbilagslinjen.</span><span class="sxs-lookup"><span data-stu-id="66b07-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="66b07-113">Denne kontoen brukes også til tilbakeføring av henvisningen, basert på finansavsetningstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="66b07-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="66b07-114">Når du avgjør hvilke kontoer som skal brukes, kan du angi hvordan bilagsnummeret skal opprettes når avsetningstransaksjoner opprettes.</span><span class="sxs-lookup"><span data-stu-id="66b07-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="66b07-115">Du kan også angi hvor ofte transaksjonene skjer, hvor mange ganger transaksjonene er opprettet, og når transaksjonene posteres.</span><span class="sxs-lookup"><span data-stu-id="66b07-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="66b07-116">Når avsetningsplanen er opprettet, kan du bruke den i noen av journalene ved hjelp av funksjonen Finansavsetninger.</span><span class="sxs-lookup"><span data-stu-id="66b07-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="66b07-117">Finansavsetninger</span><span class="sxs-lookup"><span data-stu-id="66b07-117">Ledger accruals</span></span>
<span data-ttu-id="66b07-118">Når du registrerer en journal, kan du klikke **Finansavsetninger** på **Funksjoner**-menyen.</span><span class="sxs-lookup"><span data-stu-id="66b07-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="66b07-119">Når du deretter velger avsetningsplanen, vises grunnlagsbeløpet fra journalen som fordeles over perioden i henhold til avsetningsplanen.</span><span class="sxs-lookup"><span data-stu-id="66b07-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="66b07-120">Hvis du for eksempel betaler en ansatts forsikring for hele året i januar, og beløpet er 120 000, må du gjenkjenne denne utgiften hver måned.</span><span class="sxs-lookup"><span data-stu-id="66b07-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="66b07-121">Du kan velge startdatoen.</span><span class="sxs-lookup"><span data-stu-id="66b07-121">You can select the start date.</span></span> <span data-ttu-id="66b07-122">Du kan også angi om det påløpte beløpet er basert på kontoen eller motkontoen.</span><span class="sxs-lookup"><span data-stu-id="66b07-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="66b07-123">Når du har foretatt valgene, klikker du **Transaksjoner** for å vise alle transaksjonene som er opprettet basert på avsetningsplanen.</span><span class="sxs-lookup"><span data-stu-id="66b07-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="66b07-124">Hvis du for eksempel fordeler 120 000 i forsikringsutgifter på hele året, ser du 10 000 for hver måned.</span><span class="sxs-lookup"><span data-stu-id="66b07-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="66b07-125">Når du har postert journalen, kan du vise transaksjonene ved hjelp av forespørselssiden **Bilagstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="66b07-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="66b07-126">Hvis en avsetningsplan ikke kan brukes (for eksempel når en salgsordrefaktura eller bestillingsfaktura er involvert), kan du kreditere det forskuddsbetalte beløpet og debitere utgiftsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="66b07-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="66b07-127">Deretter kan du velge **Motregn** når du bruker avsetningsplanen.</span><span class="sxs-lookup"><span data-stu-id="66b07-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="66b07-128">Hvis du vil ha mer informasjon, se [Opprette avsetningsplaner](tasks/create-accrual-schemes.md) og [Opprette finansavsetningstransaksjoner](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="66b07-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>
