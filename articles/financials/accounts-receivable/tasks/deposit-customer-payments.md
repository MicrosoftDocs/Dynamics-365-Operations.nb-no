--- 
title: Innbetale kundebetalinger
description: Betale inn kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dbf21bd5df70cd80e4fe3f2f5d699aa82b62423b
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="476ef-103">Innbetale kundebetalinger</span><span class="sxs-lookup"><span data-stu-id="476ef-103">Deposit customer payments</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="476ef-104">Betale inn kundebetalinger.</span><span class="sxs-lookup"><span data-stu-id="476ef-104">Deposit customer payments.</span></span> <span data-ttu-id="476ef-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="476ef-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="476ef-106">Gå til Kunder > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="476ef-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="476ef-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="476ef-107">Click New.</span></span>
3. <span data-ttu-id="476ef-108">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="476ef-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="476ef-109">Velg betalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="476ef-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="476ef-110">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="476ef-110">Click Lines.</span></span>
6. <span data-ttu-id="476ef-111">Velg kunden du registrerer betalingen for, i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="476ef-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="476ef-112">Angi betalingsbeløpet i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="476ef-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="476ef-113">Du kan velge å la beløpet stå tomt, og la programmet beregne det ved å velge fakturaene som ble betalt.</span><span class="sxs-lookup"><span data-stu-id="476ef-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="476ef-114">Skriv inn en verdi i Betalingsreferanse-feltet.</span><span class="sxs-lookup"><span data-stu-id="476ef-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="476ef-115">Betalingsreferansen kan være sjekknummeret for betalingen du angir.</span><span class="sxs-lookup"><span data-stu-id="476ef-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="476ef-116">Betalingsreferansen er nødvendig hvis du skal inkludere betalingen på et betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="476ef-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="476ef-117">Merk av for Bruk et betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="476ef-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="476ef-118">Hvis betalingen skal inkluderes i innbetalingen, kan du endre denne innstillingen til Ja.</span><span class="sxs-lookup"><span data-stu-id="476ef-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="476ef-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="476ef-119">Click New.</span></span>
11. <span data-ttu-id="476ef-120">Velg kunden for den neste betalingen i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="476ef-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="476ef-121">Angi betalingsbeløpet i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="476ef-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="476ef-122">Skriv inn en verdi i Betalingsreferanse-feltet.</span><span class="sxs-lookup"><span data-stu-id="476ef-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="476ef-123">Merk av for Bruk et betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="476ef-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="476ef-124">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="476ef-124">Click Post.</span></span>
    * <span data-ttu-id="476ef-125">Betalinger må være postert før betalingsbilaget kan genereres.</span><span class="sxs-lookup"><span data-stu-id="476ef-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="476ef-126">Dette sikrer at betalingene ikke endres etter at betalingsbilaget er generert.</span><span class="sxs-lookup"><span data-stu-id="476ef-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="476ef-127">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="476ef-127">Click Functions.</span></span>
17. <span data-ttu-id="476ef-128">Klikk betalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="476ef-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="476ef-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="476ef-129">Click OK.</span></span>
    * <span data-ttu-id="476ef-130">Den første siden brukes til å opprette betalingsbilaget.</span><span class="sxs-lookup"><span data-stu-id="476ef-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="476ef-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="476ef-131">Click OK.</span></span>
    * <span data-ttu-id="476ef-132">Det andre trinnet er å skrive ut betalingsbilaget, men dette trinnet er ikke nødvendig.</span><span class="sxs-lookup"><span data-stu-id="476ef-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


