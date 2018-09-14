--- 
title: Opprette kundebetalingsgebyrer
description: Opprett betalingsgebyrer for kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5acb202d46ef39376a01ca592f60926786d11186
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="451c8-103">Opprette kundebetalingsgebyrer</span><span class="sxs-lookup"><span data-stu-id="451c8-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="451c8-104">Opprett betalingsgebyrer for kundebetalinger.</span><span class="sxs-lookup"><span data-stu-id="451c8-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="451c8-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="451c8-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="451c8-106">Gå til Kunder > Betalingsoppsett > Betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="451c8-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="451c8-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="451c8-107">Click New.</span></span>
3. <span data-ttu-id="451c8-108">Angi en gebyr-ID i Gebyr-ID-feltet.</span><span class="sxs-lookup"><span data-stu-id="451c8-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="451c8-109">Gebyr-IDen vises i betalingsjournaler, så gjør den beskrivende for å forstå hvilket gebyr som vurderes.</span><span class="sxs-lookup"><span data-stu-id="451c8-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="451c8-110">Angi et gebyrnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="451c8-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="451c8-111">I feltet Gebyrbeskrivelse skriver du inn en beskrivelse for gebyret.</span><span class="sxs-lookup"><span data-stu-id="451c8-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="451c8-112">Velg om gebyret skal belastes kunden eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="451c8-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="451c8-113">Hvis kunden blir vurdert gebyret, velger du Kunde.</span><span class="sxs-lookup"><span data-stu-id="451c8-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="451c8-114">Hvis gebyret skal vurderes for organisasjonen som en utgift, velger du Finans.</span><span class="sxs-lookup"><span data-stu-id="451c8-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="451c8-115">Velg Kunde for denne aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="451c8-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="451c8-116">Velg journaltypen som kan bruke dette betalingsgebyret.</span><span class="sxs-lookup"><span data-stu-id="451c8-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="451c8-117">Hvis disse gebyrene brukes for betalinger fra kunder, blir sannsynligvis journaltypen Kundebetaling.</span><span class="sxs-lookup"><span data-stu-id="451c8-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="451c8-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="451c8-118">Click Save.</span></span>
9. <span data-ttu-id="451c8-119">Klikk Oppsett av betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="451c8-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="451c8-120">Betalingsgebyroppsettet brukes til å definere kriteriene for når betalingsgebyret vurderes.</span><span class="sxs-lookup"><span data-stu-id="451c8-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="451c8-121">Du kan for eksempel definere at avgiften beregnes hvis bankkontoen er USMF OPER og betalingsmåten er Sjekk.</span><span class="sxs-lookup"><span data-stu-id="451c8-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="451c8-122">Velg Tabell, Gruppe eller Alle for å definere hvilke bankkontoer som skal vurderes for dette gebyret.</span><span class="sxs-lookup"><span data-stu-id="451c8-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="451c8-123">Hvis du velger alle, kan alle bankkontoer bli vurdert for denne avgiften.</span><span class="sxs-lookup"><span data-stu-id="451c8-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="451c8-124">Hvis du velger Tabell, kan bare bankkontoen du velger, vurderes for denne avgiften.</span><span class="sxs-lookup"><span data-stu-id="451c8-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="451c8-125">Hvis du velger Gruppe, kan bare bankkontoene i den valgte bankgruppen vurderes for denne avgiften.</span><span class="sxs-lookup"><span data-stu-id="451c8-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="451c8-126">Velg en bankkonto eller en bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="451c8-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="451c8-127">Hvis du valgte Tabell, vil oppslaget vise bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="451c8-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="451c8-128">Hvis du valgte Gruppe, vil oppslaget vise bankgrupper.</span><span class="sxs-lookup"><span data-stu-id="451c8-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="451c8-129">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="451c8-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="451c8-130">Velg betalingsmåten som dette gebyret skal vurderes for.</span><span class="sxs-lookup"><span data-stu-id="451c8-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="451c8-131">Du kan for eksempel vurdere et gebyr til kunder hvis de sender betalinger som en sjekk, i stedet for elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="451c8-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="451c8-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="451c8-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="451c8-133">Hvis relevant, angi en betalingsvaluta.</span><span class="sxs-lookup"><span data-stu-id="451c8-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="451c8-134">Betalingsvalutaen brukes som et tilleggskriterium for om gebyret vurderes.</span><span class="sxs-lookup"><span data-stu-id="451c8-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="451c8-135">Banken kan for eksempel betale en ekstra avgift for betalinger som er mottatt i USD som valuta, siden de vanligvis bare overfører i Euro-valutaen.</span><span class="sxs-lookup"><span data-stu-id="451c8-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="451c8-136">Velg om gebyret skal være en prosent, beløp eller intervall.</span><span class="sxs-lookup"><span data-stu-id="451c8-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="451c8-137">Angi prosenten eller beløpet til gebyret.</span><span class="sxs-lookup"><span data-stu-id="451c8-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="451c8-138">Hvis Prosent/beløp-feltet er Prosent, vil verdien du angir her, være en prosent.</span><span class="sxs-lookup"><span data-stu-id="451c8-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="451c8-139">Hvis Prosent/beløp-feltet er Beløp, vil verdien du angir her, være et beløp.</span><span class="sxs-lookup"><span data-stu-id="451c8-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="451c8-140">Hvis Prosent/beløp-feltet er Intervall, bruker du kategorien Intervall til å definere lagene.</span><span class="sxs-lookup"><span data-stu-id="451c8-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="451c8-141">Velg valutaen for gebyret i Gebyrvaluta-feltet.</span><span class="sxs-lookup"><span data-stu-id="451c8-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="451c8-142">Dette er valutaen som gebyret skal opprettes i.</span><span class="sxs-lookup"><span data-stu-id="451c8-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="451c8-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="451c8-143">Click Save.</span></span>


