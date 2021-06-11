---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 20. mai 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 20. mai 2021.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: afa64474e8eaf4c7b73e4f76d85e379f77b570a7
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111573"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 20. mai 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4189.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Platform update 10.0.18 (42) | -- | [Plattformoppdateringer for versjon 10.0.18 av Finance and Operations-apper (mai 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Human Resources-app for Microsoft Teams støtter nå funksjoner for halvdagsdefinisjoner og delingsdager | -- | [Behandle permisjonsforespørsler i Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem |  beskrivelse |
| --- | --- | --- |
| 583776 | Masseregistreringer av ansatte i permisjonsplaner forårsaker en duplikat postfeil | Denne feilen er fikset i den siste frigivelsen, og massepermisjonsplaner skal nå behandles på riktig måte. |
| 582263 | Kan ikke kjøre levetidsbehandling for alle arbeidere samtidig | Når **Arbeider**-feltet er tomt for levetidsbehandling, behandles alle arbeidere. |
| 558383 | Primær mottaker ikke merket som 100 % hvis standard mottaker ikke er valgt | Feilen er fikset, slik at brukeren bare trenger å velge veksleknapp for primær mottaker.|
| 509404 | Arbeidsstokkanalyse for avdeling tar ikke hensyn til flytting av ansatte mellom avdelinger |Analysen er oppdatert, slik at den omfatter overføringer av ansatte mellom avdelinger|
| 579420 | Frysing av kolonner i rutenettfunksjonen skal ennå ikke være tilgjengelig | Funksjonen for **Frys kolonnene i rutenett**, som ikke er tilgjengelig i Human Resources, var oppført som tilgjengelig i Funksjonsbehandling. Funksjonen er fjernet fra listen over funksjoner som skal aktiveres. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Egendefinerte felt-støtte i rettighetsregler for fordelsbehandling | [Egendefinert felt-støtte for rettighetsbehandling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Konfigurere rettighetsregler](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Forbedringer i permisjon og fravær-arbeidsflyt | [Forbedringer i permisjon og fravær-arbeidsflyt](https://go.microsoft.com/fwlink/?linkid=2147528) | [Be om fritid](hr-employee-self-service-request-time-off.md)|
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)|
| Overvåking av permisjonsavsetningstransaksjon | - | [Overvåking av permisjonsavsetningstransaksjon](hr-leave-and-absence-accrue.md#preview-leave-accrual-transaction-auditing)|

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
|  Aktivere fraværsbehandling for å administrere permisjon | [Aktivere fraværsbehandling for å administrere permisjon](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
