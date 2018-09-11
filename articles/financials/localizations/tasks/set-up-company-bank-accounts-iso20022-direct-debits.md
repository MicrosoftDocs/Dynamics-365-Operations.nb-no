--- 
title: Definere firmaets bankkontoer for ISO20022-avtalegiroer
description: "Denne oppgaven hjelper deg med å definere den firmaspesifikke bankkontoinformasjonen som kreves for å generere kundebetalingsfiler."
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 71ea8d1e03115480e8148d66af31e5edb618e557
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="2d641-103">Definere firmaets bankkontoer for ISO20022-avtalegiroer</span><span class="sxs-lookup"><span data-stu-id="2d641-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d641-104">Denne oppgaven hjelper deg med å definere den firmaspesifikke bankkontoinformasjonen som kreves for å generere kundebetalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="2d641-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="2d641-105">Denne fremgangsmåten bruker ISO 20022-avtalegiroformatet som eksempel.</span><span class="sxs-lookup"><span data-stu-id="2d641-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="2d641-106">Andre formater kan kreve mer oppsettsinformasjon som firma-ID eller sorteringskode.</span><span class="sxs-lookup"><span data-stu-id="2d641-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="2d641-107">Denne oppgaven ble opprettet med demonstrasjonsdatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="2d641-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="2d641-108">Dette er den andre av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="2d641-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="2d641-109">Definere IBAN- og SWIFT-kodene</span><span class="sxs-lookup"><span data-stu-id="2d641-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="2d641-110">Gå til Kontant- og bankbehandling > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="2d641-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="2d641-111">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="2d641-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="2d641-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2d641-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2d641-113">For eksempel, klikk DEMF OPER for å åpne bankkontodetaljene.</span><span class="sxs-lookup"><span data-stu-id="2d641-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="2d641-114">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="2d641-114">Click Edit.</span></span>
5. <span data-ttu-id="2d641-115">Vis eller skjul delen Tilleggsidentifikasjon.</span><span class="sxs-lookup"><span data-stu-id="2d641-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="2d641-116">Skriv inn en verdi i IBAN-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d641-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="2d641-117">Skriv for eksempel DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="2d641-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="2d641-118">Skriv inn en verdi i SWIFT-kode-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d641-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="2d641-119">Skriv for eksempel DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="2d641-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="2d641-120">Vær oppmerksom på at SWIFT\BIC ikke er obligatorisk for mange betalingsformater, men det anbefales at det er registrert for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2d641-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="2d641-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2d641-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="2d641-122">Definere en bankkonto for juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="2d641-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="2d641-123">Gå til Organisasjonsstyring > Organisasjoner > Juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="2d641-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="2d641-124">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="2d641-124">Click Edit.</span></span>
3. <span data-ttu-id="2d641-125">Vis eller skjul delen Bankkontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="2d641-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="2d641-126">Klikk rullegardinknappen i Bankkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="2d641-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2d641-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2d641-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2d641-128">For eksempel, velg "DEMF OPER" bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2d641-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="2d641-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2d641-129">Click Save.</span></span>


