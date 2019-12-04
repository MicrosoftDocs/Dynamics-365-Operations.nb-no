---
title: Integrerte områder og lagre
description: Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations og Common Data Service.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771000"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="a9cc3-103">Integrerte områder og lagre</span><span class="sxs-lookup"><span data-stu-id="a9cc3-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9cc3-104">Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="a9cc3-105">Driftssteder og -lagre er vanlige begreper i et Supply Chain Management-program.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="a9cc3-106">De brukes til å modellere forsyningskjeden til firmaet.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="a9cc3-107">Maler</span><span class="sxs-lookup"><span data-stu-id="a9cc3-107">Templates</span></span>

<span data-ttu-id="a9cc3-108">Med integrasjonen med Common Data Service er disse begrepene og all relatert informasjon tilgjengelige i Common Data Service ved bruk av enhetene for områder og datalagre i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="a9cc3-109">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="a9cc3-109">Finance and Operations apps</span></span> | <span data-ttu-id="a9cc3-110">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="a9cc3-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="a9cc3-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a9cc3-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="a9cc3-112">Siter</span><span class="sxs-lookup"><span data-stu-id="a9cc3-112">Sites</span></span> | <span data-ttu-id="a9cc3-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="a9cc3-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="a9cc3-114">Lagre</span><span class="sxs-lookup"><span data-stu-id="a9cc3-114">Warehouses</span></span> | <span data-ttu-id="a9cc3-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="a9cc3-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

