---
title: Opprette en rekvisisjon som bruker en tilbudsforespørsel
description: Dette emnet viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 205cba2325e76dae9572301e44e0e89cbcfd106e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434277"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="27814-103">Opprette en rekvisisjon som bruker en tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="27814-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27814-104">Dette emnet viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="27814-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="27814-105">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF, og du må være logget på som administrator for å fullføre alle trinnene.</span><span class="sxs-lookup"><span data-stu-id="27814-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="27814-106">Oppgavene i denne veiledningen utføres vanligvis av innkjøpsansvarlige.</span><span class="sxs-lookup"><span data-stu-id="27814-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="27814-107">Opprette en rekvisisjon</span><span class="sxs-lookup"><span data-stu-id="27814-107">Create a requisition</span></span>
1. <span data-ttu-id="27814-108">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Innkjøpsrekvisisjoner > Innkjøpsrekvisisjoner klargjort av meg**.</span><span class="sxs-lookup"><span data-stu-id="27814-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="27814-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="27814-109">Select **New**.</span></span>
3. <span data-ttu-id="27814-110">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27814-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="27814-111">Angi en dato i feltet **Ønsket dato**.</span><span class="sxs-lookup"><span data-stu-id="27814-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="27814-112">Angi en dato i feltet **Regnskapsdato**.</span><span class="sxs-lookup"><span data-stu-id="27814-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="27814-113">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="27814-113">Select **OK**.</span></span>
7. <span data-ttu-id="27814-114">Angi eller velg en verdi i **Årsak**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27814-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="27814-115">Velg **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="27814-115">Select **Add line**.</span></span>
9. <span data-ttu-id="27814-116">Velg en kategori i treet i **Innkjøpskategori**-feltet, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="27814-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="27814-117">Skriv inn en verdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="27814-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="27814-118">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27814-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="27814-119">Angi eller velg en verdi i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27814-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="27814-120">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="27814-120">Select **Save**.</span></span>
14. <span data-ttu-id="27814-121">Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="27814-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="27814-122">Velg **Send**.</span><span class="sxs-lookup"><span data-stu-id="27814-122">Select **Submit**.</span></span>
16. <span data-ttu-id="27814-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="27814-123">Close the page.</span></span>
17. <span data-ttu-id="27814-124">Velg **Send**.</span><span class="sxs-lookup"><span data-stu-id="27814-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="27814-125">Tilordne en arbeidsflytoppgave på nytt</span><span class="sxs-lookup"><span data-stu-id="27814-125">Reassign a workflow task</span></span>
<span data-ttu-id="27814-126">Den neste oppgaven er å opprette en tilbudsforespørsel for å få bud fra leverandører for produktet.</span><span class="sxs-lookup"><span data-stu-id="27814-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="27814-127">I demonstrasjonsdataene for USMF er rekvisisjonsarbeidsflyten definert med en regel slik at hvis en leverandør ikke er valgt, eller enhetsprisen er 0 for en linje, tilordnes en oppgave til en bestemt arbeider for å opprette en tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="27814-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="27814-128">Du må tilordne oppgaven på nytt til en annen bruker (deg selv) for å fortsette med denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="27814-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="27814-129">Du kan bare gjøre dette hvis du er logget på som administrator.</span><span class="sxs-lookup"><span data-stu-id="27814-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="27814-130">Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="27814-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="27814-131">Velg **Vis logg**.</span><span class="sxs-lookup"><span data-stu-id="27814-131">Select **View history**.</span></span>
3. <span data-ttu-id="27814-132">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="27814-132">Refresh the page.</span></span>
4. <span data-ttu-id="27814-133">Vis delen **Sporingsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="27814-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="27814-134">I treet velger du linjen som begynner med Linjeelementarbeidsflyt aktivert på.</span><span class="sxs-lookup"><span data-stu-id="27814-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="27814-135">Velg **Vis arbeidsflytdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="27814-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="27814-136">Vis delen **Arbeidselementer**.</span><span class="sxs-lookup"><span data-stu-id="27814-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="27814-137">Velg **Tilordne på nytt**.</span><span class="sxs-lookup"><span data-stu-id="27814-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="27814-138">Velg **Administrator** i **Bruker**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27814-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="27814-139">Velg **Tilordne på nytt**.</span><span class="sxs-lookup"><span data-stu-id="27814-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="27814-140">Lukk de to sidene.</span><span class="sxs-lookup"><span data-stu-id="27814-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="27814-141">Opprette en tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="27814-141">Create an RFQ</span></span>

1. <span data-ttu-id="27814-142">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="27814-142">Refresh the page.</span></span>
2. <span data-ttu-id="27814-143">Velg **Tilbudsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="27814-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="27814-144">Velg **USMF** i feltet **Kjøpende juridisk enhet**.</span><span class="sxs-lookup"><span data-stu-id="27814-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="27814-145">Du må velge den samme juridiske enheten som er på rekvisisjonslinjen.</span><span class="sxs-lookup"><span data-stu-id="27814-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="27814-146">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="27814-146">In the list, mark the selected row.</span></span> <span data-ttu-id="27814-147">Hvis du har flere linjer på innkjøpsrekvisisjonen din, velger du alle linjene som du vil legge til i tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="27814-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="27814-148">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="27814-148">Select **OK**.</span></span>
6. <span data-ttu-id="27814-149">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="27814-149">Refresh the page.</span></span>
7. <span data-ttu-id="27814-150">Kontroller at faktaboksen er åpen, og vis deretter delen **Relaterte dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="27814-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="27814-151">Klikk koblingen i **Tilbudsforespørsel**-feltet for å åpne tilbudsforespørselen som nettopp ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="27814-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="27814-152">Velg **Topptekst**.</span><span class="sxs-lookup"><span data-stu-id="27814-152">Select **Header**.</span></span>
10. <span data-ttu-id="27814-153">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="27814-153">Select **Add**.</span></span>
11. <span data-ttu-id="27814-154">Angi eller velg en verdi i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27814-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="27814-155">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="27814-155">Select **Add**.</span></span>
13. <span data-ttu-id="27814-156">Angi eller velg en verdi i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27814-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="27814-157">Velg **Send**.</span><span class="sxs-lookup"><span data-stu-id="27814-157">Select **Send**.</span></span>
15. <span data-ttu-id="27814-158">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="27814-158">Select **OK**.</span></span>
16. <span data-ttu-id="27814-159">Velg **Angi svar**.</span><span class="sxs-lookup"><span data-stu-id="27814-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="27814-160">Velg **Svar** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="27814-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="27814-161">Velg **Kopier data til svar**.</span><span class="sxs-lookup"><span data-stu-id="27814-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="27814-162">Dette kopierer data, for eksempel antall og datoer, fra tilbudsforespørselen til svaret.</span><span class="sxs-lookup"><span data-stu-id="27814-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="27814-163">Angi et tall i **Enhetspris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27814-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="27814-164">Dette er prisen du har mottatt fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="27814-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="27814-165">Du kan også angi tilleggsinformasjon fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="27814-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="27814-166">Velg **Godta**.</span><span class="sxs-lookup"><span data-stu-id="27814-166">Select **Accept**.</span></span>
21. <span data-ttu-id="27814-167">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="27814-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="27814-168">Kontrollere at leverandøren prisen er overfør til rekvisisjonen</span><span class="sxs-lookup"><span data-stu-id="27814-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="27814-169">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="27814-169">Close the page.</span></span>
2. <span data-ttu-id="27814-170">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="27814-170">Select **Lines**.</span></span>
3. <span data-ttu-id="27814-171">Velg **Relatert informasjon**.</span><span class="sxs-lookup"><span data-stu-id="27814-171">Select **Related information**.</span></span>
4. <span data-ttu-id="27814-172">Velg **Innkjøpsrekvisisjon**.</span><span class="sxs-lookup"><span data-stu-id="27814-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="27814-173">Velg linjen som ble overført til tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="27814-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="27814-174">Kontroller at prisen og leverandøren er kopiert til rekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="27814-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="27814-175">Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="27814-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="27814-176">Velg Fullført.</span><span class="sxs-lookup"><span data-stu-id="27814-176">Select Complete.</span></span>
8. <span data-ttu-id="27814-177">Velg siden.</span><span class="sxs-lookup"><span data-stu-id="27814-177">Select the page.</span></span>
9. <span data-ttu-id="27814-178">Velg Fullført.</span><span class="sxs-lookup"><span data-stu-id="27814-178">Select Complete.</span></span>

