---
title: Fullføre grunnleggende oppsett av en frigitt produktstandard
description: Dette emnet viser hvordan du fullfører minimumsoppsettet som kreves før produktstandarden kan brukes i stykklisteversjoner.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f93f3db022b7b338bfa18ff6aea79f8086ea997f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147946"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="c69df-103">Fullføre grunnleggende oppsett av en frigitt produktstandard</span><span class="sxs-lookup"><span data-stu-id="c69df-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c69df-104">Dette emnet viser hvordan du fullfører minimumsoppsettet som kreves før produktstandarden kan brukes i stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="c69df-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="c69df-105">Dette er den tredje fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="c69df-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="c69df-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="c69df-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c69df-107">Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="c69df-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="c69df-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c69df-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="c69df-109">Velg produktstandarden du har frigitt i den andre prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c69df-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="c69df-110">Denne produktstandarden opprettes ved hjelp av dimensjonsbasert konfigurasjon-teknologi.</span><span class="sxs-lookup"><span data-stu-id="c69df-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="c69df-111">Klikk på **Produkt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c69df-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="c69df-112">Velg **Dimensjonsgrupper** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="c69df-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="c69df-113">Klikk på rullegardinknappen i **Lagringsdimensjonsgruppe**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c69df-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c69df-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c69df-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="c69df-115">Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner som skal brukes for produkttransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="c69df-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="c69df-116">Velg **Område** for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c69df-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="c69df-117">Klikk på rullegardinknappen i **Sporingsdimensjonsgruppe**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c69df-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c69df-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c69df-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="c69df-119">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner som skal brukes for produkttransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="c69df-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="c69df-120">Velg **Ingen** for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c69df-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="c69df-121">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c69df-121">Click **OK**.</span></span>
10. <span data-ttu-id="c69df-122">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c69df-122">Click **Edit**.</span></span>
11. <span data-ttu-id="c69df-123">Klikk på rullegardinknappen i feltet **Varemodellgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c69df-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c69df-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c69df-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="c69df-125">Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger.</span><span class="sxs-lookup"><span data-stu-id="c69df-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="c69df-126">De bestemmer også hvordan vareforbruk beregnes.</span><span class="sxs-lookup"><span data-stu-id="c69df-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="c69df-127">Velg **FIFO** for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c69df-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="c69df-128">Vis delen **Styr kostnader**.</span><span class="sxs-lookup"><span data-stu-id="c69df-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="c69df-129">Klikk på rullegardinknappen i feltet **Varegruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c69df-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c69df-130">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c69df-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="c69df-131">Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper.</span><span class="sxs-lookup"><span data-stu-id="c69df-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="c69df-132">Velg **CarAudio** for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c69df-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="c69df-133">Velg **Plan** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c69df-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="c69df-134">Velg **Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="c69df-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="c69df-135">Velg et alternativ i feltet **Standard ordretype**.</span><span class="sxs-lookup"><span data-stu-id="c69df-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="c69df-136">Velg **Produksjon** for å angi at standardforsyningsalternativet for denne produktstandarden skal produsere den.</span><span class="sxs-lookup"><span data-stu-id="c69df-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="c69df-137">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c69df-137">Select **Save**.</span></span>
20. <span data-ttu-id="c69df-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c69df-138">Close the page.</span></span>
21. <span data-ttu-id="c69df-139">Lukk skjemaet **Detaljer om frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="c69df-139">Close the **Released product details** form.</span></span>

