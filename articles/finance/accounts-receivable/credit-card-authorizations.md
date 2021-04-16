---
title: Oppsett av kredittkort, autorisasjon og registrering
description: Denne artikkelen gir en oversikt over kredittkortautorisering i Microsoft Dynamics 365 Finance. Den inneholder informasjon om å sette opp en betalingstjeneste, legge til et kredittkort til en salgsordre og annullere en autorisering.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b59d54df9427961e2c4fb6f1387646d6fe8dfc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837135"
---
# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="7ccc2-104">Oppsett av kredittkort, autorisasjon og registrering</span><span class="sxs-lookup"><span data-stu-id="7ccc2-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ccc2-105">Denne artikkelen gir en oversikt over kredittkortautorisering i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="7ccc2-106">Den inneholder informasjon om å sette opp en betalingstjeneste, legge til et kredittkort til en salgsordre og annullere en autorisering.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="7ccc2-107">Konfigurere kredittkortbetalingstjenesten</span><span class="sxs-lookup"><span data-stu-id="7ccc2-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="7ccc2-108">Hvis du vil bruke kredittkort, må du definere og aktivere en betalingstjeneste på siden Betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="7ccc2-109">En betalingstjeneste fungerer som et bindeledd mellom den juridiske enheten og banken som behandler kundens kredittkortbelastninger.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="7ccc2-110">Du må kontakte en kredittkortleverandør som er oppført i feltet Betalingskobling og sette opp en konto hos denne leverandøren.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="7ccc2-111">Deretter må du definere de andre alternativene på siden Betalingstjenester, definere kredittkorttyper for American Express, Discover, MasterCard og Discover på siden Kredittkorttyper, og aktivere leverandøren som standardleverandøren.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="7ccc2-112">Du må også følge disse trinnene for å fullføre oppsettet:</span><span class="sxs-lookup"><span data-stu-id="7ccc2-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="7ccc2-113">Angi parametere for å bruke kredittkortautoriseringer på siden Kundeparametere.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="7ccc2-114">På siden Betalingsbetingelser defineres betalingsbetingelsene for kredittkort.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="7ccc2-115">Velg Kredittkort i Betalingstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="7ccc2-116">Angi kredittkortinformasjonen for kunder på siden Kundekredittkort.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="7ccc2-117">Legge til et nytt kredittkort</span><span class="sxs-lookup"><span data-stu-id="7ccc2-117">Adding a new credit card</span></span>
<span data-ttu-id="7ccc2-118">Du kan opprette nye kredittkortoppføringer på Kunder-siden ved hjelp av Kunde, Oppsett, Kredittkort.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="7ccc2-119">Du kan også opprette kredittkortposter når du registrerer salgsordrer på siden Salgsordre ved hjelp av Behandle, Kunde, Kredittkort, Registrer.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>

<a name="adding-a-credit-card-to-a-sales-order"></a><span data-ttu-id="7ccc2-120">Legge til et kredittkort i en salgsordre</span><span class="sxs-lookup"><span data-stu-id="7ccc2-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="7ccc2-121">Du kan legge til et kredittkort i en salgsordre ved å velge et kredittkort i kredittkortoppslaget i hurtigfanen Pris og rabatter på siden Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="7ccc2-122">Velg Kredittkort og Autoriser i kategorien Behandle i handlingsruten for å starte godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>

<a name="authorizing-a-credit-card"></a><span data-ttu-id="7ccc2-123">Autorisere et kredittkort</span><span class="sxs-lookup"><span data-stu-id="7ccc2-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="7ccc2-124">Når et kredittkort autoriseres, verifiseres kredittkortnummeret og kredittkortinnehaverens navn, og tilgjengelig kredittkortsaldo kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="7ccc2-125">Du kan også autorisere verdien for kortbekreftelse og kortinnehaverens adresse.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="7ccc2-126">Deretter trekkes fakturabeløpet fra kundens tilgjengelige kredittkortsaldo.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="7ccc2-127">Betalingstjenesten sender informasjon som angir om kredittkortet er godkjent eller ikke.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="7ccc2-128">Når salgsordren faktureres, belastes kredittkortet med fakturabeløpet.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="7ccc2-129">Verdi for kortbekreftelse</span><span class="sxs-lookup"><span data-stu-id="7ccc2-129">Card verification value</span></span>

<span data-ttu-id="7ccc2-130">Du kan kreve verdi for kortbekreftelse, som noen ganger kalles kortets sikkerhetskode.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="7ccc2-131">Dette er en firesifret verdi for American Express.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="7ccc2-132">Discover, MasterCard og Visa har en tresifret verdi.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="7ccc2-133">Adressebekreftelse</span><span class="sxs-lookup"><span data-stu-id="7ccc2-133">Address verification</span></span>

<span data-ttu-id="7ccc2-134">Informasjon om adressebekreftelse sendes alltid til betalingsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="7ccc2-135">Du kan bestemme hvor mye informasjon som er nødvendig for at en transaksjon skal godtas.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="7ccc2-136">Husk å ta kontakt med leverandøren din for å finne ut om de godtar denne informasjonen.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="7ccc2-137">Her er alternativene for adressebekreftelse:</span><span class="sxs-lookup"><span data-stu-id="7ccc2-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="7ccc2-138">**Alltid godta transaksjon** – godta transaksjonen uavhengig av resultatet av adressebekreftelse.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="7ccc2-139">**Kontoinnehaver** – sammenlign kortinnehaverens navn fra transaksjonen med kredittkortfirmaets informasjon.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="7ccc2-140">**Faktureringsadresse** – sammenlign kortinnehaverens navn og faktureringsadresse fra transaksjonen med kredittkortfirmaets informasjon.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="7ccc2-141">**Postnummer for fakturering** – sammenlign kortholderen navn, faktureringsadresse og postnummer fra transaksjonen med kredittkortfirmaets informasjon.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="7ccc2-142">Datastøtte</span><span class="sxs-lookup"><span data-stu-id="7ccc2-142">Data support</span></span>
<span data-ttu-id="7ccc2-143">For hver kredittkorttype som støttes, kan du angi nivået for datastøtte.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="7ccc2-144">Nivået kontrollerer hvor mye informasjon om en transaksjon som overføres til betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="7ccc2-145">Husk å ta kontakt med leverandøren din for å finne ut om de kan gi denne informasjonen.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="7ccc2-146">Her er alternativene for nivå for datastøtte:</span><span class="sxs-lookup"><span data-stu-id="7ccc2-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="7ccc2-147">**Nivå 1** – overfør transaksjonsdatoen, transaksjonsbeløpet og beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="7ccc2-148">**Nivå 2** – overfør all informasjon på nivå 1, pluss leverings-og forhandleradresser og avgiftsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="7ccc2-149">**Nivå 3** – overfør all nivå 2-informasjon, pluss ordrelinjeinformasjon.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="7ccc2-150">Delbetalinger</span><span class="sxs-lookup"><span data-stu-id="7ccc2-150">Partial payments</span></span>
<span data-ttu-id="7ccc2-151">Hvis du sender en del av en ordre, registreres beløpet for den delvise ordren, og autorisasjonen, som var for beløpet for hele ordren, lukkes.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="7ccc2-152">En ny godkjenning sendes deretter for det gjenstående beløpet for ordren som ikke er levert.</span><span class="sxs-lookup"><span data-stu-id="7ccc2-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="7ccc2-153">Annullere en autorisasjon </span><span class="sxs-lookup"><span data-stu-id="7ccc2-153">Voiding an authorization</span></span>
<span data-ttu-id="7ccc2-154">Hvis du vil annullere en kredittkortautorisasjon, kan du endre betalingsmåten til en annen metode som ikke har en type kredittkort</span><span class="sxs-lookup"><span data-stu-id="7ccc2-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]