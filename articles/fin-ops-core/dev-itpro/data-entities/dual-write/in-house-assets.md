---
title: Interne aktiva for vedlikehold
description: Dette emnet beskriver hvordan du kan bruke Microsoft Dynamics 365 Field Service til å vedlikeholde både kunde- og interne aktiva.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0e87a3d645c19fab3bb0560ba5114d193e2d0be7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997176"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="a1547-103">Interne aktiva for vedlikehold</span><span class="sxs-lookup"><span data-stu-id="a1547-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a1547-104">Microsoft Dynamics 365 Field Service er utviklet for å betjene kundeeiendeler.</span><span class="sxs-lookup"><span data-stu-id="a1547-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="a1547-105">Aktivakontroll for Dynamics 365 Supply Chain Management er utformet for vedlikehold av interne anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="a1547-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="a1547-106">Ved hjelp av integrering av disse to appene kan du bruke Field Service til å vedlikeholde både kunde- og interne aktiva.</span><span class="sxs-lookup"><span data-stu-id="a1547-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="a1547-107">Du kan også klassifisere anleggsmidlene basert på arbeidssted eller hierarki, og spore vedlikehold på et detaljert nivå.</span><span class="sxs-lookup"><span data-stu-id="a1547-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="a1547-108">Hvis du vil ha mer informasjon, se [Integrere Dynamics 365 Field Service og Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="a1547-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="a1547-109">Maler</span><span class="sxs-lookup"><span data-stu-id="a1547-109">Templates</span></span>

<span data-ttu-id="a1547-110">Interne aktiva inkluderer en samling enhetstilordninger for viktige områder som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="a1547-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="a1547-111">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="a1547-111">Finance and Operations apps</span></span> | <span data-ttu-id="a1547-112">Modelldrevne apper i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a1547-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="a1547-113">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a1547-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="a1547-114">Aktivabehandling, livsløpsmodeller for aktiva</span><span class="sxs-lookup"><span data-stu-id="a1547-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="a1547-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="a1547-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="a1547-116">Aktivabehandling, livsløpstilstander for aktiva</span><span class="sxs-lookup"><span data-stu-id="a1547-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="a1547-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="a1547-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="a1547-118">Aktivabehandling, aktiva</span><span class="sxs-lookup"><span data-stu-id="a1547-118">Asset management assets</span></span> | <span data-ttu-id="a1547-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="a1547-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="a1547-120">Aktivabehandling, aktivatyper</span><span class="sxs-lookup"><span data-stu-id="a1547-120">Asset management asset types</span></span> | <span data-ttu-id="a1547-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="a1547-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="a1547-122">Aktivabehandling, livsløpsmodeller for arbeidssted</span><span class="sxs-lookup"><span data-stu-id="a1547-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="a1547-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="a1547-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="a1547-124">Aktivabehandling, livsløpstilstander for arbeidssted</span><span class="sxs-lookup"><span data-stu-id="a1547-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="a1547-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="a1547-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="a1547-126">Aktivabehandling, arbeidssteder</span><span class="sxs-lookup"><span data-stu-id="a1547-126">Asset management functional locations</span></span> | <span data-ttu-id="a1547-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="a1547-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="a1547-128">Aktivabehandling, arbeidsstedstyper</span><span class="sxs-lookup"><span data-stu-id="a1547-128">Asset management functional location types</span></span> | <span data-ttu-id="a1547-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="a1547-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="a1547-130">Aktivabehandling, produsenter</span><span class="sxs-lookup"><span data-stu-id="a1547-130">Asset management manufacturers</span></span> | <span data-ttu-id="a1547-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="a1547-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="a1547-132">Aktivabehandling, modeller</span><span class="sxs-lookup"><span data-stu-id="a1547-132">Asset management models</span></span> | <span data-ttu-id="a1547-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="a1547-133">msdyn\_models</span></span> | |
| <span data-ttu-id="a1547-134">Aktivabehandling, garanti</span><span class="sxs-lookup"><span data-stu-id="a1547-134">Asset management warranty</span></span> | <span data-ttu-id="a1547-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="a1547-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
