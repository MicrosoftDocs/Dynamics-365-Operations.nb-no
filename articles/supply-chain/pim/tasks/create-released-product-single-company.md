---
title: Opprette et frigitt produkt for ett firma
description: Denne prosedyren viser hvordan du oppretter ett enkelt frigitt produkt i konteksten for én enkelt juridisk enhet.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe1f34f268c6427c1381a9cfced49334893acc00
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833287"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="649e5-103">Opprette et frigitt produkt for ett firma</span><span class="sxs-lookup"><span data-stu-id="649e5-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="649e5-104">Denne prosedyren viser hvordan du oppretter ett enkelt frigitt produkt i konteksten for én enkelt juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="649e5-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="649e5-105">Når det frigitte produktet er opprettet, er det umiddelbart tilgjengelig bare i denne enheten.</span><span class="sxs-lookup"><span data-stu-id="649e5-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="649e5-106">Du kan gå gjennom denne prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="649e5-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="649e5-107">Denne oppgaven utføres vanligvis av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="649e5-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="649e5-108">Opprett et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="649e5-108">Create a released product</span></span>
1. <span data-ttu-id="649e5-109">Gå til Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="649e5-109">Go to Released products.</span></span>
2. <span data-ttu-id="649e5-110">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="649e5-110">Click New.</span></span>
3. <span data-ttu-id="649e5-111">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="649e5-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="649e5-112">Hvis et produktnummer ikke angis automatisk i feltet produkt, skriver du inn et unikt produktnummer.</span><span class="sxs-lookup"><span data-stu-id="649e5-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="649e5-113">Dette trinnet er bare nødvendig hvis ingen nummerserie er definert for produktnumre.</span><span class="sxs-lookup"><span data-stu-id="649e5-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="649e5-114">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="649e5-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="649e5-115">Produktnavnet hentes som standard til et søkenavn.</span><span class="sxs-lookup"><span data-stu-id="649e5-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="649e5-116">Hvis du trenger, kan du velge for å endre søkenavnet.</span><span class="sxs-lookup"><span data-stu-id="649e5-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="649e5-117">Klikk på rullegardinknappen i feltet Varemodellgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-118">Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger.</span><span class="sxs-lookup"><span data-stu-id="649e5-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="649e5-119">Innstillingene bestemmer også hvordan forbruk av varer skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="649e5-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="649e5-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="649e5-121">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="649e5-122">Klikk på rullegardinknappen i feltet Varegruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-123">Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper basert på vareegenskaper.</span><span class="sxs-lookup"><span data-stu-id="649e5-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="649e5-124">Hvis du fore eksempel vil styre hvordan informasjon er postert til hovedkontoer, kan du opprette en serie med forskjellige varegrupper som er knyttet til bestemte hovedkontoer.</span><span class="sxs-lookup"><span data-stu-id="649e5-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="649e5-125">Dette gjør det mulig for deg å spore lagerverdien for varer på forskjellige stadier.</span><span class="sxs-lookup"><span data-stu-id="649e5-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="649e5-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="649e5-127">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="649e5-128">Klikk på rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-129">Lagringsdimensjoner hjelper deg styre hvordan varer lagres og hentes fra lageret.</span><span class="sxs-lookup"><span data-stu-id="649e5-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="649e5-130">En lagringsdimensjon kan for eksempel være Område og lager.</span><span class="sxs-lookup"><span data-stu-id="649e5-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="649e5-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="649e5-132">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="649e5-133">Klikk på rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-134">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du kan legge til et produkt.</span><span class="sxs-lookup"><span data-stu-id="649e5-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="649e5-135">Parti- eller serienummer brukes for eksempel til å spore varer på lager.</span><span class="sxs-lookup"><span data-stu-id="649e5-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="649e5-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="649e5-137">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="649e5-138">Klikk på rullegardinknappen i feltet Lagerenhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-139">Lagerenheten bestemmer hvordan produktet er bestemmes mengdemessig når de lagres på lageret.</span><span class="sxs-lookup"><span data-stu-id="649e5-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="649e5-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="649e5-141">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="649e5-142">Klikk på rullegardinknappen i feltet Innkjøpsenhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-143">Innkjøpsenheten bestemmer hvordan produktet bestemmes mengdemessig når det er kjøpt fra en leverandør.</span><span class="sxs-lookup"><span data-stu-id="649e5-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="649e5-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="649e5-145">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="649e5-146">Klikk på rullegardinknappen i feltet Salgsenhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-147">Salgsenheten bestemmer hvordan produktet bestemmes mengdemessig når det selges til en kunde.</span><span class="sxs-lookup"><span data-stu-id="649e5-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="649e5-148">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="649e5-149">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="649e5-150">Klikk på rullegardinknappen i feltet Stykklisteenhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-151">Stykklisteenheten bestemmer hvordan produktet er bestemmes mengdemessig når du bruker den i en stykkliste (BOM).</span><span class="sxs-lookup"><span data-stu-id="649e5-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="649e5-152">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="649e5-153">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="649e5-154">Klikk på rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-155">Mva-gruppen for vare i Salgsavgift-gruppen bestemmer hvordan mva beregnes for hver vare.</span><span class="sxs-lookup"><span data-stu-id="649e5-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="649e5-156">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="649e5-157">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="649e5-158">Klikk på rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="649e5-159">Mva-gruppen for vare i Kjøpsavgift-gruppen bestemmer hvordan innkjøpsavgift beregnes for hver vare.</span><span class="sxs-lookup"><span data-stu-id="649e5-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="649e5-160">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="649e5-161">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="649e5-162">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="649e5-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="649e5-163">Legg til produktegenskaper</span><span class="sxs-lookup"><span data-stu-id="649e5-163">Add product characteristics</span></span>
1. <span data-ttu-id="649e5-164">Vis eller skjul delen Administrer lager.</span><span class="sxs-lookup"><span data-stu-id="649e5-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="649e5-165">Angi et tall i feltet Nettovekt.</span><span class="sxs-lookup"><span data-stu-id="649e5-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="649e5-166">Angi et tall i feltet Taravekt.</span><span class="sxs-lookup"><span data-stu-id="649e5-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="649e5-167">Angi et nummer i Bruttodybde-feltet.</span><span class="sxs-lookup"><span data-stu-id="649e5-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="649e5-168">Angi et nummer i Bruttobredde-feltet.</span><span class="sxs-lookup"><span data-stu-id="649e5-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="649e5-169">Angi et tall i Bruttohøyde-feltet.</span><span class="sxs-lookup"><span data-stu-id="649e5-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="649e5-170">Angi et tall i feltet Volum.</span><span class="sxs-lookup"><span data-stu-id="649e5-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="649e5-171">Legg til finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="649e5-171">Add financial dimensions</span></span>
1. <span data-ttu-id="649e5-172">Vis eller skjul delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="649e5-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="649e5-173">Klikk på rullegardinknappen i feltet BusinessUnit for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="649e5-174">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="649e5-175">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="649e5-176">Klikk på rullegardinknappen i feltet CostCenter for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="649e5-177">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="649e5-178">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="649e5-179">Klikk på rullegardinknappen i Avdeling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="649e5-180">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="649e5-181">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="649e5-182">Klikk på rullegardinknappen i feltet ItemGroup for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="649e5-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="649e5-183">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="649e5-184">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="649e5-184">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]