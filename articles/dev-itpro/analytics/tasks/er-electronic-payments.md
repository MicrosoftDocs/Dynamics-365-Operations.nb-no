---
title: ER Generere elektroniske dokumenter for betalinger ved hjelp av en formatkonfigurasjon
description: De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan bruke en ny formatkonfigurasjon for elektronisk rapportering (ER) til å generere elektroniske betalingsdokumenter for behandling av betalinger.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf2ae8fb451eba1054bb94edbce009dcfa8c872c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "348325"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="4838c-103">ER Generere elektroniske dokumenter for betalinger ved hjelp av en formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="4838c-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4838c-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan bruke en ny formatkonfigurasjon for elektronisk rapportering (ER) til å generere elektroniske betalingsdokumenter for behandling av betalinger.</span><span class="sxs-lookup"><span data-stu-id="4838c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="4838c-105">Denne fremgangsmåten kan utføres i GBSI-eksempelfirmaet.</span><span class="sxs-lookup"><span data-stu-id="4838c-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="4838c-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjon med formatet betalingsdokument".</span><span class="sxs-lookup"><span data-stu-id="4838c-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="4838c-107">Endre konfigurasjonen for den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="4838c-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="4838c-108">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="4838c-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="4838c-109">Aktiver/deaktiver filformatdelen for å vise den ved behov.</span><span class="sxs-lookup"><span data-stu-id="4838c-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="4838c-110">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="4838c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4838c-111">Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien Elektronisk.</span><span class="sxs-lookup"><span data-stu-id="4838c-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="4838c-112">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="4838c-112">Click Edit.</span></span>
5. <span data-ttu-id="4838c-113">Sett feltet Generell elektronisk rapportering til Ja.</span><span class="sxs-lookup"><span data-stu-id="4838c-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="4838c-114">Velg Ja hvis du vil bruke det generelle elektroniske rapporteringsmønsteret for generering av betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="4838c-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="4838c-115">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4838c-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4838c-116">Velg formatkonfigurasjonen BACS (Storbritannia fiktivt).</span><span class="sxs-lookup"><span data-stu-id="4838c-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="4838c-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4838c-117">Click Save.</span></span>
9. <span data-ttu-id="4838c-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4838c-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="4838c-119">Teste formatet for genererte betalingsfiler</span><span class="sxs-lookup"><span data-stu-id="4838c-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="4838c-120">Gå til Leverandører > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="4838c-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="4838c-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4838c-121">Click New.</span></span>
3. <span data-ttu-id="4838c-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4838c-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4838c-123">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4838c-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4838c-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4838c-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4838c-125">Velg VendPay.</span><span class="sxs-lookup"><span data-stu-id="4838c-125">Select VendPay.</span></span>  
6. <span data-ttu-id="4838c-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4838c-126">Click Save.</span></span>
7. <span data-ttu-id="4838c-127">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="4838c-127">Click Lines.</span></span>
8. <span data-ttu-id="4838c-128">Skriv DEMF i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="4838c-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="4838c-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="4838c-129">DEMF</span></span>  
9. <span data-ttu-id="4838c-130">Angi verdiene DE-01001 i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="4838c-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="4838c-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="4838c-131">DE-01001</span></span>  
10. <span data-ttu-id="4838c-132">Skriv inn Betaling i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="4838c-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="4838c-133">Betaling</span><span class="sxs-lookup"><span data-stu-id="4838c-133">Payment</span></span>  
11. <span data-ttu-id="4838c-134">Angi et tall i Debet-feltet.</span><span class="sxs-lookup"><span data-stu-id="4838c-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="4838c-135">10 000</span><span class="sxs-lookup"><span data-stu-id="4838c-135">1000</span></span>  
12. <span data-ttu-id="4838c-136">Klikk kategorien Betaling.</span><span class="sxs-lookup"><span data-stu-id="4838c-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="4838c-137">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4838c-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="4838c-138">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4838c-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4838c-139">Velg den elektroniske verdien.</span><span class="sxs-lookup"><span data-stu-id="4838c-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="4838c-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4838c-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="4838c-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4838c-141">Click Save.</span></span>
17. <span data-ttu-id="4838c-142">Klikk Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="4838c-142">Click Generate payments.</span></span>
18. <span data-ttu-id="4838c-143">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4838c-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="4838c-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4838c-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4838c-145">Velg den elektroniske verdien.</span><span class="sxs-lookup"><span data-stu-id="4838c-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="4838c-146">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4838c-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4838c-147">Velg den elektroniske verdien.</span><span class="sxs-lookup"><span data-stu-id="4838c-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="4838c-148">Skriv inn en verdi i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="4838c-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="4838c-149">Skriv for eksempel betalinger.</span><span class="sxs-lookup"><span data-stu-id="4838c-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="4838c-150">Klikk rullegardinknappen i Bankkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4838c-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="4838c-151">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4838c-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4838c-152">Velg verdien GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="4838c-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="4838c-153">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4838c-153">Click OK.</span></span>
25. <span data-ttu-id="4838c-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4838c-154">Click OK.</span></span>
    * <span data-ttu-id="4838c-155">Analyser den opprettede betalingsfilen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="4838c-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="4838c-156">Sammenligne den med det utformede dokumentoppsettet og de definerte attributtene for betalingtransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="4838c-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

