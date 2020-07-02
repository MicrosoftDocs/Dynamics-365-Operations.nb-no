---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
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
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443924"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="9850d-103">Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9850d-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9850d-104">Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9850d-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="9850d-105">En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.</span><span class="sxs-lookup"><span data-stu-id="9850d-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="9850d-106">En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="9850d-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="9850d-107">Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.</span><span class="sxs-lookup"><span data-stu-id="9850d-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="9850d-108">Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="9850d-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="9850d-109">Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="9850d-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a><span data-ttu-id="9850d-110">Fjernede eller avskrevne funksjoner i Commerce 10.0.11</span><span class="sxs-lookup"><span data-stu-id="9850d-110">Features removed or deprecated in the Commerce 10.0.11 release</span></span>
### <a name="data-action-hooks"></a><span data-ttu-id="9850d-111">Datahandlingsbindinger</span><span class="sxs-lookup"><span data-stu-id="9850d-111">Data action hooks</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9850d-112">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="9850d-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9850d-113">Funksjonen for datahandlingsbindinger er avskrevet på grunn av ytelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="9850d-113">The data action hooks feature has been deprecated due to performance issues.</span></span> |
| <span data-ttu-id="9850d-114">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="9850d-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9850d-115">Det anbefales å i stedet bruke [overstyringer for datahandling](../e-commerce-extensibility/data-action-overrides.md) til å endre forretningslogikken i datahandlingslaget.</span><span class="sxs-lookup"><span data-stu-id="9850d-115">It is recommended to instead use [data action overrides](../e-commerce-extensibility/data-action-overrides.md) to modify business logic in the data action layer.</span></span>|
| <span data-ttu-id="9850d-116">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="9850d-116">**Product areas affected**</span></span>         | <span data-ttu-id="9850d-117">Datahandlinger for utvidelsesmuligheter for e-handel</span><span class="sxs-lookup"><span data-stu-id="9850d-117">E-Commerce extensibility data actions</span></span> |
| <span data-ttu-id="9850d-118">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="9850d-118">**Deployment option**</span></span>              | <span data-ttu-id="9850d-119">Alle</span><span class="sxs-lookup"><span data-stu-id="9850d-119">All</span></span> |
| <span data-ttu-id="9850d-120">**Status**</span><span class="sxs-lookup"><span data-stu-id="9850d-120">**Status**</span></span>                         | <span data-ttu-id="9850d-121">Avskrevet: Fra og med versjon 10.0.11</span><span class="sxs-lookup"><span data-stu-id="9850d-121">Deprecated: As of release 10.0.11</span></span> |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="9850d-122">Fjernede eller avskrevne funksjoner i Commerce 10.0.10</span><span class="sxs-lookup"><span data-stu-id="9850d-122">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="9850d-123">POS-operasjon 803 - Plukk og mottak</span><span class="sxs-lookup"><span data-stu-id="9850d-123">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9850d-124">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="9850d-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9850d-125">Plukk- og mottaksoperasjoner avskrives på grunn av ny utforming av den nye operasjonen.</span><span class="sxs-lookup"><span data-stu-id="9850d-125">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="9850d-126">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="9850d-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9850d-127">Ja.</span><span class="sxs-lookup"><span data-stu-id="9850d-127">Yes.</span></span> <span data-ttu-id="9850d-128">Den er erstattet av to nye POS-operasjoner: innkommende operasjon (804) og utgående operasjon (805).</span><span class="sxs-lookup"><span data-stu-id="9850d-128">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="9850d-129">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="9850d-129">**Product areas affected**</span></span>         | <span data-ttu-id="9850d-130">Salgsstedsapplikasjon</span><span class="sxs-lookup"><span data-stu-id="9850d-130">Point of sale (POS) application</span></span> |
| <span data-ttu-id="9850d-131">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="9850d-131">**Deployment option**</span></span>              | <span data-ttu-id="9850d-132">Alle</span><span class="sxs-lookup"><span data-stu-id="9850d-132">All</span></span> |
| <span data-ttu-id="9850d-133">**Status**</span><span class="sxs-lookup"><span data-stu-id="9850d-133">**Status**</span></span>                         | <span data-ttu-id="9850d-134">Avskrevet: Etter utgivelse 10.0.10 vil ikke plukk- og mottaksoperasjonen lenger motta nye funksjonsoppdateringer.</span><span class="sxs-lookup"><span data-stu-id="9850d-134">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="9850d-135">Bare kritiske feilrettinger vil bli utført for denne operasjonen i fremtidige versjoner.</span><span class="sxs-lookup"><span data-stu-id="9850d-135">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="9850d-136">Alle kunder oppfordres til å flytte til nye [innkommende operasjoner](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) og [utgående operasjoner](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), som vil fortsette å være en del av vårt langsiktig produktveikart.</span><span class="sxs-lookup"><span data-stu-id="9850d-136">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="9850d-137">Fjernede eller avskrevne funksjoner i Commerce 10.0.7</span><span class="sxs-lookup"><span data-stu-id="9850d-137">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="9850d-138">API-er for Commerce GetProductAvailabilities og GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="9850d-138">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9850d-139">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="9850d-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9850d-140">Nye optimaliserte API-er er opprettet for å erstatte API-ene GetProductAvailabilities og GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="9850d-140">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="9850d-141">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="9850d-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9850d-142">Ja: Den erstattes av APIene GetEstimatedAvailability og GetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="9850d-142">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="9850d-143">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="9850d-143">**Product areas affected**</span></span>         | <span data-ttu-id="9850d-144">SDK for e-handelsprogram</span><span class="sxs-lookup"><span data-stu-id="9850d-144">e-Commerce application SDK</span></span> |
| <span data-ttu-id="9850d-145">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="9850d-145">**Deployment option**</span></span>              | <span data-ttu-id="9850d-146">Alle</span><span class="sxs-lookup"><span data-stu-id="9850d-146">All</span></span> |
| <span data-ttu-id="9850d-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="9850d-147">**Status**</span></span>                         | <span data-ttu-id="9850d-148">Avskrevet: Etter versjon 10.0.7 vil det ikke lenger gjøres tekniske investeringer for GetProductAvailabilities og GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="9850d-148">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="9850d-149">Organisasjoner som bruker disse APIene i sine e-handelsdistribusjoner, bør konvertere dem til de nye GetEstimatedAvailability og GetEstimatedProductWarehouseAvailability-APIene og aktivere [funksjonen for beregning av optimalisert produkttilgjengelighet](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="9850d-149">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="9850d-150">Tidligere kunngjøringer om fjernede eller avskrevne funksjoner</span><span class="sxs-lookup"><span data-stu-id="9850d-150">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="9850d-151">Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="9850d-151">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
