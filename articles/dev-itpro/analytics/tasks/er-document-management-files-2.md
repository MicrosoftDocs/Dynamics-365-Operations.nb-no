--- 
title: "Utvide datamodell for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="c56e3-103">Utvide datamodell for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="c56e3-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c56e3-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="c56e3-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="c56e3-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="c56e3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c56e3-106">For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER Bruke dokumentbehandlingsfiler i formatutdata (del 1: Klargjøre datamodell).</span><span class="sxs-lookup"><span data-stu-id="c56e3-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="c56e3-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="c56e3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="c56e3-108">Utvide datamodellen for å presentere dokumentbehandlingsfilene i modellen</span><span class="sxs-lookup"><span data-stu-id="c56e3-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="c56e3-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="c56e3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c56e3-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="c56e3-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c56e3-111">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="c56e3-112">Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="c56e3-113">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="c56e3-113">Click Designer.</span></span>
6. <span data-ttu-id="c56e3-114">Velg Kundefakturamodell(InvoiceCustomer) i treet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="c56e3-115">Vi vil utvide denne datamodellen for å vise alle filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.</span><span class="sxs-lookup"><span data-stu-id="c56e3-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="c56e3-116">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="c56e3-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="c56e3-117">Skriv inn Fakturavedlegg i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="c56e3-118">Fakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="c56e3-118">Invoice attachments</span></span>  
9. <span data-ttu-id="c56e3-119">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="c56e3-120">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="c56e3-120">Click Add.</span></span>
11. <span data-ttu-id="c56e3-121">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="c56e3-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c56e3-122">Skriv inn Filinnhold i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="c56e3-123">Filinnhold</span><span class="sxs-lookup"><span data-stu-id="c56e3-123">File content</span></span>  
13. <span data-ttu-id="c56e3-124">Velg Container i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="c56e3-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="c56e3-125">Click Add.</span></span>
15. <span data-ttu-id="c56e3-126">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="c56e3-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="c56e3-127">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="c56e3-128">Filnavn</span><span class="sxs-lookup"><span data-stu-id="c56e3-128">File name</span></span>  
17. <span data-ttu-id="c56e3-129">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="c56e3-130">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="c56e3-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="c56e3-131">Tilordne nye datamodellelementer til Dynamics 365 for Finance and Operations-datakilder</span><span class="sxs-lookup"><span data-stu-id="c56e3-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="c56e3-132">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="c56e3-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="c56e3-133">Bruk hurtigfilteret til å filtrere på Definisjon-feltet med en verdi lik InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="c56e3-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="c56e3-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="c56e3-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="c56e3-135">Vi vil tilordne nye modellelementer til aktuelle datakilder.</span><span class="sxs-lookup"><span data-stu-id="c56e3-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="c56e3-136">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="c56e3-136">Click Designer.</span></span>
4. <span data-ttu-id="c56e3-137">Velg Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="c56e3-138">Utvid Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="c56e3-139">Velg Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="c56e3-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="c56e3-140">Click Edit.</span></span>
8. <span data-ttu-id="c56e3-141">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="c56e3-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="c56e3-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="c56e3-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c56e3-143">Click Save.</span></span>
10. <span data-ttu-id="c56e3-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c56e3-144">Close the page.</span></span>
11. <span data-ttu-id="c56e3-145">I treet velger du Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="c56e3-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="c56e3-146">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="c56e3-146">Click Edit.</span></span>
13. <span data-ttu-id="c56e3-147">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="c56e3-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="c56e3-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="c56e3-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c56e3-149">Click Save.</span></span>
15. <span data-ttu-id="c56e3-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c56e3-150">Close the page.</span></span>
16. <span data-ttu-id="c56e3-151">Velg Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="c56e3-152">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="c56e3-152">Click Edit.</span></span>
18. <span data-ttu-id="c56e3-153">Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="c56e3-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="c56e3-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="c56e3-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="c56e3-155">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c56e3-155">Click Save.</span></span>
20. <span data-ttu-id="c56e3-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c56e3-156">Close the page.</span></span>
21. <span data-ttu-id="c56e3-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c56e3-157">Click Save.</span></span>
22. <span data-ttu-id="c56e3-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c56e3-158">Close the page.</span></span>
23. <span data-ttu-id="c56e3-159">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c56e3-159">Close the page.</span></span>
24. <span data-ttu-id="c56e3-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c56e3-160">Close the page.</span></span>
25. <span data-ttu-id="c56e3-161">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="c56e3-161">Click Change status.</span></span>
26. <span data-ttu-id="c56e3-162">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="c56e3-162">Click Complete.</span></span>
27. <span data-ttu-id="c56e3-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c56e3-163">Click OK.</span></span>


