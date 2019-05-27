---
title: Definere arbeidspolicyer for lager (program, mai 2016)
description: Lagerprosesser inkluderer ikke alltid lagerarbeid.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569085"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="87804-103">Definere arbeidspolicyer for lager (program, mai 2016)</span><span class="sxs-lookup"><span data-stu-id="87804-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87804-104">Lagerprosesser inkluderer ikke alltid lagerarbeid.</span><span class="sxs-lookup"><span data-stu-id="87804-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="87804-105">Ved å definere en arbeidspolicy, kan du hindre oppretting av arbeid for råvareplukking og plassering av ferdige varer for et sett med produkter på bestemte lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="87804-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="87804-106">USMF-demodatafirmaet ble brukt til å opprette denne registreringen.</span><span class="sxs-lookup"><span data-stu-id="87804-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="87804-107">Denne oppgaveveiledningen krever Dynamics AX 7.0.1 eller senere.</span><span class="sxs-lookup"><span data-stu-id="87804-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="87804-108">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidspolicyer.</span><span class="sxs-lookup"><span data-stu-id="87804-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="87804-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="87804-109">Click New.</span></span>
3. <span data-ttu-id="87804-110">Skriv inn 'Ingen ferdigvarearbeid' i navnefeltet for arbeidspolicyen.</span><span class="sxs-lookup"><span data-stu-id="87804-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="87804-111">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="87804-111">Click Save.</span></span>
5. <span data-ttu-id="87804-112">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="87804-112">Click Add.</span></span>
6. <span data-ttu-id="87804-113">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87804-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="87804-114">Velg Plasser ferdigvarer i feltet for Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="87804-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="87804-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="87804-115">Click Add.</span></span>
9. <span data-ttu-id="87804-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87804-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="87804-117">Velg Plasser koprodukt og biprodukt i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="87804-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="87804-118">Vis delen Lagerlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="87804-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="87804-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="87804-119">Click Add.</span></span>
13. <span data-ttu-id="87804-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87804-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="87804-121">Angi 51 i Lager-listen.</span><span class="sxs-lookup"><span data-stu-id="87804-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="87804-122">Velg 001 i feltet Lokasjon.</span><span class="sxs-lookup"><span data-stu-id="87804-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="87804-123">Utvid seksjonen Produkter.</span><span class="sxs-lookup"><span data-stu-id="87804-123">Expand the Products section.</span></span>
17. <span data-ttu-id="87804-124">Velg Valgt i feltet Produktvalg.</span><span class="sxs-lookup"><span data-stu-id="87804-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="87804-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="87804-125">Click Add.</span></span>
19. <span data-ttu-id="87804-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="87804-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="87804-127">Angi eller velg L0101 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="87804-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="87804-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="87804-128">Click Save.</span></span>

