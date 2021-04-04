---
title: Integrerte områder og lagre
description: Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations-apper og Dataverse.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560367"
---
# <a name="integrated-sites-and-warehouses"></a>Integrerte områder og lagre

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emnet beskriver integreringen av område- og lagerdata mellom Finance and Operations-apper og Dataverse. Driftssteder og -lagre er vanlige begreper i et Supply Chain Management-program. De brukes til å modellere forsyningskjeden til firmaet.

## <a name="templates"></a>Maler

Med integrasjonen med Dataverse er disse begrepene og all relatert informasjon tilgjengelige i Dataverse ved bruk av datatabellene for områder og lagre i tabellen nedenfor.

Finance and Operations-apper | Andre Dynamics 365-apper | beskrivelse
--------------------------|---------------------------|---
Siter | msdyn_operationalsites | 
Lagre | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]