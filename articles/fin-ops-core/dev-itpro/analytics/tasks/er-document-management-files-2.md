---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 2 - Utvide datamodell)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24eba0402caefb611a212db19cdb8feafa7c1fee
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550746"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="876f4-103">ER Bruke dokumentbehandlingsfiler i formatutdata (del 2 - Utvide datamodell)</span><span class="sxs-lookup"><span data-stu-id="876f4-103">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="876f4-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="876f4-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="876f4-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="876f4-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="876f4-106">For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER Bruke dokumentbehandlingsfiler i formatutdata (del 1: Klargjøre datamodell).</span><span class="sxs-lookup"><span data-stu-id="876f4-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="876f4-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="876f4-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="876f4-108">Utvide datamodellen for å presentere dokumentbehandlingsfilene i modellen</span><span class="sxs-lookup"><span data-stu-id="876f4-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="876f4-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="876f4-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="876f4-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="876f4-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="876f4-111">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="876f4-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="876f4-112">Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="876f4-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="876f4-113">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="876f4-113">Click Designer.</span></span>
6. <span data-ttu-id="876f4-114">Velg Kundefakturamodell(InvoiceCustomer) i treet.</span><span class="sxs-lookup"><span data-stu-id="876f4-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="876f4-115">Vi vil utvide denne datamodellen for å vise alle filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.</span><span class="sxs-lookup"><span data-stu-id="876f4-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="876f4-116">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="876f4-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="876f4-117">Skriv inn Fakturavedlegg i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="876f4-118">Fakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="876f4-118">Invoice attachments</span></span>  
9. <span data-ttu-id="876f4-119">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="876f4-120">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="876f4-120">Click Add.</span></span>
11. <span data-ttu-id="876f4-121">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="876f4-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="876f4-122">Skriv inn Filinnhold i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="876f4-123">Filinnhold</span><span class="sxs-lookup"><span data-stu-id="876f4-123">File content</span></span>  
13. <span data-ttu-id="876f4-124">Velg Container i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="876f4-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="876f4-125">Click Add.</span></span>
15. <span data-ttu-id="876f4-126">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="876f4-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="876f4-127">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="876f4-128">Filnavn</span><span class="sxs-lookup"><span data-stu-id="876f4-128">File name</span></span>  
17. <span data-ttu-id="876f4-129">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="876f4-130">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="876f4-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="876f4-131">Tilordne nye datamodellelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="876f4-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="876f4-132">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="876f4-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="876f4-133">Bruk hurtigfilteret til å filtrere på Definisjon-feltet med en verdi lik InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="876f4-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="876f4-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="876f4-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="876f4-135">Vi vil tilordne nye modellelementer til aktuelle datakilder.</span><span class="sxs-lookup"><span data-stu-id="876f4-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="876f4-136">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="876f4-136">Click Designer.</span></span>
4. <span data-ttu-id="876f4-137">Velg Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="876f4-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="876f4-138">Utvid Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="876f4-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="876f4-139">Velg Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="876f4-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="876f4-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="876f4-140">Click Edit.</span></span>
8. <span data-ttu-id="876f4-141">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="876f4-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="876f4-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="876f4-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="876f4-143">Click Save.</span></span>
10. <span data-ttu-id="876f4-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="876f4-144">Close the page.</span></span>
11. <span data-ttu-id="876f4-145">I treet velger du Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="876f4-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="876f4-146">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="876f4-146">Click Edit.</span></span>
13. <span data-ttu-id="876f4-147">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="876f4-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="876f4-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="876f4-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="876f4-149">Click Save.</span></span>
15. <span data-ttu-id="876f4-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="876f4-150">Close the page.</span></span>
16. <span data-ttu-id="876f4-151">Velg Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="876f4-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="876f4-152">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="876f4-152">Click Edit.</span></span>
18. <span data-ttu-id="876f4-153">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="876f4-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="876f4-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="876f4-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="876f4-155">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="876f4-155">Click Save.</span></span>
20. <span data-ttu-id="876f4-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="876f4-156">Close the page.</span></span>
21. <span data-ttu-id="876f4-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="876f4-157">Click Save.</span></span>
22. <span data-ttu-id="876f4-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="876f4-158">Close the page.</span></span>
23. <span data-ttu-id="876f4-159">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="876f4-159">Close the page.</span></span>
24. <span data-ttu-id="876f4-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="876f4-160">Close the page.</span></span>
25. <span data-ttu-id="876f4-161">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="876f4-161">Click Change status.</span></span>
26. <span data-ttu-id="876f4-162">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="876f4-162">Click Complete.</span></span>
27. <span data-ttu-id="876f4-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="876f4-163">Click OK.</span></span>

