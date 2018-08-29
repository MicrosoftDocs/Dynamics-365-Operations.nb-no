--- 
title: "Kjøre formater for å bruke dokumentbehandlingsfiler i ER-utdata"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: e0c01a44bde47860b3ad587da73dc2760e9ef4fc
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="f5ca3-103">Kjøre formater for å bruke dokumentbehandlingsfiler i ER-utdata</span><span class="sxs-lookup"><span data-stu-id="f5ca3-103">Run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5ca3-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f5ca3-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f5ca3-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 3: Opprette format).</span><span class="sxs-lookup"><span data-stu-id="f5ca3-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="f5ca3-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="f5ca3-108">Legge til nødvendige vedlegg for salgsordre for én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="f5ca3-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="f5ca3-109">Gå til Kunder > Fakturaer > Åpne kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="f5ca3-110">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f5ca3-111">Du kan for eksempel filtrere på Faktura-feltet med verdien CIV-000148.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="f5ca3-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="f5ca3-112">CIV-000148</span></span>  
3. <span data-ttu-id="f5ca3-113">Klikk for å følge koblingen for den valgte fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="f5ca3-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="f5ca3-114">CIV-000148</span></span>  
4. <span data-ttu-id="f5ca3-115">Klikk for å følge koblingen i feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="f5ca3-116">000148</span><span class="sxs-lookup"><span data-stu-id="f5ca3-116">000148</span></span>  
5. <span data-ttu-id="f5ca3-117">Velg alternativet Hode i feltet Linjer eller hode.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="f5ca3-118">Velg toppteksten for å angi at dette vil være målet for å legge til vedlegg.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="f5ca3-119">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-119">Click Attach.</span></span>
    * <span data-ttu-id="f5ca3-120">Legg til noen filer som vedlegg for denne salgsordren.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="f5ca3-121">Bruk filene med dokumenttyper som støttes av dokumentbehandling (med filtypen DOCX, DPF, XML, JPG osv.).</span><span class="sxs-lookup"><span data-stu-id="f5ca3-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="f5ca3-122">Bla gjennom og velg filer som skal legges ved og ytterligere behandles med den tilknyttede fakturaen i den elektroniske ER-meldingen.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="f5ca3-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-123">Click New.</span></span>
8. <span data-ttu-id="f5ca3-124">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-124">Click File.</span></span>
9. <span data-ttu-id="f5ca3-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-125">Click New.</span></span>
10. <span data-ttu-id="f5ca3-126">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-126">Click File.</span></span>
11. <span data-ttu-id="f5ca3-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-127">Close the page.</span></span>
12. <span data-ttu-id="f5ca3-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-128">Close the page.</span></span>
13. <span data-ttu-id="f5ca3-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-129">Close the page.</span></span>
14. <span data-ttu-id="f5ca3-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="f5ca3-131">Kjøre den utformede rapporten for den valgte fakturaen</span><span class="sxs-lookup"><span data-stu-id="f5ca3-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="f5ca3-132">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f5ca3-133">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="f5ca3-134">Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="f5ca3-135">Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="f5ca3-136">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-136">Click Run.</span></span>
6. <span data-ttu-id="f5ca3-137">Utvid delen Poster som skal inkluderes ().</span><span class="sxs-lookup"><span data-stu-id="f5ca3-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="f5ca3-138">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-138">Click Filter.</span></span>
8. <span data-ttu-id="f5ca3-139">Merk raden for feltet Kundefakturajournal og Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="f5ca3-140">Skriv inn 000148 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="f5ca3-141">I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="f5ca3-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-142">Click OK.</span></span>
11. <span data-ttu-id="f5ca3-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-143">Click OK.</span></span>
    * <span data-ttu-id="f5ca3-144">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-144">Review the generated output.</span></span> <span data-ttu-id="f5ca3-145">Legg merke til at for hvert vedlegg er det opprettet en enkelt XML-node.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="f5ca3-146">Innholdet i vedlegget blir fylt ut i XML-utdataene i MIME (base64)-tekstformat.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  


