---
title: Interne aktiva for betjening
description: Denne artikkelen beskriver hvordan du kan bruke Microsoft Dynamics 365 Field Service til å vedlikeholde både kundeaktiva og interne aktiva.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289258"
---
# <a name="in-house-assets-for-servicing"></a>Interne aktiva for betjening

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service er utviklet for å betjene kundeeiendeler. Aktivakontroll for Dynamics 365 Supply Chain Management er utformet for vedlikehold av interne anleggsmidler. Ved hjelp av integrering av disse to appene kan du bruke Field Service til å vedlikeholde både kunde- og interne aktiva. Du kan også klassifisere anleggsmidlene basert på arbeidssted eller hierarki, og spore vedlikehold på et detaljert nivå.

Hvis du vil ha mer informasjon, se [Integrere Dynamics 365 Field Service og Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Maler

Interne aktiva inkluderer en samling tabelltilordninger for viktige områder som fungerer sammen under datasamhandling, som vist i følgende tabell.

| Finance and Operations-apper | Kundeengasjementsapper | beskrivelse |
|-----------------------------|-----------------------------------|-------------|
[Aktivabehandling, livsløpsmodeller for aktiva](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Aktivabehandling, livsløpstilstander for aktiva](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Aktivabehandling, aktivatyper](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Aktivabehandling, aktiva](mapping-reference.md#125) | msdyn_customerassets | |
[Aktivabehandling, livsløpsmodeller for arbeidssted](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Aktivabehandling, livsløpstilstander for arbeidssted](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Aktivabehandling, arbeidsstedstyper](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Aktivabehandling, arbeidssteder](mapping-reference.md#136) | msdyn_functionallocations | |
[Aktivabehandling, produsenter](mapping-reference.md#153) | msdyn_manufacturers | |
[Aktivabehandling, modeller](mapping-reference.md#154) | msdyn_models | |
[Aktivabehandling, garanti](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
