---
title: NO-00002 Kundebetaling basert på betalings-ID
description: Denne oppgaven hjelper deg med å konfigurere og vedlikeholde norske betalings-ID-er.
author: EvgenyPopovMBS
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
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22a6b781bf7faf1ab32d8a7855d6ea6421d4784e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183805"
---
# <a name="no-00002-customer-payment-based-on-payment-id"></a><span data-ttu-id="fba3c-103">NO-00002 Kundebetaling basert på betalings-ID</span><span class="sxs-lookup"><span data-stu-id="fba3c-103">NO-00002 Customer payment based on payment ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fba3c-104">Denne oppgaven hjelper deg med å konfigurere og vedlikeholde norske betalings-ID-er.</span><span class="sxs-lookup"><span data-stu-id="fba3c-104">This task walks you through setting up and maintaining Norwegian payment IDs.</span></span> 

<span data-ttu-id="fba3c-105">En betalingsidentifikasjon (ID) er en unik identifikator for kundebetalinger som utlignes elektronisk.</span><span class="sxs-lookup"><span data-stu-id="fba3c-105">A payment identification (ID) is a unique identifier for customer payments that are settled electronically.</span></span> <span data-ttu-id="fba3c-106">Den kan deles inn i ulike deler, for eksempel kundekontonummer, fakturanummer, prefiks, suffiks og ekstern referanse.</span><span class="sxs-lookup"><span data-stu-id="fba3c-106">It can be divided into different parts, such as the customer account number, invoice number, prefix, suffix, and external reference.</span></span> <span data-ttu-id="fba3c-107">Når du mottar en betaling fra en kunde, identifiserer betalings-IDen betalingstransaksjonen for en salgsfaktura som er mottatt fra en bank.</span><span class="sxs-lookup"><span data-stu-id="fba3c-107">When you receive a payment from a customer, the payment ID identifies the payment transaction for a sales invoice that is received from a bank.</span></span>

<span data-ttu-id="fba3c-108">Denne oppgaven ble opprettet med demodatafirmaet DEMF med land/område for primæradresse for juridisk enhet oppdatert til å være Norge.</span><span class="sxs-lookup"><span data-stu-id="fba3c-108">This task was created using the demo data company DEMF with the country/region of legal entity primary address updated to be Norway.</span></span> <span data-ttu-id="fba3c-109">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="fba3c-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-a-payment-id"></a><span data-ttu-id="fba3c-110">Konfigurere en betalings-ID</span><span class="sxs-lookup"><span data-stu-id="fba3c-110">Set up a payment ID</span></span>
1. <span data-ttu-id="fba3c-111">Gå til Kunder > Betalingsoppsett > Betalings-ID.</span><span class="sxs-lookup"><span data-stu-id="fba3c-111">Go to Accounts receivable > Payments setup > Payment ID.</span></span>
2. <span data-ttu-id="fba3c-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fba3c-112">Click New.</span></span>
3. <span data-ttu-id="fba3c-113">Skriv inn en verdi i Betalings-ID-feltet.</span><span class="sxs-lookup"><span data-stu-id="fba3c-113">In the Payment ID type field, type a value.</span></span>
4. <span data-ttu-id="fba3c-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="fba3c-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="fba3c-115">Angi en verdi i feltet Lengde på betalings-ID.</span><span class="sxs-lookup"><span data-stu-id="fba3c-115">In the Payment ID length field, enter a number.</span></span>
6. <span data-ttu-id="fba3c-116">Angi et tall i feltet Konto fra posisjon.</span><span class="sxs-lookup"><span data-stu-id="fba3c-116">In the Account from position field, enter a number.</span></span>
7. <span data-ttu-id="fba3c-117">Angi et tall i feltet Konto til posisjon.</span><span class="sxs-lookup"><span data-stu-id="fba3c-117">In the Account to position field, enter a number.</span></span>
8. <span data-ttu-id="fba3c-118">Angi et tall i feltet Faktura fra posisjon.</span><span class="sxs-lookup"><span data-stu-id="fba3c-118">In the Invoice from position field, enter a number.</span></span>
9. <span data-ttu-id="fba3c-119">Angi et tall i feltet Faktura til posisjon.</span><span class="sxs-lookup"><span data-stu-id="fba3c-119">In the Invoice to position field, enter a number.</span></span>
10. <span data-ttu-id="fba3c-120">Velg et Modulus 10 i feltet Modulus.</span><span class="sxs-lookup"><span data-stu-id="fba3c-120">In the Modulo field, select 'Modulo 10'.</span></span>
    * <span data-ttu-id="fba3c-121">Velg moduluskontrollmetoden som skal beregne sjekknummeret.</span><span class="sxs-lookup"><span data-stu-id="fba3c-121">Select the modulo check method to calculate the check number.</span></span> <span data-ttu-id="fba3c-122">Det siste sifferet i en betalings-ID er reservert for sjekknummeret for å verifisere at betalings-IDen er gyldig.</span><span class="sxs-lookup"><span data-stu-id="fba3c-122">The last digit of a payment ID is reserved for the check number to verify that the payment ID is valid.</span></span> <span data-ttu-id="fba3c-123">Følgende alternativer er tilgjengelige: - Modulus 10 – Samlet lengde på betalings ID-en deles på 10.</span><span class="sxs-lookup"><span data-stu-id="fba3c-123">The following options are available:     Modulo 10 – The total length of the payment ID is divided by 10.</span></span> <span data-ttu-id="fba3c-124">Resten blir sjekknummeret.</span><span class="sxs-lookup"><span data-stu-id="fba3c-124">The remainder is the check number.</span></span>   <span data-ttu-id="fba3c-125">Modulus 11 – Samlet lengde på betalings-ID-en deles på 11.</span><span class="sxs-lookup"><span data-stu-id="fba3c-125">Modulo 11 – The total length of the payment ID is divided by 11.</span></span> <span data-ttu-id="fba3c-126">Resten blir sjekknummeret.</span><span class="sxs-lookup"><span data-stu-id="fba3c-126">The remainder is the check number.</span></span>   <span data-ttu-id="fba3c-127">- (Ingen) – Sjekknummer beregnes ikke.</span><span class="sxs-lookup"><span data-stu-id="fba3c-127">- (None) – No check number is calculated.</span></span>  
11. <span data-ttu-id="fba3c-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fba3c-128">Click Save.</span></span>
    * <span data-ttu-id="fba3c-129">Når du har lagret posten, kan du forhåndsvise den valgte betalings-ID-en i feltet Betalings-ID-test.</span><span class="sxs-lookup"><span data-stu-id="fba3c-129">After saving the record, you can preview the selected payment ID in the Payment ID test field.</span></span>  
12. <span data-ttu-id="fba3c-130">Gå til Kunder > Betalingsoppsett > Betalings-ID per land/område.</span><span class="sxs-lookup"><span data-stu-id="fba3c-130">Go to Accounts receivable > Payments setup > Payment ID per country/region.</span></span>
13. <span data-ttu-id="fba3c-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fba3c-131">Click New.</span></span>
14. <span data-ttu-id="fba3c-132">Angi eller velg en verdi i Land/område-feltet.</span><span class="sxs-lookup"><span data-stu-id="fba3c-132">In the Country/region field, enter or select a value.</span></span>
15. <span data-ttu-id="fba3c-133">Angi eller velg en verdi i feltet Betalings-ID-type.</span><span class="sxs-lookup"><span data-stu-id="fba3c-133">In the Payment ID type field, enter or select a value.</span></span>
16. <span data-ttu-id="fba3c-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fba3c-134">Click Save.</span></span>

## <a name="attach-a-payment-id-to-a-customer"></a><span data-ttu-id="fba3c-135">Knytte en betalings-ID til en kunde</span><span class="sxs-lookup"><span data-stu-id="fba3c-135">Attach a payment ID to a customer</span></span>
1. <span data-ttu-id="fba3c-136">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="fba3c-136">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="fba3c-137">Bruk hurtigfilteret til å filtrere på Konto-feltet med en verdi lik DE-010.</span><span class="sxs-lookup"><span data-stu-id="fba3c-137">Use the Quick Filter to filter on the Account field with a value of 'DE-010'.</span></span>
3. <span data-ttu-id="fba3c-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fba3c-138">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fba3c-139">Utvid delen Betalingstandarder.</span><span class="sxs-lookup"><span data-stu-id="fba3c-139">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="fba3c-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="fba3c-140">Click Edit.</span></span>
6. <span data-ttu-id="fba3c-141">Angi eller velg en verdi i feltet Betalings-ID-type.</span><span class="sxs-lookup"><span data-stu-id="fba3c-141">In the Payment ID type field, enter or select a value.</span></span>
7. <span data-ttu-id="fba3c-142">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fba3c-142">Click Save.</span></span>
8. <span data-ttu-id="fba3c-143">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="fba3c-143">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
9. <span data-ttu-id="fba3c-144">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="fba3c-144">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fba3c-145">Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien ELEKTRONISK.</span><span class="sxs-lookup"><span data-stu-id="fba3c-145">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
10. <span data-ttu-id="fba3c-146">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="fba3c-146">Click Edit.</span></span>
11. <span data-ttu-id="fba3c-147">Utvid delen Betalingskontroll.</span><span class="sxs-lookup"><span data-stu-id="fba3c-147">Expand the Payment control section.</span></span>
12. <span data-ttu-id="fba3c-148">Angi eller velg en verdi i feltet Betalings-ID-type.</span><span class="sxs-lookup"><span data-stu-id="fba3c-148">In the Payment ID type field, enter or select a value.</span></span>
13. <span data-ttu-id="fba3c-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fba3c-149">Click Save.</span></span>
14. <span data-ttu-id="fba3c-150">Gå til Kunder > Oppsett > Kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="fba3c-150">Go to Accounts receivable > Setup > Customer groups.</span></span>
15. <span data-ttu-id="fba3c-151">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="fba3c-151">Click Edit.</span></span>
16. <span data-ttu-id="fba3c-152">Angi eller velg en verdi i feltet Betalings-ID-type.</span><span class="sxs-lookup"><span data-stu-id="fba3c-152">In the Payment ID type field, enter or select a value.</span></span>
17. <span data-ttu-id="fba3c-153">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fba3c-153">Click Save.</span></span>

## <a name="update-the-payment-id"></a><span data-ttu-id="fba3c-154">Oppdatere betalings-ID-en</span><span class="sxs-lookup"><span data-stu-id="fba3c-154">Update the payment ID</span></span>
1. <span data-ttu-id="fba3c-155">Gå til Kunder > Periodiske oppgaver > Oppdater betalings-ID for faktura.</span><span class="sxs-lookup"><span data-stu-id="fba3c-155">Go to Accounts receivable > Periodic tasks > Update invoice payment ID.</span></span>
2. <span data-ttu-id="fba3c-156">Merk av for Slett betalings-ID hvis du vil slette betalings-ID-informasjon fra alle dokumenter.</span><span class="sxs-lookup"><span data-stu-id="fba3c-156">Select the Delete payment ID check box to delete the payment ID information from all documents</span></span>
    * <span data-ttu-id="fba3c-157">Dette alternativet bør bare brukes når du vil fjerne eller oppdatere betalings-ID-er for dokumenter som fikk tilordnet betalings-ID-er.</span><span class="sxs-lookup"><span data-stu-id="fba3c-157">This option should be used only when you want to remove or update Payment IDs for documents that got Payment IDs assigned.</span></span> <span data-ttu-id="fba3c-158">Du vil se en dialogboks der du kan slette betalings-ID fra bestemte dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="fba3c-158">You will be offered a dialog to delete Payment ID from specific type of documents.</span></span>  
3. <span data-ttu-id="fba3c-159">Velg Ja i feltet Oppdater betalings-ID for faktura.</span><span class="sxs-lookup"><span data-stu-id="fba3c-159">Select Yes in the Update invoice payment ID field.</span></span>
4. <span data-ttu-id="fba3c-160">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fba3c-160">Click OK.</span></span>
5. <span data-ttu-id="fba3c-161">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="fba3c-161">Click Yes.</span></span>
6. <span data-ttu-id="fba3c-162">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="fba3c-162">Click Yes.</span></span>
7. <span data-ttu-id="fba3c-163">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="fba3c-163">Click Yes.</span></span>
8. <span data-ttu-id="fba3c-164">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="fba3c-164">Click Yes.</span></span>

## <a name="view-the-payment-id"></a><span data-ttu-id="fba3c-165">Vise betalings-ID-en</span><span class="sxs-lookup"><span data-stu-id="fba3c-165">View the payment ID</span></span>
1. <span data-ttu-id="fba3c-166">Gå til Kundereskontro > Forespørsler og rapporter > Fakturaer > Fakturajournal.</span><span class="sxs-lookup"><span data-stu-id="fba3c-166">Go to Accounts receivable > Inquiries and reports > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="fba3c-167">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="fba3c-167">Click Show filters.</span></span>
3. <span data-ttu-id="fba3c-168">Bruk følgende filtre: Angi en filterverdi for "" i feltet "Betalings-ID" ved hjelp av filteroperatoren "er ikke".</span><span class="sxs-lookup"><span data-stu-id="fba3c-168">Apply the following filters: Enter a filter value of "" on the "Payment ID" field using the "is not" filter operator.</span></span>

