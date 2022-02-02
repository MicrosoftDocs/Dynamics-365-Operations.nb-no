---
title: Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.24 (februar 2022)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.24.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d7dd3bbb0d1aa701757ad7fa525aba04fe9419c9
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986309"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.24 (februar 2022)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.24. Denne versjonen har et build-nummer 10.0.1084, og er tilgjengelig som følger:

- **Forhåndsversjon:** desember 2021
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** januar 2022
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** februar 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Dette emnet kan være oppdatert for å inkludere funksjoner som ble tatt med i builden etter at dette emnet ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Distribuert hybridtopologi | [Utvidede lagerkjøringsbelastninger på skalaenheter](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Skalaenheter for sky og kant for arbeidsbelastninger for lagerstyring](../cloud-edge/cloud-edge-workload-warehousing.md) | Aktivert som standard. |
| Planlegging | [Planleggingsoptimaliseringsstøtte for gjenbestillingsmargin og avgangsmargin](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Sikkerhetsmarginer](../master-planning/planning-optimization/safety-margins.md) | Aktivert som standard. |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt).

Hvis du vil slå noen av disse funksjonene på eller av, må du gjøre dette i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Produksjonskontroll | Kontroll av materialtilgjengelighet etter behov for produksjonsordrer | Denne funksjonen gjør det raskere å åpne siden **Produksjonsordrer som skal frigis**, som er tilgjengelig fra arbeidsområdet **Produksjonsstyring**. Uten denne funksjonen kontrollerer systemet automatisk om materialer er tilgjengelige for alle oppførte produksjonsordrer så snart du åpner siden, noe som kan ta lang tid hvis du har et stort antall ordrer. Når denne funksjonen er aktivert, gir systemet i stedet en verktøylinjeknapp, som du kan bruke til å starte materialkontrollen bare for valgte ordrer og ved behov. |
| Produksjonskontroll | (Forhåndsversjon) Registrer materialforbruk i grensesnittet for produksjonsutførelse (ikke-lager) | Ved hjelp av denne funksjonen kan arbeidere bruke grensesnittet for produksjonsutførelse til å registrere materialforbruk, partinumre og serienumre. Denne funksjonen støtter bare varer som ikke er aktivert til å bruke avanserte lagerprosesser (WMS). Støtte for WMS-aktiverte varer er planlagt for en fremtidig frigivelse.<p>Noen produsenter, spesielt de som finnes i prosessindustrien, må uttrykkelig registrere mengden material som forbrukes for hvert parti eller hver produksjonsordre. Arbeiderne kan for eksempel bruke en vekt til å veie mengden material som brukes når de arbeider. For å sikre full materialsporing må disse organisasjonene også registrere hvilke partinumre som ble forbrukt under produksjonen av hvert produkt. |
| Produksjonskontroll | Ferdigmelde arbeidsbelastning for warehouse management for sky- og kantskalaenhet | Denne funksjonen gjør at ansatte kan bruke mobilappen Warehouse Management til å ferdigmelde en produksjons- eller partiordre når appen kjører mot en Warehouse Management-arbeidsbelastning på en sky- eller kantskalaenhet. Hvis du vil ha mer informasjon, kan du se [Ferdigmeld og plasser på en skalaenhet](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Produksjonskontroll | Starte produksjonsordre på Warehouse Management-arbeidsbelastning for sky- og kantskalaenhet | Denne funksjonen gjør at ansatte kan bruke Warehouse Management-mobilappen til å starte en produksjons- eller partiordre når appen kjører mot en Warehouse Management-arbeidsbelastning på en sky- eller kantskalaenhet. |
| Lagerstyring | Nye sider for arbeidsområde for lastplanlegging | Aktiverer to nye arbeidsområdesider for lastplanlegging: **arbeidsområde for planlegging av innkommende last** og **arbeidsområde for planlegging av utgående last**. |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeemner. Disse emnene er ikke nødvendigvis knyttet til de nye funksjonene som ble lagt til i denne versjonen, som vist i forrige del. De kan imidlertid hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte emner |
|---|---|
| Kostnadsstyring | [Lagerverdirapporter](../cost-management/inventory-value-report-storage.md) |
| Kostnadsstyring | [Eksempler og logikk for lagerverdirapport](../cost-management/inventory-value-report-examples.md) |
| Hovedplanlegging | [Parametere for dato og klokkeslett som brukes av planleggingsoptimalisering](../master-planning/planning-optimization/date-time-used.md) |
| Hovedplanlegging | [Oppsett av behovsprognose](../master-planning/demand-forecasting-setup.md) |
| Hovedplanlegging | [Bruk sikkerhetslagerjournalen til å oppdatere minste dekning for varer](../master-planning/safety-stock-journal.md) |
| Produksjonskontroll | [Tilpass grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-customize.md) |
| Produksjonskontroll | [Utforme grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-styles.md) |
| Salg og markedsføring | [Forbedringer av ytelse for opprydding i salgshistorikk](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Lagerstyring | [Brukerkontoer for mobilenhet](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for Finance and Operations-apper

Microsoft Dynamics 365 Supply Chain Management 10.0.24 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.24 av Finance and Operations-apper (november 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.24, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2021

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2021](/dynamics365-release-plan/2021wave2/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Emnet [Fjernede eller avskrevne funksjonene i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i emnet [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
