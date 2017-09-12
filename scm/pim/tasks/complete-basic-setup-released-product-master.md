--- 
title: "Fullføre grunnleggende oppsett av en frigitt produktstandard"
description: "Denne fremgangsmåten viser hvordan du fullfører minimumsoppsett som kreves før produktstandarden kan brukes i stykklisteversjoner."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c42476ca3ffee41e303457150ef15da0f5af8a8f
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="d9e06-103">Fullføre grunnleggende oppsett av en frigitt produktstandard</span><span class="sxs-lookup"><span data-stu-id="d9e06-103">Complete basic setup of a released product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9e06-104">Denne fremgangsmåten viser hvordan du fullfører minimumsoppsett som kreves før produktstandarden kan brukes i stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="d9e06-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="d9e06-105">Dette er den tredje fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d9e06-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="d9e06-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d9e06-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d9e06-107">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="d9e06-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="d9e06-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d9e06-109">Velg produktstandarden du har frigitt i den andre prosedyren.</span><span class="sxs-lookup"><span data-stu-id="d9e06-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="d9e06-110">Denne produktstandarden opprettes ved hjelp av dimensjonsbasert konfigurasjon-teknologi.</span><span class="sxs-lookup"><span data-stu-id="d9e06-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="d9e06-111">Klikk Produkt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d9e06-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="d9e06-112">Klikk Dimensjonsgrupper for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="d9e06-113">Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d9e06-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d9e06-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d9e06-115">Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner som skal brukes for produkttransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="d9e06-116">Velg Område for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="d9e06-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="d9e06-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d9e06-118">Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d9e06-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d9e06-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d9e06-120">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner som skal brukes for produkttransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="d9e06-121">Velg Ingen for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="d9e06-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="d9e06-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="d9e06-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="d9e06-123">Click OK.</span></span>
12. <span data-ttu-id="d9e06-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d9e06-125">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="d9e06-125">Click Edit.</span></span>
    * <span data-ttu-id="d9e06-126">Åpne skjemaet Detaljer om frigitt produkt for å fortsette oppgaven for oppsettet.</span><span class="sxs-lookup"><span data-stu-id="d9e06-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="d9e06-127">Klikk rullegardinknappen i feltet Varemodellgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d9e06-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="d9e06-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d9e06-129">Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger.</span><span class="sxs-lookup"><span data-stu-id="d9e06-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="d9e06-130">De bestemmer også hvordan vareforbruk beregnes.</span><span class="sxs-lookup"><span data-stu-id="d9e06-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="d9e06-131">Velg FIFO for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="d9e06-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="d9e06-132">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="d9e06-133">Vis eller skjul delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="d9e06-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="d9e06-134">Klikk rullegardinknappen i feltet Varegruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d9e06-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="d9e06-135">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d9e06-136">Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper.</span><span class="sxs-lookup"><span data-stu-id="d9e06-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="d9e06-137">Velg CarAudio for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="d9e06-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="d9e06-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d9e06-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="d9e06-139">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d9e06-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="d9e06-140">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="d9e06-140">Click Default order settings.</span></span>
23. <span data-ttu-id="d9e06-141">Velg et alternativ i feltet Standard ordretype.</span><span class="sxs-lookup"><span data-stu-id="d9e06-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="d9e06-142">Velg Produksjon for å angi at standardforsyningsalternativet for denne produktstandarden skal produsere den.</span><span class="sxs-lookup"><span data-stu-id="d9e06-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="d9e06-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d9e06-143">Close the page.</span></span>
25. <span data-ttu-id="d9e06-144">Lukk skjemaet Detaljer om frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="d9e06-144">Close the Released product details form.</span></span>


