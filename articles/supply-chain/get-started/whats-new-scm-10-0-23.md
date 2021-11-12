---
title: Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.23
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.23.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 3cf30c203d936f171796d9dd8d766cbbb8c997e0
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647845"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10023"></a>Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.23

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management-forhåndsversjonen 10.0.23. Denne versjonen har et build-nummer 10.0.1037, og er tilgjengelig som følger:

- **Forhåndsversjon:** oktober 2021
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** desember 2021

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. *Funksjon*-kolonnen gir koblinger til [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), der du kan se de offisielle frigivelsesdatoene for hver funksjon. Kolonnen *Mer informasjon* inneholder mer informasjon og/eller koblinger til tilknyttet dokumentasjon. Hvis du vil bestemme hvordan en funksjon skal aktiveres, kan du se *Aktivert av*-kolonnen. Hvis du vil ha mer informasjon om hvordan du bruker funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Dette emnet kan være oppdatert for å inkludere funksjoner som ble tatt med i builden etter at dette emnet ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Global adressebok | Definere en standard delstat/område for hvert land/område i adresseoppsett | Du kan nå definere en standard delstat/område for hvert land/område i adresseoppsettet for den globale adresseboken. Når en standard delstat/område er definert, vil det være standardverdien som angis i delstats-/områdefeltene når du oppretter en ny region- eller bypost for dette landet/området. Se også [Adresseoppsett](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Aktivert som standard. |
| Lager&nbsp;og&nbsp;logistikk | [Sette oppgaver på pause i mobilappen Warehouse Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Konfigurere omveier for trinn i menyelementer for mobilenheter](../warehousing/warehouse-app-detours.md) | Funksjonsstyring (*omveier i Warehouse Management-app*) |
| Lager&nbsp;og&nbsp;logistikk | [Forfremmede felter for lagerapp](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Konfigurere forfremmede felt for trinn i mobilenheten](../warehousing/warehouse-app-promoted-fields.md)| Funksjonsstyring (*forfremmede felt for lagerapp*) |
| Produksjonskontroll | [Rapport om ko- og biprodukter fra grensesnittet for produksjonsutførelse](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Hvordan arbeidere bruker grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-use.md) | Funksjonsbehandling (*Rapport om ko- og biprodukter fra grensesnittet for produksjonsutførelse*) |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer som er nye i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt).

Hvis du vil slå noen av disse funksjonene på eller av, må du gjøre det i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), der de vises med navnene som vises i kolonnen *Funksjonsnavn i funksjonsbehandling* i følgende tabell.

| Modul | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Ressursbehandling | Motkonto for utgifter i arbeidsordrejournaler | Ved hjelp av denne funksjonen kan du angi en motkonto for hver utgift som er oppført i en arbeidsordrejournal. Du kan vanligvis knytte en leverandørkonto til hver utgift, men andre kontotyper støttes også. Det legger til to nye kolonner (**motkontotype** og **motkonto**) i hurtigfanen **Utgift** på siden **Arbeidsordrejournal**.|
| Lagerstyring | \[Russland\] Poster økonomiske lagertransaksjoner for Storno i henhold til korrigeringsårsaken i finansbilaget for salgsordrer | Denne funksjonen påvirker funksjonaliteten for kreditnotakorrigeringer for Russland. Dette gjør det mulig å postere lagertransaksjoner for salgsfakturaer i henhold til rettelsesalternativet i økonomimodulen. Når denne funksjonen er aktivert, er det ingen flere avvik mellom **Korrigering**-flagget på finansbilaget for lagertransaksjonen og **Storno**-flagget på lagertransaksjoner. |
| Lagerstyring | (Russland) Kjør rapportberegning av beholdningssaldoomsetning i parti | For russiske lokaliseringer av Supply Chain Management gir denne funksjonen mulighet til å kjøre rapporten *Rapport for beholdningssaldoomsetning* i parti, for å lagre den og vise rapportene som ble generert tidligere. |
| Lagerstyring | (Russland) Bruk oversettelser til lokalt språk i lands- eller områdespesifikke primære skjemaer i lagerstyring | For russiske lokaliseringer av Supply Chain Management gjør funksjonen det mulig å bruke russiske oversettelser for produkt-/varenavn og måleenheter i følgende russiskspesifikke lagerutskrifter: tellingsliste (INV-3),tellingsliste (INV-5), og tellingsliste (INV-6). |
| Innkjøp og leverandører | Rydd opp i oppdateringshistorikk for bestilling | Ved hjelp av denne funksjonen kan du rydde opp i midlertidige historiske poster i forbindelse med bestillingsoppdateringer. Den legger til en ny knapp kalt **Opprydding av oppdateringshistorikk for innkjøp** i handlingsruten på siden **Alle bestillinger**. Denne funksjonen er aktivert som standard. |
| Produksjonskontroll | (Forhåndsversjon) Automatisk plukking av lageraktiverte materialer for automatisk posterte plukklister | Med denne funksjonen kan du plukke og løse lagerdimensjoner for automatisk posterte, avledede/etterkalkulerte plukklistejournaler. |
| Produksjonskontroll | Valider utløp av råvarer mot dato for planlagt forbruk | Denne funksjonen endrer hvordan utløpsdatoer for partier valideres når du reserverer et parti råvarer som skal brukes under produksjonen. Når denne funksjonen er aktivert, valideres utløpsdatoen for partiet mot den planlagte forbruksdatoen (råvaredatoen), slik den er fastsatt på produksjonsstykklistelinjen eller formellinjen for partiordren. Når denne funksjonen deaktiveres, valideres utløpsdatoen for partiet mot den planlagte leveringsdatoen til produksjons- eller partiordren (som tidligere). |
| Salg og markedsføring | Rydd opp i oppdateringshistorikk for salgsordre | Ved hjelp av denne funksjonen kan du rydde opp i midlertidige historiske poster i forbindelse med salgordreoppdateringer. Den legger til en ny knapp kalt **Rydd opp i salgsoppdateringshistorikk** i handlingsruten for detalj- og listesider for salgsordrer. |
| Salg og markedsføring | Forbedre ytelsen til rapport om Topp 100-kunder | Denne funksjonen forbedrer ytelsen til **Topp 100**-kunderapporten ved alltid å kjøre rapporten på tvers av alle kunder (som er tiltenkt bruk) i stedet for å tillate egendefinerte spørringer. Når denne funksjonen er aktivert, deaktiveres alle **oppføringer som skal tas med** i dialogboksen **Topp 100**-rapport. |
| Lagerstyring | Skaler enhetsstøtte for frigivelse til lager av utgående ordrer | Når denne funksjonen er aktivert, kan utgående ordrer frigis fra senteret direkte til skalaenheten, der ordrene skal oppfylles. |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeemner. Disse emnene er ikke nødvendigvis knyttet til de nye funksjonene som ble lagt til i denne versjonen, som vist i forrige del. De kan imidlertid hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte emner |
|---|---|
| Styring av teknisk endring | [Tekniske attributter og søk i tekniske attributter](../engineering-change-management/engineering-attributes-and-search.md) beskriver nå hvordan teknisk attributt-arv fungerer. |
| Hovedplanlegging | [Hovedplanlegging med behovsprognoser](../master-planning/planning-optimization/demand-forecast.md) og [Prognosereduksjonsnøkler](../master-planning/reduction-keys.md) gir nå mer informasjon om hvordan du arbeider med reduksjonstaster. |
| Hovedplanlegging | [Fullføring av sikkerhetslager for varer](../master-planning/safety-stock-replenishment.md) gir nå mer informasjon om bruk av minimums-/maksimumsnøkler. |
| Hovedplanlegging | [Lagerprognoser](../master-planning/inventory-forecast.md) gir nå mer informasjon om tildeling av prognoser. |
| Hovedplanlegging | [Forsyningsplan](../master-planning/supply-schedule.md) |
| Lagerstyring | [Globale mobilenhetsparametere](../warehousing/mobile-device-parameters.md) |
| Lagerstyring | [Forankring](../warehousing/anchoring.md) |
| Salg og markedsføring | Konsernintern handel er nå beskrevet i detalj, og starter med [Definere konsernintern handel](../sales-marketing/intercompany-trade-set-up.md) og beslektede emner. |
| Beholdningsstyring | Dokumentasjonen for lagersynlighet har blitt utvidet og oppdatert, fra og med [Oversikt over tillegget for lagersynlighet](../inventory/inventory-visibility.md) og relaterte emner. |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformoppdateringer for Finance and Operations-apper

Microsoft Dynamics 365 Supply Chain Management 10.0.23 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.23 av Finance and Operations-apper (november 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.23, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910).

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
