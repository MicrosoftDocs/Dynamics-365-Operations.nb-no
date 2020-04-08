---
title: NO-00003 Betalingsformater for kunde og leverandør
description: Denne oppgaven hjelper deg med å konfigurere og vedlikeholde norske betalings-ID-er.
author: epodkolz
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCustPaymIdTable, LogisticsCountryRegionPaymentIdType_NO, CustTable, CustPaymMode, CustGroup,  CustInvoiceJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Norway
ms.author: epodkolz
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05d513099de8535f2625c27ddda441ee1845bb9b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140618"
---
# <a name="no-00003-customer-and-vendor-payment-formats"></a><span data-ttu-id="549c3-103">NO-00003 Betalingsformater for kunde og leverandør</span><span class="sxs-lookup"><span data-stu-id="549c3-103">NO-00003 Customer and vendor payment formats</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="549c3-104">Denne oppgaven hjelper deg med å konfigurere og vedlikeholde norske betalings-ID-er.</span><span class="sxs-lookup"><span data-stu-id="549c3-104">This task walks you through setting up and maintaining Norwegian payment IDs.</span></span> 



<span data-ttu-id="549c3-105">En betalingsidentifikasjon (ID) er en unik identifikator for kundebetalinger som utlignes elektronisk.</span><span class="sxs-lookup"><span data-stu-id="549c3-105">A payment identification (ID) is a unique identifier for customer payments that are settled electronically.</span></span> <span data-ttu-id="549c3-106">Den kan deles inn i ulike deler, for eksempel kundekontonummer, fakturanummer, prefiks, suffiks og ekstern referanse.</span><span class="sxs-lookup"><span data-stu-id="549c3-106">It can be divided into different parts, such as the customer account number, invoice number, prefix, suffix, and external reference.</span></span> <span data-ttu-id="549c3-107">Når du mottar en betaling fra en kunde, identifiserer betalings-IDen betalingstransaksjonen for en salgsfaktura som er mottatt fra en bank.</span><span class="sxs-lookup"><span data-stu-id="549c3-107">When you receive a payment from a customer, the payment ID identifies the payment transaction for a sales invoice that is received from a bank.</span></span>



<span data-ttu-id="549c3-108">Denne oppgaven ble opprettet med demodatafirmaet DEMF med land/område for primæradresse for juridisk enhet oppdatert til å være Norge.</span><span class="sxs-lookup"><span data-stu-id="549c3-108">This task was created using the demo data company DEMF with the country/region of legal entity primary address updated to be Norway.</span></span>


## <a name="set-up-payment-ids"></a><span data-ttu-id="549c3-109">Definer betalings-IDer</span><span class="sxs-lookup"><span data-stu-id="549c3-109">Set up payment IDs</span></span>
1. <span data-ttu-id="549c3-110">Gå til Kunder > Betalingsoppsett > Betalings-ID.</span><span class="sxs-lookup"><span data-stu-id="549c3-110">Go to Accounts receivable > Payments setup > Payment ID.</span></span>
2. <span data-ttu-id="549c3-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="549c3-111">Click New.</span></span>
3. <span data-ttu-id="549c3-112">Skriv inn en verdi i Betalings-ID-feltet.</span><span class="sxs-lookup"><span data-stu-id="549c3-112">In the Payment ID type field, type a value.</span></span>
4. <span data-ttu-id="549c3-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="549c3-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="549c3-114">Angi en verdi i feltet Lengde på betalings-ID.</span><span class="sxs-lookup"><span data-stu-id="549c3-114">In the Payment ID length field, enter a number.</span></span>
6. <span data-ttu-id="549c3-115">Angi et tall i feltet Konto fra posisjon.</span><span class="sxs-lookup"><span data-stu-id="549c3-115">In the Account from position field, enter a number.</span></span>
7. <span data-ttu-id="549c3-116">Angi et tall i feltet Konto til posisjon.</span><span class="sxs-lookup"><span data-stu-id="549c3-116">In the Account to position field, enter a number.</span></span>
8. <span data-ttu-id="549c3-117">Angi et tall i feltet Faktura fra posisjon.</span><span class="sxs-lookup"><span data-stu-id="549c3-117">In the Invoice from position field, enter a number.</span></span>
9. <span data-ttu-id="549c3-118">Angi et tall i feltet Faktura til posisjon.</span><span class="sxs-lookup"><span data-stu-id="549c3-118">In the Invoice to position field, enter a number.</span></span>
10. <span data-ttu-id="549c3-119">Velg et Modulus 10 i feltet Modulus.</span><span class="sxs-lookup"><span data-stu-id="549c3-119">In the Modulo field, select 'Modulo 10'.</span></span>
    * <span data-ttu-id="549c3-120">Velg moduluskontrollmetoden som skal beregne sjekknummeret.</span><span class="sxs-lookup"><span data-stu-id="549c3-120">Select the modulo check method to calculate the check number.</span></span> <span data-ttu-id="549c3-121">Det siste sifferet i en betalings-ID er reservert for sjekknummeret for å verifisere at betalings-IDen er gyldig.</span><span class="sxs-lookup"><span data-stu-id="549c3-121">The last digit of a payment ID is reserved for the check number to verify that the payment ID is valid.</span></span> <span data-ttu-id="549c3-122">Følgende alternativer er tilgjengelige: - Modulus 10 – Samlet lengde på betalings ID-en deles på 10.</span><span class="sxs-lookup"><span data-stu-id="549c3-122">The following options are available:     - Modulo 10 – The total length of the payment ID is divided by 10.</span></span> <span data-ttu-id="549c3-123">Resten blir sjekknummeret.</span><span class="sxs-lookup"><span data-stu-id="549c3-123">The remainder is the check number.</span></span>   <span data-ttu-id="549c3-124">- Modulus 11 – Samlet lengde på betalings-ID-en deles på 11.</span><span class="sxs-lookup"><span data-stu-id="549c3-124">- Modulo 11 – The total length of the payment ID is divided by 11.</span></span> <span data-ttu-id="549c3-125">Resten blir sjekknummeret.</span><span class="sxs-lookup"><span data-stu-id="549c3-125">The remainder is the check number.</span></span>   <span data-ttu-id="549c3-126">- (Ingen) – Sjekknummer beregnes ikke.</span><span class="sxs-lookup"><span data-stu-id="549c3-126">- (None) – No check number is calculated.</span></span>  
11. <span data-ttu-id="549c3-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="549c3-127">Click Save.</span></span>
    * <span data-ttu-id="549c3-128">Når du har lagret posten, kan du forhåndsvise den valgte betalings-ID-en i feltet Betalings-ID-test.</span><span class="sxs-lookup"><span data-stu-id="549c3-128">After saving the record, you can preview the selected payment ID in the Payment ID test field.</span></span>  
12. <span data-ttu-id="549c3-129">Gå til Kunder > Betalingsoppsett > Betalings-ID per land/område.</span><span class="sxs-lookup"><span data-stu-id="549c3-129">Go to Accounts receivable > Payments setup > Payment ID per country/region.</span></span>
13. <span data-ttu-id="549c3-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="549c3-130">Click New.</span></span>
14. <span data-ttu-id="549c3-131">Angi eller velg en verdi i Land/område-feltet.</span><span class="sxs-lookup"><span data-stu-id="549c3-131">In the Country/region field, enter or select a value.</span></span>
15. <span data-ttu-id="549c3-132">Angi eller velg en verdi i feltet Betalings-ID-type.</span><span class="sxs-lookup"><span data-stu-id="549c3-132">In the Payment ID type field, enter or select a value.</span></span>
16. <span data-ttu-id="549c3-133">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="549c3-133">Click Save.</span></span>

## <a name="attach-the-payment-id"></a><span data-ttu-id="549c3-134">Tilknytte betalings-ID-en</span><span class="sxs-lookup"><span data-stu-id="549c3-134">Attach the payment ID</span></span>
1. <span data-ttu-id="549c3-135">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="549c3-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="549c3-136">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="549c3-136">Use the Quick Filter to find records.</span></span> <span data-ttu-id="549c3-137">Du kan for eksempel filtrere på Konto-feltet med verdien DE-010.</span><span class="sxs-lookup"><span data-stu-id="549c3-137">For example, filter on the Account field with a value of 'DE-010'.</span></span>
3. <span data-ttu-id="549c3-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="549c3-138">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="549c3-139">Utvid delen Betalingstandarder.</span><span class="sxs-lookup"><span data-stu-id="549c3-139">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="549c3-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="549c3-140">Click Edit.</span></span>
6. <span data-ttu-id="549c3-141">Angi eller velg en verdi i feltet Betalings-ID-type.</span><span class="sxs-lookup"><span data-stu-id="549c3-141">In the Payment ID type field, enter or select a value.</span></span>
7. <span data-ttu-id="549c3-142">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="549c3-142">Click Save.</span></span>
8. <span data-ttu-id="549c3-143">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="549c3-143">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
9. <span data-ttu-id="549c3-144">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="549c3-144">Use the Quick Filter to find records.</span></span> <span data-ttu-id="549c3-145">Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien ELEKTRONISK.</span><span class="sxs-lookup"><span data-stu-id="549c3-145">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
10. <span data-ttu-id="549c3-146">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="549c3-146">Click Edit.</span></span>
11. <span data-ttu-id="549c3-147">Utvid delen Betalingskontroll.</span><span class="sxs-lookup"><span data-stu-id="549c3-147">Expand the Payment control section.</span></span>
12. <span data-ttu-id="549c3-148">Angi eller velg en verdi i feltet Betalings-ID-type.</span><span class="sxs-lookup"><span data-stu-id="549c3-148">In the Payment ID type field, enter or select a value.</span></span>
13. <span data-ttu-id="549c3-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="549c3-149">Click Save.</span></span>
14. <span data-ttu-id="549c3-150">Gå til Kunder > Oppsett > Kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="549c3-150">Go to Accounts receivable > Setup > Customer groups.</span></span>
15. <span data-ttu-id="549c3-151">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="549c3-151">Click Edit.</span></span>
16. <span data-ttu-id="549c3-152">Angi eller velg en verdi i feltet Betalings-ID-type.</span><span class="sxs-lookup"><span data-stu-id="549c3-152">In the Payment ID type field, enter or select a value.</span></span>
17. <span data-ttu-id="549c3-153">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="549c3-153">Click Save.</span></span>

## <a name="update-the-payment-id"></a><span data-ttu-id="549c3-154">Oppdatere betalings-ID-en</span><span class="sxs-lookup"><span data-stu-id="549c3-154">Update the payment ID</span></span>
1. <span data-ttu-id="549c3-155">Gå til Kunder > Periodiske oppgaver > Oppdater betalings-ID for faktura.</span><span class="sxs-lookup"><span data-stu-id="549c3-155">Go to Accounts receivable > Periodic tasks > Update invoice payment ID.</span></span>
2. <span data-ttu-id="549c3-156">Merk av for Slett betalings-ID hvis du vil slette betalings-ID-informasjon fra alle dokumenter.</span><span class="sxs-lookup"><span data-stu-id="549c3-156">Select the Delete payment ID check box to delete the payment ID information from all documents</span></span>
    * <span data-ttu-id="549c3-157">Dette alternativet bør bare brukes når du vil fjerne eller oppdatere betalings-ID-er for dokumenter som fikk tilordnet betalings-ID-er.</span><span class="sxs-lookup"><span data-stu-id="549c3-157">This option should be used only when you want to remove or update Payment IDs for documents that got Payment IDs assigned.</span></span> <span data-ttu-id="549c3-158">Du vil se en dialogboks der du kan slette betalings-ID fra bestemte dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="549c3-158">You will be offered a dialog to delete Payment ID from specific type of documents.</span></span>  
3. <span data-ttu-id="549c3-159">Velg Ja i feltet Oppdater betalings-ID for faktura.</span><span class="sxs-lookup"><span data-stu-id="549c3-159">Select Yes in the Update invoice payment ID field.</span></span>
4. <span data-ttu-id="549c3-160">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="549c3-160">Click OK.</span></span>
5. <span data-ttu-id="549c3-161">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="549c3-161">Click Yes.</span></span>
6. <span data-ttu-id="549c3-162">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="549c3-162">Click Yes.</span></span>
7. <span data-ttu-id="549c3-163">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="549c3-163">Click Yes.</span></span>
8. <span data-ttu-id="549c3-164">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="549c3-164">Click Yes.</span></span>

## <a name="view-the-payment-id"></a><span data-ttu-id="549c3-165">Vise betalings-ID-en</span><span class="sxs-lookup"><span data-stu-id="549c3-165">View the payment ID</span></span>
1. <span data-ttu-id="549c3-166">Gå til Kundereskontro > Forespørsler og rapporter > Fakturaer > Fakturajournal.</span><span class="sxs-lookup"><span data-stu-id="549c3-166">Go to Accounts receivable > Inquiries and reports > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="549c3-167">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="549c3-167">Click Show filters.</span></span>
3. <span data-ttu-id="549c3-168">Bruk følgende filtre: Angi en filterverdi for "" i feltet "Betalings-ID" ved hjelp av filteroperatoren "er ikke".</span><span class="sxs-lookup"><span data-stu-id="549c3-168">Apply the following filters: Enter a filter value of "" on the "Payment ID" field using the "is not" filter operator.</span></span>

