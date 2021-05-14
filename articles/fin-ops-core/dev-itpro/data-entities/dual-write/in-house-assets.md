---
title: Interne aktiva for betjening
description: Dette emnet beskriver hvordan du kan bruke Microsoft Dynamics 365 Field Service til å vedlikeholde både kundeaktiva og interne aktiva.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941420"
---
# <a name="in-house-assets-for-servicing"></a>Interne aktiva for betjening

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service er utviklet for å betjene kundeeiendeler. Aktivakontroll for Dynamics 365 Supply Chain Management er utformet for vedlikehold av interne anleggsmidler. Ved hjelp av integrering av disse to appene kan du bruke Field Service til å vedlikeholde både kunde- og interne aktiva. Du kan også klassifisere anleggsmidlene basert på arbeidssted eller hierarki, og spore vedlikehold på et detaljert nivå.

Hvis du vil ha mer informasjon, se [Integrere Dynamics 365 Field Service og Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Maler

Interne aktiva inkluderer en samling tabelltilordninger for viktige områder som fungerer sammen under datasamhandling, som vist i følgende tabell.

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]