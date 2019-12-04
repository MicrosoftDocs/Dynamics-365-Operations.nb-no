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
# <a name="integrated-sites-and-warehouses"></a>Integrerte områder og lagre

[!include [banner](../includes/banner.md)]

Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations og Common Data Service. Driftssteder og -lagre er vanlige begreper i et Supply Chain Management-program. De brukes til å modellere forsyningskjeden til firmaet.

## <a name="templates"></a>Maler

Med integrasjonen med Common Data Service er disse begrepene og all relatert informasjon tilgjengelige i Common Data Service ved bruk av enhetene for områder og datalagre i tabellen nedenfor.

Finance and Operations-apper | Andre Dynamics 365-apper | Beskrivelse
--------------------------|---------------------------|---
Siter | msdyn_operationalsites | 
Lagre | msdyn_warehouses | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

