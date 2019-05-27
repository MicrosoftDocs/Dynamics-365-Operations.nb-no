---
title: Opprette et nytt avtalegiromandat for en kunde
description: Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572541"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="8db60-103">Opprette et nytt avtalegiromandat for en kunde</span><span class="sxs-lookup"><span data-stu-id="8db60-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8db60-104">Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura.</span><span class="sxs-lookup"><span data-stu-id="8db60-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="8db60-105">Opprette en bankkonto</span><span class="sxs-lookup"><span data-stu-id="8db60-105">Create a bank account</span></span>
1. <span data-ttu-id="8db60-106">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="8db60-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="8db60-107">Velg for eksempel US-001.</span><span class="sxs-lookup"><span data-stu-id="8db60-107">For example, select US-001</span></span>
3. <span data-ttu-id="8db60-108">Klikk Kunde i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8db60-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="8db60-109">Klikk Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="8db60-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="8db60-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8db60-110">Click New.</span></span>
6. <span data-ttu-id="8db60-111">Skriv inn en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="8db60-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="8db60-113">Skriv inn en verdi i IBAN-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="8db60-114">Skriv inn en verdi i Valuta-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="8db60-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8db60-115">Click Save.</span></span>
11. <span data-ttu-id="8db60-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8db60-116">Close the page.</span></span>
12. <span data-ttu-id="8db60-117">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="8db60-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="8db60-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8db60-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="8db60-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8db60-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="8db60-120">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="8db60-120">Click Edit.</span></span>
16. <span data-ttu-id="8db60-121">Vis delen Tilleggsidentifikasjon.</span><span class="sxs-lookup"><span data-stu-id="8db60-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="8db60-122">Skriv inn en verdi i feltet Direkte debet-ID.</span><span class="sxs-lookup"><span data-stu-id="8db60-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="8db60-123">Skriv inn en verdi i IBAN-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="8db60-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8db60-124">Close the page.</span></span>
20. <span data-ttu-id="8db60-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8db60-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="8db60-126">Definere den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="8db60-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="8db60-127">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="8db60-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="8db60-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8db60-128">Click New.</span></span>
3. <span data-ttu-id="8db60-129">Skriv inn en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="8db60-130">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8db60-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8db60-131">Betalingstypen for betalingsmåten avtalegiromandat må være elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="8db60-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="8db60-132">I feltet Krever mandat velger du Ja.</span><span class="sxs-lookup"><span data-stu-id="8db60-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="8db60-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8db60-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="8db60-134">Legg til et avtalegiromandat for en kunde.</span><span class="sxs-lookup"><span data-stu-id="8db60-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="8db60-135">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="8db60-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="8db60-136">Velg for eksempel US-001.</span><span class="sxs-lookup"><span data-stu-id="8db60-136">For example, select US-001</span></span>
3. <span data-ttu-id="8db60-137">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="8db60-137">Click Edit.</span></span>
4. <span data-ttu-id="8db60-138">Utvid delen Betalingstandarder.</span><span class="sxs-lookup"><span data-stu-id="8db60-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="8db60-139">Angi eller velg en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="8db60-140">Utvid delen Betalingstandarder.</span><span class="sxs-lookup"><span data-stu-id="8db60-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="8db60-141">Utvid delen Avtalegiromandater.</span><span class="sxs-lookup"><span data-stu-id="8db60-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="8db60-142">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8db60-142">Click Add.</span></span>
9. <span data-ttu-id="8db60-143">Angi eller velg en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="8db60-144">Angi eller velg en verdi i Kreditors bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="8db60-145">Angi antall betalinger som du forventer å behandle for dette mandatet.</span><span class="sxs-lookup"><span data-stu-id="8db60-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="8db60-146">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8db60-146">Click OK.</span></span>
13. <span data-ttu-id="8db60-147">Klikk Skriv ut.</span><span class="sxs-lookup"><span data-stu-id="8db60-147">Click Print.</span></span>
14. <span data-ttu-id="8db60-148">Klikk Mandatrapport.</span><span class="sxs-lookup"><span data-stu-id="8db60-148">Click Mandate report.</span></span>
15. <span data-ttu-id="8db60-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8db60-149">Close the page.</span></span>
16. <span data-ttu-id="8db60-150">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="8db60-150">Click Edit.</span></span>
17. <span data-ttu-id="8db60-151">Angi en dato i Signaturdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="8db60-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="8db60-152">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="8db60-152">Click Yes.</span></span>
19. <span data-ttu-id="8db60-153">Angi stedet mandatet ble signert.</span><span class="sxs-lookup"><span data-stu-id="8db60-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="8db60-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8db60-154">Click OK.</span></span>
21. <span data-ttu-id="8db60-155">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8db60-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="8db60-156">Opprette en fritekstfaktura med mandat</span><span class="sxs-lookup"><span data-stu-id="8db60-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="8db60-157">Gå til Kunder > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="8db60-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="8db60-158">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8db60-158">Click New.</span></span>
3. <span data-ttu-id="8db60-159">Velg kunden du har lagt til mandatet til.</span><span class="sxs-lookup"><span data-stu-id="8db60-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="8db60-160">Angi eller velg en verdi i feltet ID for avtalegiromandat.</span><span class="sxs-lookup"><span data-stu-id="8db60-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

