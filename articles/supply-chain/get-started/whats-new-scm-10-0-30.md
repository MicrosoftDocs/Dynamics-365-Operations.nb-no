---
title: Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.30 (november 2022)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.30.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 477b27bf77d2a3ef91a5c2d39f2dfb06d8ad4e59
ms.sourcegitcommit: 562ea02e1f7409f18ee1cc4750a838bff4381e91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429130"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10030-november-2022"></a>Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.30 (november 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, forhåndsversjon 10.0.30. Denne versjonen har et build-nummer 10.0.1362, og er tilgjengelig på følgende tidsplan:

- **Forhåndsversjon:** september 2022
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** oktober 2022
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** november 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Denne artikkelen kan være oppdatert for å inkludere funksjoner som ble lagt til i builden etter at denne artikkelen opprinnelig ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Produksjon | [Overvåk utstyr med Sensordataintelligens](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Startside for sensordataintelligens](../sensor-data-intelligence/sdi-home-page.md) | Funksjonsbehandling:<br>*(Forhåndsversjon) Sensordataintelligens* |
| Lagerstyring | Omveier med flere nivåer for mobilappen Warehouse Management <!-- KFM: Add link when RP updates --> | [Konfigurere omveier for trinn i menyelementer for mobilenheter](../warehousing/warehouse-app-detours.md) | Funksjonsbehandling:<br>*Omveier med flere nivåer for mobilappen Warehouse Management* |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt).

Hvis du vil slå noen av disse funksjonene på eller av, må du gjøre dette i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Produksjonskontroll | Side for beholdningsinformasjon i produksjonsordrer som skal frigis | Legger til en kolonne for lagerbeholdningsantallet for linjevaren i linjedelen på siden **Produksjonsordrer som skal frigis**. |
| Transportstyring | Tildel forsendelser til relaterte rutesegmenter | Ved hjelp av denne funksjonen kan systemet beregne forsendelsesfraktkostnader mer nøyaktig, inkludert for belastninger med flere forsendelser som leveres til forskjellige segmentmål langs en enkelt rute. Den tilordner hver forsendelse til det best egnede rutesegmentet basert på måladressene til forsendelsen og segmentet. Funksjonen beregner deretter fraktkostnaden for hver forsendelse som en del av belastningens totale fraktkostnader, basert på forsendelsens relative vekt, volum, antall og reiseavstand. Denne funksjonen gjelder bare forsendelser som administreres ved hjelp av TMS-modulen (Transportstyring). |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Supply Chain Management 10.0.30 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.30 av Finance and Operations-apper (november 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md). <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av versjon 10.0.29, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 1 for 2022

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2022](/dynamics365-release-plan/2022wave2/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
