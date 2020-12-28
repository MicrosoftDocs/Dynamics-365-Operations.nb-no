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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 227ff0dd03f8917f4551ce08067ef26c6204b059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434208"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="46e55-103">Masseopprett salgstilbud</span><span class="sxs-lookup"><span data-stu-id="46e55-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46e55-104">Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder.</span><span class="sxs-lookup"><span data-stu-id="46e55-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="46e55-105">Denne massetilbudsopprettelsen er basert på tilbudsmaler.</span><span class="sxs-lookup"><span data-stu-id="46e55-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="46e55-106">Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="46e55-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="46e55-107">Opprette en tilbudsmal</span><span class="sxs-lookup"><span data-stu-id="46e55-107">Create a quotation template</span></span>
1. <span data-ttu-id="46e55-108">Gå til Salg og markedsføring > Oppsett > Tilbud > Malgrupper.</span><span class="sxs-lookup"><span data-stu-id="46e55-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="46e55-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="46e55-109">Click New.</span></span>
3. <span data-ttu-id="46e55-110">Skriv inn en ID som du velger, i Gruppe-ID-feltet.</span><span class="sxs-lookup"><span data-stu-id="46e55-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="46e55-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="46e55-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="46e55-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="46e55-112">Click Save.</span></span>
6. <span data-ttu-id="46e55-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="46e55-113">Close the page.</span></span>
7. <span data-ttu-id="46e55-114">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="46e55-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="46e55-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="46e55-115">Click New.</span></span>
9. <span data-ttu-id="46e55-116">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="46e55-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="46e55-117">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="46e55-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="46e55-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="46e55-118">Click OK.</span></span>
    * <span data-ttu-id="46e55-119">Du må utføre trinnene for oppsettet i tilbudshodet for at et tilbud skal bli en mal.</span><span class="sxs-lookup"><span data-stu-id="46e55-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="46e55-120">Dette må gjøres før du kan legge til linjer i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="46e55-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="46e55-121">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="46e55-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="46e55-122">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="46e55-122">Click Change view.</span></span>
14. <span data-ttu-id="46e55-123">Klikk Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="46e55-123">Click Header view.</span></span>
15. <span data-ttu-id="46e55-124">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="46e55-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="46e55-125">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="46e55-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="46e55-126">Angi en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="46e55-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="46e55-127">Velg Ja i Aktiv-feltet.</span><span class="sxs-lookup"><span data-stu-id="46e55-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="46e55-128">Bare aktive maler kan brukes når du bruker en mal på et nytt salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="46e55-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="46e55-129">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="46e55-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="46e55-130">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="46e55-130">Click Change view.</span></span>
21. <span data-ttu-id="46e55-131">Klikk Linjevisning.</span><span class="sxs-lookup"><span data-stu-id="46e55-131">Click Line view.</span></span>
22. <span data-ttu-id="46e55-132">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="46e55-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="46e55-133">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="46e55-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="46e55-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="46e55-134">Close the page.</span></span>
25. <span data-ttu-id="46e55-135">Angi et tall i feltet Rabattprosent.</span><span class="sxs-lookup"><span data-stu-id="46e55-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="46e55-136">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="46e55-136">Click Add line.</span></span>
27. <span data-ttu-id="46e55-137">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="46e55-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="46e55-138">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="46e55-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="46e55-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="46e55-139">Close the page.</span></span>
30. <span data-ttu-id="46e55-140">I Enhetspris-feltet angir du en ny pris eller endrer den gjeldende.</span><span class="sxs-lookup"><span data-stu-id="46e55-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="46e55-141">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="46e55-141">Click Add line.</span></span>
32. <span data-ttu-id="46e55-142">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="46e55-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="46e55-143">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="46e55-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="46e55-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="46e55-144">Close the page.</span></span>
35. <span data-ttu-id="46e55-145">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="46e55-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="46e55-146">Angi et tall i feltet Rabatt.</span><span class="sxs-lookup"><span data-stu-id="46e55-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="46e55-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="46e55-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="46e55-148">Bruke malen for å opprette ett enkelt tilbud</span><span class="sxs-lookup"><span data-stu-id="46e55-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="46e55-149">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="46e55-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="46e55-150">Legg merke til at tilbudet du nettopp opprettet, merkes som mal.</span><span class="sxs-lookup"><span data-stu-id="46e55-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="46e55-151">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="46e55-151">Click New.</span></span>
3. <span data-ttu-id="46e55-152">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="46e55-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="46e55-153">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="46e55-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="46e55-154">Utvid delen Mal.</span><span class="sxs-lookup"><span data-stu-id="46e55-154">Expand the Template section.</span></span>
6. <span data-ttu-id="46e55-155">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="46e55-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="46e55-156">Angi eller velg en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="46e55-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="46e55-157">Velg Basert på malverdier i feltet Beregningsmåte.</span><span class="sxs-lookup"><span data-stu-id="46e55-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="46e55-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="46e55-158">Click OK.</span></span>
    * <span data-ttu-id="46e55-159">Det nye tilbudet er nå opprettet, basert på data og vilkår for malen.</span><span class="sxs-lookup"><span data-stu-id="46e55-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="46e55-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="46e55-160">Close the page.</span></span>
11. <span data-ttu-id="46e55-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="46e55-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="46e55-162">Bruke malen for å masseopprette tilbud</span><span class="sxs-lookup"><span data-stu-id="46e55-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="46e55-163">Gå til Salg og markedsføring > Salgstilbud > Tilbudsoppdatering > Masseopprett tilbud.</span><span class="sxs-lookup"><span data-stu-id="46e55-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="46e55-164">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="46e55-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="46e55-165">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="46e55-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="46e55-166">Angi eller velg en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="46e55-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="46e55-167">Velg Basert på malverdier i feltet Beregningsmåte.</span><span class="sxs-lookup"><span data-stu-id="46e55-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="46e55-168">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="46e55-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="46e55-169">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="46e55-169">Click Filter.</span></span>
8. <span data-ttu-id="46e55-170">Angi filteret til å dekke et valgt område av kunder du vil ha med i denne opprettelsen av massetilbud i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="46e55-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="46e55-171">Bruk følgende format Kunde1..KundeN.</span><span class="sxs-lookup"><span data-stu-id="46e55-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="46e55-172">Du kan for eksempel sette filteret til: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="46e55-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="46e55-173">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="46e55-173">Click OK.</span></span>
10. <span data-ttu-id="46e55-174">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="46e55-174">Click OK.</span></span>
11. <span data-ttu-id="46e55-175">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="46e55-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="46e55-176">Kontroller at tilbud er opprettet for alle kunder som er angitt i rutinen Masseoppdatering, basert på den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="46e55-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

