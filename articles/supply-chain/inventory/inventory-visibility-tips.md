---
title: Tips for lagersynlighet
description: Dette emnet inneholder noen tips du bør vurdere når du definerer og bruker tillegget for lagersynlighet.
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
ms.openlocfilehash: 1f6ade36ac184a3c8bf790fc0d899ea01d90c8d2
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952421"
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
