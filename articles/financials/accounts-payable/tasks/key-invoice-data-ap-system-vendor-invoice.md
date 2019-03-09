---
title: Hovedfakturadata i AP-systemet ved hjelp av leverandørfaktura
description: Denne oppgaveveiledningen hjelper deg med å opprette en leverandørfaktura fra en bestilling og vise resultatene av å samsvare bestillingen, kvitteringen og fakturaen (treveis kontroll).
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "359112"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="d18ae-103">Hovedfakturadata i AP-systemet ved hjelp av leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="d18ae-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d18ae-104">Denne oppgaveveiledningen hjelper deg med å opprette en leverandørfaktura fra en bestilling og vise resultatene av å samsvare bestillingen, kvitteringen og fakturaen (treveis kontroll).</span><span class="sxs-lookup"><span data-stu-id="d18ae-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="d18ae-105">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="d18ae-105">Create a purchase order</span></span>
1. <span data-ttu-id="d18ae-106">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="d18ae-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="d18ae-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d18ae-107">Click New.</span></span>
3. <span data-ttu-id="d18ae-108">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d18ae-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d18ae-109">Finn en leverandør å velge.</span><span class="sxs-lookup"><span data-stu-id="d18ae-109">Find a vendor to select.</span></span> <span data-ttu-id="d18ae-110">Bla for eksempel ned til USA – 104.</span><span class="sxs-lookup"><span data-stu-id="d18ae-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="d18ae-111">Velg leverandør USA – 104.</span><span class="sxs-lookup"><span data-stu-id="d18ae-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="d18ae-112">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="d18ae-112">Click OK.</span></span>
7. <span data-ttu-id="d18ae-113">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d18ae-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d18ae-114">Velg en lagervare.</span><span class="sxs-lookup"><span data-stu-id="d18ae-114">Select an inventory item.</span></span> <span data-ttu-id="d18ae-115">Velg for eksempel varenummer 1000.</span><span class="sxs-lookup"><span data-stu-id="d18ae-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="d18ae-116">Vis eller skjul Linjedetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="d18ae-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="d18ae-117">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="d18ae-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="d18ae-118">Du kan overstyre kontrollpolicyen for å bruke ingen kontroll, toveis kontroll eller treveis kontroll.</span><span class="sxs-lookup"><span data-stu-id="d18ae-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="d18ae-119">Vis eller skjul Linjedetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="d18ae-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="d18ae-120">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d18ae-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="d18ae-121">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="d18ae-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="d18ae-122">Motta produktene</span><span class="sxs-lookup"><span data-stu-id="d18ae-122">Receive the products</span></span>
1. <span data-ttu-id="d18ae-123">Klikk Motta i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d18ae-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="d18ae-124">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="d18ae-124">Click Product receipt.</span></span>
3. <span data-ttu-id="d18ae-125">I feltet Produktkvittering angir du produktkvitteringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="d18ae-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="d18ae-126">Skriv for eksempel inn PR123.</span><span class="sxs-lookup"><span data-stu-id="d18ae-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="d18ae-127">Klikk OK for å postere produktkvitteringen.</span><span class="sxs-lookup"><span data-stu-id="d18ae-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="d18ae-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d18ae-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="d18ae-129">Opprette en leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="d18ae-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="d18ae-130">Gå til Leverandører > Bestillinger > Bestillinger er mottatt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="d18ae-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="d18ae-131">Velg bestillingen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="d18ae-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="d18ae-132">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d18ae-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="d18ae-133">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="d18ae-133">Click Invoice.</span></span>
5. <span data-ttu-id="d18ae-134">I feltet Nummer angir du fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="d18ae-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="d18ae-135">Skriv inn en verdi i feltet Fakturabeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d18ae-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="d18ae-136">Angi en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="d18ae-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="d18ae-137">Angi 1200 i Enhetspris-feltet.</span><span class="sxs-lookup"><span data-stu-id="d18ae-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="d18ae-138">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="d18ae-138">Click Add line.</span></span>
10. <span data-ttu-id="d18ae-139">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d18ae-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d18ae-140">Finn varenummeret for installasjonstillegget i listen.</span><span class="sxs-lookup"><span data-stu-id="d18ae-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="d18ae-141">For eksempel S0001</span><span class="sxs-lookup"><span data-stu-id="d18ae-141">For example, S0001</span></span>
12. <span data-ttu-id="d18ae-142">Velg varenummeret for installasjonstillegget.</span><span class="sxs-lookup"><span data-stu-id="d18ae-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="d18ae-143">Legg merke til at det ikke er utført kontroll etter at du har gjort endringene.</span><span class="sxs-lookup"><span data-stu-id="d18ae-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="d18ae-144">Klikk Oppdater samsvarsstatus.</span><span class="sxs-lookup"><span data-stu-id="d18ae-144">Click Update match status.</span></span>
14. <span data-ttu-id="d18ae-145">Klikk Gå gjennom i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d18ae-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="d18ae-146">Klikk Samsvarende detaljer.</span><span class="sxs-lookup"><span data-stu-id="d18ae-146">Click Matching details.</span></span>
    * <span data-ttu-id="d18ae-147">Den nye linjen med tjenester trenger ikke kontrolleres, så statusen forblir "Ikke utført".</span><span class="sxs-lookup"><span data-stu-id="d18ae-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="d18ae-148">Velg produktkvitteringen for lagervaren du har mottatt.</span><span class="sxs-lookup"><span data-stu-id="d18ae-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="d18ae-149">Linjen med produktkvitteringen ble samsvart, men det er ikke samsvar mellom antall eller pris, slik at den mislykkes.</span><span class="sxs-lookup"><span data-stu-id="d18ae-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="d18ae-150">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="d18ae-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="d18ae-151">Nå som salgsprisen samsvarer, oppdateres statusen til Bestått.</span><span class="sxs-lookup"><span data-stu-id="d18ae-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="d18ae-152">Hvis policyen tillater avvik, eller hvis samsvar bare er en advarsel, kan du fortsatt postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="d18ae-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="d18ae-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d18ae-153">Close the page.</span></span>
19. <span data-ttu-id="d18ae-154">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="d18ae-154">Click Post.</span></span>
20. <span data-ttu-id="d18ae-155">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="d18ae-155">Close the form.</span></span>
    * <span data-ttu-id="d18ae-156">Legg merke til at bestillingen ikke lenger er oppført som mottatt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="d18ae-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

