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
ms.openlocfilehash: ebc9c1fbb7c0738af13b2a16aafeeb03fa6aaed0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684011"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="652d8-103">Interne aktiva for vedlikehold</span><span class="sxs-lookup"><span data-stu-id="652d8-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="652d8-104">Microsoft Dynamics 365 Field Service er utviklet for å betjene kundeeiendeler.</span><span class="sxs-lookup"><span data-stu-id="652d8-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="652d8-105">Aktivakontroll for Dynamics 365 Supply Chain Management er utformet for vedlikehold av interne anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="652d8-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="652d8-106">Ved hjelp av integrering av disse to appene kan du bruke Field Service til å vedlikeholde både kunde- og interne aktiva.</span><span class="sxs-lookup"><span data-stu-id="652d8-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="652d8-107">Du kan også klassifisere anleggsmidlene basert på arbeidssted eller hierarki, og spore vedlikehold på et detaljert nivå.</span><span class="sxs-lookup"><span data-stu-id="652d8-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="652d8-108">Hvis du vil ha mer informasjon, se [Integrere Dynamics 365 Field Service og Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="652d8-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="652d8-109">Maler</span><span class="sxs-lookup"><span data-stu-id="652d8-109">Templates</span></span>

<span data-ttu-id="652d8-110">Interne aktiva inkluderer en samling tabelltilordninger for viktige områder som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="652d8-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="652d8-111">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="652d8-111">Finance and Operations apps</span></span> | <span data-ttu-id="652d8-112">Modelldrevne apper i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="652d8-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="652d8-113">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="652d8-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="652d8-114">Aktivabehandling, livsløpsmodeller for aktiva</span><span class="sxs-lookup"><span data-stu-id="652d8-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="652d8-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="652d8-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="652d8-116">Aktivabehandling, livsløpstilstander for aktiva</span><span class="sxs-lookup"><span data-stu-id="652d8-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="652d8-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="652d8-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="652d8-118">Aktivabehandling, aktiva</span><span class="sxs-lookup"><span data-stu-id="652d8-118">Asset management assets</span></span> | <span data-ttu-id="652d8-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="652d8-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="652d8-120">Aktivabehandling, aktivatyper</span><span class="sxs-lookup"><span data-stu-id="652d8-120">Asset management asset types</span></span> | <span data-ttu-id="652d8-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="652d8-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="652d8-122">Aktivabehandling, livsløpsmodeller for arbeidssted</span><span class="sxs-lookup"><span data-stu-id="652d8-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="652d8-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="652d8-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="652d8-124">Aktivabehandling, livsløpstilstander for arbeidssted</span><span class="sxs-lookup"><span data-stu-id="652d8-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="652d8-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="652d8-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="652d8-126">Aktivabehandling, arbeidssteder</span><span class="sxs-lookup"><span data-stu-id="652d8-126">Asset management functional locations</span></span> | <span data-ttu-id="652d8-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="652d8-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="652d8-128">Aktivabehandling, arbeidsstedstyper</span><span class="sxs-lookup"><span data-stu-id="652d8-128">Asset management functional location types</span></span> | <span data-ttu-id="652d8-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="652d8-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="652d8-130">Aktivabehandling, produsenter</span><span class="sxs-lookup"><span data-stu-id="652d8-130">Asset management manufacturers</span></span> | <span data-ttu-id="652d8-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="652d8-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="652d8-132">Aktivabehandling, modeller</span><span class="sxs-lookup"><span data-stu-id="652d8-132">Asset management models</span></span> | <span data-ttu-id="652d8-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="652d8-133">msdyn\_models</span></span> | |
| <span data-ttu-id="652d8-134">Aktivabehandling, garanti</span><span class="sxs-lookup"><span data-stu-id="652d8-134">Asset management warranty</span></span> | <span data-ttu-id="652d8-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="652d8-135">msdyn\_warranties</span></span> | |

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
