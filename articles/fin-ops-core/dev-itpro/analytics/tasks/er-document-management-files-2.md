---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 2 - Utvide datamodell)
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det bruker dokumentbehandlingsfiler (vedlegg) i ER-utdata. (Del 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754920"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="a1756-104">ER Bruke dokumentbehandlingsfiler i formatutdata (del 2 - Utvide datamodell)</span><span class="sxs-lookup"><span data-stu-id="a1756-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1756-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="a1756-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="a1756-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="a1756-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a1756-107">For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER Bruke dokumentbehandlingsfiler i formatutdata (del 1: Klargjøre datamodell).</span><span class="sxs-lookup"><span data-stu-id="a1756-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="a1756-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="a1756-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="a1756-109">Utvide datamodellen for å presentere dokumentbehandlingsfilene i modellen</span><span class="sxs-lookup"><span data-stu-id="a1756-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="a1756-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="a1756-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a1756-111">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a1756-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a1756-112">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="a1756-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="a1756-113">Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="a1756-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="a1756-114">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="a1756-114">Click Designer.</span></span>
6. <span data-ttu-id="a1756-115">Velg Kundefakturamodell(InvoiceCustomer) i treet.</span><span class="sxs-lookup"><span data-stu-id="a1756-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="a1756-116">Vi vil utvide denne datamodellen for å vise alle filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.</span><span class="sxs-lookup"><span data-stu-id="a1756-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="a1756-117">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1756-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="a1756-118">Skriv inn Fakturavedlegg i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="a1756-119">Fakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="a1756-119">Invoice attachments</span></span>  
9. <span data-ttu-id="a1756-120">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="a1756-121">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="a1756-121">Click Add.</span></span>
11. <span data-ttu-id="a1756-122">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1756-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="a1756-123">Skriv inn Filinnhold i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="a1756-124">Filinnhold</span><span class="sxs-lookup"><span data-stu-id="a1756-124">File content</span></span>  
13. <span data-ttu-id="a1756-125">Velg Container i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="a1756-126">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="a1756-126">Click Add.</span></span>
15. <span data-ttu-id="a1756-127">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1756-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="a1756-128">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="a1756-129">Filnavn</span><span class="sxs-lookup"><span data-stu-id="a1756-129">File name</span></span>  
17. <span data-ttu-id="a1756-130">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="a1756-131">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="a1756-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="a1756-132">Tilordne nye datamodellelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="a1756-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="a1756-133">Klikk på Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="a1756-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="a1756-134">Bruk hurtigfilteret til å filtrere på Definisjon-feltet med en verdi lik InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="a1756-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="a1756-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="a1756-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="a1756-136">Vi vil tilordne nye modellelementer til aktuelle datakilder.</span><span class="sxs-lookup"><span data-stu-id="a1756-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="a1756-137">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="a1756-137">Click Designer.</span></span>
4. <span data-ttu-id="a1756-138">Velg Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="a1756-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="a1756-139">Utvid Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="a1756-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="a1756-140">Velg Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="a1756-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="a1756-141">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="a1756-141">Click Edit.</span></span>
8. <span data-ttu-id="a1756-142">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="a1756-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="a1756-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="a1756-144">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="a1756-144">Click Save.</span></span>
10. <span data-ttu-id="a1756-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a1756-145">Close the page.</span></span>
11. <span data-ttu-id="a1756-146">I treet velger du Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="a1756-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="a1756-147">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="a1756-147">Click Edit.</span></span>
13. <span data-ttu-id="a1756-148">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="a1756-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="a1756-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="a1756-150">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="a1756-150">Click Save.</span></span>
15. <span data-ttu-id="a1756-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a1756-151">Close the page.</span></span>
16. <span data-ttu-id="a1756-152">Velg Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="a1756-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="a1756-153">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="a1756-153">Click Edit.</span></span>
18. <span data-ttu-id="a1756-154">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1756-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="a1756-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="a1756-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="a1756-156">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="a1756-156">Click Save.</span></span>
20. <span data-ttu-id="a1756-157">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a1756-157">Close the page.</span></span>
21. <span data-ttu-id="a1756-158">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="a1756-158">Click Save.</span></span>
22. <span data-ttu-id="a1756-159">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a1756-159">Close the page.</span></span>
23. <span data-ttu-id="a1756-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a1756-160">Close the page.</span></span>
24. <span data-ttu-id="a1756-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a1756-161">Close the page.</span></span>
25. <span data-ttu-id="a1756-162">Klikk på Endre status.</span><span class="sxs-lookup"><span data-stu-id="a1756-162">Click Change status.</span></span>
26. <span data-ttu-id="a1756-163">Klikk på Fullført.</span><span class="sxs-lookup"><span data-stu-id="a1756-163">Click Complete.</span></span>
27. <span data-ttu-id="a1756-164">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1756-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]