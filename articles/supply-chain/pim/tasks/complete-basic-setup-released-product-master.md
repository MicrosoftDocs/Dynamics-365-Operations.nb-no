---
title: Fullføre grunnleggende oppsett av en frigitt produktstandard
description: Dette emnet viser hvordan du fullfører minimumsoppsettet som kreves før produktstandarden kan brukes i stykklisteversjoner.
author: ShylaThompson
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c41e9e3267f72a2452eddfeb15f8f5cba79b0b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820160"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="8d923-103">Fullføre grunnleggende oppsett av en frigitt produktstandard</span><span class="sxs-lookup"><span data-stu-id="8d923-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d923-104">Dette emnet viser hvordan du fullfører minimumsoppsettet som kreves før produktstandarden kan brukes i stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="8d923-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="8d923-105">Dette er den tredje fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="8d923-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="8d923-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8d923-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8d923-107">Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="8d923-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="8d923-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8d923-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="8d923-109">Velg produktstandarden du har frigitt i den andre prosedyren.</span><span class="sxs-lookup"><span data-stu-id="8d923-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="8d923-110">Denne produktstandarden opprettes ved hjelp av dimensjonsbasert konfigurasjon-teknologi.</span><span class="sxs-lookup"><span data-stu-id="8d923-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="8d923-111">Klikk på **Produkt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8d923-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="8d923-112">Velg **Dimensjonsgrupper** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="8d923-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="8d923-113">Klikk på rullegardinknappen i **Lagringsdimensjonsgruppe**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8d923-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8d923-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8d923-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="8d923-115">Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner som skal brukes for produkttransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="8d923-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="8d923-116">Velg **Område** for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="8d923-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="8d923-117">Klikk på rullegardinknappen i **Sporingsdimensjonsgruppe**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8d923-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8d923-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8d923-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="8d923-119">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner som skal brukes for produkttransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="8d923-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="8d923-120">Velg **Ingen** for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="8d923-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="8d923-121">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d923-121">Click **OK**.</span></span>
10. <span data-ttu-id="8d923-122">Klikk på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="8d923-122">Click **Edit**.</span></span>
11. <span data-ttu-id="8d923-123">Klikk på rullegardinknappen i feltet **Varemodellgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8d923-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="8d923-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8d923-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="8d923-125">Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger.</span><span class="sxs-lookup"><span data-stu-id="8d923-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="8d923-126">De bestemmer også hvordan vareforbruk beregnes.</span><span class="sxs-lookup"><span data-stu-id="8d923-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="8d923-127">Velg **FIFO** for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="8d923-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="8d923-128">Vis delen **Styr kostnader**.</span><span class="sxs-lookup"><span data-stu-id="8d923-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="8d923-129">Klikk på rullegardinknappen i feltet **Varegruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8d923-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="8d923-130">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8d923-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="8d923-131">Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper.</span><span class="sxs-lookup"><span data-stu-id="8d923-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="8d923-132">Velg **CarAudio** for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="8d923-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="8d923-133">Velg **Plan** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8d923-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="8d923-134">Velg **Standard ordreinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="8d923-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="8d923-135">Velg et alternativ i feltet **Standard ordretype**.</span><span class="sxs-lookup"><span data-stu-id="8d923-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="8d923-136">Velg **Produksjon** for å angi at standardforsyningsalternativet for denne produktstandarden skal produsere den.</span><span class="sxs-lookup"><span data-stu-id="8d923-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="8d923-137">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8d923-137">Select **Save**.</span></span>
20. <span data-ttu-id="8d923-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8d923-138">Close the page.</span></span>
21. <span data-ttu-id="8d923-139">Lukk skjemaet **Detaljer om frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="8d923-139">Close the **Released product details** form.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]