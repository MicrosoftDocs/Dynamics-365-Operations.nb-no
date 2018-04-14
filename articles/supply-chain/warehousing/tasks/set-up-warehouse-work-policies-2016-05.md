--- 
title: 'Definere arbeidspolicyer for lager '
description: Lagerprosesser inkluderer ikke alltid lagerarbeid.
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe237543770fd05198b46cc7fc72b21926177807
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="474a6-103">Definere arbeidspolicyer for lager </span><span class="sxs-lookup"><span data-stu-id="474a6-103">Set up warehouse work policies</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="474a6-104">Lagerprosesser inkluderer ikke alltid lagerarbeid.</span><span class="sxs-lookup"><span data-stu-id="474a6-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="474a6-105">Ved å definere en arbeidspolicy, kan du hindre oppretting av arbeid for råvareplukking og plassering av ferdige varer for et sett med produkter på bestemte lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="474a6-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="474a6-106">USMF-demodatafirmaet ble brukt til å opprette denne registreringen.</span><span class="sxs-lookup"><span data-stu-id="474a6-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="474a6-107">Denne oppgaveveiledningen krever Dynamics AX 7.0.1 eller senere.</span><span class="sxs-lookup"><span data-stu-id="474a6-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="474a6-108">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidspolicyer.</span><span class="sxs-lookup"><span data-stu-id="474a6-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="474a6-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="474a6-109">Click New.</span></span>
3. <span data-ttu-id="474a6-110">Skriv inn 'Ingen ferdigvarearbeid' i navnefeltet for arbeidspolicyen.</span><span class="sxs-lookup"><span data-stu-id="474a6-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="474a6-111">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="474a6-111">Click Save.</span></span>
5. <span data-ttu-id="474a6-112">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="474a6-112">Click Add.</span></span>
6. <span data-ttu-id="474a6-113">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="474a6-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="474a6-114">Velg Plasser ferdigvarer i feltet for Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="474a6-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="474a6-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="474a6-115">Click Add.</span></span>
9. <span data-ttu-id="474a6-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="474a6-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="474a6-117">Velg Plasser koprodukt og biprodukt i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="474a6-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="474a6-118">Vis delen Lagerlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="474a6-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="474a6-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="474a6-119">Click Add.</span></span>
13. <span data-ttu-id="474a6-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="474a6-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="474a6-121">Angi 51 i Lager-listen.</span><span class="sxs-lookup"><span data-stu-id="474a6-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="474a6-122">Velg 001 i feltet Lokasjon.</span><span class="sxs-lookup"><span data-stu-id="474a6-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="474a6-123">Utvid seksjonen Produkter.</span><span class="sxs-lookup"><span data-stu-id="474a6-123">Expand the Products section.</span></span>
17. <span data-ttu-id="474a6-124">Velg Valgt i feltet Produktvalg.</span><span class="sxs-lookup"><span data-stu-id="474a6-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="474a6-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="474a6-125">Click Add.</span></span>
19. <span data-ttu-id="474a6-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="474a6-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="474a6-127">Angi eller velg L0101 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="474a6-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="474a6-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="474a6-128">Click Save.</span></span>


