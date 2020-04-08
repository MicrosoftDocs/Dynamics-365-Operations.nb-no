---
title: Definere leverandørbetalingsgebyrer
description: Definer leverandørbetalingsgebyrer.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 404bd1e22caa8098f114a2dcc67dd420509cce2b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140473"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="b034b-103">Definere leverandørbetalingsgebyrer</span><span class="sxs-lookup"><span data-stu-id="b034b-103">Define vendor payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b034b-104">Definer leverandørbetalingsgebyrer.</span><span class="sxs-lookup"><span data-stu-id="b034b-104">Set up vendor payment fees.</span></span> <span data-ttu-id="b034b-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="b034b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b034b-106">Gå til Leverandører > Betalingsoppsett > Betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="b034b-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="b034b-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b034b-107">Click New.</span></span>
3. <span data-ttu-id="b034b-108">Skriv inn en verdi i feltet Gebyr-ID.</span><span class="sxs-lookup"><span data-stu-id="b034b-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="b034b-109">Gebyr-IDen må beskrive når dette gebyret skal brukes, for eksempel "EFT_gebyr".</span><span class="sxs-lookup"><span data-stu-id="b034b-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="b034b-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b034b-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b034b-111">Skriv inn en verdi i Gebyrbeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="b034b-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="b034b-112">Legg til en beskrivelse for å gi flere detaljer om når gebyret blir vurdert.</span><span class="sxs-lookup"><span data-stu-id="b034b-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="b034b-113">I Tillegg-feltet velger du Leverandør eller Finans.</span><span class="sxs-lookup"><span data-stu-id="b034b-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="b034b-114">Finans brukes når gebyret skal oppføres som utgift for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="b034b-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="b034b-115">Leverandør brukes når gebyret vurderes til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="b034b-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="b034b-116">Angi en hovedkonto for der gebyret skal utgiftsføres.</span><span class="sxs-lookup"><span data-stu-id="b034b-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="b034b-117">Dette alternativet er bare tilgjengelig når Finans er valgt som Tillegg-alternativet.</span><span class="sxs-lookup"><span data-stu-id="b034b-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="b034b-118">Velg journalen som dette gebyret kan brukes i.</span><span class="sxs-lookup"><span data-stu-id="b034b-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="b034b-119">For betalingsgebyr for en leverandør velger du journalen Leverandørbetaling.</span><span class="sxs-lookup"><span data-stu-id="b034b-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="b034b-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b034b-120">Click Save.</span></span>
10. <span data-ttu-id="b034b-121">Klikk Oppsett av betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="b034b-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="b034b-122">Fortsett til betalingsgebyroppsettet for å definere når gebyret skal brukes i den valgte journalen.</span><span class="sxs-lookup"><span data-stu-id="b034b-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="b034b-123">Velg enten Tabell Gruppe eller Alle.</span><span class="sxs-lookup"><span data-stu-id="b034b-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="b034b-124">Tabell brukes til å velge én bankkonto, Gruppe brukes til å velge en bankgruppe, og Alle er for å bruke dette gebyroppsettet for alle bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="b034b-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="b034b-125">Velg en bankkonto eller en bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="b034b-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="b034b-126">Oppslaget viser bankgruppen hvis du valgte Gruppe, og viser bankkontoer hvis du valgte Tabell.</span><span class="sxs-lookup"><span data-stu-id="b034b-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="b034b-127">Velg betalingsmåten for når dette gebyret skal vurderes.</span><span class="sxs-lookup"><span data-stu-id="b034b-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="b034b-128">Velg betalingsspesifikasjonen for gjeldende betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="b034b-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="b034b-129">Betalingsspesifikasjonen brukes med betalingsmåter for elektronisk pengeoverføring.</span><span class="sxs-lookup"><span data-stu-id="b034b-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="b034b-130">Velg om gebyret skal være en prosent, beløp eller intervall.</span><span class="sxs-lookup"><span data-stu-id="b034b-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="b034b-131">Angi prosenten eller beløpet til gebyret.</span><span class="sxs-lookup"><span data-stu-id="b034b-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="b034b-132">Hvis gebyret er en prosent, kan du angi prosenten.</span><span class="sxs-lookup"><span data-stu-id="b034b-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="b034b-133">Hvis gebyret er et beløp, kan du angi beløpet til gebyret.</span><span class="sxs-lookup"><span data-stu-id="b034b-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="b034b-134">Hvis gebyret er et intervall, kan du bruke kategorien Intervall til å definere trinnvise gebyrer.</span><span class="sxs-lookup"><span data-stu-id="b034b-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="b034b-135">Velg valutaen som gebyret vurderes i, i Gebyrvaluta-feltet.</span><span class="sxs-lookup"><span data-stu-id="b034b-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="b034b-136">Denne valutaen er for gebyret.</span><span class="sxs-lookup"><span data-stu-id="b034b-136">This currency is for the fee.</span></span> <span data-ttu-id="b034b-137">Betalingsvalutaen brukes til å angi når gebyrregelen skal vurderes basert på betalingsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="b034b-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="b034b-138">Banken kan for eksempel belaste deg med et gebyr når en betaling foretas i euro, men alle andre betalinger er uten gebyr.</span><span class="sxs-lookup"><span data-stu-id="b034b-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="b034b-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b034b-139">Click Save.</span></span>

