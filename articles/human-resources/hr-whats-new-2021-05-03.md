---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 3. mai 2021
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 3. mai 2021.
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df8bd0277e4f27c23ba25c886d12f589913e5d46
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066231"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 3. mai 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4140.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Legg til informasjonslinje når livshendelser opprettes. | - | Når du oppretter en livshendelse, viser informasjonslinjen en melding som angir hvilken type livshendelse som opprettes.

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Denne artikkelen kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at denne artikkelen ble publisert.

| Utstedelsesnummer | Problem |  Beskrivelse |
| --- | --- | --- |
| 559312 |  Nivå vises ikke når det opprettes en fast kompensasjonsplan for en ansatt. |  Når det er en tidssonekonflikt mellom brukerens tidssone og firmaets tidssone, kunne ikke kompensasjonsnivået på jobben leses. Spørringen er oppdatert til å hente basert på UTC-tid. |
| 573676  | Kan ikke legge til en ny periode i **Fordelsplan**-skjemaet. | Oppdaterte skjemaet slik at **Ny**-knappen aktiveres i hurtigfanen **Periode** i **Fordelsplaner**. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Forbedringer i permisjon og fravær-arbeidsflyt | [Forbedringer i permisjon og fravær-arbeidsflyt](https://go.microsoft.com/fwlink/?linkid=2147528) | [Be om fritid](hr-employee-self-service-request-time-off.md)|
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)|
| Overvåking av permisjonsavsetningstransaksjon | - | [Overvåking av permisjonsavsetningstransaksjon](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| Platform update 10.0.18 (42) | Plattformoppdatering 10.0.18 planlegges å rulle ut med serviceversjon 17. mai 2021. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.18 av økonomi- og driftsapper (mai 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Egendefinerte felt-støtte i rettighetsregler for fordelsbehandling  | [Egendefinert felt-støtte for rettighetsbehandling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

