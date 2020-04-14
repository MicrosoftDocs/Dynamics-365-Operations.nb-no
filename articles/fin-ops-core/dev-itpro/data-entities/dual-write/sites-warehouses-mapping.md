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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 1b9181211bbb65cdfc46e63f3cee0e9f5bc9f6a4
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173068"
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

