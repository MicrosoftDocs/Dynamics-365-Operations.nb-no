---
title: Integrerte områder og lagre
description: Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations-apper og Dataverse.
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
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679326"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="e0e05-103">Integrerte områder og lagre</span><span class="sxs-lookup"><span data-stu-id="e0e05-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="e0e05-104">Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e0e05-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="e0e05-105">Driftssteder og -lagre er vanlige begreper i et Supply Chain Management-program.</span><span class="sxs-lookup"><span data-stu-id="e0e05-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="e0e05-106">De brukes til å modellere forsyningskjeden til firmaet.</span><span class="sxs-lookup"><span data-stu-id="e0e05-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="e0e05-107">Maler</span><span class="sxs-lookup"><span data-stu-id="e0e05-107">Templates</span></span>

<span data-ttu-id="e0e05-108">Med integrasjonen med Dataverse er disse begrepene og all relatert informasjon tilgjengelige i Dataverse ved bruk av datatabellene for områder og lagre i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e0e05-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="e0e05-109">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="e0e05-109">Finance and Operations apps</span></span> | <span data-ttu-id="e0e05-110">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="e0e05-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="e0e05-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e0e05-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="e0e05-112">Siter</span><span class="sxs-lookup"><span data-stu-id="e0e05-112">Sites</span></span> | <span data-ttu-id="e0e05-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="e0e05-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="e0e05-114">Lagre</span><span class="sxs-lookup"><span data-stu-id="e0e05-114">Warehouses</span></span> | <span data-ttu-id="e0e05-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="e0e05-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

