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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569638"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="5df5e-103">Hovedfakturadata i AP-systemet ved hjelp av leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="5df5e-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5df5e-104">Denne oppgaveveiledningen hjelper deg med å opprette en leverandørfaktura fra en bestilling og vise resultatene av å samsvare bestillingen, kvitteringen og fakturaen (treveis kontroll).</span><span class="sxs-lookup"><span data-stu-id="5df5e-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="5df5e-105">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="5df5e-105">Create a purchase order</span></span>
1. <span data-ttu-id="5df5e-106">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="5df5e-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="5df5e-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5df5e-107">Click New.</span></span>
3. <span data-ttu-id="5df5e-108">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5df5e-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5df5e-109">Finn en leverandør å velge.</span><span class="sxs-lookup"><span data-stu-id="5df5e-109">Find a vendor to select.</span></span> <span data-ttu-id="5df5e-110">Bla for eksempel ned til USA – 104.</span><span class="sxs-lookup"><span data-stu-id="5df5e-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="5df5e-111">Velg leverandør USA – 104.</span><span class="sxs-lookup"><span data-stu-id="5df5e-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="5df5e-112">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5df5e-112">Click OK.</span></span>
7. <span data-ttu-id="5df5e-113">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5df5e-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5df5e-114">Velg en lagervare.</span><span class="sxs-lookup"><span data-stu-id="5df5e-114">Select an inventory item.</span></span> <span data-ttu-id="5df5e-115">Velg for eksempel varenummer 1000.</span><span class="sxs-lookup"><span data-stu-id="5df5e-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="5df5e-116">Vis eller skjul Linjedetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="5df5e-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="5df5e-117">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="5df5e-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="5df5e-118">Du kan overstyre kontrollpolicyen for å bruke ingen kontroll, toveis kontroll eller treveis kontroll.</span><span class="sxs-lookup"><span data-stu-id="5df5e-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="5df5e-119">Vis eller skjul Linjedetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="5df5e-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="5df5e-120">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5df5e-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="5df5e-121">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="5df5e-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="5df5e-122">Motta produktene</span><span class="sxs-lookup"><span data-stu-id="5df5e-122">Receive the products</span></span>
1. <span data-ttu-id="5df5e-123">Klikk Motta i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5df5e-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="5df5e-124">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="5df5e-124">Click Product receipt.</span></span>
3. <span data-ttu-id="5df5e-125">I feltet Produktkvittering angir du produktkvitteringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="5df5e-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="5df5e-126">Skriv for eksempel inn PR123.</span><span class="sxs-lookup"><span data-stu-id="5df5e-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="5df5e-127">Klikk OK for å postere produktkvitteringen.</span><span class="sxs-lookup"><span data-stu-id="5df5e-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="5df5e-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5df5e-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="5df5e-129">Opprette en leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="5df5e-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="5df5e-130">Gå til Leverandører > Bestillinger > Bestillinger er mottatt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="5df5e-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="5df5e-131">Velg bestillingen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="5df5e-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="5df5e-132">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5df5e-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="5df5e-133">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="5df5e-133">Click Invoice.</span></span>
5. <span data-ttu-id="5df5e-134">I feltet Nummer angir du fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="5df5e-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="5df5e-135">Skriv inn en verdi i feltet Fakturabeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="5df5e-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="5df5e-136">Angi en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="5df5e-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="5df5e-137">Angi 1200 i Enhetspris-feltet.</span><span class="sxs-lookup"><span data-stu-id="5df5e-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="5df5e-138">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="5df5e-138">Click Add line.</span></span>
10. <span data-ttu-id="5df5e-139">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5df5e-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5df5e-140">Finn varenummeret for installasjonstillegget i listen.</span><span class="sxs-lookup"><span data-stu-id="5df5e-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="5df5e-141">For eksempel S0001</span><span class="sxs-lookup"><span data-stu-id="5df5e-141">For example, S0001</span></span>
12. <span data-ttu-id="5df5e-142">Velg varenummeret for installasjonstillegget.</span><span class="sxs-lookup"><span data-stu-id="5df5e-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="5df5e-143">Legg merke til at det ikke er utført kontroll etter at du har gjort endringene.</span><span class="sxs-lookup"><span data-stu-id="5df5e-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="5df5e-144">Klikk Oppdater samsvarsstatus.</span><span class="sxs-lookup"><span data-stu-id="5df5e-144">Click Update match status.</span></span>
14. <span data-ttu-id="5df5e-145">Klikk Gå gjennom i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5df5e-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="5df5e-146">Klikk Samsvarende detaljer.</span><span class="sxs-lookup"><span data-stu-id="5df5e-146">Click Matching details.</span></span>
    * <span data-ttu-id="5df5e-147">Den nye linjen med tjenester trenger ikke kontrolleres, så statusen forblir "Ikke utført".</span><span class="sxs-lookup"><span data-stu-id="5df5e-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="5df5e-148">Velg produktkvitteringen for lagervaren du har mottatt.</span><span class="sxs-lookup"><span data-stu-id="5df5e-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="5df5e-149">Linjen med produktkvitteringen ble samsvart, men det er ikke samsvar mellom antall eller pris, slik at den mislykkes.</span><span class="sxs-lookup"><span data-stu-id="5df5e-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="5df5e-150">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="5df5e-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="5df5e-151">Nå som salgsprisen samsvarer, oppdateres statusen til Bestått.</span><span class="sxs-lookup"><span data-stu-id="5df5e-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="5df5e-152">Hvis policyen tillater avvik, eller hvis samsvar bare er en advarsel, kan du fortsatt postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="5df5e-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="5df5e-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5df5e-153">Close the page.</span></span>
19. <span data-ttu-id="5df5e-154">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="5df5e-154">Click Post.</span></span>
20. <span data-ttu-id="5df5e-155">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="5df5e-155">Close the form.</span></span>
    * <span data-ttu-id="5df5e-156">Legg merke til at bestillingen ikke lenger er oppført som mottatt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="5df5e-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

