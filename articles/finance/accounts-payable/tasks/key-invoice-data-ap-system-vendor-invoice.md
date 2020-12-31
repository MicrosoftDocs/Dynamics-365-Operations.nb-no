---
title: Hovedfakturadata i AP ved hjelp av en leverandørfaktura
description: Denne oppgaveveiledningen hjelper deg med å opprette en leverandørfaktura fra en bestilling og vise resultatene av å samsvare bestillingen, kvitteringen og fakturaen (treveis kontroll).
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f80c88b7fb3542f624d233f670cd7cd6ccd48b94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446233"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="8f55f-103">Hovedfakturadata i AP ved hjelp av en leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="8f55f-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f55f-104">Denne oppgaveveiledningen hjelper deg med å opprette en leverandørfaktura fra en bestilling og vise resultatene av å samsvare bestillingen, kvitteringen og fakturaen (treveis kontroll).</span><span class="sxs-lookup"><span data-stu-id="8f55f-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="8f55f-105">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="8f55f-105">Create a purchase order</span></span>
1. <span data-ttu-id="8f55f-106">I navigasjonsruten går du til **Moduler > Leverandører > Bestillinger > Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="8f55f-107">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-107">Click **New**.</span></span>
3. <span data-ttu-id="8f55f-108">Klikk rullegardinknappen i **Leverandørkonto**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8f55f-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8f55f-109">Finn en leverandør å velge.</span><span class="sxs-lookup"><span data-stu-id="8f55f-109">Find a vendor to select.</span></span> <span data-ttu-id="8f55f-110">Bla for eksempel ned til USA – 104.</span><span class="sxs-lookup"><span data-stu-id="8f55f-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="8f55f-111">Velg leverandør USA – 104.</span><span class="sxs-lookup"><span data-stu-id="8f55f-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="8f55f-112">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-112">Click **OK**.</span></span>
7. <span data-ttu-id="8f55f-113">Klikk rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8f55f-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8f55f-114">Velg en lagervare.</span><span class="sxs-lookup"><span data-stu-id="8f55f-114">Select an inventory item.</span></span> <span data-ttu-id="8f55f-115">Velg for eksempel varenummer 1000.</span><span class="sxs-lookup"><span data-stu-id="8f55f-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="8f55f-116">Utvid hurtigfanen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="8f55f-117">Klikk på kategorien **Oppsett**. Du kan overstyre kontrollpolicyen for å bruke ingen kontroll, toveis kontroll eller treveis kontroll.</span><span class="sxs-lookup"><span data-stu-id="8f55f-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="8f55f-118">Klikk **Innkjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8f55f-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="8f55f-119">Klikk **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="8f55f-120">Motta produktene</span><span class="sxs-lookup"><span data-stu-id="8f55f-120">Receive the products</span></span>
1. <span data-ttu-id="8f55f-121">Klikk **Motta** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8f55f-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="8f55f-122">Klikk **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="8f55f-123">I feltet **Produktkvittering** angir du produktkvitteringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="8f55f-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="8f55f-124">Skriv for eksempel inn PR123.</span><span class="sxs-lookup"><span data-stu-id="8f55f-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="8f55f-125">Klikk på **OK** for å postere produktkvitteringen.</span><span class="sxs-lookup"><span data-stu-id="8f55f-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="8f55f-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8f55f-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="8f55f-127">Opprette en leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="8f55f-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="8f55f-128">I navigasjonsruten går du til **Moduler > Leverandører > Bestillinger > Bestillinger er mottatt, men ikke fakturert**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="8f55f-129">Velg bestillingen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="8f55f-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="8f55f-130">Klikk på **Faktura** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8f55f-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="8f55f-131">Klikk på **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="8f55f-132">I feltet **Nummer** angir du fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="8f55f-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="8f55f-133">Skriv inn en verdi i feltet **Fakturabeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="8f55f-134">Angi en dato i **Fakturadato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8f55f-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="8f55f-135">Angi 1200 i **Enhetspris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8f55f-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="8f55f-136">Klikk **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-136">Click **Add line**.</span></span>
10. <span data-ttu-id="8f55f-137">Klikk rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8f55f-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8f55f-138">Finn varenummeret for installasjonstillegget i listen.</span><span class="sxs-lookup"><span data-stu-id="8f55f-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="8f55f-139">For eksempel S0001</span><span class="sxs-lookup"><span data-stu-id="8f55f-139">For example, S0001</span></span>
12. <span data-ttu-id="8f55f-140">Velg varenummeret for installasjonstillegget.</span><span class="sxs-lookup"><span data-stu-id="8f55f-140">Select the installation charge item number.</span></span> <span data-ttu-id="8f55f-141">Legg merke til at det ikke er utført kontroll etter at du har gjort endringene.</span><span class="sxs-lookup"><span data-stu-id="8f55f-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="8f55f-142">Klikk på **Oppdater samsvarsstatus**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="8f55f-143">Klikk **Gå gjennom** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8f55f-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="8f55f-144">Klikk **Samsvarende detaljer**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-144">Click **Matching details**.</span></span> <span data-ttu-id="8f55f-145">Den nye linjen med tjenester trenger ikke kontrolleres, så statusen forblir "Ikke utført".</span><span class="sxs-lookup"><span data-stu-id="8f55f-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="8f55f-146">Velg produktkvitteringen for lagervaren du har mottatt.</span><span class="sxs-lookup"><span data-stu-id="8f55f-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="8f55f-147">Linjen med produktkvitteringen ble samsvart, men det er ikke samsvar mellom antall eller pris, slik at den mislykkes.</span><span class="sxs-lookup"><span data-stu-id="8f55f-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="8f55f-148">Angi et tall i **Enhetspris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8f55f-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="8f55f-149">Nå som salgsprisen samsvarer, oppdateres statusen til Bestått.</span><span class="sxs-lookup"><span data-stu-id="8f55f-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="8f55f-150">Hvis policyen tillater avvik, eller hvis samsvar bare er en advarsel, kan du fortsatt postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="8f55f-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="8f55f-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8f55f-151">Close the page.</span></span>
19. <span data-ttu-id="8f55f-152">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="8f55f-152">Click **Post**.</span></span>
20. <span data-ttu-id="8f55f-153">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="8f55f-153">Close the form.</span></span> <span data-ttu-id="8f55f-154">Legg merke til at bestillingen ikke lenger er oppført som mottatt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="8f55f-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

