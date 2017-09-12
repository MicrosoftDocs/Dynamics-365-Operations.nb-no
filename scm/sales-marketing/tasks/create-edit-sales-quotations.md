--- 
title: Opprette og redigere salgstilbud
description: "Denne fremgangsmåten beskriver hvordan du oppretter og oppdaterer et salgstilbud."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f56b495131836689395a2124d5a834579e1646b7
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="26c7c-103">Opprette og redigere salgstilbud</span><span class="sxs-lookup"><span data-stu-id="26c7c-103">Create and edit sales quotations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26c7c-104">Denne fremgangsmåten beskriver hvordan du oppretter og oppdaterer et salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="26c7c-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="26c7c-105">Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="26c7c-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="26c7c-106">Opprett et salgstilbud</span><span class="sxs-lookup"><span data-stu-id="26c7c-106">Create a sales quotation</span></span>
1. <span data-ttu-id="26c7c-107">Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="26c7c-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="26c7c-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="26c7c-108">Click New.</span></span>
3. <span data-ttu-id="26c7c-109">Velg Kundeemne i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="26c7c-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="26c7c-110">Angi eller velg en verdi i feltet Kundeemne.</span><span class="sxs-lookup"><span data-stu-id="26c7c-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="26c7c-111">Utvid seksjonen Generelt.</span><span class="sxs-lookup"><span data-stu-id="26c7c-111">Expand the General section.</span></span>
    * <span data-ttu-id="26c7c-112">Fordi du valgte å opprette et tilbud fra området Salg og markedsføring settes typen automatisk til Salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="26c7c-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="26c7c-113">Hvis du vil opprette et tilbud for et prosjekt, må du åpne det fra prosjektstyrings- og regnskapsmodulen.</span><span class="sxs-lookup"><span data-stu-id="26c7c-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="26c7c-114">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="26c7c-114">Click OK.</span></span>
    * <span data-ttu-id="26c7c-115">Feltene og handlinger i tilbudslinjene er veldig lik de i salgsordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="26c7c-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="26c7c-116">Som salgsordrer kan du kan opprette tilbud for en bestemt vare, eller når varenummeret er ukjent eller ikke finnes på tidspunktet for oppretting av tilbud, kan tilbud opprettes for en salgskategori.</span><span class="sxs-lookup"><span data-stu-id="26c7c-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="26c7c-117">Angi eller velg en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="26c7c-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="26c7c-118">Skriv inn en verdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="26c7c-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="26c7c-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="26c7c-119">Close the page.</span></span>
10. <span data-ttu-id="26c7c-120">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="26c7c-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="26c7c-121">Hvis det finnes gyldige forretningsavtaler for varen som er valgt på linjen, kopieres den aktuelle prisen og rabattene automatisk til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="26c7c-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="26c7c-122">Kontroller at Enhetspris-feltet inneholder en verdi, og du kan også angi rabattverdier hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="26c7c-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="26c7c-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="26c7c-123">Click Save.</span></span>
12. <span data-ttu-id="26c7c-124">Klikk Salgstilbud i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="26c7c-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="26c7c-125">Klikk Totaler.</span><span class="sxs-lookup"><span data-stu-id="26c7c-125">Click Totals.</span></span>
14. <span data-ttu-id="26c7c-126">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="26c7c-126">Click OK.</span></span>
15. <span data-ttu-id="26c7c-127">Klikk Salgstilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="26c7c-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="26c7c-128">Klikk Priser.</span><span class="sxs-lookup"><span data-stu-id="26c7c-128">Click Prices.</span></span>
    * <span data-ttu-id="26c7c-129">På siden Kjør prissimulering kan du eksperimentere med å justere forventet omsetning eller lønnsomhet for tilbudet basert på ønsket enhetspris, rabattbeløp, rabattprosent, totalbeløp, margin eller dekningsgrad.</span><span class="sxs-lookup"><span data-stu-id="26c7c-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="26c7c-130">Når du er fornøyd med måltallene, du bruker forslaget på tilbudslinjen, og de prisrelaterte feltene oppdateres tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="26c7c-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="26c7c-131">Du kan opprette så mange prissimuleringer som du ønsker.</span><span class="sxs-lookup"><span data-stu-id="26c7c-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="26c7c-132">Når du klikker Ny, kopieres prisbetingelsene fra gjeldende tilbudslinje til siden.</span><span class="sxs-lookup"><span data-stu-id="26c7c-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="26c7c-133">Du kan deretter endre verdiene i de prisrelaterte feltene til målene.</span><span class="sxs-lookup"><span data-stu-id="26c7c-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="26c7c-134">En endring i ett av feltene vil utløse omberegning i alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="26c7c-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="26c7c-135">For at systemet skal beregne salgsmargin og dekningsgrad, må produktets enhetskostnad være kjent.</span><span class="sxs-lookup"><span data-stu-id="26c7c-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="26c7c-136">Bruk kategorien Simulerte priser for en detaljert visning av de opprinnelige prisene, foreslåtte endringer og deres virkning på tilbudstotalene.</span><span class="sxs-lookup"><span data-stu-id="26c7c-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="26c7c-137">Som regel når en simulering som angir et nytt beløp brukes for tilbudslinjen, beregner systemet på nytt og angir en ny verdi i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="26c7c-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="26c7c-138">Hvis simuleringen er basert på en ny margin eller et nytt dekningsbidrag, oppdateres bare feltet Nettobeløp og enhetsprisen er tom.</span><span class="sxs-lookup"><span data-stu-id="26c7c-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="26c7c-139">I begge tilfeller slettes eventuelle rabatter som var på tilbudslinjen før simuleringen.</span><span class="sxs-lookup"><span data-stu-id="26c7c-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="26c7c-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="26c7c-140">Close the page.</span></span>
18. <span data-ttu-id="26c7c-141">Klikk Tilbud i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="26c7c-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="26c7c-142">Velg Send tilbud.</span><span class="sxs-lookup"><span data-stu-id="26c7c-142">Click Send quotation.</span></span>
20. <span data-ttu-id="26c7c-143">Velg Ja i feltet Skriv ut tilbud.</span><span class="sxs-lookup"><span data-stu-id="26c7c-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="26c7c-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="26c7c-144">Click OK.</span></span>
    * <span data-ttu-id="26c7c-145">Rapporten kan ta litt tid å generere.</span><span class="sxs-lookup"><span data-stu-id="26c7c-145">The report may take a minute to generate.</span></span> <span data-ttu-id="26c7c-146">Ikke lukk siden før dette gjøres.</span><span class="sxs-lookup"><span data-stu-id="26c7c-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="26c7c-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="26c7c-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="26c7c-148">Oppdater et salgstilbud</span><span class="sxs-lookup"><span data-stu-id="26c7c-148">Update a sales quotation</span></span>
1. <span data-ttu-id="26c7c-149">Klikk Følg opp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="26c7c-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="26c7c-150">Klikk Konverter til kunde.</span><span class="sxs-lookup"><span data-stu-id="26c7c-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="26c7c-151">Angi en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="26c7c-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="26c7c-152">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="26c7c-152">Click Check.</span></span>
    * <span data-ttu-id="26c7c-153">Kontroller at det vises en melding om at kontonummeret som du skrev inn, er ledig for bruk.</span><span class="sxs-lookup"><span data-stu-id="26c7c-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="26c7c-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="26c7c-154">Click OK.</span></span>
    * <span data-ttu-id="26c7c-155">Systemet har nå opprettet en ny kundekonto for kundeemnet på tilbudet.</span><span class="sxs-lookup"><span data-stu-id="26c7c-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="26c7c-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="26c7c-156">Close the page.</span></span>
7. <span data-ttu-id="26c7c-157">Klikk Følg opp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="26c7c-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="26c7c-158">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="26c7c-158">Click Confirm.</span></span>
9. <span data-ttu-id="26c7c-159">Angi eller velg en verdi i feltet Årsak.</span><span class="sxs-lookup"><span data-stu-id="26c7c-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="26c7c-160">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="26c7c-160">Click OK.</span></span>
11. <span data-ttu-id="26c7c-161">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="26c7c-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="26c7c-162">Klikk Salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="26c7c-162">Click Sales orders.</span></span>
13. <span data-ttu-id="26c7c-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="26c7c-163">Close the page.</span></span>


