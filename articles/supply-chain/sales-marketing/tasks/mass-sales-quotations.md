---
title: Masseopprett salgstilbud
description: Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0422817576d9d93d0ec6bbfb5f3777013ee09ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817707"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="8778d-103">Masseopprett salgstilbud</span><span class="sxs-lookup"><span data-stu-id="8778d-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8778d-104">Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder.</span><span class="sxs-lookup"><span data-stu-id="8778d-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="8778d-105">Denne massetilbudsopprettelsen er basert på tilbudsmaler.</span><span class="sxs-lookup"><span data-stu-id="8778d-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="8778d-106">Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="8778d-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="8778d-107">Opprette en tilbudsmal</span><span class="sxs-lookup"><span data-stu-id="8778d-107">Create a quotation template</span></span>
1. <span data-ttu-id="8778d-108">Gå til Salg og markedsføring > Oppsett > Tilbud > Malgrupper.</span><span class="sxs-lookup"><span data-stu-id="8778d-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="8778d-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="8778d-109">Click New.</span></span>
3. <span data-ttu-id="8778d-110">Skriv inn en ID som du velger, i Gruppe-ID-feltet.</span><span class="sxs-lookup"><span data-stu-id="8778d-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="8778d-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8778d-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8778d-112">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="8778d-112">Click Save.</span></span>
6. <span data-ttu-id="8778d-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8778d-113">Close the page.</span></span>
7. <span data-ttu-id="8778d-114">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="8778d-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="8778d-115">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="8778d-115">Click New.</span></span>
9. <span data-ttu-id="8778d-116">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="8778d-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="8778d-117">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8778d-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="8778d-118">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="8778d-118">Click OK.</span></span>
    * <span data-ttu-id="8778d-119">Du må utføre trinnene for oppsettet i tilbudshodet for at et tilbud skal bli en mal.</span><span class="sxs-lookup"><span data-stu-id="8778d-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="8778d-120">Dette må gjøres før du kan legge til linjer i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="8778d-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="8778d-121">Klikk på Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8778d-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="8778d-122">Klikk på Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="8778d-122">Click Change view.</span></span>
14. <span data-ttu-id="8778d-123">Klikk på Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="8778d-123">Click Header view.</span></span>
15. <span data-ttu-id="8778d-124">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="8778d-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="8778d-125">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="8778d-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="8778d-126">Angi en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8778d-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="8778d-127">Velg Ja i Aktiv-feltet.</span><span class="sxs-lookup"><span data-stu-id="8778d-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="8778d-128">Bare aktive maler kan brukes når du bruker en mal på et nytt salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="8778d-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="8778d-129">Klikk på Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8778d-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="8778d-130">Klikk på Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="8778d-130">Click Change view.</span></span>
21. <span data-ttu-id="8778d-131">Klikk på Linjevisning.</span><span class="sxs-lookup"><span data-stu-id="8778d-131">Click Line view.</span></span>
22. <span data-ttu-id="8778d-132">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8778d-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="8778d-133">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8778d-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="8778d-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8778d-134">Close the page.</span></span>
25. <span data-ttu-id="8778d-135">Angi et tall i feltet Rabattprosent.</span><span class="sxs-lookup"><span data-stu-id="8778d-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="8778d-136">Klikk på Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="8778d-136">Click Add line.</span></span>
27. <span data-ttu-id="8778d-137">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8778d-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="8778d-138">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8778d-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="8778d-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8778d-139">Close the page.</span></span>
30. <span data-ttu-id="8778d-140">I Enhetspris-feltet angir du en ny pris eller endrer den gjeldende.</span><span class="sxs-lookup"><span data-stu-id="8778d-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="8778d-141">Klikk på Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="8778d-141">Click Add line.</span></span>
32. <span data-ttu-id="8778d-142">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8778d-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="8778d-143">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8778d-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="8778d-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8778d-144">Close the page.</span></span>
35. <span data-ttu-id="8778d-145">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="8778d-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="8778d-146">Angi et tall i feltet Rabatt.</span><span class="sxs-lookup"><span data-stu-id="8778d-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="8778d-147">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="8778d-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="8778d-148">Bruke malen for å opprette ett enkelt tilbud</span><span class="sxs-lookup"><span data-stu-id="8778d-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="8778d-149">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="8778d-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="8778d-150">Legg merke til at tilbudet du nettopp opprettet, merkes som mal.</span><span class="sxs-lookup"><span data-stu-id="8778d-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="8778d-151">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="8778d-151">Click New.</span></span>
3. <span data-ttu-id="8778d-152">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="8778d-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="8778d-153">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8778d-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="8778d-154">Utvid delen Mal.</span><span class="sxs-lookup"><span data-stu-id="8778d-154">Expand the Template section.</span></span>
6. <span data-ttu-id="8778d-155">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="8778d-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="8778d-156">Angi eller velg en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8778d-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="8778d-157">Velg Basert på malverdier i feltet Beregningsmåte.</span><span class="sxs-lookup"><span data-stu-id="8778d-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="8778d-158">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="8778d-158">Click OK.</span></span>
    * <span data-ttu-id="8778d-159">Det nye tilbudet er nå opprettet, basert på data og vilkår for malen.</span><span class="sxs-lookup"><span data-stu-id="8778d-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="8778d-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8778d-160">Close the page.</span></span>
11. <span data-ttu-id="8778d-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8778d-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="8778d-162">Bruke malen for å masseopprette tilbud</span><span class="sxs-lookup"><span data-stu-id="8778d-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="8778d-163">Gå til Salg og markedsføring > Salgstilbud > Tilbudsoppdatering > Masseopprett tilbud.</span><span class="sxs-lookup"><span data-stu-id="8778d-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="8778d-164">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="8778d-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="8778d-165">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="8778d-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="8778d-166">Angi eller velg en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8778d-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="8778d-167">Velg Basert på malverdier i feltet Beregningsmåte.</span><span class="sxs-lookup"><span data-stu-id="8778d-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="8778d-168">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="8778d-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="8778d-169">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="8778d-169">Click Filter.</span></span>
8. <span data-ttu-id="8778d-170">Angi filteret til å dekke et valgt område av kunder du vil ha med i denne opprettelsen av massetilbud i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="8778d-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="8778d-171">Bruk følgende format Kunde1..KundeN.</span><span class="sxs-lookup"><span data-stu-id="8778d-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="8778d-172">Du kan for eksempel sette filteret til: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="8778d-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="8778d-173">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="8778d-173">Click OK.</span></span>
10. <span data-ttu-id="8778d-174">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="8778d-174">Click OK.</span></span>
11. <span data-ttu-id="8778d-175">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="8778d-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="8778d-176">Kontroller at tilbud er opprettet for alle kunder som er angitt i rutinen Masseoppdatering, basert på den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="8778d-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]