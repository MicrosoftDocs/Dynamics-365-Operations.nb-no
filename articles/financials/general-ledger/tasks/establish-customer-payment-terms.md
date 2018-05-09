--- 
title: Opprette kundebetalingsbetingelser
description: Dette definerer et oppsett for kontantrabatt og forfallsdato.
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3183b00cf2ff4d882399d3f44ca8046e50eda507
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="248b7-103">Opprette kundebetalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="248b7-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="248b7-104">Dette definerer et oppsett for kontantrabatt og forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="248b7-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="248b7-105">Denne oppgaveveiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="248b7-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="248b7-106">Gå til Kunder > Betalingsoppsett > Betalingsdager.</span><span class="sxs-lookup"><span data-stu-id="248b7-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="248b7-107">Oppsettet for betalingsbetingelsene er delt for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="248b7-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="248b7-108">Hvis du definerer det i modulen, vil det være tilgjengelig i den andre modulen også.</span><span class="sxs-lookup"><span data-stu-id="248b7-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="248b7-109">For denne veiledningen har jeg definert alle betalingsbetingelsene under Kunder.</span><span class="sxs-lookup"><span data-stu-id="248b7-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="248b7-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="248b7-110">Click New.</span></span>
    * <span data-ttu-id="248b7-111">Opprett en betalingsdag hvis betalingsbetingelsene krever en bestemt dag i uken (mandag, tirsdag osv) eller en bestemt dato i måneden (5., 10. osv).</span><span class="sxs-lookup"><span data-stu-id="248b7-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="248b7-112">I feltet Betalingsdag angir du en ID for betalingsdagen i feltet Betalingsdag.</span><span class="sxs-lookup"><span data-stu-id="248b7-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="248b7-113">I Beskrivelse-feltet angir du en beskrivelse av betalingsdagen.</span><span class="sxs-lookup"><span data-stu-id="248b7-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="248b7-114">I Uke/måned-feltet velger du enten Uke eller Måned.</span><span class="sxs-lookup"><span data-stu-id="248b7-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="248b7-115">Hvis du vil angi en dag i uken, for eksempel mandag, velger du Uke.</span><span class="sxs-lookup"><span data-stu-id="248b7-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="248b7-116">Hvis du vil angi en dato i måneden, for eksempel den 10., velger du Måned.</span><span class="sxs-lookup"><span data-stu-id="248b7-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="248b7-117">Velg Måned for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="248b7-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="248b7-118">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="248b7-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="248b7-119">Datoen må angis som et tall, for eksempel "10", og ikke som "10.".</span><span class="sxs-lookup"><span data-stu-id="248b7-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="248b7-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="248b7-120">Click Save.</span></span>
8. <span data-ttu-id="248b7-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="248b7-121">Close the page.</span></span>
9. <span data-ttu-id="248b7-122">Gå til Kunder > Betalingsoppsett > Betalingsbetingelser.</span><span class="sxs-lookup"><span data-stu-id="248b7-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="248b7-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="248b7-123">Click New.</span></span>
    * <span data-ttu-id="248b7-124">Betalingsbetingelsene brukes til å definere hvordan forfallsdatoene beregnes.</span><span class="sxs-lookup"><span data-stu-id="248b7-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="248b7-125">Dato for oppsett av kontantrabatten er definert i en egen side.</span><span class="sxs-lookup"><span data-stu-id="248b7-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="248b7-126">Angi en ID i feltet Betalingsbetingelser.</span><span class="sxs-lookup"><span data-stu-id="248b7-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="248b7-127">Angi en beskrivelse i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="248b7-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="248b7-128">Velg en betalingsmåte, for eksempel Oppkrav, Netto, Gjeldende måned og så videre.</span><span class="sxs-lookup"><span data-stu-id="248b7-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="248b7-129">Betalingsmåten brukes til å definere starten på hvordan forfallsdatoene beregnes.</span><span class="sxs-lookup"><span data-stu-id="248b7-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="248b7-130">Netto brukes for eksempel hvis forfallsdatoen alltid er et angitt antall måneder eller dager etter fakturadato.</span><span class="sxs-lookup"><span data-stu-id="248b7-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="248b7-131">Oppkrav kan brukes når betaling kreves ved faktura, slik at en forfallsdato ikke blir beregnet.</span><span class="sxs-lookup"><span data-stu-id="248b7-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="248b7-132">Velg Gjeldende måned for denne oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="248b7-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="248b7-133">Velg en betalingsdag hvis en bestemt dag i uken eller dato skal tas med i beregningen.</span><span class="sxs-lookup"><span data-stu-id="248b7-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="248b7-134">Avhengig av betalingsbetingelsene, kan du angi et antall i måneder eller dager.</span><span class="sxs-lookup"><span data-stu-id="248b7-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="248b7-135">Eller du bruke betalingsplanen eller betalingsdagen for å legge til på slutten av betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="248b7-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="248b7-136">Hvis forfallsdatoen alltid skal være den 10. i neste måned, velger du en betalingsdag på den 10.</span><span class="sxs-lookup"><span data-stu-id="248b7-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="248b7-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="248b7-137">Click Save.</span></span>
16. <span data-ttu-id="248b7-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="248b7-138">Close the page.</span></span>
17. <span data-ttu-id="248b7-139">Gå til Kunder > Betalingsoppsett > Kontantrabatt.</span><span class="sxs-lookup"><span data-stu-id="248b7-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="248b7-140">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="248b7-140">Click New.</span></span>
    * <span data-ttu-id="248b7-141">Denne siden brukes til å definere hvordan kontantrabatten skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="248b7-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="248b7-142">Angi en ID i feltet Kontantrabatt i feltet Kontantrabatt.</span><span class="sxs-lookup"><span data-stu-id="248b7-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="248b7-143">Angi en beskrivelse i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="248b7-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="248b7-144">Hvis en trinnvis kontantrabatt er tilgjengelig, velger du den neste rabattkoden som er relevant etter denne nye kontantrabatten.</span><span class="sxs-lookup"><span data-stu-id="248b7-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="248b7-145">Angi hvor mange dager som brukes til å beregne kontantrabattdatoen.</span><span class="sxs-lookup"><span data-stu-id="248b7-145">Enter the number of days used to calculate the cash discount date.</span></span>
    * <span data-ttu-id="248b7-146">Hvis nettoprinsippet er valgt, legges antallet dager til fakturadatoen for å beregne kontantrabattdatoen.</span><span class="sxs-lookup"><span data-stu-id="248b7-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="248b7-147">Angi prosenten for kontantrabatten.</span><span class="sxs-lookup"><span data-stu-id="248b7-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="248b7-148">Angi hovedkontoen som kontantrabatten skal posteres til for kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="248b7-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="248b7-149">Velg et alternativ i feltet Motkontoer for rabatt.</span><span class="sxs-lookup"><span data-stu-id="248b7-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="248b7-150">Hvis du velger "Kontoer på fakturalinjene", posteres kontantrabatten til samme anleggsmiddel/utgiftshovedkontoen på linjene i leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="248b7-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="248b7-151">Hvis du velger "Bruk hovedkontoen for leverandørfakturaer", posteres kontantrabatten til hovedkontoen du definerer i "Hovedkonto for leverandørfakturaer".</span><span class="sxs-lookup"><span data-stu-id="248b7-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="248b7-152">I dette eksemplet velger du "Bruk hovedkontoen for leverandørfakturaer".</span><span class="sxs-lookup"><span data-stu-id="248b7-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="248b7-153">Angi hovedkontoen som kontantrabatten skal posteres til for leverandørfakturaer.</span><span class="sxs-lookup"><span data-stu-id="248b7-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="248b7-154">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="248b7-154">Click Save.</span></span>


