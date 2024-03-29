---
title: Hva er nytt eller endret i Dynamics 365 Supply Chain Management (10.0.20. august 2021)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Supply Chain Management 10.0.20.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d99a7a7d0261ba0afd19efbb237dff329527723d
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219162"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Hva er nytt eller endret i Dynamics 365 Supply Chain Management (10.0.20. august 2021)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.20. Denne versjonen har et build-nummer 10.0.886, og er tilgjengelig som følger:

- **Forhåndsversjon:** mai 2021
- **Allmenn tilgjengelighet av versjon (selvoppdatering):** Juli 2021
- **Allmenn tilgjengelighet av versjon (automatisk oppdatering):** August 2021

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. *Funksjon*-kolonnen gir koblinger til [frigivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), der du kan se de offisielle frigivelsesdatoene for hver funksjon. Kolonnen *Mer informasjon* inneholder mer informasjon og/eller koblinger til tilknyttet dokumentasjon.

De fleste av disse funksjonene må aktiveres ved hjelp av [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) før du kan bruke dem.

| Funksjonsområde | Funksjon | Mer informasjon |
|---|---|---|
| Lager&nbsp;og&nbsp;logistikk | [Ytelsesforbedring for salgsordredetaljer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Denne funksjonen gjør brukergrensesnittet mer brukervennlig når det åpnes salgsordrer, spesielt ordrer som omfatter mange linjer. |
| Produksjon | [Starte prosessautomeringsflyter for å opprette kvalitetsordrer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Starte prosessautomeringsflyter for å opprette kvalitetsordrer](../production-control/process-automation-quality-orders.md ) |
| Produksjon | [Forbedret grensesnitt for produksjonsutførelse for produksjon](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Konfigurere grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) |
| Planlegging | [Uendelig kapasitetsplanlegging for Planleggingsoptimalisering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [Planlegging med ubegrenset kapasitet](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Behandling av produktinformasjon | [Administrer endringer i formler og ingrediensene](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Behandle endringer i formler og ingrediensene](../engineering-change-management/manage-formula-changes.md) |
| Behandling av produktinformasjon | [Produktklargjøringskontroller](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Produktklargjøring](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt). Hvis du vil bruke noen av disse funksjonene, må du uttrykkelig aktivere dem i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjons&nbsp;navn&nbsp; i funksjons&nbsp;behandling | Mer informasjon |
|---|---|---|
| Hovedplanlegging | Parallell autorisasjon av justert behovsprognose | Denne funksjonen tillater parallell autorisasjon av justert behovsprognose fra siden **Justert behovsprognose**. Hensikten med denne funksjonen er å øke ytelsen når et høyt antall prognoser godkjennes. Ved autorisasjon kan brukeren angi **Antall tråder** i den autorisasjonsdialogboksen. |
| Hovedplanlegging | Autorisasjon og konsolidering av planlagte masse- og pakkepartiordrer | Med denne funksjonen kan du bruke satsvise jobber til å autorisere og konsolidere planlagte masse- og pakkeordrer. |
| Produksjonskontroll | Kopier generelle ruter | Denne funksjonen forbedrer kopieringsrutefunksjonen, slik at brukere kan kopiere ruter som ikke er varespesifikke. Det gjør at systemet kan oppdatere all relevant informasjon (for eksempel område, rutegruppe, ressursbehov og ulike tidspunkt) etter at kopieringsrutefunksjonen er brukt til å overskrive en rute som ennå ikke er tilordnet en vare. |
| Produksjonskontroll | Oppdater relaterte ressursbehov når en ruteoperasjon endres | Denne funksjonen gjør det mulig for systemet å oppdatere de relaterte ressursbehovene etter at en bruker endrer operasjonen for et eksisterende rutetrinn. |
| Behandling av produktinformasjon | Stykklisterapport før behandling for å forhindre tidsavbrudd | Denne funksjonen fører til at stykklisterapporten blir forhåndsbehandlet. Dette vil unngå tidsavbruddsproblemer når det er en stor databelastning for rapporten. |
| Innkjøp og leverandører | Aktiver tilbakestilling av innkjøpsrelaterte arbeidsflyter | Ved hjelp av denne evalueringsfunksjonaliteten kan du tilbakestille følgende arbeidsflyter til utkaststatus: Bestilling, Leverandørendring og Innkjøpsrekvisisjoner. |
| Transportstyring | Aktiver oppretting av en leverandørfakturajournal når du forkaster et fraktbrev | Når denne funksjonen er aktivert, blir det bare opprettet en tilsvarende leverandørfakturajournal av avstemmingshensyn når du bruker alternativet for lønnsleverandør. Ellers vil fakturajournalen alltid bli opprettet. |
| Lagerstyring | Valider maler som er valgt for etterfyllingsjobber | Denne funksjonen sikrer at brukerne velger gyldige etterfyllingsmaler når de konfigurerer en etterfyllingsjobb. Den hindrer brukere i å opprette en etterfyllingsjobb uten en mal, og fra å velge maler av typen *Bølgebehov*, som ikke vil opprette noe etterfyllingsarbeid, og som kan ta lang tid å behandle. |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeartikler. De er ikke nødvendigvis knyttet til de nye funksjonene som er lagt til for denne versjonen, som oppført i den forrige delen, men de kan hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte artikler |
|---|---|
| Styring av teknisk endring | [Produktstatuser og transaksjoner](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Beholdningsstyring | [Tillegg for lagersynlighet](../inventory/inventory-visibility.md)<br><br>[Oversikt over kvalitets- og avviksstyring](../inventory/quality-management-processes.md) (pluss alle tilknyttede artikler for kvalitetsstyring) |
| Innkjøp og leverandører | [Vedlikehold leverandørsertifisering](../../finance/public-sector/manage-vendor-certification.md) |
| Produksjonskontroll | [Utforme grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-styles.md) |
| Lagerstyring | [Tilordne trinnikoner og -titler for mobilappen Warehouse Management](../warehousing/step-icons-titles.md)<br><br>[Utsatt behandling av manuell lagerbevegelse](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Supply Chain Management 10.0.20 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.20 av økonomi- og driftsapper (juli 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.20, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021-frigivelsesbølge 1-planen

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Se [Dynamics 365: 2021-frigivelsesbølge 1-planen](/dynamics365-release-plan/2021wave1/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

