--- 
title: "Godkjenne leverandører for bestemte produkter"
description: "Denne fremgangsmåten viser hvordan du godkjenner leverandører for bestemte produkter."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1e6669d632d4f6228dcbe98d82258eb97a6b255f
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="91bad-103">Godkjenne leverandører for bestemte produkter</span><span class="sxs-lookup"><span data-stu-id="91bad-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91bad-104">Denne fremgangsmåten viser hvordan du godkjenner leverandører for bestemte produkter.</span><span class="sxs-lookup"><span data-stu-id="91bad-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="91bad-105">Dette lar deg kontrollere hvilke leverandører som kan brukes når produktet legges til en bestilling.</span><span class="sxs-lookup"><span data-stu-id="91bad-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="91bad-106">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="91bad-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="91bad-107">Denne oppgaven utføres vanligvis av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="91bad-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="91bad-108">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="91bad-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="91bad-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="91bad-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="91bad-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="91bad-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="91bad-111">Vis delen Kjøp.</span><span class="sxs-lookup"><span data-stu-id="91bad-111">Expand the Purchase section.</span></span>
    * <span data-ttu-id="91bad-112">Hvis det finnes en hovedleverandør i Leverandør-feltet, må du legge til denne leverandøren som en godkjent leverandør i fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="91bad-112">If there is a primary vendor shown in the Vendor field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="91bad-113">Noter nummeret til leverandøren, hvis det vises et.</span><span class="sxs-lookup"><span data-stu-id="91bad-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="91bad-114">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="91bad-114">On the Action Pane, click Purchase.</span></span>
6. <span data-ttu-id="91bad-115">Klikk Oppsett.</span><span class="sxs-lookup"><span data-stu-id="91bad-115">Click Setup.</span></span>
7. <span data-ttu-id="91bad-116">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="91bad-116">Click Add.</span></span>
8. <span data-ttu-id="91bad-117">Angi eller velg en verdi i feltet Leverandør.</span><span class="sxs-lookup"><span data-stu-id="91bad-117">In the Vendor field, enter or select a value.</span></span>
    * <span data-ttu-id="91bad-118">Velg den godkjente leverandøren.</span><span class="sxs-lookup"><span data-stu-id="91bad-118">Select the approved vendor.</span></span> <span data-ttu-id="91bad-119">Minst én av linjene må være hovedleverandøren, hvis det var en i produktposten.</span><span class="sxs-lookup"><span data-stu-id="91bad-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="91bad-120">Hvis du har notert nummeret til leverandøren tidligere, kan du angi det her.</span><span class="sxs-lookup"><span data-stu-id="91bad-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="91bad-121">Angi en dato i Utløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="91bad-121">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="91bad-122">Velg en dato som er et par måneder fremover.</span><span class="sxs-lookup"><span data-stu-id="91bad-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="91bad-123">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="91bad-123">Click Add.</span></span>
11. <span data-ttu-id="91bad-124">Angi eller velg en verdi i feltet Leverandør.</span><span class="sxs-lookup"><span data-stu-id="91bad-124">In the Vendor field, enter or select a value.</span></span>
12. <span data-ttu-id="91bad-125">Angi en dato i Utløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="91bad-125">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="91bad-126">Velg en dato som er forskjellig fra forrige utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="91bad-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="91bad-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="91bad-127">Close the page.</span></span>
14. <span data-ttu-id="91bad-128">Klikk Godkjente leverandører.</span><span class="sxs-lookup"><span data-stu-id="91bad-128">Click Approved vendors.</span></span>
15. <span data-ttu-id="91bad-129">Angi en dato i Utløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="91bad-129">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="91bad-130">Denne datoen fungerer som et filter, slik at du kan se hvem de godkjente leverandørene er opptil en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="91bad-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="91bad-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="91bad-131">Close the page.</span></span>
17. <span data-ttu-id="91bad-132">Klikk Gyldig periode.</span><span class="sxs-lookup"><span data-stu-id="91bad-132">Click Effective period.</span></span>
18. <span data-ttu-id="91bad-133">Angi en dato i feltet Vis leverandører utløpt etter.</span><span class="sxs-lookup"><span data-stu-id="91bad-133">In the Show vendors expired by field, enter a date.</span></span>
    * <span data-ttu-id="91bad-134">Du kan bruke denne siden til å identifisere leverandører med godkjenningsstatus som utløper etter en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="91bad-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="91bad-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="91bad-135">Close the page.</span></span>
20. <span data-ttu-id="91bad-136">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="91bad-136">Click Edit.</span></span>
21. <span data-ttu-id="91bad-137">Velg et alternativ i feltet Godkjent leverandørkontrollmetode.</span><span class="sxs-lookup"><span data-stu-id="91bad-137">In the Approved vendor check method field, select an option.</span></span>
    * <span data-ttu-id="91bad-138">Dette feltet lar deg velge policyen for hva som skal skje hvis produktet blir lagt til en bestillingslinje der leverandøren ikke er en godkjent leverandør.</span><span class="sxs-lookup"><span data-stu-id="91bad-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="91bad-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="91bad-139">Click Save.</span></span>
23. <span data-ttu-id="91bad-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="91bad-140">Close the page.</span></span>
24. <span data-ttu-id="91bad-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="91bad-141">Close the page.</span></span>
25. <span data-ttu-id="91bad-142">Gå til Innkjøp og leverandører > Leverandører > Leverandør-/varerelasjoner Z Liste over godkjente leverandører etter vare.</span><span class="sxs-lookup"><span data-stu-id="91bad-142">Go to Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item.</span></span>
    * <span data-ttu-id="91bad-143">Denne siden gir deg en oversikt over alle produkter og godkjente leverandører.</span><span class="sxs-lookup"><span data-stu-id="91bad-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="91bad-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="91bad-144">Close the page.</span></span>
27. <span data-ttu-id="91bad-145">Gå til Innkjøp og leverandører > Leverandører > Alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="91bad-145">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
    * <span data-ttu-id="91bad-146">Du kan også starte fra en leverandør og deretter går til listen over godkjente produkter for denne leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="91bad-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="91bad-147">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="91bad-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="91bad-148">Klikk Innkjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="91bad-148">On the Action Pane, click Procurement.</span></span>
30. <span data-ttu-id="91bad-149">Klikk Liste over godkjente leverandører etter leverandør.</span><span class="sxs-lookup"><span data-stu-id="91bad-149">Click Approved vendor list by vendor.</span></span>
31. <span data-ttu-id="91bad-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="91bad-150">Close the page.</span></span>
32. <span data-ttu-id="91bad-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="91bad-151">Close the page.</span></span>


