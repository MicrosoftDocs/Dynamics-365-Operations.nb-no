---
title: Masseopprett salgstilbud
description: Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7aaa4e1fee12092be0389f0641e64712e869e6a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260365"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="3cbc0-103">Masseopprett salgstilbud</span><span class="sxs-lookup"><span data-stu-id="3cbc0-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cbc0-104">Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="3cbc0-105">Denne massetilbudsopprettelsen er basert på tilbudsmaler.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="3cbc0-106">Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="3cbc0-107">Opprette en tilbudsmal</span><span class="sxs-lookup"><span data-stu-id="3cbc0-107">Create a quotation template</span></span>
1. <span data-ttu-id="3cbc0-108">Gå til Salg og markedsføring > Oppsett > Tilbud > Malgrupper.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="3cbc0-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-109">Click New.</span></span>
3. <span data-ttu-id="3cbc0-110">Skriv inn en ID som du velger, i Gruppe-ID-feltet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="3cbc0-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3cbc0-112">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-112">Click Save.</span></span>
6. <span data-ttu-id="3cbc0-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-113">Close the page.</span></span>
7. <span data-ttu-id="3cbc0-114">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="3cbc0-115">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-115">Click New.</span></span>
9. <span data-ttu-id="3cbc0-116">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="3cbc0-117">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="3cbc0-118">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-118">Click OK.</span></span>
    * <span data-ttu-id="3cbc0-119">Du må utføre trinnene for oppsettet i tilbudshodet for at et tilbud skal bli en mal.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="3cbc0-120">Dette må gjøres før du kan legge til linjer i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="3cbc0-121">Klikk på Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="3cbc0-122">Klikk på Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-122">Click Change view.</span></span>
14. <span data-ttu-id="3cbc0-123">Klikk på Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-123">Click Header view.</span></span>
15. <span data-ttu-id="3cbc0-124">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="3cbc0-125">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="3cbc0-126">Angi en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="3cbc0-127">Velg Ja i Aktiv-feltet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="3cbc0-128">Bare aktive maler kan brukes når du bruker en mal på et nytt salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="3cbc0-129">Klikk på Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="3cbc0-130">Klikk på Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-130">Click Change view.</span></span>
21. <span data-ttu-id="3cbc0-131">Klikk på Linjevisning.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-131">Click Line view.</span></span>
22. <span data-ttu-id="3cbc0-132">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="3cbc0-133">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="3cbc0-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-134">Close the page.</span></span>
25. <span data-ttu-id="3cbc0-135">Angi et tall i feltet Rabattprosent.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="3cbc0-136">Klikk på Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-136">Click Add line.</span></span>
27. <span data-ttu-id="3cbc0-137">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="3cbc0-138">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="3cbc0-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-139">Close the page.</span></span>
30. <span data-ttu-id="3cbc0-140">I Enhetspris-feltet angir du en ny pris eller endrer den gjeldende.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="3cbc0-141">Klikk på Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-141">Click Add line.</span></span>
32. <span data-ttu-id="3cbc0-142">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="3cbc0-143">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="3cbc0-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-144">Close the page.</span></span>
35. <span data-ttu-id="3cbc0-145">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="3cbc0-146">Angi et tall i feltet Rabatt.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="3cbc0-147">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="3cbc0-148">Bruke malen for å opprette ett enkelt tilbud</span><span class="sxs-lookup"><span data-stu-id="3cbc0-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="3cbc0-149">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="3cbc0-150">Legg merke til at tilbudet du nettopp opprettet, merkes som mal.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="3cbc0-151">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-151">Click New.</span></span>
3. <span data-ttu-id="3cbc0-152">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="3cbc0-153">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="3cbc0-154">Utvid delen Mal.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-154">Expand the Template section.</span></span>
6. <span data-ttu-id="3cbc0-155">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="3cbc0-156">Angi eller velg en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="3cbc0-157">Velg Basert på malverdier i feltet Beregningsmåte.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="3cbc0-158">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-158">Click OK.</span></span>
    * <span data-ttu-id="3cbc0-159">Det nye tilbudet er nå opprettet, basert på data og vilkår for malen.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="3cbc0-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-160">Close the page.</span></span>
11. <span data-ttu-id="3cbc0-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="3cbc0-162">Bruke malen for å masseopprette tilbud</span><span class="sxs-lookup"><span data-stu-id="3cbc0-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="3cbc0-163">Gå til Salg og markedsføring > Salgstilbud > Tilbudsoppdatering > Masseopprett tilbud.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="3cbc0-164">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="3cbc0-165">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="3cbc0-166">Angi eller velg en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="3cbc0-167">Velg Basert på malverdier i feltet Beregningsmåte.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="3cbc0-168">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="3cbc0-169">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-169">Click Filter.</span></span>
8. <span data-ttu-id="3cbc0-170">Angi filteret til å dekke et valgt område av kunder du vil ha med i denne opprettelsen av massetilbud i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="3cbc0-171">Bruk følgende format Kunde1..KundeN.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="3cbc0-172">Du kan for eksempel sette filteret til: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="3cbc0-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="3cbc0-173">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-173">Click OK.</span></span>
10. <span data-ttu-id="3cbc0-174">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-174">Click OK.</span></span>
11. <span data-ttu-id="3cbc0-175">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="3cbc0-176">Kontroller at tilbud er opprettet for alle kunder som er angitt i rutinen Masseoppdatering, basert på den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="3cbc0-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]