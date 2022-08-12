---
title: Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.27. (juli 2022)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.27.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: ff92e6904b8042232159a0aea095d7a91c17d4b7
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124108"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10027-july-2022"></a>Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.27. (juli 2022)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.27. Denne versjonen har et build-nummer 10.0.1227, og er tilgjengelig på følgende tidsplan:

- **Forhåndsversjon:** april 2022
- **Allmenn tilgjengelighet av versjon (selvoppdatering):** Juni 2022
- **Allmenn tilgjengelighet av versjon (automatisk oppdatering):** Juli 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Denne artikkelen kan være oppdatert for å inkludere funksjoner som ble lagt til i builden etter at denne artikkelen opprinnelig ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Lager og logistikk | [Lagertildeling for tilleggsprogrammet for lagersynlighet](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Lagertildeling for lagersynlighet](../inventory/inventory-visibility-allocation.md) | Aktivert som standard |
| Produksjon | Visningen Min dag for grensesnittet for produksjonsutførelse | [Hvordan arbeidere bruker grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-use.md) og [Vis feriesaldoer i grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-payroll-stats.md) | Funksjonsbehandling:<br>*Visningen Min dag for grensesnittet for produksjonsutførelse* |
| Planlegging | [Støtte i Planleggingsoptimalisering for utsetting](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Administrer utsettingsarbeid i produksjon](../production-control/manage-subcontract-work-production.md) | Aktivert som standard |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt).

Hvis du vil slå noen av disse funksjonene på eller av, må du gjøre dette i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Hovedplanlegging | Vurder lagerleveringstid ved oppretting av en planlagt overføringsordre | Når en overføringsordre opprettes, får denne funksjonen systemet til å vurdere lagerleveringstiden som er angitt i varens standard ordreinnstillinger, ved beregning av mottaksdatoen for den planlagte overføringsordren for leveringsdatokontrolloppsett som leveringstid til typen *Ingen* eller *Salg*. Når leveringstiden for overføring angis, brukes verdien for mottaksdatoberegningen, og transportdager ignoreres. |
| Innkjøp og leverandører | Avgiftsinformasjon for standard meglerkontrakt på leverandørfakturalinjer | Denne funksjonen introduserer logikk for å definere standardverdier for feltene **Merverdiavgift** og **Merverdiavgift for vare** på fakturalinjer for meglerkontraktleverandør. Denne logikken brukes bare når tilleggtypen på meglerkontraktlinjen er finans/finans. Merverdiavgiftsgruppen for vare tar sin standardverdi, enten fra megleransvarsinnkjøpskategorien (hvis den er definert) eller fra gebyrtypen. Merverdiavgiftsgruppen tar standardverdien fra leverandørkontoen. |
| Innkjøp og leverandører | Begrens antall bestillingslinjer per partioppgave | Ved hjelp av denne funksjonen kan du optimalisere systemytelsen når bekreftelser og produktmottak posteres. Det legges til en ny innstilling med navnet **Linjer per oppgave**, i fanen **Levering** på siden **Innkjøps- og fraktparametere**. Med denne nye innstillingen kan du begrense antall bestillingslinjer som hver satsvise oppgaveprosess. Det kan derfor bidra til å hindre at store satsvise oppgaver reduserer hastigheten på systemet. |
| Behandling av produktinformasjon | Fyll ut produktattributtverdier | Denne funksjonen legger til en periodisk oppgave med navnet *Fyll ut produktattributtverdier*. Denne nye periodiske oppgaven oppretter manglende verdiposter for produktattributter for attributter som er tilknyttet produkter via en produktkategori. |
| Produksjonskontroll | Tilleggskonfigurasjon i grensesnittet for produksjonsutførelse | <p>Denne funksjonen legger til følgende alternativer på siden **Konfigurer produksjonsgulvutførelse**:</p><ul><li>**Åpne startdialogboks automatisk ved fullføring av søk** – Når dette alternativet er aktivert, åpnes dialogboksen **Start jobb** automatisk når arbeidere bruker søkefeltet til å finne en jobb.</li><li>**Åpne rapportfremdriftsdialogboks automatisk ved fullføring av søk** – Når dette alternativet er aktivert, åpnes dialogboksen **Rapportfremdrift for jobben** automatisk når arbeidere bruker søkefeltet til å finne en jobb.</li><li>**Standard restantall i dialogboksen for rapportfremdrift** – Når dette alternativet er aktivert, viser dialogboksen **Rapportfremdrift** restantall som skal rapporteres på en produksjonsjobb.</li></ul><p>Hvis du vil ha mer informasjon, kan du se [Konfigurere grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md).</p> |
| Produksjonskontroll | Produksjonsteam i grensesnittet for produksjonsutførelse | <p>Når flere arbeidere er tildelt samme produksjonsjobb, kan de nå velge én arbeider som leder. De gjenværende arbeiderne blir automatisk assistenter til lederen. For resultatgruppen må bare lederen registrere jobbstatus, mens tidsposter gjelder alle gruppemedlemmer. Denne funksjonen støtter også et scenario som kalles *hjelperessurs*. I dette scenarioet kan en arbeider registrere seg som assistent til en annen arbeider, som deretter blir leder for den nylig utformede gruppen.</p><p>Hvis du vil ha mer informasjon, kan du se [Hvordan arbeidere bruker grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-use.md).</p> |
| Produksjonskontroll | Rapport om planleggingsvarer i grensesnittet for produksjonsutførelse | Denne funksjonen forenkler prosessen med rapportering av partiordrer for planleggingselementer i grensesnittet for produksjonsutførelse. Når en partiordre opprettes for et produkt som har produksjonstypen *Planleggingselement*, kan ferdigmelding bare utføres på koproduktene og biprodukter etter produktene for denne partiordren. Partiordrer for planleggingsvarer brukes vanligvis til å støtte demonteringsprosesser, der et råvareprodukt demonteres sammen i flere atskilte produkter. Når en arbeider rapporterer en partiordre for et planleggingselement som ferdig, viser dialogboksen **Rapportfremdrift** nå bare koproduktene og biproduktene. Tidligere viste det også planleggingselementet, og denne virkemåten kan føre til at arbeidere blir forveksler. |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeartikler. Disse artiklene er ikke nødvendigvis knyttet til de nye funksjonene som ble lagt til i denne versjonen, som vist i de forrige delene. De kan imidlertid hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte artikler |
|---|---|
| Kostnadsstyring | [Dato for avveid gjennomsnitt med Inkluder fysisk verdi og merking](../cost-management/weighted-average-date.md) |
| Distribuert hybridtopologi | [Prøv storskalaenheter i en distribuert hybridtopologi](../cloud-edge/cloud-edge-try-out.md) |
| Dobbel skriving | [Synkronisere med prismotoren for Supply Chain Management ved behov](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Lagerstyring | [Frigi til lager](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Supply Chain Management 10.0.27 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.27 av økonomi- og driftsapper (juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.27, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

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

