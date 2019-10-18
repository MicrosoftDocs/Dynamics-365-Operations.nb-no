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
ms.openlocfilehash: 032f9c5707294ee33cc848ecc6990c1ef5bbfdbb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185043"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="79613-103">ER Bruke dokumentbehandlingsfiler i formatutdata (del 2: Utvide datamodell)</span><span class="sxs-lookup"><span data-stu-id="79613-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79613-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="79613-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="79613-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="79613-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="79613-106">For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER Bruke dokumentbehandlingsfiler i formatutdata (del 1: Klargjøre datamodell).</span><span class="sxs-lookup"><span data-stu-id="79613-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="79613-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="79613-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="79613-108">Utvide datamodellen for å presentere dokumentbehandlingsfilene i modellen</span><span class="sxs-lookup"><span data-stu-id="79613-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="79613-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="79613-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="79613-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="79613-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="79613-111">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="79613-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="79613-112">Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="79613-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="79613-113">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="79613-113">Click Designer.</span></span>
6. <span data-ttu-id="79613-114">Velg Kundefakturamodell(InvoiceCustomer) i treet.</span><span class="sxs-lookup"><span data-stu-id="79613-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="79613-115">Vi vil utvide denne datamodellen for å vise alle filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.</span><span class="sxs-lookup"><span data-stu-id="79613-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="79613-116">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="79613-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="79613-117">Skriv inn Fakturavedlegg i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="79613-118">Fakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="79613-118">Invoice attachments</span></span>  
9. <span data-ttu-id="79613-119">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="79613-120">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="79613-120">Click Add.</span></span>
11. <span data-ttu-id="79613-121">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="79613-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="79613-122">Skriv inn Filinnhold i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="79613-123">Filinnhold</span><span class="sxs-lookup"><span data-stu-id="79613-123">File content</span></span>  
13. <span data-ttu-id="79613-124">Velg Container i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="79613-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="79613-125">Click Add.</span></span>
15. <span data-ttu-id="79613-126">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="79613-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="79613-127">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="79613-128">Filnavn</span><span class="sxs-lookup"><span data-stu-id="79613-128">File name</span></span>  
17. <span data-ttu-id="79613-129">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="79613-130">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="79613-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="79613-131">Tilordne nye datamodellelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="79613-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="79613-132">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="79613-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="79613-133">Bruk hurtigfilteret til å filtrere på Definisjon-feltet med en verdi lik InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="79613-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="79613-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="79613-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="79613-135">Vi vil tilordne nye modellelementer til aktuelle datakilder.</span><span class="sxs-lookup"><span data-stu-id="79613-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="79613-136">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="79613-136">Click Designer.</span></span>
4. <span data-ttu-id="79613-137">Velg Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="79613-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="79613-138">Utvid Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="79613-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="79613-139">Velg Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="79613-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="79613-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="79613-140">Click Edit.</span></span>
8. <span data-ttu-id="79613-141">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="79613-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="79613-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="79613-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="79613-143">Click Save.</span></span>
10. <span data-ttu-id="79613-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="79613-144">Close the page.</span></span>
11. <span data-ttu-id="79613-145">I treet velger du Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="79613-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="79613-146">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="79613-146">Click Edit.</span></span>
13. <span data-ttu-id="79613-147">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="79613-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="79613-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="79613-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="79613-149">Click Save.</span></span>
15. <span data-ttu-id="79613-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="79613-150">Close the page.</span></span>
16. <span data-ttu-id="79613-151">Velg Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="79613-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="79613-152">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="79613-152">Click Edit.</span></span>
18. <span data-ttu-id="79613-153">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="79613-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="79613-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="79613-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="79613-155">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="79613-155">Click Save.</span></span>
20. <span data-ttu-id="79613-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="79613-156">Close the page.</span></span>
21. <span data-ttu-id="79613-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="79613-157">Click Save.</span></span>
22. <span data-ttu-id="79613-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="79613-158">Close the page.</span></span>
23. <span data-ttu-id="79613-159">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="79613-159">Close the page.</span></span>
24. <span data-ttu-id="79613-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="79613-160">Close the page.</span></span>
25. <span data-ttu-id="79613-161">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="79613-161">Click Change status.</span></span>
26. <span data-ttu-id="79613-162">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="79613-162">Click Complete.</span></span>
27. <span data-ttu-id="79613-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="79613-163">Click OK.</span></span>

