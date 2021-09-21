---
title: Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.22 (november 2021)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.22.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6fc4b9d0a0f5319c8a75e7d687ee82ea81497844
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471866"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10022-november-2021"></a>Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.22 (november 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management-forhåndsversjonen 10.0.22. Denne versjonen har et build-nummer 10.0.995, og er tilgjengelig som følger:

- **Forhåndsversjon:** september 2021
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** oktober 2021
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** november 2021

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. *Funksjon*-kolonnen gir koblinger til [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), der du kan se de offisielle frigivelsesdatoene for hver funksjon. Kolonnen *Mer informasjon* inneholder mer informasjon og/eller koblinger til tilknyttet dokumentasjon. Hvis du vil bestemme hvordan en funksjon skal aktiveres, kan du se *Aktivert av*-kolonnen. Hvis du vil ha mer informasjon om hvordan du bruker funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Dette emnet kan være oppdatert for å inkludere funksjoner som ble tatt med i builden etter at dette emnet ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Planlegging | [Planlegge optimaliseringsstøtte for funksjonsbasert ressurstildeling](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Planlegging med ubegrenset kapasitet](../master-planning/planning-optimization/infinite-capacity-planning.md) | Funksjonsbehandling (*Uendelig kapasitetsplanlegging for Planleggingsoptimalisering*) |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt). Hvis du vil bruke noen av disse funksjonene, må du uttrykkelig aktivere dem i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funksjonsområde | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Kostnadsstyring | Opprette tilknyttede bilag for standard kostnadsavrundingsrevalueringer | <p>Når det utføres en økonomisk lagerpostering (for eksempel en salgsordrefaktura eller lagertransaksjon), fører denne funksjonen til at systemet oppretter et separat bilag for eventuelle relaterte standard kostnadsavrundingsrevalueringer og knytter det til det økonomiske posteringsbilaget som et tilknyttet bilag.</p><p>Uten denne funksjonen registrerer systemet standard kostnadsavrundingsrevalueringer på samme bilagspostering. Denne virkemåten kan noen ganger forårsake motstridende datoinformasjon, fordi revalueringene bruker økt- eller systemdatoen, mens økonomiske posteringer bruker posteringsdatoen.</p> |
| Distribuert hybridtopologi | *(Ingen funksjonsbehandling er nødvendig.)* | <p>Denne versjonen utvider funksjonene for utgående belastningsplanlegging for lagerstyringens arbeidsmengde for sky- og kantskaleringsenheter.</p><p>Hvis du vil ha mer informasjon, kan du se [Arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Styring av teknisk endring | Variantgenerering for tekniske produkter | <p>Ved hjelp av denne funksjonen kan du generere flere varianter for et teknisk produkt, basert på farge-, størrelses-, stil- eller konfigurasjonsdimensjoner.</p><p>Hvis du vil ha mer informasjon, kan du se [Generere varianter for tekniske produkter](../engineering-change-management/engineering-variants.md).</p> |
| Lagerstyring | Integrering av lagersynlighet med reservasjonsmotkonto | <p>Denne funksjonen kan bare aktiveres etter at funksjonen *Integrering av lagersynlighet* er aktivert. Den gir funksjonalitet for å motpostere reserveringer som gjøres på lagersynlighet.</p><p>Hvis du vil ha mer informasjon, kan du se [Lagersynlighetsreservasjoner](../inventory/inventory-visibility-reservations.md).</p> |
| Salg og markedsføring | Begrens antall salgsordrer som kan velges for postering | <p>Denne funksjonen er automatisk aktivert. Den legger til feltet **Maks. antall salgsordrer for postering** på siden **Kundeparametere**. Ved hjelp av dette feltet kan du definere maksimalt antall salgsordrer som kan velges ved postering av bekreftelser, plukklister, følgesedler og fakturaer fra listesiden for salgsordrer. Standardverdien er *100*.</p><p>Funksjonen bidrar til å forbedre ytelsen på listesiden for salgsordrer når et betydelig antall salgsordrer velges. Den har ingen innvirkning på antall salgsordrer som kan behandles av en periodisk oppgave.</p> |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeemner. Disse emnene er ikke nødvendigvis knyttet til de nye funksjonene som ble lagt til i denne versjonen, som vist i forrige del. De kan imidlertid hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte emner |
|---|---|
| Styring av teknisk endring | [Oversikt over styring av teknisk endring](../engineering-change-management/product-engineering-overview.md) viser nå alle relaterte, valgfrie funksjoner som er tilgjengelige i funksjonsadministrasjon |
| Hovedplanlegging | [Oppsett av behovsprognose](../master-planning/demand-forecasting-setup.md) |
| Hovedplanlegging | [Nettobehov og utligningsinformasjon med planleggingsoptimalisering](../master-planning/planning-optimization/net-requirements.md) |
| Lagerstyring | [Frigi til lager](../warehousing/release-to-warehouse-process.md) gir en detaljert oversikt over fullstendig frigivelse til lagerprosess |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformoppdateringer for Finance and Operations-apper

Microsoft Dynamics 365 Supply Chain Management 10.0.22 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.22 av Finance and Operations-apper (november 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.22, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

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
