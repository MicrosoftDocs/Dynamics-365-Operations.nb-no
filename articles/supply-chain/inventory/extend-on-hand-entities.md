---
title: Utvide dataenheter for lagerbeholdning
description: Dette emnet inneholder et eksempel som viser hvordan du legger til utvidede felt i INVENTORSITEONHANDENTITY- og INVENTWAREHOUSEONHANDENTITY-visningene, slik at egenskapene til lagerbeholdningsdataenhetene kan fungere med tilleggene.
author: sherry-zheng
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7863f37e66727e2e80ea8c8b013ee49930e7c684
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829914"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="789ec-103">Utvide dataenheter for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="789ec-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="789ec-104">Microsoft Dynamics 365 Supply Chain Management tilbyr [utvidelsesfunksjoner](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) som lar deg [legge til felt i tabeller ved hjelp av utvidelser](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span><span class="sxs-lookup"><span data-stu-id="789ec-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span></span> <span data-ttu-id="789ec-105">Dette emnet inneholder et eksempel som viser hvordan du legger til utvidede felt i `INVENTORSITEONHANDENTITY`- og `INVENTWAREHOUSEONHANDENTITY`-visningene, slik at egenskapene til lagerbeholdningsdataenhetene kan fungere med tilleggene.</span><span class="sxs-lookup"><span data-stu-id="789ec-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="789ec-106">Hvis du vil ha mer informasjon om dataenheter, kan du se [Oversikt over databehandling](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="789ec-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="789ec-107">Her er en liste over noen av lagerbeholdningsdataenhetene:</span><span class="sxs-lookup"><span data-stu-id="789ec-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="789ec-108">Lagerbeholdning etter område</span><span class="sxs-lookup"><span data-stu-id="789ec-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="789ec-109">Lagerbeholdning etter område V2</span><span class="sxs-lookup"><span data-stu-id="789ec-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="789ec-110">Lagerbeholdning etter lager</span><span class="sxs-lookup"><span data-stu-id="789ec-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="789ec-111">Lagerbeholdning etter lager v2</span><span class="sxs-lookup"><span data-stu-id="789ec-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="789ec-112">Når du har lagt til felt i tabeller som brukes av `inventSiteOnHandView`-visningen, må du synkronisere motoren, slik at utvidelsene blir gjenkjent på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="789ec-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="789ec-113">Utvid `InventSiteOnHandView`-visningen ved å legge til utvidelsesfeltet.</span><span class="sxs-lookup"><span data-stu-id="789ec-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="789ec-114">Utvid `InventSiteOnHandAggregatedView`-visningen med utvidelsesfeltene.</span><span class="sxs-lookup"><span data-stu-id="789ec-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="789ec-115">Utvid `InventSiteOnHandAggregatedViewBuilder` viewBuilder-klassen ved å endre `getExtensionFields()`-metoden.</span><span class="sxs-lookup"><span data-stu-id="789ec-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="789ec-116">På denne måten tilordner du gamle visningsfelt til nye visningsfelt når viewBuilder-synkronisering kjøres.</span><span class="sxs-lookup"><span data-stu-id="789ec-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="789ec-117">Du har for eksempel lagt til følgende fire felt i `InventTable`-tabellen via utvidelse:</span><span class="sxs-lookup"><span data-stu-id="789ec-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="789ec-118">Egendefinert felt 1</span><span class="sxs-lookup"><span data-stu-id="789ec-118">Custom field 1</span></span>
- <span data-ttu-id="789ec-119">Egendefinert felt 2</span><span class="sxs-lookup"><span data-stu-id="789ec-119">Custom field 2</span></span>
- <span data-ttu-id="789ec-120">Egendefinert felt 3</span><span class="sxs-lookup"><span data-stu-id="789ec-120">Custom field 3</span></span>
- <span data-ttu-id="789ec-121">Egendefinert felt 4</span><span class="sxs-lookup"><span data-stu-id="789ec-121">Custom field 4</span></span>

<span data-ttu-id="789ec-122">I dette tilfellet må du endre `getExtensionFields()`-metoden på følgende måte.</span><span class="sxs-lookup"><span data-stu-id="789ec-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="789ec-123">Når du har fullført disse trinnene, kan du utvide lagerbeholdningen etter område og lagerbeholdningen etter lagerdataenheter ved å legge til de nye feltene.</span><span class="sxs-lookup"><span data-stu-id="789ec-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="789ec-124">På denne måten sikrer du at de utvidede feltene gjenkjennes og tas med under dataoverføring som bruker disse dataenhetene.</span><span class="sxs-lookup"><span data-stu-id="789ec-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]