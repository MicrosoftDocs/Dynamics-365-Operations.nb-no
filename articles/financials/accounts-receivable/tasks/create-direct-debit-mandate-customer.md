--- 
title: Opprette et nytt avtalegiromandat for en kunde
description: "Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 66aa30e88cec914a9cd4d02a0992ff7570d1ced2
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="c0922-103">Opprette et nytt avtalegiromandat for en kunde</span><span class="sxs-lookup"><span data-stu-id="c0922-103">Create a direct debit mandate for a customer</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0922-104">Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura.</span><span class="sxs-lookup"><span data-stu-id="c0922-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="c0922-105">Opprette en bankkonto</span><span class="sxs-lookup"><span data-stu-id="c0922-105">Create a bank account</span></span>
1. <span data-ttu-id="c0922-106">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="c0922-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="c0922-107">Velg for eksempel US-001.</span><span class="sxs-lookup"><span data-stu-id="c0922-107">For example, select US-001</span></span>
3. <span data-ttu-id="c0922-108">Klikk Kunde i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c0922-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="c0922-109">Klikk Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="c0922-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="c0922-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c0922-110">Click New.</span></span>
6. <span data-ttu-id="c0922-111">Skriv inn en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="c0922-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="c0922-113">Skriv inn en verdi i IBAN-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="c0922-114">Skriv inn en verdi i Valuta-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="c0922-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c0922-115">Click Save.</span></span>
11. <span data-ttu-id="c0922-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c0922-116">Close the page.</span></span>
12. <span data-ttu-id="c0922-117">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="c0922-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="c0922-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c0922-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c0922-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c0922-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="c0922-120">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="c0922-120">Click Edit.</span></span>
16. <span data-ttu-id="c0922-121">Vis delen Tilleggsidentifikasjon.</span><span class="sxs-lookup"><span data-stu-id="c0922-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="c0922-122">Skriv inn en verdi i feltet Direkte debet-ID.</span><span class="sxs-lookup"><span data-stu-id="c0922-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="c0922-123">Skriv inn en verdi i IBAN-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="c0922-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c0922-124">Close the page.</span></span>
20. <span data-ttu-id="c0922-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c0922-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="c0922-126">Definere den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="c0922-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="c0922-127">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="c0922-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="c0922-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c0922-128">Click New.</span></span>
3. <span data-ttu-id="c0922-129">Skriv inn en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="c0922-130">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c0922-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c0922-131">Betalingstypen for betalingsmåten avtalegiromandat må være elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="c0922-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="c0922-132">I feltet Krever mandat velger du Ja.</span><span class="sxs-lookup"><span data-stu-id="c0922-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="c0922-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c0922-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="c0922-134">Legg til et avtalegiromandat for en kunde.</span><span class="sxs-lookup"><span data-stu-id="c0922-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="c0922-135">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="c0922-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="c0922-136">Velg for eksempel US-001.</span><span class="sxs-lookup"><span data-stu-id="c0922-136">For example, select US-001</span></span>
3. <span data-ttu-id="c0922-137">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="c0922-137">Click Edit.</span></span>
4. <span data-ttu-id="c0922-138">Utvid delen Betalingstandarder.</span><span class="sxs-lookup"><span data-stu-id="c0922-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="c0922-139">Angi eller velg en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="c0922-140">Utvid delen Betalingstandarder.</span><span class="sxs-lookup"><span data-stu-id="c0922-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="c0922-141">Utvid delen Avtalegiromandater.</span><span class="sxs-lookup"><span data-stu-id="c0922-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="c0922-142">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="c0922-142">Click Add.</span></span>
9. <span data-ttu-id="c0922-143">Angi eller velg en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="c0922-144">Angi eller velg en verdi i Kreditors bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="c0922-145">Angi antall betalinger som du forventer å behandle for dette mandatet.</span><span class="sxs-lookup"><span data-stu-id="c0922-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="c0922-146">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c0922-146">Click OK.</span></span>
13. <span data-ttu-id="c0922-147">Klikk Skriv ut.</span><span class="sxs-lookup"><span data-stu-id="c0922-147">Click Print.</span></span>
14. <span data-ttu-id="c0922-148">Klikk Mandatrapport.</span><span class="sxs-lookup"><span data-stu-id="c0922-148">Click Mandate report.</span></span>
15. <span data-ttu-id="c0922-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c0922-149">Close the page.</span></span>
16. <span data-ttu-id="c0922-150">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="c0922-150">Click Edit.</span></span>
17. <span data-ttu-id="c0922-151">Angi en dato i Signaturdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0922-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="c0922-152">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="c0922-152">Click Yes.</span></span>
19. <span data-ttu-id="c0922-153">Angi stedet mandatet ble signert.</span><span class="sxs-lookup"><span data-stu-id="c0922-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="c0922-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c0922-154">Click OK.</span></span>
21. <span data-ttu-id="c0922-155">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c0922-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="c0922-156">Opprette en fritekstfaktura med mandat</span><span class="sxs-lookup"><span data-stu-id="c0922-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="c0922-157">Gå til Kunder > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="c0922-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="c0922-158">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c0922-158">Click New.</span></span>
3. <span data-ttu-id="c0922-159">Velg kunden du har lagt til mandatet til.</span><span class="sxs-lookup"><span data-stu-id="c0922-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="c0922-160">Angi eller velg en verdi i feltet ID for avtalegiromandat.</span><span class="sxs-lookup"><span data-stu-id="c0922-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


