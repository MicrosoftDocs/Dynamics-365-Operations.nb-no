--- 
title: "Definere leverandørbetalingsgebyrer"
description: "Definer leverandørbetalingsgebyrer."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a12bdb1532527fff7c3ce0d2b1e34b61b73e8fbc
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="c5b5d-103">Definere leverandørbetalingsgebyrer</span><span class="sxs-lookup"><span data-stu-id="c5b5d-103">Define vendor payment fees</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5b5d-104">Definer leverandørbetalingsgebyrer.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-104">Set up vendor payment fees.</span></span> <span data-ttu-id="c5b5d-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c5b5d-106">Gå til Leverandører > Betalingsoppsett > Betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="c5b5d-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-107">Click New.</span></span>
3. <span data-ttu-id="c5b5d-108">Skriv inn en verdi i feltet Gebyr-ID.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="c5b5d-109">Gebyr-IDen må beskrive når dette gebyret skal brukes, for eksempel "EFT_gebyr".</span><span class="sxs-lookup"><span data-stu-id="c5b5d-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="c5b5d-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c5b5d-111">Skriv inn en verdi i Gebyrbeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="c5b5d-112">Legg til en beskrivelse for å gi flere detaljer om når gebyret blir vurdert.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="c5b5d-113">I Tillegg-feltet velger du Leverandør eller Finans.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="c5b5d-114">Finans brukes når gebyret skal oppføres som utgift for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="c5b5d-115">Leverandør brukes når gebyret vurderes til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="c5b5d-116">Angi en hovedkonto for der gebyret skal utgiftsføres.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="c5b5d-117">Dette alternativet er bare tilgjengelig når Finans er valgt som Tillegg-alternativet.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="c5b5d-118">Velg journalen som dette gebyret kan brukes i.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="c5b5d-119">For betalingsgebyr for en leverandør velger du journalen Leverandørbetaling.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="c5b5d-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-120">Click Save.</span></span>
10. <span data-ttu-id="c5b5d-121">Klikk Oppsett av betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="c5b5d-122">Fortsett til betalingsgebyroppsettet for å definere når gebyret skal brukes i den valgte journalen.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="c5b5d-123">Velg enten Tabell Gruppe eller Alle.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="c5b5d-124">Tabell brukes til å velge én bankkonto, Gruppe brukes til å velge en bankgruppe, og Alle er for å bruke dette gebyroppsettet for alle bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="c5b5d-125">Velg en bankkonto eller en bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="c5b5d-126">Oppslaget viser bankgruppen hvis du valgte Gruppe, og viser bankkontoer hvis du valgte Tabell.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="c5b5d-127">Velg betalingsmåten for når dette gebyret skal vurderes.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="c5b5d-128">Velg betalingsspesifikasjonen for gjeldende betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="c5b5d-129">Betalingsspesifikasjonen brukes med betalingsmåter for elektronisk pengeoverføring.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="c5b5d-130">Velg om gebyret skal være en prosent, beløp eller intervall.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="c5b5d-131">Angi prosenten eller beløpet til gebyret.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="c5b5d-132">Hvis gebyret er en prosent, kan du angi prosenten.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="c5b5d-133">Hvis gebyret er et beløp, kan du angi beløpet til gebyret.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="c5b5d-134">Hvis gebyret er et intervall, kan du bruke kategorien Intervall til å definere trinnvise gebyrer.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="c5b5d-135">Velg valutaen som gebyret vurderes i, i Gebyrvaluta-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="c5b5d-136">Denne valutaen er for gebyret.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-136">This currency is for the fee.</span></span> <span data-ttu-id="c5b5d-137">Betalingsvalutaen brukes til å angi når gebyrregelen skal vurderes basert på betalingsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="c5b5d-138">Banken kan for eksempel belaste deg med et gebyr når en betaling foretas i euro, men alle andre betalinger er uten gebyr.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="c5b5d-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c5b5d-139">Click Save.</span></span>


