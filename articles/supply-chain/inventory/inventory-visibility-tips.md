---
title: Tips for lagersynlighet
description: Denne artikkelen inneholder noen tips du bør vurdere når du definerer og bruker tillegget for lagersynlighet.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306093"
---
# <a name="inventory-visibility-tips"></a>Tips for lagersynlighet

[!include [banner](../includes/banner.md)]

Her er noen tips du bør vurdere når du definerer og bruker tillegget for lagersynlighet:

- For øyeblikket støtter tillegget for lagersynlighet bare Microsoft Dataverse-miljøer som ble opprettet ved å bruke Microsoft Dynamics Lifecycle Services (LCS). Hvis Dataverse-miljøet ble opprettet på en annen måte (for eksempel ved å bruke Power Apps-administrasjonssenteret), og hvis det er koblet til Dynamics 365 Supply Chain Management-miljøet ditt, må du først be produktgruppen i lagersynlighet om å løse tilordningsproblemet. Du kan kontakte gruppen på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Gruppen gir deg beskjed når miljøet er klart til å installere Lagersynlighet.
- Hvis du har mer enn ett LCS-miljø, oppretter du et annet Azure Active Directory-program (Azure AD) for hvert miljø. Hvis du bruker samme program-ID og leie-ID til å installere tillegget for lagersynlighet for forskjellige miljøer, vil det oppstå et tokenproblem for eldre miljøer. Bare den siste forekomsten av tillegget for lagersynlighet som ble installert, er gyldig.
- Lagersynlighet støttes for øyeblikket ikke for skybaserte miljøer. Den støttes bare for Nivå 2+-miljøer.
- Programmeringsgrensesnittet for programmet (API) støtter for øyeblikket spørringer på opptil 100 individuelle varer etter `ProductID`-verdi. Flere `SiteID`- og `LocationID`-verdier kan også angis i hver spørring. Maksimumsgrensen defineres som `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Bulk-API-en kan returnere maksimalt 512 poster for hver forespørsel.
- Datakilden `fno` er reservert for Supply Chain Management. Hvis tillegget for lagersynlighet er integrert med et Supply Chain Management-miljø, anbefaler vi at du ikke sletter konfigurasjoner som er relatert til `fno` i [datakilden](inventory-visibility-configuration.md#data-source-configuration).
- Lagersynlighet kan ikke endre noen data for `fno`-datakilden. Dataflyten er enveisveis, som betyr at alle antallsendringer for datakilden `fno` må komme fra Supply Chain Management-miljøet. Derfor kan du ikke bruke API til å sende lagerendrings- og reserveringsforespørsler for `fno`-datakilden.
- Hvis du legger til ett eller flere nye mål i Supply Chain Management-miljøet, bør du også legge dem til i Lagersynlighet. Men alle antallsendringer for nye mål må komme fra Supply Chain Management-miljøet.
- [Partisjonskonfigurasjonen](inventory-visibility-configuration.md#partition-configuration) består for øyeblikket av to basisdimensjoner (`SiteId` og `LocationId`) som angir hvordan dataene skal distribueres. Operasjoner under samme partisjon kan levere høyere ytelse til lavere kostnad. Løsningen inkluderer denne partisjonskonfigurasjonen som standard. Derfor *trenger du ikke å omberegne manuelt*. Ikke tilpass standard partisjonskonfigurasjon. Hvis du sletter eller endrer den, vil du sannsynligvis forårsake en uventet feil.
- Basisdimensjoner som er definert i partisjonskonfigurasjonen, bør ikke defineres i [konfigurasjonen for produktindekshierarki](inventory-visibility-configuration.md#index-configuration).
- [Konfigurasjonen for produktindekshierarkiet](inventory-visibility-configuration.md#index-configuration) må ha minst ett indekshierarki (som for eksempel inneholder basisdimensjonen `Empty`), ellers vil spørringene mislykkes med feilen "Ingen indekshierarki er angitt".
- Datakilden `@iv` er en forhåndsdefinert datakilde, og de fysiske målene som er definert i `@iv` med prefiks `@`, er forhåndsdefinerte mål. Disse målene er en forhåndsdefinert konfigurasjon for fordelingsfunksjonen, så ikke endre eller slett dem, ellers vil du sannsynligvis oppleve uventede feil når du bruker fordelingsfunksjonen.
- Du kan legge til nye fysiske mål i det forhåndsdefinerte beregnede målet `@iv.@available_to_allocate`, men du må ikke endre navnet.
- Hvis du gjenoppretter en Supply Chain Management-database, kan den gjenopprettede databasen inneholde data som ikke lenger er konsekvent med data som tidligere er synkronisert med Lagersynlighet til Dataverse. Denne datainkonsekvensen kan forårsake systemfeil og andre problemer. Det er derfor viktig at du alltid renser alle relaterte lagersynlighetsdata fra Dataverse før du gjenoppretter en Supply Chain Management-database. Hvis du vil ha mer informasjon, kan du se [Rens lagersynlighetsdata fra Dataverse før gjenoppretting av Supply Chain Management-databasen](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
