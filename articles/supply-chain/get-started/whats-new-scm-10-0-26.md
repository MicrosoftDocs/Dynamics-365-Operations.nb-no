---
title: Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.26. (mai) 2022
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.26.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 8be79f259505c084a8680c453ec15a4cef1a890f
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124506"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.26. (mai) 2022

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.26. Denne versjonen har et build-nummer 10.0.1192, og er tilgjengelig som følger:

- **Forhåndsversjon:** Mars 2022
- **Allmenn tilgjengelighet av versjon (selvoppdatering):** April 2022
- **Allmenn tilgjengelighet av versjon (automatisk oppdatering):** Mai 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Denne artikkelen kan være oppdatert for å inkludere funksjoner som ble tatt med i builden etter at denne artikkelen ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Lager og logistikk | [Beholdningsspørring for lagersynlighet for å støtte varer i avansert lagerstyring](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Inventory Visibility-støtte for WMS-varer](../inventory/inventory-visibility-whs-support.md) | Funksjonsbehandling:<br>*Aktiver lagervarer i lagersynlighet* |
| Lager og logistikk | [Tilgjengelig for ordre for tilleggsprogrammet for lagersynlighet](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Tidsplaner for lagerendringer i Lagersynlighet og leveringskapasitet](../inventory/inventory-visibility-available-to-promise.md) | Aktivert av tjenestekonfigurasjon |
| Produksjon | [Faktisk vekt-varer for grensesnittet for produksjonsutførelse](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Hvordan arbeidere bruker grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-use.md) | Funksjonsbehandling:<br>*(Forhåndsversjon) Rapport om faktisk vekt-varer fra grensesnittet for produksjonsutførelse* |
| Produksjon | Fanen Mine jobber i grensesnittet for produksjonsutførelse <!-- KFM: Add link to release plan when available --> | [Hvordan arbeidere bruker grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-use.md) | Funksjonsbehandling:<br>*Fanen Mine jobber i grensesnittet for produksjonsutførelse* |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt).

Hvis du vil slå noen av disse funksjonene på eller av, må du gjøre dette i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Innkjøp og leverandører | Poster registrerte antall lagerførte produkter og rester av ikke-lagerførte produkter for kvitteringer og leverandørfakturaer | Denne funksjonen endrer hvordan antall produkter som ikke er lagerført (for eksempel tjenester), posteres ved behandling av leverandørfakturaer og innkommende forsendelser mot bestillinger. Funksjonen endrer hvordan antallsalternativet *Registrerte antall og tjenester* fungerer for postering av kvitteringer og leverandørfakturaer, ved å endre det slik at det fungerer som alternativet *Registrert antall og ikke-lagerførte produkter* som allerede finnes ved postering av antall for salgsfølgesedler.<br><br>Når du posterer en produktkvittering eller leverandørfaktura ved hjelp av alternativet *Registrerte antall og tjenester*, posterer systemet det registrerte antallet lagerførte produkter og det gjenstående antallet ikke-lagerførte produkter (inkludert både tjenester og ikke-tjenester). Uten denne funksjonen posterer systemet fortsatt det registrerte antallet lagerførte produkter (inkludert tjenester som er konfigurert som lagerførte varer), men posterer alltid hele det bestilte antallet ikke-lagerførte tjenesteprodukter (og ignorerer ikke-lagerførte produkter som ikke er av typen *Tjeneste*). |
| Innkjøp og leverandører | Synkroniser sporingsdimensjoner på konserninterne salgsordre- og bestillingslinjer | Du kan bruke denne funksjonen til å styre om sporingsdimensjonene for serie- og partinummer skal synkroniseres på tvers av konserninterne salgs- og bestillingslinjer. Den legger til nye innstillinger i fanene **Bestillingspolicyer** og **Salgsordrepolicyer** og salgsordrepolicyer på konfigurasjonssiden **Konserninternt** for kunder og leverandører. Den oppdaterer også navnene på noen få relaterte innstillinger i nærheten for å gjøre ting klarere.<br><br>Hvis du bruker Warehouse Management-prosesser (WMS), må du være oppmerksom på at denne funksjonen bare synkroniserer parti- og serienumre når disse dimensjonene er over lokasjonen i målreservasjonshierarkiet. |
| Behandling av produktinformasjon | Rydd opp produktattributtverdier | Denne funksjonen legger til en periodisk oppgave kalt **Rydd opp produktattributtverdier**, som rydder opp poster for produktattributtverdier som ikke lenger er knyttet til produkter via en produktkategori. |
| Lagerstyring | (Russland) Hindre avvik ved utstedelse av GTD-er for bestillinger som inkluderer WMS-aktiverte varer | Denne funksjonen er bare for russisk lokalisering. Den forhindrer avvik som oppstår ved utstedelse av russiske tolldeklareringsnumre (GTD-er) for import av bestillinger som omfatter varer som er aktivert for Warehouse Management-prosesser (WMS). GTD-utstedelsesprosessen endrer enkelte lagerdimensjonsverdier i de relaterte lagertransaksjonene for fakturaer som er inkludert i den egendefinerte journalen, noe som fører til avvik mellom arbeidspostene for bestillingen og lagertransaksjonene for kjøpet. Når denne funksjonen er aktivert, genererer GTD-utstedelsesprosessen justeringsarbeid som fjerner slike avvik. |
| Lagerstyring | Forbedret analyse for GS1-strekkoder | Denne funksjonen legger til en forbedret analyse for GS1-symboldata. Den nye analysen implementerer GS1-algoritmen for generell spesifikasjon for analyse av GS1-symboler og gir sterkere datavalidering. Hvis du vil ha mer informasjon, kan du se [GS1-strekkodeskanning](../warehousing/gs1-barcodes.md). |
| Lagerstyring | Nye sider for arbeidsområde for lastplanlegging | Legger til to nye arbeidsområdesider for lastplanlegging: **Arbeidsområde for planlegging av innkommende last** og **Arbeidsområde for planlegging av utgående last**. |
| Lagerstyring | Lagerstyringsprogram – tom GTD | Denne funksjonen er bare for russisk lokalisering. Den gjør at arbeidere som bruker mobilappen Warehouse Management, kan la russiske tolldeklareringsnumre (GTD-er) stå tomme når det er nødvendig. Hvis GTD-sporingsdimensjonen er konfigurert slik at tomme verdier tillates, godtar systemet tomme verdier for GTD for lageroperasjoner forutsatt at lagerbeholdning er tilgjengelig. |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeartikler. Disse artiklene er ikke nødvendigvis knyttet til de nye funksjonene som ble lagt til i denne versjonen, som vist i de forrige delene. De kan imidlertid hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte artikler |
|---|---|
| Kostnadsstyring | Oppdaterte eksempler og diagrammer ble lagt til i hvert av de følgende artiklene:<ul><li>[FIFO med fysisk verdi og merking](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO med fysisk verdi og merking](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO-dato med fysisk verdi og merking](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Løpende gjennomsnittlig kostpris](../cost-management/running-average-cost-price.md)</li><li>[Direkte utligning med fysisk verdi og merking](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Supply Chain Management 10.0.26 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.26 av økonomi- og driftsapper (mai 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.26, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

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

