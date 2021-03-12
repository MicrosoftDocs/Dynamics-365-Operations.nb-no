---
title: Innbetale kundebetalinger
description: Betale inn kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9221101581a6a130889b7c941ca228070a000c56
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003162"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="121a8-103">Innbetale kundebetalinger</span><span class="sxs-lookup"><span data-stu-id="121a8-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="121a8-104">Betale inn kundebetalinger.</span><span class="sxs-lookup"><span data-stu-id="121a8-104">Deposit customer payments.</span></span> <span data-ttu-id="121a8-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="121a8-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="121a8-106">Gå til **Moduler > Kunder > Betalinger > Betalingsjournal** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="121a8-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="121a8-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="121a8-107">Select **New**.</span></span>
3. <span data-ttu-id="121a8-108">I **Navn**-feltet velger du **CustPay** i rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="121a8-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="121a8-109">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="121a8-109">Select **Lines**.</span></span>
5. <span data-ttu-id="121a8-110">Velg kunden du registrerer betalingen for, i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="121a8-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="121a8-111">Angi betalingsbeløpet i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="121a8-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="121a8-112">Du kan velge å la beløpet stå tomt, og la programmet beregne det ved å velge fakturaene som ble betalt.</span><span class="sxs-lookup"><span data-stu-id="121a8-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="121a8-113">Skriv inn en verdi i **Betalingsreferanse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="121a8-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="121a8-114">Betalingsreferansen kan være sjekknummeret for betalingen du angir.</span><span class="sxs-lookup"><span data-stu-id="121a8-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="121a8-115">Betalingsreferansen er nødvendig hvis du skal inkludere betalingen på et betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="121a8-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="121a8-116">Merk av for Bruk et betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="121a8-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="121a8-117">Hvis betalingen skal inkluderes i innbetalingen, kan du endre denne innstillingen til Ja.</span><span class="sxs-lookup"><span data-stu-id="121a8-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="121a8-118">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="121a8-118">Select **New**.</span></span>
10. <span data-ttu-id="121a8-119">Velg kunden for den neste betalingen i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="121a8-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="121a8-120">Angi betalingsbeløpet i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="121a8-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="121a8-121">Skriv inn en verdi i **Betalingsreferanse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="121a8-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="121a8-122">Merk av for **Bruk et betalingsbilag**.</span><span class="sxs-lookup"><span data-stu-id="121a8-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="121a8-123">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="121a8-123">Select **Post**.</span></span> <span data-ttu-id="121a8-124">Betalinger må være postert før betalingsbilaget kan genereres.</span><span class="sxs-lookup"><span data-stu-id="121a8-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="121a8-125">Dette sikrer at betalingene ikke endres etter at betalingsbilaget er generert.</span><span class="sxs-lookup"><span data-stu-id="121a8-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="121a8-126">Velg **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="121a8-126">Select **Functions**.</span></span>
16. <span data-ttu-id="121a8-127">Velg **Betalingsbilag**.</span><span class="sxs-lookup"><span data-stu-id="121a8-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="121a8-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="121a8-128">Select **OK**.</span></span> <span data-ttu-id="121a8-129">Den første siden brukes til å opprette betalingsbilaget.</span><span class="sxs-lookup"><span data-stu-id="121a8-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="121a8-130">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="121a8-130">Select **OK**.</span></span> <span data-ttu-id="121a8-131">Det andre trinnet er å skrive ut betalingsbilaget, men dette trinnet er ikke nødvendig.</span><span class="sxs-lookup"><span data-stu-id="121a8-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

