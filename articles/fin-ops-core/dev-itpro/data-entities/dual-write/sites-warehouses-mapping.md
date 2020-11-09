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
# <a name="integrated-sites-and-warehouses"></a>Integrerte områder og lagre

[!include [banner](../../includes/banner.md)]



Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations-apper og Common Data Service. Driftssteder og -lagre er vanlige begreper i et Supply Chain Management-program. De brukes til å modellere forsyningskjeden til firmaet.

## <a name="templates"></a>Maler

Med integrasjonen med Common Data Service er disse begrepene og all relatert informasjon tilgjengelige i Common Data Service ved bruk av enhetene for områder og datalagre i tabellen nedenfor.

Finance and Operations-apper | Andre Dynamics 365-apper | Beskrivelse
--------------------------|---------------------------|---
Siter | msdyn_operationalsites | 
Lagre | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

