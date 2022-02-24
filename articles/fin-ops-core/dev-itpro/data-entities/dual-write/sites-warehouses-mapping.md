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

