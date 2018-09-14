--- 
title: "Opprette kundebetalingsmåte"
description: "Opprett en betalingsmåte for kundebetalinger."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: ab035c6268b701c78da32d589e99ece38c31781d
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="a2cf7-103">Opprette kundebetalingsmåte</span><span class="sxs-lookup"><span data-stu-id="a2cf7-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2cf7-104">Opprett en betalingsmåte for kundebetalinger.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="a2cf7-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a2cf7-106">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="a2cf7-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-107">Click New.</span></span>
3. <span data-ttu-id="a2cf7-108">Angi en ID for betalingsmåten i feltet Betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="a2cf7-109">Metoden for betalings-ID vises på fakturaer og betalinger, så gjør den beskrivende nok til å forstå hvilken type betaling som blir registrert, og for hvilken bankkonto.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="a2cf7-110">Angi en beskrivelse i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="a2cf7-111">Velg hvilken betalingsstatus som er nødvendig for at betalinger som skal posteres.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="a2cf7-112">Når du oppretter en kundebetaling, kan den bare posteres når betalingsstatusen samsvarer med betalingsstatusen du definerer her.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="a2cf7-113">Velg hvordan betalinger for kunder skal opprettes for fakturaer.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="a2cf7-114">Dette alternativet brukes bare når du kjører et betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="a2cf7-115">Et betalingsforslag kan brukes for kundebetalinger ved bruk av avtalegiro, og når du trekker penger fra kundenes bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="a2cf7-116">Velg betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-116">Select the type of payment.</span></span>
    * <span data-ttu-id="a2cf7-117">Betalingstypen vil hjelpe deg med å finne ut om noen validering utføres eller ikke i betalingen.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="a2cf7-118">Velg hvilken kontotype betalinger skal posteres til.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="a2cf7-119">Banken vil vanligvis være valgt for dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="a2cf7-120">Velg bankkontoen som denne betalingen blir registrert i.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="a2cf7-121">Angi banktransaksjonstypen for å identifisere typen betaling som brukes av banken.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="a2cf7-122">Banktransaksjonstypen brukes under bankavstemmingsprosessen, og kan forenkle avstemming.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="a2cf7-123">Velg om denne betalingen skal posteres midlertidig til en mellomkonto.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="a2cf7-124">Hvis du vil prøve flyttidspunktet for en betaling som skal klares av banken, kan du bruke funksjonen mellompostering.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="a2cf7-125">Betalingen posteres midlertidig til en finanskonto før den klareres av banken, og betalingen flyttes da til bankkontoen du har definert her.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="a2cf7-126">Angi hovedkontoen som brukes for mellompostering.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="a2cf7-127">Dette er hovedkontoen som betalingen midlertidig posteres til hvis du bruker mellompostering.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="a2cf7-128">Bruk kategorien Filformat til å definere innstillinger for elektroniske betalinger.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="a2cf7-129">Bruk kategorien Betalingskontroll til å definere felt som er obligatoriske.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="a2cf7-130">Hvis du for eksempel trenger at alle betalinger med denne betalingsmåten skal innbetales, kan du velge dette alternativet i denne kategorien.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="a2cf7-131">Bruk kategorien Betalingsattributter til å definere hvilke betalingsattributter du vil bruke for denne betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-131">Use the Payment atrributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="a2cf7-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a2cf7-132">Click Save.</span></span>


