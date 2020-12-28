---
title: Opprette et nytt lageroppsett
description: Dette emnet beskriver hvordan du definerer informasjon om lokasjoner i et lager.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09666e95cc90913f1bf8555b9ff2c48aa55369ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434673"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="31bc0-103">Opprette et nytt lageroppsett</span><span class="sxs-lookup"><span data-stu-id="31bc0-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31bc0-104">Dette emnet beskriver hvordan du definerer informasjon om lokasjoner i et lager.</span><span class="sxs-lookup"><span data-stu-id="31bc0-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="31bc0-105">Dette gjelder bare for lagrene som er opprettet ved hjelp av "grunnleggende lageraktiviteter" i lagermodulen, ikke for lagre som er opprettet i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="31bc0-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="31bc0-106">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="31bc0-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="31bc0-107">Angi standard lokasjonskapasitet</span><span class="sxs-lookup"><span data-stu-id="31bc0-107">Set the default location capacity</span></span>
1. <span data-ttu-id="31bc0-108">I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="31bc0-109">Velg fanen **Lokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="31bc0-110">Angi et nummer i **Standardbredde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="31bc0-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="31bc0-111">Angi et nummer i **Standarddybde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="31bc0-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="31bc0-112">Angi et tall i **Standardhøyde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="31bc0-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="31bc0-113">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-113">Select **Save**.</span></span>
7. <span data-ttu-id="31bc0-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="31bc0-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="31bc0-115">Definer formatet for plasseringsnavn</span><span class="sxs-lookup"><span data-stu-id="31bc0-115">Define the location name format</span></span>
1. <span data-ttu-id="31bc0-116">I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Lageroppdeling > Lagre**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="31bc0-117">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-117">Select **New**.</span></span>
3. <span data-ttu-id="31bc0-118">Skriv inn en verdi i **Lager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="31bc0-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="31bc0-119">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="31bc0-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="31bc0-120">Velg det ønskede oppslaget i **Område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="31bc0-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="31bc0-121">Aktiver/deaktiver utvidelsen av delen **Lokasjonsnavn**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="31bc0-122">Alternativene i denne delen definerer standardformatet for lokasjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="31bc0-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="31bc0-123">I vårt eksempel skal vi ta med gangnummer, reolnummer og hyllenummer.</span><span class="sxs-lookup"><span data-stu-id="31bc0-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="31bc0-124">Sett alternativet **Inkluder gang** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="31bc0-125">Sett alternativet **Ta med reol** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="31bc0-126">I **Format**-feltet velger du en verdi for reolen.</span><span class="sxs-lookup"><span data-stu-id="31bc0-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="31bc0-127">Sett alternativet **Ta med hylle** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="31bc0-128">I **Format**-feltet velger du en verdi for hyllen.</span><span class="sxs-lookup"><span data-stu-id="31bc0-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="31bc0-129">Definer lagerlokasjoner</span><span class="sxs-lookup"><span data-stu-id="31bc0-129">Define warehouse locations</span></span>
1. <span data-ttu-id="31bc0-130">Velg **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="31bc0-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="31bc0-131">Velg **Lokasjonsveiviser**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="31bc0-132">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-132">Select **Next**.</span></span>
4. <span data-ttu-id="31bc0-133">Fjern merkingen av alternativet **Utleveringsporter**</span><span class="sxs-lookup"><span data-stu-id="31bc0-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="31bc0-134">Fjern merkingen av alternativet **Bulklokasjoner**</span><span class="sxs-lookup"><span data-stu-id="31bc0-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="31bc0-135">Velg **Neste** til du kommer til alternativet for å velge **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="31bc0-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="31bc0-136">Close the page.</span></span>
8. <span data-ttu-id="31bc0-137">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="31bc0-137">Refresh the page.</span></span>

