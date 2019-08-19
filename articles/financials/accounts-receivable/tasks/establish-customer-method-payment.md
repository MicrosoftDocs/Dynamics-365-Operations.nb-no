---
title: Opprette kundebetalingsmåte
description: Opprett en betalingsmåte for kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 477f1ff72fd8012c3403d22aa128d97e45d5559f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842911"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="fcafe-103">Opprette kundebetalingsmåte</span><span class="sxs-lookup"><span data-stu-id="fcafe-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fcafe-104">Opprett en betalingsmåte for kundebetalinger.</span><span class="sxs-lookup"><span data-stu-id="fcafe-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="fcafe-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="fcafe-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="fcafe-106">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="fcafe-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="fcafe-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fcafe-107">Click New.</span></span>
3. <span data-ttu-id="fcafe-108">Angi en ID for betalingsmåten i feltet Betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="fcafe-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="fcafe-109">Metoden for betalings-ID vises på fakturaer og betalinger, så gjør den beskrivende nok til å forstå hvilken type betaling som blir registrert, og for hvilken bankkonto.</span><span class="sxs-lookup"><span data-stu-id="fcafe-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="fcafe-110">Angi en beskrivelse i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="fcafe-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="fcafe-111">Velg hvilken betalingsstatus som er nødvendig for at betalinger som skal posteres.</span><span class="sxs-lookup"><span data-stu-id="fcafe-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="fcafe-112">Når du oppretter en kundebetaling, kan den bare posteres når betalingsstatusen samsvarer med betalingsstatusen du definerer her.</span><span class="sxs-lookup"><span data-stu-id="fcafe-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="fcafe-113">Velg hvordan betalinger for kunder skal opprettes for fakturaer.</span><span class="sxs-lookup"><span data-stu-id="fcafe-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="fcafe-114">Dette alternativet brukes bare når du kjører et betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="fcafe-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="fcafe-115">Et betalingsforslag kan brukes for kundebetalinger ved bruk av avtalegiro, og når du trekker penger fra kundenes bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="fcafe-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="fcafe-116">Velg betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="fcafe-116">Select the type of payment.</span></span>
    * <span data-ttu-id="fcafe-117">Betalingstypen vil hjelpe deg med å finne ut om noen validering utføres eller ikke i betalingen.</span><span class="sxs-lookup"><span data-stu-id="fcafe-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="fcafe-118">Velg hvilken kontotype betalinger skal posteres til.</span><span class="sxs-lookup"><span data-stu-id="fcafe-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="fcafe-119">Banken vil vanligvis være valgt for dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="fcafe-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="fcafe-120">Velg bankkontoen som denne betalingen blir registrert i.</span><span class="sxs-lookup"><span data-stu-id="fcafe-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="fcafe-121">Angi banktransaksjonstypen for å identifisere typen betaling som brukes av banken.</span><span class="sxs-lookup"><span data-stu-id="fcafe-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="fcafe-122">Banktransaksjonstypen brukes under bankavstemmingsprosessen, og kan forenkle avstemming.</span><span class="sxs-lookup"><span data-stu-id="fcafe-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="fcafe-123">Velg om denne betalingen skal posteres midlertidig til en mellomkonto.</span><span class="sxs-lookup"><span data-stu-id="fcafe-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="fcafe-124">Hvis du vil prøve flyttidspunktet for en betaling som skal klares av banken, kan du bruke funksjonen mellompostering.</span><span class="sxs-lookup"><span data-stu-id="fcafe-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="fcafe-125">Betalingen posteres midlertidig til en finanskonto før den klareres av banken, og betalingen flyttes da til bankkontoen du har definert her.</span><span class="sxs-lookup"><span data-stu-id="fcafe-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="fcafe-126">Angi hovedkontoen som brukes for mellompostering.</span><span class="sxs-lookup"><span data-stu-id="fcafe-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="fcafe-127">Dette er hovedkontoen som betalingen midlertidig posteres til hvis du bruker mellompostering.</span><span class="sxs-lookup"><span data-stu-id="fcafe-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="fcafe-128">Bruk kategorien Filformat til å definere innstillinger for elektroniske betalinger.</span><span class="sxs-lookup"><span data-stu-id="fcafe-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="fcafe-129">Bruk kategorien Betalingskontroll til å definere felt som er obligatoriske.</span><span class="sxs-lookup"><span data-stu-id="fcafe-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="fcafe-130">Hvis du for eksempel trenger at alle betalinger med denne betalingsmåten skal innbetales, kan du velge dette alternativet i denne kategorien.</span><span class="sxs-lookup"><span data-stu-id="fcafe-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="fcafe-131">Bruk kategorien Betalingsattributter til å definere hvilke betalingsattributter du vil bruke for denne betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="fcafe-131">Use the Payment atrributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="fcafe-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fcafe-132">Click Save.</span></span>

