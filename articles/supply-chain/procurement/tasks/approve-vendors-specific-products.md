---
title: Godkjenne leverandører for bestemte produkter
description: Denne fremgangsmåten viser hvordan du godkjenner leverandører for bestemte produkter.
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fafa2f7da5575206d452f31bb297790874369dfd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434354"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="9f599-103">Godkjenne leverandører for bestemte produkter</span><span class="sxs-lookup"><span data-stu-id="9f599-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f599-104">Denne fremgangsmåten viser hvordan du godkjenner leverandører for bestemte produkter.</span><span class="sxs-lookup"><span data-stu-id="9f599-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="9f599-105">Dette lar deg kontrollere hvilke leverandører som kan brukes når produktet legges til en bestilling.</span><span class="sxs-lookup"><span data-stu-id="9f599-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="9f599-106">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="9f599-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="9f599-107">Denne oppgaven utføres vanligvis av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="9f599-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="9f599-108">I navigasjonsruten går du til **Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="9f599-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="9f599-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9f599-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9f599-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9f599-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9f599-111">Vis hurtigfanen **Innkjøp**.</span><span class="sxs-lookup"><span data-stu-id="9f599-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="9f599-112">Hvis det finnes en hovedleverandør i **Leverandør**-feltet, må du legge til denne leverandøren som en godkjent leverandør i fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9f599-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="9f599-113">Noter nummeret til leverandøren, hvis det vises et.</span><span class="sxs-lookup"><span data-stu-id="9f599-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="9f599-114">Klikk **Innkjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9f599-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="9f599-115">Klikk på **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="9f599-115">Click **Setup**.</span></span>
7. <span data-ttu-id="9f599-116">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="9f599-116">Click **Add**.</span></span>
8. <span data-ttu-id="9f599-117">Angi eller velg en verdi i feltet Leverandør.</span><span class="sxs-lookup"><span data-stu-id="9f599-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="9f599-118">Velg den godkjente leverandøren.</span><span class="sxs-lookup"><span data-stu-id="9f599-118">Select the approved vendor.</span></span> <span data-ttu-id="9f599-119">Minst én av linjene må være hovedleverandøren, hvis det var en i produktposten.</span><span class="sxs-lookup"><span data-stu-id="9f599-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="9f599-120">Hvis du har notert nummeret til leverandøren tidligere, kan du angi det her.</span><span class="sxs-lookup"><span data-stu-id="9f599-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="9f599-121">Angi en dato i **Utløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9f599-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="9f599-122">Velg en dato som er et par måneder fremover.</span><span class="sxs-lookup"><span data-stu-id="9f599-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="9f599-123">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="9f599-123">Click **Add**.</span></span>
11. <span data-ttu-id="9f599-124">Angi eller velg en verdi i feltet **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="9f599-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="9f599-125">Angi en dato i **Utløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9f599-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="9f599-126">Velg en dato som er forskjellig fra forrige utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="9f599-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="9f599-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f599-127">Close the page.</span></span>
14. <span data-ttu-id="9f599-128">Klikk på **Godkjente leverandører** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9f599-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="9f599-129">Angi en dato i **Utløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9f599-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="9f599-130">Denne datoen fungerer som et filter, slik at du kan se hvem de godkjente leverandørene er opptil en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="9f599-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="9f599-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f599-131">Close the page.</span></span>
17. <span data-ttu-id="9f599-132">Klikk på **Gyldig periode** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9f599-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="9f599-133">Angi en dato i feltet **Vis leverandører utløpt etter**.</span><span class="sxs-lookup"><span data-stu-id="9f599-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="9f599-134">Du kan bruke denne siden til å identifisere leverandører med godkjenningsstatus som utløper etter en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="9f599-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="9f599-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f599-135">Close the page.</span></span>
20. <span data-ttu-id="9f599-136">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="9f599-136">Click **Edit**.</span></span>
21. <span data-ttu-id="9f599-137">Velg et alternativ i feltet **Godkjent leverandørkontrollmetode**.</span><span class="sxs-lookup"><span data-stu-id="9f599-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="9f599-138">Dette feltet lar deg velge policyen for hva som skal skje hvis produktet blir lagt til en bestillingslinje der leverandøren ikke er en godkjent leverandør.</span><span class="sxs-lookup"><span data-stu-id="9f599-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="9f599-139">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9f599-139">Click **Save**.</span></span>
23. <span data-ttu-id="9f599-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f599-140">Close the page.</span></span>
24. <span data-ttu-id="9f599-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f599-141">Close the page.</span></span>
25. <span data-ttu-id="9f599-142">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Leverandører > Leverandør-/varerelasjoner > Liste over godkjente leverandører etter vare**.</span><span class="sxs-lookup"><span data-stu-id="9f599-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="9f599-143">Denne siden gir deg en oversikt over alle produkter og godkjente leverandører.</span><span class="sxs-lookup"><span data-stu-id="9f599-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="9f599-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f599-144">Close the page.</span></span>
27. <span data-ttu-id="9f599-145">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Leverandører > Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="9f599-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="9f599-146">Du kan også starte fra en leverandør og deretter går til listen over godkjente produkter for denne leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="9f599-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="9f599-147">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9f599-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="9f599-148">Klikk på **Innkjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9f599-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="9f599-149">Klikk på **Liste over godkjente leverandører etter leverandør**.</span><span class="sxs-lookup"><span data-stu-id="9f599-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="9f599-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f599-150">Close the page.</span></span>
32. <span data-ttu-id="9f599-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f599-151">Close the page.</span></span>

