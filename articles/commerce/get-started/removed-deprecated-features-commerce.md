---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335282"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="46254-103">Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="46254-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46254-104">Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="46254-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="46254-105">En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.</span><span class="sxs-lookup"><span data-stu-id="46254-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="46254-106">En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="46254-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="46254-107">Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.</span><span class="sxs-lookup"><span data-stu-id="46254-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="46254-108">Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="46254-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="46254-109">Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="46254-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="46254-110">Fjernede eller avskrevne funksjoner i Commerce 10.0.10</span><span class="sxs-lookup"><span data-stu-id="46254-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="46254-111">POS-operasjon 803 - Plukk og mottak</span><span class="sxs-lookup"><span data-stu-id="46254-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="46254-112">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="46254-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="46254-113">Plukk- og mottaksoperasjoner avskrives på grunn av ny utforming av den nye operasjonen.</span><span class="sxs-lookup"><span data-stu-id="46254-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="46254-114">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="46254-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="46254-115">Ja.</span><span class="sxs-lookup"><span data-stu-id="46254-115">Yes.</span></span> <span data-ttu-id="46254-116">Den er erstattet av to nye POS-operasjoner: innkommende operasjon (804) og utgående operasjon (805).</span><span class="sxs-lookup"><span data-stu-id="46254-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="46254-117">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="46254-117">**Product areas affected**</span></span>         | <span data-ttu-id="46254-118">Salgsstedsapplikasjon</span><span class="sxs-lookup"><span data-stu-id="46254-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="46254-119">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="46254-119">**Deployment option**</span></span>              | <span data-ttu-id="46254-120">Alle</span><span class="sxs-lookup"><span data-stu-id="46254-120">All</span></span> |
| <span data-ttu-id="46254-121">**Status**</span><span class="sxs-lookup"><span data-stu-id="46254-121">**Status**</span></span>                         | <span data-ttu-id="46254-122">Avskrevet: Etter utgivelse 10.0.10 vil ikke plukk- og mottaksoperasjonen lenger motta nye funksjonsoppdateringer.</span><span class="sxs-lookup"><span data-stu-id="46254-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="46254-123">Bare kritiske feilrettinger vil bli utført for denne operasjonen i fremtidige versjoner.</span><span class="sxs-lookup"><span data-stu-id="46254-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="46254-124">Alle kunder oppfordres til å flytte til nye [innkommende operasjoner](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) og [utgående operasjoner](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), som vil fortsette å være en del av vårt langsiktig produktveikart.</span><span class="sxs-lookup"><span data-stu-id="46254-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="46254-125">Fjernede eller avskrevne funksjoner i Commerce 10.0.7</span><span class="sxs-lookup"><span data-stu-id="46254-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="46254-126">API-er for Commerce GetProductAvailabilities og GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="46254-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="46254-127">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="46254-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="46254-128">Nye optimaliserte API-er er opprettet for å erstatte API-ene GetProductAvailabilities og GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="46254-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="46254-129">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="46254-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="46254-130">Ja: Den erstattes av APIene GetEstimatedAvailability og GetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="46254-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="46254-131">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="46254-131">**Product areas affected**</span></span>         | <span data-ttu-id="46254-132">SDK for e-handelsprogram</span><span class="sxs-lookup"><span data-stu-id="46254-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="46254-133">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="46254-133">**Deployment option**</span></span>              | <span data-ttu-id="46254-134">Alle</span><span class="sxs-lookup"><span data-stu-id="46254-134">All</span></span> |
| <span data-ttu-id="46254-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="46254-135">**Status**</span></span>                         | <span data-ttu-id="46254-136">Avskrevet: Etter versjon 10.0.7 vil det ikke lenger gjøres tekniske investeringer for GetProductAvailabilities og GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="46254-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="46254-137">Organisasjoner som bruker disse APIene i sine e-handelsdistribusjoner, bør konvertere dem til de nye GetEstimatedAvailability og GetEstimatedProductWarehouseAvailability-APIene og aktivere [funksjonen for beregning av optimalisert produkttilgjengelighet](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="46254-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="46254-138">Tidligere kunngjøringer om fjernede eller avskrevne funksjoner</span><span class="sxs-lookup"><span data-stu-id="46254-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="46254-139">Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="46254-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
