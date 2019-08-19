---
title: Opprette en rekvisisjon som bruker en tilbudsforespørsel
description: Denne veiledningen viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d80f84c148ff26bf008a97b06098bfd18c9062d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844163"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="96712-103">Opprette en rekvisisjon som bruker en tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="96712-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96712-104">Denne veiledningen viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="96712-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="96712-105">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF, og du må være logget på som administrator for å fullføre alle trinnene.</span><span class="sxs-lookup"><span data-stu-id="96712-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="96712-106">Oppgavene i denne veiledningen utføres vanligvis av innkjøpsansvarlige.</span><span class="sxs-lookup"><span data-stu-id="96712-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="96712-107">Opprette en rekvisisjon</span><span class="sxs-lookup"><span data-stu-id="96712-107">Create a requisition</span></span>
1. <span data-ttu-id="96712-108">Gå til Innkjøp og leverandører > Innkjøpsrekvisisjoner > Innkjøpsrekvisisjoner klargjort av meg.</span><span class="sxs-lookup"><span data-stu-id="96712-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="96712-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="96712-109">Click New.</span></span>
3. <span data-ttu-id="96712-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="96712-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="96712-111">Angi en dato i feltet Ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="96712-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="96712-112">Angi en dato i feltet Regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="96712-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="96712-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="96712-113">Click OK.</span></span>
7. <span data-ttu-id="96712-114">Angi eller velg en verdi i feltet Årsak.</span><span class="sxs-lookup"><span data-stu-id="96712-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="96712-115">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="96712-115">Click Add line.</span></span>
9. <span data-ttu-id="96712-116">Velg en kategori i treet i Innkjøpskategori-feltet, og klikk deretter OK.</span><span class="sxs-lookup"><span data-stu-id="96712-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="96712-117">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="96712-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="96712-118">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="96712-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="96712-119">Angi eller velg en verdi i Enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="96712-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="96712-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="96712-120">Click Save.</span></span>
14. <span data-ttu-id="96712-121">Klikk Arbeidsflyt for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="96712-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="96712-122">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="96712-122">Click Submit.</span></span>
16. <span data-ttu-id="96712-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="96712-123">Close the page.</span></span>
17. <span data-ttu-id="96712-124">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="96712-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="96712-125">Tilordne en arbeidsflytoppgave på nytt</span><span class="sxs-lookup"><span data-stu-id="96712-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="96712-126">Den neste oppgaven er å opprette en tilbudsforespørsel for å få bud fra leverandører for produktet.</span><span class="sxs-lookup"><span data-stu-id="96712-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="96712-127">I demonstrasjonsdataene for USMF er rekvisisjonsarbeidsflyten definert med en regel slik at hvis en leverandør ikke er valgt, eller enhetsprisen er 0 for en linje, tilordnes en oppgave til en bestemt arbeider for å opprette en tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="96712-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="96712-128">Du må tilordne oppgaven på nytt til en annen bruker (deg selv) for å fortsette med denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="96712-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="96712-129">Du kan bare gjøre dette hvis du er logget på som administrator.</span><span class="sxs-lookup"><span data-stu-id="96712-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="96712-130">Klikk Arbeidsflyt for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="96712-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="96712-131">Klikk Vis logg.</span><span class="sxs-lookup"><span data-stu-id="96712-131">Click View history.</span></span>
3. <span data-ttu-id="96712-132">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="96712-132">Refresh the page.</span></span>
4. <span data-ttu-id="96712-133">Vis delen Sporingsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="96712-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="96712-134">I treet velger du linjen som begynner med Linjeelementarbeidsflyt aktivert på.</span><span class="sxs-lookup"><span data-stu-id="96712-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="96712-135">Klikk Vis arbeidsflytdetaljer.</span><span class="sxs-lookup"><span data-stu-id="96712-135">Click View workflow details.</span></span>
7. <span data-ttu-id="96712-136">Vis delen Arbeidselementer.</span><span class="sxs-lookup"><span data-stu-id="96712-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="96712-137">Klikk Tilordne på nytt.</span><span class="sxs-lookup"><span data-stu-id="96712-137">Click Reassign.</span></span>
9. <span data-ttu-id="96712-138">Velg Administrator i Bruker-feltet.</span><span class="sxs-lookup"><span data-stu-id="96712-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="96712-139">Klikk Tilordne på nytt.</span><span class="sxs-lookup"><span data-stu-id="96712-139">Click Reassign.</span></span>
11. <span data-ttu-id="96712-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="96712-140">Close the page.</span></span>
12. <span data-ttu-id="96712-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="96712-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="96712-142">Opprette en tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="96712-142">Create an RFQ</span></span>
1. <span data-ttu-id="96712-143">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="96712-143">Refresh the page.</span></span>
2. <span data-ttu-id="96712-144">Klikk Svar på tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="96712-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="96712-145">Velg USMF i feltet Kjøpende juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="96712-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="96712-146">Du må velge samme juridiske enheten som er på rekvisisjonslinjen.</span><span class="sxs-lookup"><span data-stu-id="96712-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="96712-147">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="96712-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="96712-148">Hvis du har flere linjer på innkjøpsrekvisisjonen din, velger du alle linjene som du vil legge til i tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="96712-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="96712-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="96712-149">Click OK.</span></span>
6. <span data-ttu-id="96712-150">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="96712-150">Refresh the page.</span></span>
7. <span data-ttu-id="96712-151">Åpne faktaboksen, og vis deretter delen Relaterte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="96712-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="96712-152">Faktaboks er kanskje allerede åpen.</span><span class="sxs-lookup"><span data-stu-id="96712-152">You may already have the FactBox open.</span></span> <span data-ttu-id="96712-153">Se etter ikonet med en pil, til høyre for veksleknapper Linjer/hode.</span><span class="sxs-lookup"><span data-stu-id="96712-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="96712-154">Hvis pilen peker mot høyre, er faktaboksen allerede åpen.</span><span class="sxs-lookup"><span data-stu-id="96712-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="96712-155">Hvis pilen peker mot venstre, klikker du den for å åpne faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="96712-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="96712-156">Klikk koblingen i Tilbudsforespørsel-feltet for å åpne tilbudsforespørselen som nettopp ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="96712-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="96712-157">Klikk Overskrift.</span><span class="sxs-lookup"><span data-stu-id="96712-157">Click Header.</span></span>
10. <span data-ttu-id="96712-158">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="96712-158">Click Add.</span></span>
11. <span data-ttu-id="96712-159">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="96712-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="96712-160">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="96712-160">Click Add.</span></span>
13. <span data-ttu-id="96712-161">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="96712-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="96712-162">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="96712-162">Click Send.</span></span>
15. <span data-ttu-id="96712-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="96712-163">Click OK.</span></span>
16. <span data-ttu-id="96712-164">Klikk Angi svar.</span><span class="sxs-lookup"><span data-stu-id="96712-164">Click Enter reply.</span></span>
17. <span data-ttu-id="96712-165">Klikk Svar i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="96712-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="96712-166">Klikk Kopier data for å svare.</span><span class="sxs-lookup"><span data-stu-id="96712-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="96712-167">Dette kopierer data, for eksempel antall og datoer, fra tilbudsforespørselen til svaret.</span><span class="sxs-lookup"><span data-stu-id="96712-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="96712-168">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="96712-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="96712-169">Dette er prisen du har mottatt fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="96712-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="96712-170">Du kan også angi tilleggsinformasjon fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="96712-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="96712-171">Klikk Godta.</span><span class="sxs-lookup"><span data-stu-id="96712-171">Click Accept.</span></span>
21. <span data-ttu-id="96712-172">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="96712-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="96712-173">Kontrollere at leverandøren prisen er overfør til rekvisisjonen</span><span class="sxs-lookup"><span data-stu-id="96712-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="96712-174">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="96712-174">Close the page.</span></span>
2. <span data-ttu-id="96712-175">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="96712-175">Click Lines.</span></span>
3. <span data-ttu-id="96712-176">Klikk Relatert informasjon.</span><span class="sxs-lookup"><span data-stu-id="96712-176">Click Related information.</span></span>
4. <span data-ttu-id="96712-177">Klikk Innkjøpsrekvisisjonslinjer.</span><span class="sxs-lookup"><span data-stu-id="96712-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="96712-178">Velg linjen som ble overført til tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="96712-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="96712-179">Kontroller at prisen og leverandøren er kopiert til rekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="96712-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="96712-180">Klikk Arbeidsflyt for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="96712-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="96712-181">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="96712-181">Click Complete.</span></span>
8. <span data-ttu-id="96712-182">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="96712-182">Close the page.</span></span>
9. <span data-ttu-id="96712-183">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="96712-183">Click Complete.</span></span>

