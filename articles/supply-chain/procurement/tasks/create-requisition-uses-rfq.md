---
title: Opprette en rekvisisjon som bruker en tilbudsforespørsel
description: Dette emnet viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6083afe0e2bfafd337d572863a198330e8cb6cc8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812140"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="fc0b7-103">Opprette en rekvisisjon som bruker en tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="fc0b7-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc0b7-104">Dette emnet viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="fc0b7-105">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF, og du må være logget på som administrator for å fullføre alle trinnene.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="fc0b7-106">Oppgavene i denne veiledningen utføres vanligvis av innkjøpsansvarlige.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="fc0b7-107">Opprette en rekvisisjon</span><span class="sxs-lookup"><span data-stu-id="fc0b7-107">Create a requisition</span></span>
1. <span data-ttu-id="fc0b7-108">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Innkjøpsrekvisisjoner > Innkjøpsrekvisisjoner klargjort av meg**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="fc0b7-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-109">Select **New**.</span></span>
3. <span data-ttu-id="fc0b7-110">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="fc0b7-111">Angi en dato i feltet **Ønsket dato**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="fc0b7-112">Angi en dato i feltet **Regnskapsdato**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="fc0b7-113">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-113">Select **OK**.</span></span>
7. <span data-ttu-id="fc0b7-114">Angi eller velg en verdi i **Årsak**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="fc0b7-115">Velg **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-115">Select **Add line**.</span></span>
9. <span data-ttu-id="fc0b7-116">Velg en kategori i treet i **Innkjøpskategori**-feltet, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="fc0b7-117">Skriv inn en verdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="fc0b7-118">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="fc0b7-119">Angi eller velg en verdi i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="fc0b7-120">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-120">Select **Save**.</span></span>
14. <span data-ttu-id="fc0b7-121">Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="fc0b7-122">Velg **Send**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-122">Select **Submit**.</span></span>
16. <span data-ttu-id="fc0b7-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-123">Close the page.</span></span>
17. <span data-ttu-id="fc0b7-124">Velg **Send**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="fc0b7-125">Tilordne en arbeidsflytoppgave på nytt</span><span class="sxs-lookup"><span data-stu-id="fc0b7-125">Reassign a workflow task</span></span>
<span data-ttu-id="fc0b7-126">Den neste oppgaven er å opprette en tilbudsforespørsel for å få bud fra leverandører for produktet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="fc0b7-127">I demonstrasjonsdataene for USMF er rekvisisjonsarbeidsflyten definert med en regel slik at hvis en leverandør ikke er valgt, eller enhetsprisen er 0 for en linje, tilordnes en oppgave til en bestemt arbeider for å opprette en tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="fc0b7-128">Du må tilordne oppgaven på nytt til en annen bruker (deg selv) for å fortsette med denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="fc0b7-129">Du kan bare gjøre dette hvis du er logget på som administrator.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="fc0b7-130">Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="fc0b7-131">Velg **Vis logg**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-131">Select **View history**.</span></span>
3. <span data-ttu-id="fc0b7-132">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-132">Refresh the page.</span></span>
4. <span data-ttu-id="fc0b7-133">Vis delen **Sporingsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="fc0b7-134">I treet velger du linjen som begynner med Linjeelementarbeidsflyt aktivert på.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="fc0b7-135">Velg **Vis arbeidsflytdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="fc0b7-136">Vis delen **Arbeidselementer**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="fc0b7-137">Velg **Tilordne på nytt**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="fc0b7-138">Velg **Administrator** i **Bruker**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="fc0b7-139">Velg **Tilordne på nytt**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="fc0b7-140">Lukk de to sidene.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="fc0b7-141">Opprette en tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="fc0b7-141">Create an RFQ</span></span>

1. <span data-ttu-id="fc0b7-142">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-142">Refresh the page.</span></span>
2. <span data-ttu-id="fc0b7-143">Velg **Tilbudsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="fc0b7-144">Velg **USMF** i feltet **Kjøpende juridisk enhet**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="fc0b7-145">Du må velge den samme juridiske enheten som er på rekvisisjonslinjen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="fc0b7-146">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-146">In the list, mark the selected row.</span></span> <span data-ttu-id="fc0b7-147">Hvis du har flere linjer på innkjøpsrekvisisjonen din, velger du alle linjene som du vil legge til i tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="fc0b7-148">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-148">Select **OK**.</span></span>
6. <span data-ttu-id="fc0b7-149">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-149">Refresh the page.</span></span>
7. <span data-ttu-id="fc0b7-150">Kontroller at faktaboksen er åpen, og vis deretter delen **Relaterte dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="fc0b7-151">Klikk på koblingen i **Tilbudsforespørsel**-feltet for å åpne tilbudsforespørselen som nettopp ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="fc0b7-152">Velg **Topptekst**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-152">Select **Header**.</span></span>
10. <span data-ttu-id="fc0b7-153">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-153">Select **Add**.</span></span>
11. <span data-ttu-id="fc0b7-154">Angi eller velg en verdi i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="fc0b7-155">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-155">Select **Add**.</span></span>
13. <span data-ttu-id="fc0b7-156">Angi eller velg en verdi i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="fc0b7-157">Velg **Send**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-157">Select **Send**.</span></span>
15. <span data-ttu-id="fc0b7-158">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-158">Select **OK**.</span></span>
16. <span data-ttu-id="fc0b7-159">Velg **Angi svar**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="fc0b7-160">Velg **Svar** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="fc0b7-161">Velg **Kopier data til svar**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="fc0b7-162">Dette kopierer data, for eksempel antall og datoer, fra tilbudsforespørselen til svaret.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="fc0b7-163">Angi et tall i **Enhetspris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="fc0b7-164">Dette er prisen du har mottatt fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="fc0b7-165">Du kan også angi tilleggsinformasjon fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="fc0b7-166">Velg **Godta**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-166">Select **Accept**.</span></span>
21. <span data-ttu-id="fc0b7-167">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="fc0b7-168">Kontrollere at leverandøren prisen er overfør til rekvisisjonen</span><span class="sxs-lookup"><span data-stu-id="fc0b7-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="fc0b7-169">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-169">Close the page.</span></span>
2. <span data-ttu-id="fc0b7-170">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-170">Select **Lines**.</span></span>
3. <span data-ttu-id="fc0b7-171">Velg **Relatert informasjon**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-171">Select **Related information**.</span></span>
4. <span data-ttu-id="fc0b7-172">Velg **Innkjøpsrekvisisjon**.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="fc0b7-173">Velg linjen som ble overført til tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="fc0b7-174">Kontroller at prisen og leverandøren er kopiert til rekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="fc0b7-175">Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="fc0b7-176">Velg Fullført.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-176">Select Complete.</span></span>
8. <span data-ttu-id="fc0b7-177">Velg siden.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-177">Select the page.</span></span>
9. <span data-ttu-id="fc0b7-178">Velg Fullført.</span><span class="sxs-lookup"><span data-stu-id="fc0b7-178">Select Complete.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]