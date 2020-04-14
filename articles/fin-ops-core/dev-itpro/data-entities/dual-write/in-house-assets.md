---
title: Interne aktiva for vedlikehold
description: Dette emnet beskriver hvordan du kan bruke Microsoft Dynamics 365 Field Service til å vedlikeholde både kunde- og interne aktiva.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 1e423199d0639db5e403e280880036b590149095
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172952"
---
# <a name="in-house-assets-for-servicing"></a>Interne aktiva for vedlikehold

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service er utviklet for å betjene kundeeiendeler. Aktivakontroll for Dynamics 365 Supply Chain Management er utformet for vedlikehold av interne anleggsmidler. Ved hjelp av integrering av disse to appene kan du bruke Field Service til å vedlikeholde både kunde- og interne aktiva. Du kan også klassifisere anleggsmidlene basert på arbeidssted eller hierarki, og spore vedlikehold på et detaljert nivå.

Hvis du vil ha mer informasjon, se [Integrere Dynamics 365 Field Service og Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Maler

Interne aktiva inkluderer en samling enhetstilordninger for viktige områder som fungerer sammen under datasamhandling, som vist i følgende tabell.

| Finance and Operations-apper | Modelldrevne apper i Dynamics 365 | beskrivelse |
|-----------------------------|-----------------------------------|-------------|
| Aktivabehandling, livsløpsmodeller for aktiva | msdyn\_assetlifecyclemodels | |
| Aktivabehandling, livsløpstilstander for aktiva | msdyn\_assetlifecyclestates | |
| Aktivabehandling, aktiva | msdyn\_customerassets | |
| Aktivabehandling, aktivatyper | msdyn\_customerassetcategories | |
| Aktivabehandling, livsløpsmodeller for arbeidssted | msdyn\_functionallocationlifecyclemodels | |
| Aktivabehandling, livsløpstilstander for arbeidssted | msdyn\_functionallocationlifecyclestates | |
| Aktivabehandling, arbeidssteder | msdyn\_functionallocations | |
| Aktivabehandling, arbeidsstedstyper | msdyn\_functionallocationtypes | |
| Aktivabehandling, produsenter | msdyn\_manufacturers | |
| Aktivabehandling, modeller | msdyn\_models | |
| Aktivabehandling, garanti | msdyn\_warranties | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
