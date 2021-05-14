---
title: Interne aktiva for betjening
description: Dette emnet beskriver hvordan du kan bruke Microsoft Dynamics 365 Field Service til å vedlikeholde både kundeaktiva og interne aktiva.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941420"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="8efaf-103">Interne aktiva for betjening</span><span class="sxs-lookup"><span data-stu-id="8efaf-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="8efaf-104">Microsoft Dynamics 365 Field Service er utviklet for å betjene kundeeiendeler.</span><span class="sxs-lookup"><span data-stu-id="8efaf-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="8efaf-105">Aktivakontroll for Dynamics 365 Supply Chain Management er utformet for vedlikehold av interne anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="8efaf-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="8efaf-106">Ved hjelp av integrering av disse to appene kan du bruke Field Service til å vedlikeholde både kunde- og interne aktiva.</span><span class="sxs-lookup"><span data-stu-id="8efaf-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="8efaf-107">Du kan også klassifisere anleggsmidlene basert på arbeidssted eller hierarki, og spore vedlikehold på et detaljert nivå.</span><span class="sxs-lookup"><span data-stu-id="8efaf-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="8efaf-108">Hvis du vil ha mer informasjon, se [Integrere Dynamics 365 Field Service og Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="8efaf-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="8efaf-109">Maler</span><span class="sxs-lookup"><span data-stu-id="8efaf-109">Templates</span></span>

<span data-ttu-id="8efaf-110">Interne aktiva inkluderer en samling tabelltilordninger for viktige områder som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="8efaf-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="8efaf-111">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="8efaf-111">Finance and Operations apps</span></span> | <span data-ttu-id="8efaf-112">Modelldrevne apper i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="8efaf-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="8efaf-113">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8efaf-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="8efaf-114">Aktivabehandling, livsløpsmodeller for aktiva</span><span class="sxs-lookup"><span data-stu-id="8efaf-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="8efaf-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="8efaf-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="8efaf-116">Aktivabehandling, livsløpstilstander for aktiva</span><span class="sxs-lookup"><span data-stu-id="8efaf-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="8efaf-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="8efaf-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="8efaf-118">Aktivabehandling, aktiva</span><span class="sxs-lookup"><span data-stu-id="8efaf-118">Asset management assets</span></span> | <span data-ttu-id="8efaf-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="8efaf-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="8efaf-120">Aktivabehandling, aktivatyper</span><span class="sxs-lookup"><span data-stu-id="8efaf-120">Asset management asset types</span></span> | <span data-ttu-id="8efaf-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="8efaf-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="8efaf-122">Aktivabehandling, livsløpsmodeller for arbeidssted</span><span class="sxs-lookup"><span data-stu-id="8efaf-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="8efaf-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="8efaf-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="8efaf-124">Aktivabehandling, livsløpstilstander for arbeidssted</span><span class="sxs-lookup"><span data-stu-id="8efaf-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="8efaf-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="8efaf-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="8efaf-126">Aktivabehandling, arbeidssteder</span><span class="sxs-lookup"><span data-stu-id="8efaf-126">Asset management functional locations</span></span> | <span data-ttu-id="8efaf-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="8efaf-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="8efaf-128">Aktivabehandling, arbeidsstedstyper</span><span class="sxs-lookup"><span data-stu-id="8efaf-128">Asset management functional location types</span></span> | <span data-ttu-id="8efaf-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="8efaf-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="8efaf-130">Aktivabehandling, produsenter</span><span class="sxs-lookup"><span data-stu-id="8efaf-130">Asset management manufacturers</span></span> | <span data-ttu-id="8efaf-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="8efaf-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="8efaf-132">Aktivabehandling, modeller</span><span class="sxs-lookup"><span data-stu-id="8efaf-132">Asset management models</span></span> | <span data-ttu-id="8efaf-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="8efaf-133">msdyn\_models</span></span> | |
| <span data-ttu-id="8efaf-134">Aktivabehandling, garanti</span><span class="sxs-lookup"><span data-stu-id="8efaf-134">Asset management warranty</span></span> | <span data-ttu-id="8efaf-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="8efaf-135">msdyn\_warranties</span></span> | |

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]