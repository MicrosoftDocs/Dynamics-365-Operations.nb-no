---
title: Angi og sammenligne tilbudsforespørsler og inngå kontrakter
description: Denne fremgangsmåten viser hvordan du registrerer svar på en tilbudsforespørsel, poengsum og sammenligner bud, og deretter gir budet til én av leverandørene.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cd4876acfebcc9595abb358cfc9b355e93041d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "350004"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="bc2be-103">Angi og sammenligne tilbudsforespørsler og inngå kontrakter</span><span class="sxs-lookup"><span data-stu-id="bc2be-103">Enter and compare RFQ bids, and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc2be-104">Denne fremgangsmåten viser hvordan du registrerer svar på en tilbudsforespørsel, poengsum og sammenligner bud, og deretter gir budet til én av leverandørene.</span><span class="sxs-lookup"><span data-stu-id="bc2be-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="bc2be-105">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="bc2be-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="bc2be-106">Før du begynner, må du ha en tilbudsforespørsel med to linjer som er sendt til minst to leverandører.</span><span class="sxs-lookup"><span data-stu-id="bc2be-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="bc2be-107">Du kan kjøre prosedyren "Opprett en tilbudsforespørsel" for å opprette dette.</span><span class="sxs-lookup"><span data-stu-id="bc2be-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="bc2be-108">Du må ha definert poengsumkriterier før du kan kjøre denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="bc2be-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="bc2be-109">Angi et svar fra en leverandør</span><span class="sxs-lookup"><span data-stu-id="bc2be-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="bc2be-110">Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="bc2be-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="bc2be-111">Velg en tilbudsforespørsel som har statusen Sendt, og klikk koblingen for saksnummeret for tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="bc2be-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="bc2be-112">Tilbudsforespørselen skulle ha vært sendt til minst to leverandører.</span><span class="sxs-lookup"><span data-stu-id="bc2be-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="bc2be-113">Klikk overskriften for å gå til listen over leverandører.</span><span class="sxs-lookup"><span data-stu-id="bc2be-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="bc2be-114">Velg leverandøren du vil angi et svar for i tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="bc2be-115">Klikk Angi svar.</span><span class="sxs-lookup"><span data-stu-id="bc2be-115">Click Enter reply.</span></span>
6. <span data-ttu-id="bc2be-116">Klikk Svar i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bc2be-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="bc2be-117">Klikk Kopier data for å svare.</span><span class="sxs-lookup"><span data-stu-id="bc2be-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="bc2be-118">Denne handlingen vil kopiere merkede data, for eksempel antallet fra saken for tilbudsforespørselen som svar på tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="bc2be-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="bc2be-119">Du kan også hoppe over denne handlingen og fylle ut alle svarfeltene manuelt når du redigerer svaret.</span><span class="sxs-lookup"><span data-stu-id="bc2be-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="bc2be-120">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="bc2be-120">Click Edit.</span></span>
9. <span data-ttu-id="bc2be-121">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="bc2be-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="bc2be-122">Velg den andre tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="bc2be-123">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="bc2be-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="bc2be-124">Gi budet poengsum</span><span class="sxs-lookup"><span data-stu-id="bc2be-124">Score the bid</span></span>
1. <span data-ttu-id="bc2be-125">Klikk overskriften for å gå til poengsummen for budet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="bc2be-126">Vis delen for poengsum for bud.</span><span class="sxs-lookup"><span data-stu-id="bc2be-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="bc2be-127">Angi et nummer for ett av poengsumkriteriene i poengsumfeltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="bc2be-128">Hvis du holder musepekeren over ett av poengkriteriene, viser et verktøytips området du må holde poengsummen innenfor.</span><span class="sxs-lookup"><span data-stu-id="bc2be-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="bc2be-129">Du kan legge til et tall mellom 1 og 5 i et av kriteriene i denne demoen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="bc2be-130">Velg et annet poengsumkriterium.</span><span class="sxs-lookup"><span data-stu-id="bc2be-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="bc2be-131">Angi et nummer i poengsumfeltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="bc2be-132">Vis delen for spørreskjemaer.</span><span class="sxs-lookup"><span data-stu-id="bc2be-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="bc2be-133">Hvis saken for tilbudsforespørsel har et spørreskjema som ble sendt til leverandørene, kan du skrive inn svarene i spørreskjemadelen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="bc2be-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bc2be-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="bc2be-135">Skriv inn et svar for en annen leverandør</span><span class="sxs-lookup"><span data-stu-id="bc2be-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="bc2be-136">Velg den neste leverandøren ved å fjerne leverandøren du akkurat har angitt for svaret, og deretter velge raden for den neste leverandøren.</span><span class="sxs-lookup"><span data-stu-id="bc2be-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="bc2be-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bc2be-138">Klikk Angi svar.</span><span class="sxs-lookup"><span data-stu-id="bc2be-138">Click Enter reply.</span></span>
4. <span data-ttu-id="bc2be-139">Klikk Kopier data for å svare.</span><span class="sxs-lookup"><span data-stu-id="bc2be-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="bc2be-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="bc2be-140">Click Edit.</span></span>
6. <span data-ttu-id="bc2be-141">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="bc2be-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="bc2be-142">Velg den andre tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="bc2be-143">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="bc2be-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="bc2be-144">Gi den andre budet poengsum</span><span class="sxs-lookup"><span data-stu-id="bc2be-144">Score the second bid</span></span>
1. <span data-ttu-id="bc2be-145">Klikk overskriften for å gå til poengsummen for budet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="bc2be-146">Angi et nummer i poengsumfeltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="bc2be-147">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bc2be-148">Angi et nummer i poengsumfeltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="bc2be-149">Sammenligne svarene</span><span class="sxs-lookup"><span data-stu-id="bc2be-149">Compare the replies</span></span>
1. <span data-ttu-id="bc2be-150">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bc2be-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="bc2be-151">Klikk Sammenlign svar.</span><span class="sxs-lookup"><span data-stu-id="bc2be-151">Click Compare replies.</span></span>
3. <span data-ttu-id="bc2be-152">Angi et tall i rangeringsfeltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="bc2be-153">Denne siden viser bud med overskrift og linjer, og den samlede poengsummen på overskriftsnivå.</span><span class="sxs-lookup"><span data-stu-id="bc2be-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="bc2be-154">Du kan sammenligne linjene ved å sortere i rutenettet, slik at tilsvarende linjer er ved siden av hverandre.</span><span class="sxs-lookup"><span data-stu-id="bc2be-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="bc2be-155">Informasjonen inneholder også: Antall: Antallet som er angitt av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="bc2be-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="bc2be-156">Dette kan være ulikt antallet angitt i tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="bc2be-157">Nettobeløp: Totalprisen en leverandør tilbyr, etter fratrekk for rabatter for varene på linjen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="bc2be-158">Avvik: Antall dager som leveringsdatoen i budhodet eller -linjen avviker fra den ønskede leveringsdatoen i tilbudsforespørselshodet eller -linjen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="bc2be-159">Du kan angi en rangering for hvert bud.</span><span class="sxs-lookup"><span data-stu-id="bc2be-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="bc2be-160">Velg overskriftslinjen for det andre budet du vil rangere.</span><span class="sxs-lookup"><span data-stu-id="bc2be-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="bc2be-161">Angi et tall i rangeringsfeltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="bc2be-162">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="bc2be-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="bc2be-163">Avvise et bud</span><span class="sxs-lookup"><span data-stu-id="bc2be-163">Reject a bid</span></span>
1. <span data-ttu-id="bc2be-164">Velg overskriftslinjen for budet du vil avvise.</span><span class="sxs-lookup"><span data-stu-id="bc2be-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="bc2be-165">Du kan bare godta, avvise eller returnere ett bud eller én linje i ett bud om gangen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="bc2be-166">Merk av for Merk.</span><span class="sxs-lookup"><span data-stu-id="bc2be-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="bc2be-167">Hvis du merker av for Merk i overskriften til budet, vil alle linjene også merkes av.</span><span class="sxs-lookup"><span data-stu-id="bc2be-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="bc2be-168">Du kan også velge å merke av et delsett av linjene i budet for å avvise eller godkjenne dem.</span><span class="sxs-lookup"><span data-stu-id="bc2be-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="bc2be-169">Det er mulig å godta budet til én leverandør for noen av linjene i en tilbudsforespørsel, og deretter gi andre linjer i tilbudsforespørselen til en annen leverandør, du må imidlertid gjøre dette i trinn 2, og for ett bud om gangen.</span><span class="sxs-lookup"><span data-stu-id="bc2be-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="bc2be-170">Hvis det finnes alternative linjer, kan du bare godta enten den opprinnelige budlinjen eller den alternative, men ikke begge.</span><span class="sxs-lookup"><span data-stu-id="bc2be-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="bc2be-171">Klikk Avvis.</span><span class="sxs-lookup"><span data-stu-id="bc2be-171">Click Reject.</span></span>
4. <span data-ttu-id="bc2be-172">Klikk Parametre for å åpne nedtrekksdialogskjemaet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="bc2be-173">Angi eller velg en verdi i Avvisningsårsak-feltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="bc2be-174">Årsaken til avvisningen lagres i svaret.</span><span class="sxs-lookup"><span data-stu-id="bc2be-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="bc2be-175">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bc2be-175">Click OK.</span></span>
7. <span data-ttu-id="bc2be-176">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bc2be-176">Click OK.</span></span>
8. <span data-ttu-id="bc2be-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bc2be-177">Close the page.</span></span>
9. <span data-ttu-id="bc2be-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bc2be-178">Close the page.</span></span>
10. <span data-ttu-id="bc2be-179">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="bc2be-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="bc2be-180">Godta et bud</span><span class="sxs-lookup"><span data-stu-id="bc2be-180">Accept a bid</span></span>
1. <span data-ttu-id="bc2be-181">Velg budet du vil godta, og deretter klikker du koblingen i Tilbudsforespørsel-feltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="bc2be-182">Klikk Svar i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bc2be-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="bc2be-183">Klikk Godta.</span><span class="sxs-lookup"><span data-stu-id="bc2be-183">Click Accept.</span></span>
    * <span data-ttu-id="bc2be-184">Hvis du har merket av for bestemte linjer og ikke andre, vil godtahandlingen bare inneholder de merkede linjene.</span><span class="sxs-lookup"><span data-stu-id="bc2be-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="bc2be-185">Hvis du vil godta alle linjer i budet, trenger du ikke merke av for linjene.</span><span class="sxs-lookup"><span data-stu-id="bc2be-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="bc2be-186">Klikk Parametre for å åpne nedtrekksdialogskjemaet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="bc2be-187">Dette lar deg registrere en årsak for å godta budet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="bc2be-188">Årsaken lagres i budet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="bc2be-189">Angi eller velg en verdi i Årsak til aksept-feltet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="bc2be-190">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bc2be-190">Click OK.</span></span>
7. <span data-ttu-id="bc2be-191">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bc2be-191">Click OK.</span></span>
    * <span data-ttu-id="bc2be-192">Dette genererer en bestilling basert på linjene som er inkludert i godkjenning av tilbudsforespørselen når du klikker OK.</span><span class="sxs-lookup"><span data-stu-id="bc2be-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="bc2be-193">Hvis det finnes andre bud som ikke er behandlet (godkjent, avvist eller returnerte), vil systemet be deg om å avvise de gjenværende budene.</span><span class="sxs-lookup"><span data-stu-id="bc2be-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="bc2be-194">Vise bestillingen som er generert</span><span class="sxs-lookup"><span data-stu-id="bc2be-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="bc2be-195">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bc2be-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="bc2be-196">Klikk Bestilling.</span><span class="sxs-lookup"><span data-stu-id="bc2be-196">Click Purchase order.</span></span>
    * <span data-ttu-id="bc2be-197">Her kan du se bestillingen som ble generert da du godtok budet.</span><span class="sxs-lookup"><span data-stu-id="bc2be-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="bc2be-198">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bc2be-198">Close the page.</span></span>
4. <span data-ttu-id="bc2be-199">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bc2be-199">Close the page.</span></span>
5. <span data-ttu-id="bc2be-200">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bc2be-200">Close the page.</span></span>
6. <span data-ttu-id="bc2be-201">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bc2be-201">Close the page.</span></span>

