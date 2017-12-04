--- 
title: Definere kunders bankkontoer for ISO20022-avtalegiroer
description: "Dette hjelper deg med å definere en kundebankkonto og et avtalegiromandat for kunde som kreves for å generere kundebetalingsfilen som ISO20022-avtalegiro."
author: mrolecki
manager: AnnBe
ms.date: 10/31/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 22fadf126dfa884520bc2fe6f94bc3fe3b612f77
ms.openlocfilehash: 86c3f62e17d4955c12d09b512624eb5f576a9cd3
ms.contentlocale: nb-no
ms.lasthandoff: 10/31/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="ee11e-103">Definere kunders bankkontoer for ISO20022-avtalegiroer</span><span class="sxs-lookup"><span data-stu-id="ee11e-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee11e-104">Dette hjelper deg med å definere en kundebankkonto og et avtalegiromandat for kunde som kreves for å generere kundebetalingsfilen som ISO20022-avtalegiro.</span><span class="sxs-lookup"><span data-stu-id="ee11e-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="ee11e-105">Avhengig av kundebetalingsformatene som er satt opp, kan det hende at det kreves ytterligere informasjon for en kunde eller en kundebankkonto (dette dekkes ikke i denne prosedyren).</span><span class="sxs-lookup"><span data-stu-id="ee11e-105">Depending on the customer payment formats that are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="ee11e-106">Denne oppgaven ble opprettet med demodatafirmaet DEMF med en primæradresse for juridisk enhet i Tyskland.</span><span class="sxs-lookup"><span data-stu-id="ee11e-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="ee11e-107">Dette er den fjerde av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="ee11e-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="ee11e-108">Definere en kundebankkonto</span><span class="sxs-lookup"><span data-stu-id="ee11e-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="ee11e-109">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="ee11e-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="ee11e-110">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="ee11e-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ee11e-111">Du kan for eksempel filtrere på Konto-feltet med verdien DE-010.</span><span class="sxs-lookup"><span data-stu-id="ee11e-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="ee11e-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ee11e-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ee11e-113">Klikk Kunde i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ee11e-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="ee11e-114">Klikk Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="ee11e-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="ee11e-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ee11e-115">Click New.</span></span>
7. <span data-ttu-id="ee11e-116">Skriv inn en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="ee11e-117">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ee11e-118">Skriv for eksempel EURO-bank.</span><span class="sxs-lookup"><span data-stu-id="ee11e-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="ee11e-119">Angi eller velg en verdi i Bankgrupper-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="ee11e-120">Skriv inn en verdi i IBAN-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="ee11e-121">Skriv for eksempel DE36200400000628808808.</span><span class="sxs-lookup"><span data-stu-id="ee11e-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="ee11e-122">Skriv inn en verdi i SWIFT-kode-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="ee11e-123">Skriv for eksempel inn COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="ee11e-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="ee11e-124">Vær oppmerksom på at SWIFT\BIC ikke er obligatorisk for mange betalingsformater, men det anbefales at det er registrert for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ee11e-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="ee11e-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ee11e-125">Click Save.</span></span>
13. <span data-ttu-id="ee11e-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ee11e-126">Close the page.</span></span>
14. <span data-ttu-id="ee11e-127">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="ee11e-127">Click Edit.</span></span>
15. <span data-ttu-id="ee11e-128">Utvid delen Betalingstandarder.</span><span class="sxs-lookup"><span data-stu-id="ee11e-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="ee11e-129">Angi eller velg en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="ee11e-130">Legg til et avtalegiromandat</span><span class="sxs-lookup"><span data-stu-id="ee11e-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="ee11e-131">Utvid delen Avtalegiromandater.</span><span class="sxs-lookup"><span data-stu-id="ee11e-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="ee11e-132">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ee11e-132">Click Add.</span></span>
3. <span data-ttu-id="ee11e-133">Angi eller velg en verdi i Kreditors bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="ee11e-134">Velg for eksempel DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="ee11e-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="ee11e-135">Angi en dato i Signaturdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="ee11e-136">Klikk Ja for å bekrefte datooppdateringen.</span><span class="sxs-lookup"><span data-stu-id="ee11e-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="ee11e-137">Angi eller velg en verdi i Signatursted-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee11e-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="ee11e-138">Angi et tall i feltet Forventet antall betalinger.</span><span class="sxs-lookup"><span data-stu-id="ee11e-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="ee11e-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ee11e-139">Click OK.</span></span>
9. <span data-ttu-id="ee11e-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ee11e-140">Click Save.</span></span>

