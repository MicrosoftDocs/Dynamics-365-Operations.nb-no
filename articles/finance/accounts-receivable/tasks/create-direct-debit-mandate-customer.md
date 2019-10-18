---
title: Opprette et nytt avtalegiromandat for en kunde
description: Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179263"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="171ac-103">Opprette et nytt avtalegiromandat for en kunde</span><span class="sxs-lookup"><span data-stu-id="171ac-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="171ac-104">Denne oppgaveveiledningen beskriver hvordan du oppretter et avtalegiromandat og bruker det på en faktura.</span><span class="sxs-lookup"><span data-stu-id="171ac-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="171ac-105">Opprette en bankkonto</span><span class="sxs-lookup"><span data-stu-id="171ac-105">Create a bank account</span></span>
1. <span data-ttu-id="171ac-106">I **navigasjonsruten** går du **Moduler > Kunder > Kunder > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="171ac-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="171ac-107">Velg en post i listen.</span><span class="sxs-lookup"><span data-stu-id="171ac-107">In the list, select a record.</span></span> <span data-ttu-id="171ac-108">Velg for eksempel US-001.</span><span class="sxs-lookup"><span data-stu-id="171ac-108">For example, select US-001</span></span>
3. <span data-ttu-id="171ac-109">Klikk **Kunde** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="171ac-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="171ac-110">Klikk **Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="171ac-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="171ac-111">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="171ac-111">Click **New**.</span></span>
6. <span data-ttu-id="171ac-112">Skriv inn en verdi i **Bankkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="171ac-113">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="171ac-114">Skriv inn en verdi i **IBAN**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="171ac-115">Skriv inn en verdi i **Valuta**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="171ac-116">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="171ac-116">Click **Save**.</span></span>
11. <span data-ttu-id="171ac-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171ac-117">Close the page.</span></span>
12. <span data-ttu-id="171ac-118">I **navigasjonsruten** går du til **Moduler > Kontant- og bankbehandling > Bankkontoer > Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="171ac-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="171ac-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="171ac-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="171ac-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="171ac-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="171ac-121">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="171ac-121">Click **Edit**.</span></span>
16. <span data-ttu-id="171ac-122">Vis hurtigfanen **Tilleggsidentifikasjon**.</span><span class="sxs-lookup"><span data-stu-id="171ac-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="171ac-123">Skriv inn en verdi i feltet **Direkte debet-ID**.</span><span class="sxs-lookup"><span data-stu-id="171ac-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="171ac-124">Skriv inn en verdi i **IBAN**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="171ac-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171ac-125">Close the page.</span></span>
20. <span data-ttu-id="171ac-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171ac-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="171ac-127">Definere den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="171ac-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="171ac-128">I **navigasjonsruten** går du til **Moduler > Kunder > Betalingsoppsett > Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="171ac-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="171ac-129">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="171ac-129">Click **New**.</span></span>
3. <span data-ttu-id="171ac-130">Skriv inn en verdi i **Betalingsmåte**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="171ac-131">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="171ac-132">Velg Elektronisk betaling i **Betalingstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="171ac-133">Betalingstypen for betalingsmåten avtalegiromandat må være elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="171ac-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="171ac-134">I feltet **Krever mandat** velger du Ja.</span><span class="sxs-lookup"><span data-stu-id="171ac-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="171ac-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171ac-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="171ac-136">Legg til et avtalegiromandat for en kunde.</span><span class="sxs-lookup"><span data-stu-id="171ac-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="171ac-137">I **navigasjonsruten** går du **Moduler > Kunder > Kunder > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="171ac-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="171ac-138">Velg en post i listen.</span><span class="sxs-lookup"><span data-stu-id="171ac-138">In the list, select a record.</span></span> <span data-ttu-id="171ac-139">Velg for eksempel US-001.</span><span class="sxs-lookup"><span data-stu-id="171ac-139">For example, select US-001</span></span>
3. <span data-ttu-id="171ac-140">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="171ac-140">Click **Edit**.</span></span>
4. <span data-ttu-id="171ac-141">Utvid hurtigfanen **Betalingstandarder**.</span><span class="sxs-lookup"><span data-stu-id="171ac-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="171ac-142">Angi eller velg en verdi i **Betalingsmåte**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="171ac-143">Utvid hurtigfanen **Betalingstandarder**.</span><span class="sxs-lookup"><span data-stu-id="171ac-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="171ac-144">Utvid hurtigfanen **Avtalegiromandater**.</span><span class="sxs-lookup"><span data-stu-id="171ac-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="171ac-145">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="171ac-145">Click **Add**.</span></span>
9. <span data-ttu-id="171ac-146">Angi eller velg en verdi i **Bankkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="171ac-147">Angi eller velg en verdi i **Kreditors bankkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="171ac-148">Angi antall betalinger som du forventer å behandle for dette mandatet, i feltet **Betalingsfrekvens**.</span><span class="sxs-lookup"><span data-stu-id="171ac-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="171ac-149">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="171ac-149">Click **OK**.</span></span>
13. <span data-ttu-id="171ac-150">Klikk **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="171ac-150">Click **Print**.</span></span>
14. <span data-ttu-id="171ac-151">Klikk **Mandatrapport**.</span><span class="sxs-lookup"><span data-stu-id="171ac-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="171ac-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171ac-152">Close the page.</span></span>
16. <span data-ttu-id="171ac-153">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="171ac-153">Click **Edit**.</span></span>
17. <span data-ttu-id="171ac-154">Angi en dato i **Signaturdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="171ac-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="171ac-155">Klikk **Ja**.</span><span class="sxs-lookup"><span data-stu-id="171ac-155">Click **Yes**.</span></span>
19. <span data-ttu-id="171ac-156">Angi stedet mandatet ble signert.</span><span class="sxs-lookup"><span data-stu-id="171ac-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="171ac-157">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="171ac-157">Click **OK**.</span></span>
21. <span data-ttu-id="171ac-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="171ac-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="171ac-159">Opprette en fritekstfaktura med mandat</span><span class="sxs-lookup"><span data-stu-id="171ac-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="171ac-160">I **navigasjonsruten** går du til **Moduler > Kunder > Fakturaer > Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="171ac-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="171ac-161">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="171ac-161">Click **New**.</span></span>
3. <span data-ttu-id="171ac-162">Velg kunden du har lagt til mandatet til.</span><span class="sxs-lookup"><span data-stu-id="171ac-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="171ac-163">Angi eller velg en verdi i feltet **ID for avtalegiromandat**.</span><span class="sxs-lookup"><span data-stu-id="171ac-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

