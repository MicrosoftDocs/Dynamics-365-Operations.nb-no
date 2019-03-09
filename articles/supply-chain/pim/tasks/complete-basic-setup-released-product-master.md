---
title: Fullføre grunnleggende oppsett av en frigitt produktstandard
description: Denne fremgangsmåten viser hvordan du fullfører minimumsoppsett som kreves før produktstandarden kan brukes i stykklisteversjoner.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "354788"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="5308f-103">Fullføre grunnleggende oppsett av en frigitt produktstandard</span><span class="sxs-lookup"><span data-stu-id="5308f-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5308f-104">Denne fremgangsmåten viser hvordan du fullfører minimumsoppsett som kreves før produktstandarden kan brukes i stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="5308f-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="5308f-105">Dette er den tredje fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="5308f-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="5308f-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5308f-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5308f-107">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="5308f-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="5308f-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5308f-109">Velg produktstandarden du har frigitt i den andre prosedyren.</span><span class="sxs-lookup"><span data-stu-id="5308f-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="5308f-110">Denne produktstandarden opprettes ved hjelp av dimensjonsbasert konfigurasjon-teknologi.</span><span class="sxs-lookup"><span data-stu-id="5308f-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="5308f-111">Klikk Produkt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5308f-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="5308f-112">Klikk Dimensjonsgrupper for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5308f-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="5308f-113">Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5308f-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5308f-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5308f-115">Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner som skal brukes for produkttransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="5308f-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="5308f-116">Velg Område for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="5308f-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="5308f-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5308f-118">Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5308f-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="5308f-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5308f-120">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner som skal brukes for produkttransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="5308f-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="5308f-121">Velg Ingen for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="5308f-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="5308f-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="5308f-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5308f-123">Click OK.</span></span>
12. <span data-ttu-id="5308f-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5308f-125">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="5308f-125">Click Edit.</span></span>
    * <span data-ttu-id="5308f-126">Åpne skjemaet Detaljer om frigitt produkt for å fortsette oppgaven for oppsettet.</span><span class="sxs-lookup"><span data-stu-id="5308f-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="5308f-127">Klikk rullegardinknappen i feltet Varemodellgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5308f-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5308f-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5308f-129">Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger.</span><span class="sxs-lookup"><span data-stu-id="5308f-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="5308f-130">De bestemmer også hvordan vareforbruk beregnes.</span><span class="sxs-lookup"><span data-stu-id="5308f-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="5308f-131">Velg FIFO for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="5308f-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="5308f-132">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="5308f-133">Vis eller skjul delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="5308f-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="5308f-134">Klikk rullegardinknappen i feltet Varegruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5308f-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="5308f-135">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5308f-136">Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper.</span><span class="sxs-lookup"><span data-stu-id="5308f-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="5308f-137">Velg CarAudio for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="5308f-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="5308f-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5308f-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="5308f-139">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5308f-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="5308f-140">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="5308f-140">Click Default order settings.</span></span>
23. <span data-ttu-id="5308f-141">Velg et alternativ i feltet Standard ordretype.</span><span class="sxs-lookup"><span data-stu-id="5308f-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="5308f-142">Velg Produksjon for å angi at standardforsyningsalternativet for denne produktstandarden skal produsere den.</span><span class="sxs-lookup"><span data-stu-id="5308f-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="5308f-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5308f-143">Close the page.</span></span>
25. <span data-ttu-id="5308f-144">Lukk skjemaet Detaljer om frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="5308f-144">Close the Released product details form.</span></span>

