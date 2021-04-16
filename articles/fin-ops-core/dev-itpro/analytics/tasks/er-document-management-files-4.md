---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 4 – Kjøre format)
description: Dette emnet beskriver hvordan du konfigurerer et elektronisk rapporteringsformat slik at det bruker dokumentbehandlingsfiler i ER-utdata. (Del 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a7c9705d8b53ef13cd3faf13290f3f1b1d1c43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749123"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="0b1d8-104">ER Bruke dokumentbehandlingsfiler i formatutdata (del 4 – Kjøre format)</span><span class="sxs-lookup"><span data-stu-id="0b1d8-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b1d8-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0b1d8-106">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="0b1d8-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 3: Opprette format).</span><span class="sxs-lookup"><span data-stu-id="0b1d8-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="0b1d8-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="0b1d8-109">Legge til nødvendige vedlegg for salgsordre for én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="0b1d8-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="0b1d8-110">Gå til Kunder > Fakturaer > Åpne kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="0b1d8-111">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0b1d8-112">Du kan for eksempel filtrere på Faktura-feltet med verdien CIV-000148.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="0b1d8-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="0b1d8-113">CIV-000148</span></span>  
3. <span data-ttu-id="0b1d8-114">Klikk på for å følge koblingen for den valgte fakturaen.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="0b1d8-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="0b1d8-115">CIV-000148</span></span>  
4. <span data-ttu-id="0b1d8-116">Klikk på for å følge koblingen i feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="0b1d8-117">000148</span><span class="sxs-lookup"><span data-stu-id="0b1d8-117">000148</span></span>  
5. <span data-ttu-id="0b1d8-118">Velg alternativet Hode i feltet Linjer eller hode.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="0b1d8-119">Velg toppteksten for å angi at dette vil være målet for å legge til vedlegg.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="0b1d8-120">Klikk på Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-120">Click Attach.</span></span>
    * <span data-ttu-id="0b1d8-121">Legg til noen filer som vedlegg for denne salgsordren.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="0b1d8-122">Bruk filene med dokumenttyper som støttes av dokumentbehandling (med filtypen DOCX, DPF, XML, JPG osv.).</span><span class="sxs-lookup"><span data-stu-id="0b1d8-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="0b1d8-123">Bla gjennom og velg filer som skal legges ved og ytterligere behandles med den tilknyttede fakturaen i den elektroniske ER-meldingen.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="0b1d8-124">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-124">Click New.</span></span>
8. <span data-ttu-id="0b1d8-125">Klikk på Fil.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-125">Click File.</span></span>
9. <span data-ttu-id="0b1d8-126">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-126">Click New.</span></span>
10. <span data-ttu-id="0b1d8-127">Klikk på Fil.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-127">Click File.</span></span>
11. <span data-ttu-id="0b1d8-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-128">Close the page.</span></span>
12. <span data-ttu-id="0b1d8-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-129">Close the page.</span></span>
13. <span data-ttu-id="0b1d8-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-130">Close the page.</span></span>
14. <span data-ttu-id="0b1d8-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="0b1d8-132">Kjøre den utformede rapporten for den valgte fakturaen</span><span class="sxs-lookup"><span data-stu-id="0b1d8-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="0b1d8-133">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0b1d8-134">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="0b1d8-135">Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="0b1d8-136">Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="0b1d8-137">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-137">Click Run.</span></span>
6. <span data-ttu-id="0b1d8-138">Utvid delen Poster som skal inkluderes ().</span><span class="sxs-lookup"><span data-stu-id="0b1d8-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="0b1d8-139">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-139">Click Filter.</span></span>
8. <span data-ttu-id="0b1d8-140">Merk raden for feltet Kundefakturajournal og Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="0b1d8-141">Skriv inn 000148 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="0b1d8-142">I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="0b1d8-143">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-143">Click OK.</span></span>
11. <span data-ttu-id="0b1d8-144">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-144">Click OK.</span></span>
    * <span data-ttu-id="0b1d8-145">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-145">Review the generated output.</span></span> <span data-ttu-id="0b1d8-146">Legg merke til at for hvert vedlegg er det opprettet en enkelt XML-node.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="0b1d8-147">Innholdet i vedlegget blir fylt ut i XML-utdataene i MIME (base64)-tekstformat.</span><span class="sxs-lookup"><span data-stu-id="0b1d8-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]