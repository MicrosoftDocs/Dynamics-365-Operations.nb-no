--- 
title: Generere elektroniske dokumenter for betalinger ved hjelp av en formatkonfigurasjon for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan bruke en ny formatkonfigurasjon for elektronisk rapportering (ER) til å generere elektroniske betalingsdokumenter for behandling av betalinger."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8a04918d6642de73016231fdb96d9ea6b0be5999
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="b2dc2-103">Generere elektroniske dokumenter for betalinger ved hjelp av en formatkonfigurasjon for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b2dc2-103">Generate electronic documents for payments using a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2dc2-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan bruke en ny formatkonfigurasjon for elektronisk rapportering (ER) til å generere elektroniske betalingsdokumenter for behandling av betalinger.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="b2dc2-105">Denne fremgangsmåten kan utføres i GBSI-eksempelfirmaet.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="b2dc2-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjon med formatet betalingsdokument".</span><span class="sxs-lookup"><span data-stu-id="b2dc2-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="b2dc2-107">Endre konfigurasjonen for den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="b2dc2-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="b2dc2-108">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="b2dc2-109">Aktiver/deaktiver filformatdelen for å vise den ved behov.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="b2dc2-110">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b2dc2-111">Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien Elektronisk.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="b2dc2-112">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-112">Click Edit.</span></span>
5. <span data-ttu-id="b2dc2-113">Sett feltet Generell elektronisk rapportering til Ja.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="b2dc2-114">Velg Ja hvis du vil bruke det generelle elektroniske rapporteringsmønsteret for generering av betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="b2dc2-115">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b2dc2-116">Velg formatkonfigurasjonen BACS (Storbritannia fiktivt).</span><span class="sxs-lookup"><span data-stu-id="b2dc2-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="b2dc2-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-117">Click Save.</span></span>
9. <span data-ttu-id="b2dc2-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="b2dc2-119">Teste formatet for genererte betalingsfiler</span><span class="sxs-lookup"><span data-stu-id="b2dc2-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="b2dc2-120">Gå til Leverandører > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b2dc2-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-121">Click New.</span></span>
3. <span data-ttu-id="b2dc2-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b2dc2-123">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b2dc2-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2dc2-125">Velg VendPay.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-125">Select VendPay.</span></span>  
6. <span data-ttu-id="b2dc2-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-126">Click Save.</span></span>
7. <span data-ttu-id="b2dc2-127">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-127">Click Lines.</span></span>
8. <span data-ttu-id="b2dc2-128">Skriv DEMF i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="b2dc2-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="b2dc2-129">DEMF</span></span>  
9. <span data-ttu-id="b2dc2-130">Angi verdiene DE-01001 i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="b2dc2-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="b2dc2-131">DE-01001</span></span>  
10. <span data-ttu-id="b2dc2-132">Skriv inn Betaling i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="b2dc2-133">Betaling</span><span class="sxs-lookup"><span data-stu-id="b2dc2-133">Payment</span></span>  
11. <span data-ttu-id="b2dc2-134">Angi et tall i Debet-feltet.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="b2dc2-135">10 000</span><span class="sxs-lookup"><span data-stu-id="b2dc2-135">1000</span></span>  
12. <span data-ttu-id="b2dc2-136">Klikk kategorien Betaling.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="b2dc2-137">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b2dc2-138">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b2dc2-139">Velg den elektroniske verdien.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="b2dc2-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b2dc2-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-141">Click Save.</span></span>
17. <span data-ttu-id="b2dc2-142">Klikk Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-142">Click Generate payments.</span></span>
18. <span data-ttu-id="b2dc2-143">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b2dc2-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b2dc2-145">Velg den elektroniske verdien.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="b2dc2-146">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2dc2-147">Velg den elektroniske verdien.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="b2dc2-148">Skriv inn en verdi i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="b2dc2-149">Skriv for eksempel betalinger.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="b2dc2-150">Klikk rullegardinknappen i Bankkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="b2dc2-151">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2dc2-152">Velg verdien GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="b2dc2-153">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-153">Click OK.</span></span>
25. <span data-ttu-id="b2dc2-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-154">Click OK.</span></span>
    * <span data-ttu-id="b2dc2-155">Analyser den opprettede betalingsfilen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="b2dc2-156">Sammenligne den med det utformede dokumentoppsettet og de definerte attributtene for betalingtransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="b2dc2-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


