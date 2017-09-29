--- 
title: Opprette et frigitt produkt for ett firma
description: "Denne prosedyren viser hvordan du oppretter ett enkelt frigitt produkt i konteksten for én enkelt juridisk enhet."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 042eafc29e377e0ad6fb8dc1499daf8eb105b7ed
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="7598f-103">Opprette et frigitt produkt for ett firma</span><span class="sxs-lookup"><span data-stu-id="7598f-103">Create a released product for a single company</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7598f-104">Denne prosedyren viser hvordan du oppretter ett enkelt frigitt produkt i konteksten for én enkelt juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="7598f-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="7598f-105">Når det frigitte produktet er opprettet, er det umiddelbart tilgjengelig bare i denne enheten.</span><span class="sxs-lookup"><span data-stu-id="7598f-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="7598f-106">Du kan gå gjennom denne prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="7598f-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="7598f-107">Denne oppgaven utføres vanligvis av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="7598f-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="7598f-108">Opprett et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="7598f-108">Create a released product</span></span>
1. <span data-ttu-id="7598f-109">Gå til Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="7598f-109">Go to Released products.</span></span>
2. <span data-ttu-id="7598f-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7598f-110">Click New.</span></span>
3. <span data-ttu-id="7598f-111">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="7598f-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7598f-112">Hvis et produktnummer ikke angis automatisk i feltet produkt, skriver du inn et unikt produktnummer.</span><span class="sxs-lookup"><span data-stu-id="7598f-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="7598f-113">Dette trinnet er bare nødvendig hvis ingen nummerserie er definert for produktnumre.</span><span class="sxs-lookup"><span data-stu-id="7598f-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="7598f-114">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="7598f-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="7598f-115">Produktnavnet hentes som standard til et søkenavn.</span><span class="sxs-lookup"><span data-stu-id="7598f-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="7598f-116">Hvis du trenger, kan du velge for å endre søkenavnet.</span><span class="sxs-lookup"><span data-stu-id="7598f-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="7598f-117">Klikk rullegardinknappen i feltet Varemodellgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-118">Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger.</span><span class="sxs-lookup"><span data-stu-id="7598f-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="7598f-119">Innstillingene bestemmer også hvordan forbruk av varer skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="7598f-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="7598f-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="7598f-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="7598f-122">Klikk rullegardinknappen i feltet Varegruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-123">Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper basert på vareegenskaper.</span><span class="sxs-lookup"><span data-stu-id="7598f-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="7598f-124">Hvis du fore eksempel vil styre hvordan informasjon er postert til hovedkontoer, kan du opprette en serie med forskjellige varegrupper som er knyttet til bestemte hovedkontoer.</span><span class="sxs-lookup"><span data-stu-id="7598f-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="7598f-125">Dette gjør det mulig for deg å spore lagerverdien for varer på forskjellige stadier.</span><span class="sxs-lookup"><span data-stu-id="7598f-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="7598f-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="7598f-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="7598f-128">Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-129">Lagringsdimensjoner hjelper deg styre hvordan varer lagres og hentes fra lageret.</span><span class="sxs-lookup"><span data-stu-id="7598f-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="7598f-130">En lagringsdimensjon kan for eksempel være Område og lager.</span><span class="sxs-lookup"><span data-stu-id="7598f-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="7598f-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="7598f-132">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7598f-133">Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-134">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du kan legge til et produkt.</span><span class="sxs-lookup"><span data-stu-id="7598f-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="7598f-135">Parti- eller serienummer brukes for eksempel til å spore varer på lager.</span><span class="sxs-lookup"><span data-stu-id="7598f-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="7598f-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="7598f-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="7598f-138">Klikk rullegardinknappen i feltet Lagerenhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-139">Lagerenheten bestemmer hvordan produktet er bestemmes mengdemessig når de lagres på lageret.</span><span class="sxs-lookup"><span data-stu-id="7598f-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="7598f-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="7598f-141">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="7598f-142">Klikk rullegardinknappen i feltet Innkjøpsenhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-143">Innkjøpsenheten bestemmer hvordan produktet er bestemmes mengdemessig når det er kjøpt fra en leverandør.</span><span class="sxs-lookup"><span data-stu-id="7598f-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="7598f-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="7598f-145">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="7598f-146">Klikk rullegardinknappen i feltet Salgsenhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-147">Salgsenheten bestemmer hvordan produktet er bestemmes mengdemessig når den selges til en kunde.</span><span class="sxs-lookup"><span data-stu-id="7598f-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="7598f-148">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="7598f-149">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="7598f-150">Klikk rullegardinknappen i feltet Stykklisteenhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-151">Stykklisteenheten bestemmer hvordan produktet er bestemmes mengdemessig når du bruker den i en stykkliste (BOM).</span><span class="sxs-lookup"><span data-stu-id="7598f-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="7598f-152">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="7598f-153">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="7598f-154">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-155">Mva-gruppen for vare i Salgsavgift-gruppen bestemmer hvordan mva beregnes for hver vare.</span><span class="sxs-lookup"><span data-stu-id="7598f-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="7598f-156">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="7598f-157">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="7598f-158">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7598f-159">Mva-gruppen for vare i Kjøpsavgift-gruppen bestemmer hvordan innkjøpsavgift beregnes for hver vare.</span><span class="sxs-lookup"><span data-stu-id="7598f-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="7598f-160">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="7598f-161">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="7598f-162">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7598f-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="7598f-163">Legg til produktegenskaper</span><span class="sxs-lookup"><span data-stu-id="7598f-163">Add product characteristics</span></span>
1. <span data-ttu-id="7598f-164">Vis eller skjul delen Administrer lager.</span><span class="sxs-lookup"><span data-stu-id="7598f-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="7598f-165">Angi et tall i feltet Nettovekt.</span><span class="sxs-lookup"><span data-stu-id="7598f-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="7598f-166">Angi et tall i feltet Taravekt.</span><span class="sxs-lookup"><span data-stu-id="7598f-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="7598f-167">Angi et nummer i Bruttodybde-feltet.</span><span class="sxs-lookup"><span data-stu-id="7598f-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="7598f-168">Angi et nummer i Bruttobredde-feltet.</span><span class="sxs-lookup"><span data-stu-id="7598f-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="7598f-169">Angi et tall i Bruttohøyde-feltet.</span><span class="sxs-lookup"><span data-stu-id="7598f-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="7598f-170">Angi et tall i feltet Volum.</span><span class="sxs-lookup"><span data-stu-id="7598f-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="7598f-171">Legg til finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="7598f-171">Add financial dimensions</span></span>
1. <span data-ttu-id="7598f-172">Vis eller skjul delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="7598f-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="7598f-173">Klikk rullegardinknappen i feltet BusinessUnit for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7598f-174">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7598f-175">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7598f-176">Klikk rullegardinknappen i feltet CostCenter for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7598f-177">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="7598f-178">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="7598f-179">Klikk rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="7598f-180">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="7598f-181">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="7598f-182">Klikk rullegardinknappen i feltet ItemGroup for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7598f-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="7598f-183">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="7598f-184">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7598f-184">In the list, click the link in the selected row.</span></span>


