--- 
title: Definere regler for salgsprovisjon
description: "Denne fremgangsmåten viser hvordan du konfigurerer og aktiverer salgprovisjonsberegning og sporing."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
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
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 3d5c38b1f07803242350fe016b45c45d49c0b59b
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="38fa1-103">Definere regler for salgsprovisjon</span><span class="sxs-lookup"><span data-stu-id="38fa1-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38fa1-104">Denne fremgangsmåten viser hvordan du konfigurerer og aktiverer salgprovisjonsberegning og sporing.</span><span class="sxs-lookup"><span data-stu-id="38fa1-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="38fa1-105">Fremgangsmåten viser hvordan du oppretter både kunde- og varegrupper for provisjon, og deretter hvordan du kobler en valgt kunde og produktet til de respektive gruppene.</span><span class="sxs-lookup"><span data-stu-id="38fa1-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="38fa1-106">Disse gruppene brukes deretter i oppsettet for beregning av provisjon for å opprette kombinasjonen av en kunde, vare og selgere som må samsvare med salgsordren for å kvalifisere selgerne til en provisjon.</span><span class="sxs-lookup"><span data-stu-id="38fa1-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="38fa1-107">Det er valgfritt å opprette kunde- og provisjonsgrupper, ettersom beregning av provisjonen også kan gjøres for en individuell kunde og/eller vare.</span><span class="sxs-lookup"><span data-stu-id="38fa1-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="38fa1-108">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="38fa1-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="38fa1-109">Definere provisjonsgrupper og provisjonssatser</span><span class="sxs-lookup"><span data-stu-id="38fa1-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="38fa1-110">Gå til Salg og markedsføring > Provisjoner > Kundegrupper for provisjon.</span><span class="sxs-lookup"><span data-stu-id="38fa1-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="38fa1-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="38fa1-111">Click New.</span></span>
3. <span data-ttu-id="38fa1-112">Skriv inn en verdi i feltet Gruppe.</span><span class="sxs-lookup"><span data-stu-id="38fa1-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="38fa1-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="38fa1-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="38fa1-114">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="38fa1-114">Click Save.</span></span>
6. <span data-ttu-id="38fa1-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="38fa1-115">Close the page.</span></span>
7. <span data-ttu-id="38fa1-116">Gå til Salg og markedsføring > Provisjoner > Varegrupper.</span><span class="sxs-lookup"><span data-stu-id="38fa1-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="38fa1-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="38fa1-117">Click New.</span></span>
9. <span data-ttu-id="38fa1-118">Skriv inn en verdi i feltet Gruppe.</span><span class="sxs-lookup"><span data-stu-id="38fa1-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="38fa1-119">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="38fa1-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="38fa1-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="38fa1-120">Close the page.</span></span>
12. <span data-ttu-id="38fa1-121">Gå til Salg og markedsføring > Provisjoner > Salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="38fa1-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="38fa1-122">En provisjonssalgsgruppe angir de ansatte i selgerroller som er berettiget til å motta en provisjon når en kunde som er knyttet til den relevante salgsgruppen kjøper visse varer.</span><span class="sxs-lookup"><span data-stu-id="38fa1-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="38fa1-123">I USMF-demodatafirmaet er det en salgsgruppe kalt Selgere USA.</span><span class="sxs-lookup"><span data-stu-id="38fa1-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="38fa1-124">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="38fa1-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="38fa1-125">Klikk Selger.</span><span class="sxs-lookup"><span data-stu-id="38fa1-125">Click Sales rep.</span></span>
    * <span data-ttu-id="38fa1-126">Selger-siden viser en liste over firmaets selgere som er knyttet til en bestemt provisjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="38fa1-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="38fa1-127">Du kan tilordne flere selgere til samme gruppe og definere deres respektive del av totale provisjonsgebyret som en prosentverdi.</span><span class="sxs-lookup"><span data-stu-id="38fa1-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="38fa1-128">Den totale provisjonsandelen for alle ansatte må ikke overskride 100.</span><span class="sxs-lookup"><span data-stu-id="38fa1-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="38fa1-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="38fa1-130">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="38fa1-130">Click Edit.</span></span>
17. <span data-ttu-id="38fa1-131">Angi Provisjonsandel som 50.</span><span class="sxs-lookup"><span data-stu-id="38fa1-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="38fa1-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="38fa1-132">Click New.</span></span>
19. <span data-ttu-id="38fa1-133">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="38fa1-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="38fa1-134">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="38fa1-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="38fa1-135">Du kan for eksempel filtrere på Navn-feltet med verdien Susan Burk.</span><span class="sxs-lookup"><span data-stu-id="38fa1-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="38fa1-136">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="38fa1-136">Click Select.</span></span>
22. <span data-ttu-id="38fa1-137">Angi Provisjonsandel som 50.</span><span class="sxs-lookup"><span data-stu-id="38fa1-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="38fa1-138">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="38fa1-138">Click Save.</span></span>
24. <span data-ttu-id="38fa1-139">Gå til Salg og markedsføring > Provisjoner > Provisjonsberegning.</span><span class="sxs-lookup"><span data-stu-id="38fa1-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="38fa1-140">Du kan definere provisjonssatsen som ansatt skal motta for en salgstransaksjon når den inneholder forhåndangitt kombinasjon av kunde og produkt, på siden Provisjonsberegning.</span><span class="sxs-lookup"><span data-stu-id="38fa1-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="38fa1-141">Som en del av provisjonssatsoppsettet, må du angi grunnlaget for provisjonsberegning og om den skal inkludere eller ekskludere rabatter.</span><span class="sxs-lookup"><span data-stu-id="38fa1-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="38fa1-142">Du kan også angi en gyldighetsperiode for når provisjonssatsen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="38fa1-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="38fa1-143">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="38fa1-143">Click New.</span></span>
26. <span data-ttu-id="38fa1-144">Velg Gruppe i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="38fa1-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="38fa1-145">Klikk rullegardinknappen i feltet Varerelasjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="38fa1-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="38fa1-146">Finn og velg gruppen du opprettet tidligere, i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="38fa1-147">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="38fa1-148">Velg Gruppe i Kundekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="38fa1-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="38fa1-149">Klikk rullegardinknappen i Kunderelasjon-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="38fa1-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="38fa1-150">Velg gruppen du definerte tidligere, i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="38fa1-151">I Selger- relasjon-feltet klikker du rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="38fa1-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="38fa1-152">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="38fa1-153">Behold alternativet "Før linjerabatt".</span><span class="sxs-lookup"><span data-stu-id="38fa1-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="38fa1-154">Behold alternativet "Omsetning" som grunnlag for beregning av provisjonsverdi.</span><span class="sxs-lookup"><span data-stu-id="38fa1-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="38fa1-155">Angi et tall i feltet Provisjonssats i prosent.</span><span class="sxs-lookup"><span data-stu-id="38fa1-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="38fa1-156">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="38fa1-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="38fa1-157">Definere provisjonspostering</span><span class="sxs-lookup"><span data-stu-id="38fa1-157">Setting up commission posting</span></span>
1. <span data-ttu-id="38fa1-158">Gå til Salg og markedsføring > Provisjoner > Provisjonspostering.</span><span class="sxs-lookup"><span data-stu-id="38fa1-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="38fa1-159">Provisjonsgebyrer betales til ansatte, og må derfor defineres til å sikre riktig økonomisk postering til de aktuelle kontoene i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="38fa1-160">Dette gjøres på siden Provisjonspostering.</span><span class="sxs-lookup"><span data-stu-id="38fa1-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="38fa1-161">Gå gjennom oppsettet som er tilgjengelig for det gjeldende firmaet.</span><span class="sxs-lookup"><span data-stu-id="38fa1-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="38fa1-162">Vanligvis posteres provisjonsbeløpene til en dedikert utgiftskonto og motregnes til en egen konto for leverandører.</span><span class="sxs-lookup"><span data-stu-id="38fa1-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="38fa1-163">Hvis du ikke har satt opp regler for provisjonspostering, vil systemet ikke kunne fullføre fakturering av en salgsordre som har kvalifiserte provisjoner.</span><span class="sxs-lookup"><span data-stu-id="38fa1-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="38fa1-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="38fa1-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="38fa1-165">Tilordne en Provisjonsgruppe til en kunde og et produkt</span><span class="sxs-lookup"><span data-stu-id="38fa1-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="38fa1-166">Gå til Salg og markedsføring > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="38fa1-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="38fa1-167">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="38fa1-168">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="38fa1-169">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="38fa1-169">Click Edit.</span></span>
5. <span data-ttu-id="38fa1-170">Utvid delen Standarder for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="38fa1-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="38fa1-171">Klikk rullegardinknappen i feltet Provisjonsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="38fa1-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="38fa1-172">Velg gruppen du opprettet tidligere, i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="38fa1-173">Klikk rullegardinknappen i feltet Salgsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="38fa1-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="38fa1-174">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="38fa1-175">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="38fa1-175">Click Save.</span></span>
11. <span data-ttu-id="38fa1-176">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="38fa1-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="38fa1-177">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="38fa1-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="38fa1-178">Du kan for eksempel filtrere på Varenummer-feltet med verdien T0020.</span><span class="sxs-lookup"><span data-stu-id="38fa1-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="38fa1-179">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="38fa1-180">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="38fa1-180">Click Edit.</span></span>
15. <span data-ttu-id="38fa1-181">Utvid Selg-delen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="38fa1-182">Klikk rullegardinknappen i feltet Provisjonsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="38fa1-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="38fa1-183">Velg provisjonsgruppen du opprettet tidligere, i listen.</span><span class="sxs-lookup"><span data-stu-id="38fa1-183">In the list, select the commission group that you created earlier.</span></span>


