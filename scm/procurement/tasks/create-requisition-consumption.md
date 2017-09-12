--- 
title: Opprette en rekvisisjon for forbruk
description: "Denne prosedyren hjelper deg gjennom prosessen for å opprette en rekvisisjon."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 07fe007005fcbbac1beecadb14dbd752376a0bd4
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="0ba8a-103">Opprette en rekvisisjon for forbruk</span><span class="sxs-lookup"><span data-stu-id="0ba8a-103">Create a requisition for consumption</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ba8a-104">Denne prosedyren hjelper deg gjennom prosessen for å opprette en rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="0ba8a-105">Den viser forskjellige måter å søke etter produkter på i innkjøpskatalogen og hvordan du legger til et produkt som ikke finnes i katalogen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-105">It shows you different ways to search for products in your procurement catalogue and how to add a product that isn’t in your catalogue.</span></span> <span data-ttu-id="0ba8a-106">Før du starter denne fremgangsmåten, må en innkjøpspolicy være definert med Forbruk som standardtype for rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="0ba8a-107">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="0ba8a-108">Prosedyren kan bare utføres av en brukerprofil som er definert som arbeider.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="0ba8a-109">Denne oppgaven vil vanligvis utføres av en ansatt.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="0ba8a-110">Med sikkerhetsrollen som ansatt kan du utføre oppgavene, eller hvis du bruker USMF, kan du logge inn med Alicia.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="0ba8a-111">Opprett en ny rekvisisjon</span><span class="sxs-lookup"><span data-stu-id="0ba8a-111">Create a new requisition</span></span>
1. <span data-ttu-id="0ba8a-112">Gå til Innkjøp og leverandører > Innkjøpsrekvisisjoner > Innkjøpsrekvisisjoner klargjort av meg.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="0ba8a-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-113">Click New.</span></span>
3. <span data-ttu-id="0ba8a-114">Gi rekvisisjonen et navn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="0ba8a-115">Angi en dato i feltet Ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="0ba8a-116">Som standard kopieres den forespurte datoen og regnskapsdatoen til innkjøpsrekvisisjonslinjene.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="0ba8a-117">De kan endres på linjenivå.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-117">They can be changed at the line level.</span></span> <span data-ttu-id="0ba8a-118">Ønsket dato er ønsket leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="0ba8a-119">Angi en dato i feltet Regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="0ba8a-120">Regnskapsdatoen brukes til å registrere regnskapsoppføringen i økonomimodulen, og til å validere hvorvidt budsjettmidler er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="0ba8a-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-121">Click OK.</span></span>
7. <span data-ttu-id="0ba8a-122">Klikk rullegardinknappen i feltet Årsak for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0ba8a-123">Bestillingsårsaken du velger, vises som standard for innkjøpsrekvisisjonslinjene, men du kan endre den på linjenivået.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="0ba8a-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="0ba8a-125">Velg årsaken</span><span class="sxs-lookup"><span data-stu-id="0ba8a-125">Select the reason</span></span>
10. <span data-ttu-id="0ba8a-126">I Detaljer-feltet angir du en mer beskrivende begrunnelse for rekvisisjonen</span><span class="sxs-lookup"><span data-stu-id="0ba8a-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="0ba8a-127">Legge til en linje i rekvisisjonen</span><span class="sxs-lookup"><span data-stu-id="0ba8a-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="0ba8a-128">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-128">Click Add line.</span></span>
    * <span data-ttu-id="0ba8a-129">Det finnes to måter å legge til linjer i innkjøpsrekvisisjonen på.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="0ba8a-130">Hvis du allerede kjenner produktnummer, eller du allerede vet at du ber om et produkt som ikke er i produktkatalogen, kan du legge til linjen direkte med "Legg til linje".</span><span class="sxs-lookup"><span data-stu-id="0ba8a-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalogueue, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="0ba8a-131">Den andre måten er å bruke "Legg til produkter", der du kan bruke søk og filtrering til å finne varer i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalogueue.</span></span>    
2. <span data-ttu-id="0ba8a-132">Klikk i raden du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="0ba8a-133">Bestilleren er arbeideren som har bedt om rekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="0ba8a-134">Som standard er personen som klargjør rekvisisjonen, arbeideren som har bedt om den.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="0ba8a-135">Du må få tillatelse til å klargjøre en rekvisisjonslinje på vegne av en annen arbeider.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="0ba8a-136">Hvis du har slike tillatelser, vises de andre arbeiderne i dette oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="0ba8a-137">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="0ba8a-138">Varene som er tilgjengelige for deg å velge, begrenses av kategoritilgangspolicyen og innkjøpskatalogen for den juridiske enheten for innkjøp. </span><span class="sxs-lookup"><span data-stu-id="0ba8a-138">The items that are available for you to choose are limited by the category access policy and the procurement catalogue for the buying legal entity.</span></span>   
4. <span data-ttu-id="0ba8a-139">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="0ba8a-140">Legge til flere produkter i rekvisisjonen</span><span class="sxs-lookup"><span data-stu-id="0ba8a-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="0ba8a-141">Klikk Legg til produkter.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-141">Click Add products.</span></span>
    * <span data-ttu-id="0ba8a-142">Dette er alternativet der du kan søke etter produkter i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-142">This is the option where you can search for products in the product catalogueue.</span></span>    
2. <span data-ttu-id="0ba8a-143">I Finn innkjøpskategorinode-feltet skriver du inn første del av navnet på kategorien du leter etter, og klikk deretter Enter.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="0ba8a-144">Skriv for eksempel comput.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-144">For example, type comput.</span></span>  
3. <span data-ttu-id="0ba8a-145">Bruk InvokeDefaultButton-snarveien.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="0ba8a-146">Bruk filteret til å filtrere listen over produkter i den valgte kategorien.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="0ba8a-147">Velg produktkortet som du vil legge til i rekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="0ba8a-148">Klikk Tilføy til linjer.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-148">Click Add to lines.</span></span>
7. <span data-ttu-id="0ba8a-149">Angi et tall i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="0ba8a-150">I Finn innkjøpskategorinode-feltet skriver du inn første del av navnet på kategorien du leter etter, og klikk deretter Enter.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="0ba8a-151">Skriv for eksempel Høy (merkepenner).</span><span class="sxs-lookup"><span data-stu-id="0ba8a-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="0ba8a-152">Bruk InvokeDefaultButton-snarveien.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="0ba8a-153">Klikk Tilføy ulistede produkter til linjer for å legge til et produkt som ikke er oppført i innkjøpskatalogen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalogue.</span></span>
11. <span data-ttu-id="0ba8a-154">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="0ba8a-155">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="0ba8a-156">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-156">Click OK.</span></span>
14. <span data-ttu-id="0ba8a-157">Legg til en beskrivelse av produktet i Varebeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="0ba8a-158">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="0ba8a-159">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="0ba8a-160">Hvis du kjenner prisen for en bestemt leverandør (som du velger i leverandørkontofeltet), kan du angi denne prisen</span><span class="sxs-lookup"><span data-stu-id="0ba8a-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="0ba8a-161">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0ba8a-162">Leverandører som er tilgjengelige i dette feltet avhenger av innkjøpspolicyer og statusen som leverandøren har for gjeldende innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="0ba8a-163">Som et alternativ til å velge en leverandør her, kan du klikke knappen Foreslå leverandør.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="0ba8a-164">Velg leverandøren du vil bruke, i listen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="0ba8a-165">Skriv inn en verdi i feltet Eksternt varenummer.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="0ba8a-166">Dette er et referansenummer for produktet som er kjent av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="0ba8a-167">Dette kan for eksempel være varenummeret for produktet i leverandørens egen katalog.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-167">For example, this could be the item number of the product in the vendor's own catalogue.</span></span>  
20. <span data-ttu-id="0ba8a-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="0ba8a-169">Fordel beløp</span><span class="sxs-lookup"><span data-stu-id="0ba8a-169">Distribute amounts</span></span>
1. <span data-ttu-id="0ba8a-170">Klikk Finans.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-170">Click Financials.</span></span>
2. <span data-ttu-id="0ba8a-171">Klikk Fordel beløp.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="0ba8a-172">Denne prosessen viser deg hvordan du distribuerer kostnaden for den første linjen mellom 2 kontoer.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="0ba8a-173">Dette kan også gjøres senere når rekvisisjonen er til vurdering.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="0ba8a-174">Klikk Del for å opprette en ny distribusjonslinje.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="0ba8a-175">Velg det første kostsenteret som skal ta del i kostnaden i feltet Finanskonto.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-175">In the Ledger account field select the first cost centre that should take part of the cost.</span></span>
5. <span data-ttu-id="0ba8a-176">Velg den andre distribusjonslinjen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="0ba8a-177">Angir det andre kostsenteret i Finanskonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-177">In the Ledger account field specify the other cost centre.</span></span>
7. <span data-ttu-id="0ba8a-178">Klikk Fordel likt.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="0ba8a-179">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="0ba8a-180">Vise linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="0ba8a-180">View line details</span></span>
1. <span data-ttu-id="0ba8a-181">Aktiver/deaktiver utvidelsen av delen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="0ba8a-182">Sende rekvisisjonen</span><span class="sxs-lookup"><span data-stu-id="0ba8a-182">Submit the requisition</span></span>
1. <span data-ttu-id="0ba8a-183">Klikk Arbeidsflyt for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="0ba8a-184">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-184">Click Submit.</span></span>
3. <span data-ttu-id="0ba8a-185">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-185">Close the page.</span></span>
4. <span data-ttu-id="0ba8a-186">I feltet Kommentar skriver du inn en merknad for godkjenneren av rekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="0ba8a-187">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-187">Click Submit.</span></span>
6. <span data-ttu-id="0ba8a-188">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-188">Close the page.</span></span>
7. <span data-ttu-id="0ba8a-189">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-189">Refresh the page.</span></span>


