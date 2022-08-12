---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 26. juli 2021
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 26. juli 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14041dfc753b508a0d68b90ee99d79510d07e622
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070088"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 26. juli 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4384.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Plattform update 10.0.20 | -- | [Plattformoppdateringer for versjon 10.0.20 av økonomi- og driftsapper (august 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Denne artikkelen kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at denne artikkelen ble publisert.

| Utstedelsesnummer | Problem |  Beskrivelse |
| --- | --- | --- |
| 600422 | Validering av lønnsadresse mislykkes for Klar til betaling. | Valideringen er oppdatert slik at det bare kreves én adresse av typen Arbeidssted for lønn, og bare én adresse av typen Arbeidslokasjon for lønn. |
| 601226 | Dataintegreringsproblem: Eksportprosjektet for lønnsintegrering har ikke muligheten til å fremskynde hele sendingen | Lønnsintegreringen i Ceridian DayForce gjorde en trinnvis sending i stedet for en fullstendig sending. Ceridian krever for alltid full oppdatering. Nå er dette problemet løst. Enhetene i dataeksportprosjektet vil ikke lenger bruker trinnvis sending. |
| 602272 | Fliser som ble lagt til i arbeidsområdet for ansattes selvbetjening, mangler, og flisene kan ikke lenger legges til i dem | Vi har løst tilpasningsproblemet for selvbetjening for ansatte. Du kan legge til nye fliser i visningen, og en eventuell eksisterende tilpasning vil være synlige for brukere |
| 600711 | Valgfelt for halvdagsdefinisjon som er aktivert for permisjonsforespørsler for hele dagen | Dette problemet er nå løst og et halvdagsdefinisjonsfelt blir bare aktivert når ansatte velger en permisjonstype med halvdagsdefinisjon aktivert og halv dag som valgt beløp |
| 602208 | Avsetningssatsenheter som viser timer i stedet for dager | Dette problemet er nå løst. **Fridager**-skjemaet viser riktig permisjonsenhet (timer eller dager) for **Avsetningssats**-kolonnen. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)|
|  Aktivere fraværsbehandling for å administrere permisjon | [Aktivere fraværsbehandling for å administrere permisjon](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | I denne versjonen oppdaterer vi visningen av arbeidsområdet for fraværsadministrasjon. Hvis du vil ha mer informasjon, kan du se [Konfigurer fraværsbehandlingsrollen](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  Konfigurere vedleggskrav per permisjonstype | [Konfigurere vedleggskrav per permisjonstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurere permisjons- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Konfigurer permisjonsenheter per permisjonstype | [Konfigurer permisjonsenheter per permisjonstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurere permisjons- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gjør det mulig for ansatte å merkes som klare til betaling | [Gjør det mulig for ansatte å merkes som klare til betaling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til betaling](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Kommer snart

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

