---
title: Integrerte områder og lagre
description: Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations-apper og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d5c2030160f6025c9de63b2c29215364f5f87e6f
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997630"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="592a2-103">Integrerte områder og lagre</span><span class="sxs-lookup"><span data-stu-id="592a2-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="592a2-104">Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="592a2-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="592a2-105">Driftssteder og -lagre er vanlige begreper i et Supply Chain Management-program.</span><span class="sxs-lookup"><span data-stu-id="592a2-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="592a2-106">De brukes til å modellere forsyningskjeden til firmaet.</span><span class="sxs-lookup"><span data-stu-id="592a2-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="592a2-107">Maler</span><span class="sxs-lookup"><span data-stu-id="592a2-107">Templates</span></span>

<span data-ttu-id="592a2-108">Med integrasjonen med Common Data Service er disse begrepene og all relatert informasjon tilgjengelige i Common Data Service ved bruk av enhetene for områder og datalagre i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="592a2-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="592a2-109">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="592a2-109">Finance and Operations apps</span></span> | <span data-ttu-id="592a2-110">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="592a2-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="592a2-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="592a2-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="592a2-112">Siter</span><span class="sxs-lookup"><span data-stu-id="592a2-112">Sites</span></span> | <span data-ttu-id="592a2-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="592a2-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="592a2-114">Lagre</span><span class="sxs-lookup"><span data-stu-id="592a2-114">Warehouses</span></span> | <span data-ttu-id="592a2-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="592a2-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

