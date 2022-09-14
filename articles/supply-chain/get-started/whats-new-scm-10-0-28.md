---
title: Hva er nytt eller endret i Dynamics 365 Supply Chain Management (10.0.28. august 2022)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.28.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: bbbd524020690b84fce34facaaa3047853fb2641
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403718"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Hva er nytt eller endret i Dynamics 365 Supply Chain Management (10.0.28. august 2022)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.28. Denne versjonen har et build-nummer 10.0.1264, og er tilgjengelig på følgende tidsplan:

- **Forhåndsversjon:** mai 2022
- **Allmenn tilgjengelighet av versjon (selvoppdatering):** Juli 2022
- **Allmenn tilgjengelighet av versjon (automatisk oppdatering):** Juli 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Denne artikkelen kan være oppdatert for å inkludere funksjoner som ble lagt til i builden etter at denne artikkelen opprinnelig ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Lager og logistikk | [Integreringsenheter for landingskostnad for tredjepartsfraktforsendere](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Oversikt over enheter for landingskostnad](../landed-cost/landed-cost-entities-overview.md) | Aktivert som standard |
| Planlegging | [DDMRP (etterspørselsdrevet planlegging av materialkrav)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Oversikt over etterspørselsdrevet planlegging av materialkrav](../master-planning/planning-optimization/ddmrp-overview.md) | Funksjonsbehandling:<br>*(Forhåndsversjon) DDMRP for planleggingsoptimalisering* |
| Planlegging | [Støtte i Planleggingsoptimalisering for leveringskapasitet (CTP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | [Beregn leveringsdatoer for salgsordrer ved hjelp av CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) | Funksjonsbehandling:<br>*(Forhåndsversjon) CTP for planleggingsoptimalisering* |
| Planlegging | [Støtte i Planleggingsoptimalisering for holdbarhet](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | [Hovedplanlegging for produkter med begrenset holdbarhet](../master-planning/planning-optimization/shelf-life.md) | Aktivert som standard |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt).

Hvis du vil slå noen av disse funksjonene på eller av, må du gjøre dette i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Lagerstyring | Aktiver konsernintern beholdning slik at den bare viser antall som ikke er null, i beholdning | Ved hjelp av denne funksjonen kan du velge om varer med null i lagerbeholdning skal inkluderes i den konserninterne lagerbeholdninglisten. Du kan styre dette alternativet ved hjelp av innstillingen **Ikke vis varer med null i lagerbeholdning i den konserninterne lagerlisten**, som denne funksjonen legger til på siden **Parametere for beholdnings- og lagerstyring**. |
| Lagerstyring | (India) For overføringsprisregler kan du ignorere lokasjon når Fra lagerkode er satt til Alle | <p>Denne funksjonen gjelder bare for Indias lokalisering. Prosessen med å definere overføringspriser for varer i lageroverføringer blir mer oversiktlig.</p><p>Du definerer overføringspriser ved å konfigurere hver vare med overføringsprissettingsregler. En måte å gjøre denne konfigurasjonen på, er å inkludere en regellinje der **Fra lagerkode**-feltet er satt til *Alle*. Denne innstillingen angir at overføringsprisen som er definert av linjen, skal gjelde uansett lageret som varen er plukket fra. Når denne funksjonen er aktivert, vil overføringsprisregler der **Fra lagerkode**-feltet er satt til *Alle*, ignorere **Sted**-innstillingen. Regelen vil derfor gjelde uansett lokasjon som er angitt i overføringsordren. Dette problemet er sannsynligvis hva som forventes, fordi lokasjonen er under lageret i lagringsdimensjonshierarkiet.</p><p>Uten denne funksjonen bruker systemet bare regler av denne typen når lokasjonen på overføringsordren samsvarer nøyaktig med lokasjonen som er angitt for regelen. (Hvis en tom lokasjon er angitt for regelen, vil systemet bare bruke regelen for overføringsordrer som også har en tom verdi for lokasjonen.)</p> |
| Lagerstyring | Opprydding av rapportdata for lagerbeholdning | Denne funksjonen gir en måte å rydde opp i dataene som brukes til å opprette rapportene *Lagring av rapport for lagerbeholdning*. |
| Produksjonskontroll | Tildel prosjektaktiviteter for serviceavtaler og serviceordrelinjer | Denne funksjonen legger til et felt kalt **Prosjektaktivitet** i serviceavtalen og serviceordrelinjer, slik at du kan angi en prosjektaktivitet for dem. Funksjonen forhindrer blokkeringsfeil når du posterer prosjektjournaler for servicestyring som krever at det angis en prosjektaktivitet.  |
| Lagerstyring | Plukktjeneste for manuell overføringslinje for administrator eller lignende klarerte brukere | Ved hjelp av denne funksjonen kan administratorer plukke lagertransaksjoner som er knyttet til overføringslinjer manuelt. Disse linjene inkluderer linjer som allerede er frigitt til lageret. Administratorer bør bare gjøre denne plukkingen i spesielle tilfeller, for eksempel når systemet er ødelagt. Hvis du vil ha mer informasjon, kan du se [Håndtere plukkunntak for salgs- og overføringslinjer manuelt](../warehousing/manual-order-line-picking-exception-handling.md). |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeartikler. Disse artiklene er ikke nødvendigvis knyttet til de nye funksjonene som ble lagt til i denne versjonen, som vist i de forrige delene. De kan imidlertid hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte artikler |
|---|---|
| Kostnadsstyring | [Fast mottakspris](../cost-management/fixed-receipt-price.md) |
| Kostnadsstyring | [Vanlige spørsmål om lagerkostnad](../cost-management/inventory-costing-faq.md) |
| Kostnadsstyring | [Regnskapsprinsippet Postere i belastningskonto](../cost-management/post-to-charge-account-accounting-principle.md) |
| Beholdningsstyring | [Lagertransaksjonsdetaljer](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Supply Chain Management 10.0.28 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.28 av økonomi- og driftsapper (juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.28, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 1 for 2022

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 1 for 2022](/dynamics365-release-plan/2022wave1/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

