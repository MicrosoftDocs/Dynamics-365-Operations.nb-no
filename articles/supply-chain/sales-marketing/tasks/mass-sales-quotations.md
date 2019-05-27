---
title: Masseopprett salgstilbud
description: Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0e9ddf38106fce3ed6a6f908826f2196c97a45a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562121"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="8bc7e-103">Masseopprett salgstilbud</span><span class="sxs-lookup"><span data-stu-id="8bc7e-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8bc7e-104">Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="8bc7e-105">Denne massetilbudsopprettelsen er basert på tilbudsmaler.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="8bc7e-106">Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="8bc7e-107">Opprette en tilbudsmal</span><span class="sxs-lookup"><span data-stu-id="8bc7e-107">Create a quotation template</span></span>
1. <span data-ttu-id="8bc7e-108">Gå til Salg og markedsføring > Oppsett > Tilbud > Malgrupper.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="8bc7e-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-109">Click New.</span></span>
3. <span data-ttu-id="8bc7e-110">Skriv inn en ID som du velger, i Gruppe-ID-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="8bc7e-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8bc7e-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-112">Click Save.</span></span>
6. <span data-ttu-id="8bc7e-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-113">Close the page.</span></span>
7. <span data-ttu-id="8bc7e-114">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="8bc7e-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-115">Click New.</span></span>
9. <span data-ttu-id="8bc7e-116">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="8bc7e-117">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="8bc7e-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-118">Click OK.</span></span>
    * <span data-ttu-id="8bc7e-119">Du må utføre trinnene for oppsettet i tilbudshodet for at et tilbud skal bli en mal.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="8bc7e-120">Dette må gjøres før du kan legge til linjer i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="8bc7e-121">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="8bc7e-122">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-122">Click Change view.</span></span>
14. <span data-ttu-id="8bc7e-123">Klikk Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-123">Click Header view.</span></span>
15. <span data-ttu-id="8bc7e-124">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="8bc7e-125">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="8bc7e-126">Angi en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="8bc7e-127">Velg Ja i Aktiv-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="8bc7e-128">Bare aktive maler kan brukes når du bruker en mal på et nytt salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="8bc7e-129">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="8bc7e-130">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-130">Click Change view.</span></span>
21. <span data-ttu-id="8bc7e-131">Klikk Linjevisning.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-131">Click Line view.</span></span>
22. <span data-ttu-id="8bc7e-132">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="8bc7e-133">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="8bc7e-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-134">Close the page.</span></span>
25. <span data-ttu-id="8bc7e-135">Angi et tall i feltet Rabattprosent.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="8bc7e-136">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-136">Click Add line.</span></span>
27. <span data-ttu-id="8bc7e-137">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="8bc7e-138">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="8bc7e-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-139">Close the page.</span></span>
30. <span data-ttu-id="8bc7e-140">I Enhetspris-feltet angir du en ny pris eller endrer den gjeldende.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="8bc7e-141">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-141">Click Add line.</span></span>
32. <span data-ttu-id="8bc7e-142">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="8bc7e-143">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="8bc7e-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-144">Close the page.</span></span>
35. <span data-ttu-id="8bc7e-145">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="8bc7e-146">Angi et tall i feltet Rabatt.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="8bc7e-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="8bc7e-148">Bruke malen for å opprette ett enkelt tilbud</span><span class="sxs-lookup"><span data-stu-id="8bc7e-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="8bc7e-149">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="8bc7e-150">Legg merke til at tilbudet du nettopp opprettet, merkes som mal.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="8bc7e-151">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-151">Click New.</span></span>
3. <span data-ttu-id="8bc7e-152">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="8bc7e-153">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="8bc7e-154">Utvid delen Mal.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-154">Expand the Template section.</span></span>
6. <span data-ttu-id="8bc7e-155">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="8bc7e-156">Angi eller velg en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="8bc7e-157">Velg Basert på malverdier i feltet Beregningsmåte.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="8bc7e-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-158">Click OK.</span></span>
    * <span data-ttu-id="8bc7e-159">Det nye tilbudet er nå opprettet, basert på data og vilkår for malen.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="8bc7e-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-160">Close the page.</span></span>
11. <span data-ttu-id="8bc7e-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="8bc7e-162">Bruke malen for å masseopprette tilbud</span><span class="sxs-lookup"><span data-stu-id="8bc7e-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="8bc7e-163">Gå til Salg og markedsføring > Salgstilbud > Tilbudsoppdatering > Masseopprett tilbud.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="8bc7e-164">Velg Kunde i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="8bc7e-165">Angi eller velg en verdi i feltet Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="8bc7e-166">Angi eller velg en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="8bc7e-167">Velg Basert på malverdier i feltet Beregningsmåte.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="8bc7e-168">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="8bc7e-169">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-169">Click Filter.</span></span>
8. <span data-ttu-id="8bc7e-170">Angi filteret til å dekke et valgt område av kunder du vil ha med i denne opprettelsen av massetilbud i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="8bc7e-171">Bruk følgende format Kunde1..KundeN.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="8bc7e-172">Du kan for eksempel sette filteret til: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="8bc7e-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="8bc7e-173">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-173">Click OK.</span></span>
10. <span data-ttu-id="8bc7e-174">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-174">Click OK.</span></span>
11. <span data-ttu-id="8bc7e-175">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="8bc7e-176">Kontroller at tilbud er opprettet for alle kunder som er angitt i rutinen Masseoppdatering, basert på den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="8bc7e-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

