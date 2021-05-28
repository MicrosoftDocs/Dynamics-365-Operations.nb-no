---
title: Kundebetalinger
description: Dette emnet beskriver hvordan du konfigurerer og behandler kundeforskuddsbetalinger (kalles også kundeinnskudd).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019426"
---
# <a name="customer-prepayments"></a><span data-ttu-id="ba95f-103">Kundebetalinger</span><span class="sxs-lookup"><span data-stu-id="ba95f-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba95f-104">Kundeforskuddsbetalinger brukes når du mottar en betaling fra en kunde, men det er ingen faktura som betalingen kan utlignes mot.</span><span class="sxs-lookup"><span data-stu-id="ba95f-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="ba95f-105">Denne typen betalinger omtales også som kundeinnbetalinger.</span><span class="sxs-lookup"><span data-stu-id="ba95f-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="ba95f-106">Prosessen med å definere og arbeide med kundeforskuddsbetalinger består av følgende grunnleggende trinn.</span><span class="sxs-lookup"><span data-stu-id="ba95f-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="ba95f-107">Opprett en kundeposteringsprofil for forskuddsbetalinger.</span><span class="sxs-lookup"><span data-stu-id="ba95f-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="ba95f-108">Angi parameteren **Posteringsprofil ved journalbilag for forskuddsbetaling**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="ba95f-109">Opprett en kundebetalingsjournal, og merk av for **Journalbilag for forskuddsbetaling** på hver linje.</span><span class="sxs-lookup"><span data-stu-id="ba95f-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="ba95f-110">Poster kundebetalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="ba95f-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="ba95f-111">Når en faktura er generert, utligner du forskuddsbetalingen med den ved å bruke siden **Utlign åpne transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="ba95f-112">Opprette en kundeposteringsprofil for forskuddsbetalinger</span><span class="sxs-lookup"><span data-stu-id="ba95f-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="ba95f-113">Når du godtar forskuddsbetaling eller innbetalinger fra kundene før varer eller tjenester leveres, eller før det finnes en faktura i systemet, ønsker du vanligvis å registrere kontanter som gjeld i stedet for aktiva i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="ba95f-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="ba95f-114">Kravene til registrering av disse beløpene i økonomimodulen kan imidlertid variere, avhengig av landet eller regionen du bes om.</span><span class="sxs-lookup"><span data-stu-id="ba95f-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="ba95f-115">Husk derfor å ta kontakt med regnskapsførere for eventuelle lokale regler som gjelder.</span><span class="sxs-lookup"><span data-stu-id="ba95f-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="ba95f-116">Generelt sett er prosessen for oppretting av en posteringsprofil som kan brukes for forskuddsbetalinger, den samme som prosessen for oppretting av andre posteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="ba95f-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="ba95f-117">Hovedforskjellen er hovedkontoen du velger i **Samlekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="ba95f-118">Hvis du vil ha mer informasjon, kan du se [Kundeposteringsprofiler](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="ba95f-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="ba95f-119">Definere parametere for kundeforskuddsbetalinger</span><span class="sxs-lookup"><span data-stu-id="ba95f-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="ba95f-120">Det er to primære kundeparametere du må vurdere når du konfigurerer systemet for kundeforskuddsbetalinger.</span><span class="sxs-lookup"><span data-stu-id="ba95f-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="ba95f-121">Gjør følgende for å konfigurere parametere.</span><span class="sxs-lookup"><span data-stu-id="ba95f-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="ba95f-122">Gå til **Kunder \> Oppsett \> Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="ba95f-123">Valgfritt: I kategorien **Finans og merverdiavgift** i hurtigfanen **Betaling** angir alternativet **Merverdiavgift på journalbilag for forskuddsbetaling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="ba95f-124">I feltet **Posteringsprofil ved journalbilag for forskuddsbetaling**, velg kundeposteringsprofilen som skal brukes når kundeforskuddsbetalinger posteres.</span><span class="sxs-lookup"><span data-stu-id="ba95f-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="ba95f-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ba95f-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="ba95f-126">Opprette kundeforskuddsbetalingsbilag</span><span class="sxs-lookup"><span data-stu-id="ba95f-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="ba95f-127">Når du oppretter kundebetalingsjournalen, må du sette alternativet **Journalbilag for forskuddsbetaling** til **Ja** på siden **Kundebetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="ba95f-128">Følg disse trinnene for å opprette en kundeforhåndsbetaling.</span><span class="sxs-lookup"><span data-stu-id="ba95f-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="ba95f-129">Gå til **Kunder \> Betalinger \> Kundebetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="ba95f-130">Velg **Ny** for å opprette en journal.</span><span class="sxs-lookup"><span data-stu-id="ba95f-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="ba95f-131">Velg journalnavnet som skal brukes, i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ba95f-132">Hvis du setter alternativet **Merverdiavgift på journalbilag for forskuddsbetaling** til **Ja** i den forrige fremgangsmåten, må du velge et journalnavn der parameteren **Beløp inkluderer mva** er valgt.</span><span class="sxs-lookup"><span data-stu-id="ba95f-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="ba95f-133">Valgfritt: Skriv inn en detaljert beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="ba95f-134">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-134">Select **Lines**.</span></span>
6. <span data-ttu-id="ba95f-135">Hvis det ikke finnes en tom linje, velger du **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="ba95f-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="ba95f-136">I feltet **Dato** angir du datoen da forskuddsbetalingen skal posteres.</span><span class="sxs-lookup"><span data-stu-id="ba95f-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="ba95f-137">Velg kunden for forskuddsbetalingen i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="ba95f-138">Valgfritt: Skriv inn en detaljert beskrivelse av transaksjonen i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="ba95f-139">Angi beløpet for forhåndsbetalingen i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="ba95f-140">Velg kontoen du vil motpostere betalingen til, i **Motkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="ba95f-141">Du kan for eksempel velge banken eller hovedkontoen som betalingen skal posteres til.</span><span class="sxs-lookup"><span data-stu-id="ba95f-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="ba95f-142">Velg kundens betalingsmåte i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="ba95f-143">Sett alternativet **Journalbilag for forskuddsbetaling** i kategorien **Betaling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="ba95f-144">Gjenta trinn 7 til og med 13 for hver ekstra forskuddsbetaling som må posteres.</span><span class="sxs-lookup"><span data-stu-id="ba95f-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="ba95f-145">Velg **Poster** for å fullføre journalen.</span><span class="sxs-lookup"><span data-stu-id="ba95f-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="ba95f-146">Utligne forskuddsbetalinger med fakturaer</span><span class="sxs-lookup"><span data-stu-id="ba95f-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="ba95f-147">Du kan bruke arbeidsområdet for **Kundebetalinger** til enkelt å finne og utligne betalinger som ikke har blitt helt utlignet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="ba95f-148">Velg flisen **Kundebetalinger** på **Start**-instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="ba95f-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="ba95f-149">Søk etter og velg betalingen som skal utlignes, i kategorien **Forfalte fakturaer** i **Kundetransaksjoner**-delen.</span><span class="sxs-lookup"><span data-stu-id="ba95f-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="ba95f-150">Velg **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="ba95f-151">Merk av for **Merk** for fakturaen og betalingen som skal utlignes.</span><span class="sxs-lookup"><span data-stu-id="ba95f-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="ba95f-152">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="ba95f-152">Select **Post**.</span></span>

<span data-ttu-id="ba95f-153">Hvis du vil ha mer informasjon om hvordan du utligner åpne transaksjoner, kan du se [Oversikt over utligning](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ba95f-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
