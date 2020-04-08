---
title: Opprette betalinger for en kunde som har avtalegiromandater
description: Denne prosedyren viser hvordan du genererer en betalingsfil for avtalegiro for ISO20022 for en kunde som har konfigurert AvtaleGiro og en faktura som skal betales.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a4714f1f1b24554684219fc1d766b4b87cff7bb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141609"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="72786-103">Opprette betalinger for en kunde som har avtalegiromandater</span><span class="sxs-lookup"><span data-stu-id="72786-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72786-104">Denne prosedyren viser hvordan du genererer en betalingsfil for avtalegiro for ISO20022 for en kunde som har konfigurert AvtaleGiro og en faktura som skal betales.</span><span class="sxs-lookup"><span data-stu-id="72786-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="72786-105">Oppretting og bokføring av en faktura er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="72786-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="72786-106">I stedet for at en faktura må betales, kan du velge et mandat i en journal før en betalingsfil genereres, for å støtte et scenario med kundeforskuddsbetaling.</span><span class="sxs-lookup"><span data-stu-id="72786-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="72786-107">Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="72786-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="72786-108">Dette er den femte av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="72786-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="72786-109">Før du kan gjøre denne oppgaven, må du fullføre de tidligere oppgavene.</span><span class="sxs-lookup"><span data-stu-id="72786-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="72786-110">Du må først importere elektroniske rapporteringskonfigurasjoner for kundebetaling, konfigurere metoder for betalinger, og du må definere informasjonen om firmaet og kunden.</span><span class="sxs-lookup"><span data-stu-id="72786-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="72786-111">Postere en fritekstfaktura AvtaleGiro-informasjon</span><span class="sxs-lookup"><span data-stu-id="72786-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="72786-112">Gå til Kunder > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="72786-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="72786-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="72786-113">Click New.</span></span>
3. <span data-ttu-id="72786-114">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="72786-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="72786-115">Velg for eksempel DE-010.</span><span class="sxs-lookup"><span data-stu-id="72786-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="72786-116">Angi eller velg en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="72786-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="72786-117">For eksempel.</span><span class="sxs-lookup"><span data-stu-id="72786-117">For example.</span></span> <span data-ttu-id="72786-118">Velg elektronisk.</span><span class="sxs-lookup"><span data-stu-id="72786-118">select Electronic.</span></span>  
5. <span data-ttu-id="72786-119">Angi eller velg en verdi i feltet ID for avtalegiromandat.</span><span class="sxs-lookup"><span data-stu-id="72786-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="72786-120">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="72786-120">Click Add line.</span></span>
7. <span data-ttu-id="72786-121">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="72786-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="72786-122">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="72786-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="72786-123">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="72786-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="72786-124">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="72786-124">Click Post.</span></span>
11. <span data-ttu-id="72786-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="72786-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="72786-126">Opprette en betaling</span><span class="sxs-lookup"><span data-stu-id="72786-126">Create a payment</span></span>
1. <span data-ttu-id="72786-127">Gå til Kunder > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="72786-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="72786-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="72786-128">Click New.</span></span>
3. <span data-ttu-id="72786-129">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="72786-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="72786-130">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="72786-130">Click Lines.</span></span>
5. <span data-ttu-id="72786-131">Klikk Betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="72786-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="72786-132">Klikk Opprett betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="72786-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="72786-133">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="72786-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="72786-134">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="72786-134">Click Filter.</span></span>
9. <span data-ttu-id="72786-135">I listen velger du raden for Kundetransaksjoner-tabellen og Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="72786-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="72786-136">Du kan bruke hvilke som helst kriterier for valg av kundetransaksjoner for å betale.</span><span class="sxs-lookup"><span data-stu-id="72786-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="72786-137">I dette eksemplet kan du bruke elektronisk som betalingsmetode for å filtrere transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="72786-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="72786-138">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="72786-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="72786-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="72786-139">Click OK.</span></span>
12. <span data-ttu-id="72786-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="72786-140">Click OK.</span></span>
13. <span data-ttu-id="72786-141">Klikk Opprett betalinger.</span><span class="sxs-lookup"><span data-stu-id="72786-141">Click Create payments.</span></span>
