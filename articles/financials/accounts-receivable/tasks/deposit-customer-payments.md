---
title: Innbetale kundebetalinger
description: Betale inn kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "313388"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="2c77a-103">Innbetale kundebetalinger</span><span class="sxs-lookup"><span data-stu-id="2c77a-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c77a-104">Betale inn kundebetalinger.</span><span class="sxs-lookup"><span data-stu-id="2c77a-104">Deposit customer payments.</span></span> <span data-ttu-id="2c77a-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="2c77a-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2c77a-106">Gå til Kunder > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="2c77a-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2c77a-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2c77a-107">Click New.</span></span>
3. <span data-ttu-id="2c77a-108">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="2c77a-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2c77a-109">Velg betalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="2c77a-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="2c77a-110">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="2c77a-110">Click Lines.</span></span>
6. <span data-ttu-id="2c77a-111">Velg kunden du registrerer betalingen for, i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="2c77a-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="2c77a-112">Angi betalingsbeløpet i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="2c77a-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="2c77a-113">Du kan velge å la beløpet stå tomt, og la programmet beregne det ved å velge fakturaene som ble betalt.</span><span class="sxs-lookup"><span data-stu-id="2c77a-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="2c77a-114">Skriv inn en verdi i Betalingsreferanse-feltet.</span><span class="sxs-lookup"><span data-stu-id="2c77a-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="2c77a-115">Betalingsreferansen kan være sjekknummeret for betalingen du angir.</span><span class="sxs-lookup"><span data-stu-id="2c77a-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="2c77a-116">Betalingsreferansen er nødvendig hvis du skal inkludere betalingen på et betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="2c77a-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="2c77a-117">Merk av for Bruk et betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="2c77a-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="2c77a-118">Hvis betalingen skal inkluderes i innbetalingen, kan du endre denne innstillingen til Ja.</span><span class="sxs-lookup"><span data-stu-id="2c77a-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="2c77a-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2c77a-119">Click New.</span></span>
11. <span data-ttu-id="2c77a-120">Velg kunden for den neste betalingen i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="2c77a-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="2c77a-121">Angi betalingsbeløpet i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="2c77a-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="2c77a-122">Skriv inn en verdi i Betalingsreferanse-feltet.</span><span class="sxs-lookup"><span data-stu-id="2c77a-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="2c77a-123">Merk av for Bruk et betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="2c77a-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="2c77a-124">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="2c77a-124">Click Post.</span></span>
    * <span data-ttu-id="2c77a-125">Betalinger må være postert før betalingsbilaget kan genereres.</span><span class="sxs-lookup"><span data-stu-id="2c77a-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="2c77a-126">Dette sikrer at betalingene ikke endres etter at betalingsbilaget er generert.</span><span class="sxs-lookup"><span data-stu-id="2c77a-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="2c77a-127">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="2c77a-127">Click Functions.</span></span>
17. <span data-ttu-id="2c77a-128">Klikk betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="2c77a-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="2c77a-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2c77a-129">Click OK.</span></span>
    * <span data-ttu-id="2c77a-130">Den første siden brukes til å opprette betalingsbilaget.</span><span class="sxs-lookup"><span data-stu-id="2c77a-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="2c77a-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2c77a-131">Click OK.</span></span>
    * <span data-ttu-id="2c77a-132">Det andre trinnet er å skrive ut betalingsbilaget, men dette trinnet er ikke nødvendig.</span><span class="sxs-lookup"><span data-stu-id="2c77a-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

