---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 28. januar 2021
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 28. januar 2021.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46bbda21c3eb2b32030b93afc2a40785c22b124e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909766"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 28. januar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.3906.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Integrere årsakskoder for fordeler i arbeidsområdet for **Personaladministrasjon** | -- | [Definer årsakskoder](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Denne artikkelen kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at denne artikkelen ble publisert.


| Utstedelsesnummer | Problem |  Beskrivelse |
| --- | --- | --- |
| 539456 | Kalenderen viser fraværstypen i teksten når **Vis bare fravær uten detaljer**-parameteren er aktivert. | Når alternativet **Vis bare fravær uten detaljer** er aktivert, vises datoen for forespørselen når pekeren føres over. |
| 528907 | Hvis du gir tilgang til en juridisk enhet for ansattrolle, får ikke ledere muligheten til å se permisjonssaldoaktivitet for ansatte i **Mitt team**-området i Employee self-service. |Hvis du setter dette alternativet nå, kan ledere fortsette å se permisjonssaldoaktiviteten. |
| 526280 | Tillatelsesfeil på HcmWorkerEntity, HcmEmployeeEntity og HcmContractorEntity. | Brukere i en ikke-systemadministratorrolle kan ikke eksportere enhetene som vises, på grunn av en tillatelsesfeil i feltet NationalityCountryRegion. Brukerne vil fortsatt ha behov for følgende rettigheter til å eksportere denne informasjonen: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain og HCMContractorEntityView. |
| 542147 | Feltene **Bankkontonummer** og **Organisasjonsnummer** er obligatoriske når du legger til bankkonto via Employee Self-service. | Vi har rettet opp feilen der ansatte ble bedt om å angi feltene for **Bankkontonummer** og **Rutingsnummer** mens de legger til bankkontodetaljer. Disse feltene er ikke lenger obligatoriske når du lagrer ny bankkontoinformasjon. |
| 543641 | Postnummeret fylles ikke ut ved elektronisk rapportering. | Fikset et problem der postnummeret ikke ble fylt ut i ACA-rapporten for dekningskoder L til Q. |
| 545402 | Legg til rutingsendring for UserBranding.js-filen for å fjerne 404-feil. | Brukeren skal ikke lenger se 404-feil i konsollen. |

## <a name="in-preview"></a>I forhåndsvisning   

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)<br>[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md) |
| Visning av permisjon for ledere på tvers av firmaer | [Visning av ansattpermisjon for ledere på tvers av firmaer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere permisjons- og fraværsparametere](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| E-postbekreftelse for fordelsregistreringer | Denne funksjonen vil gi et alternativ for å sende en bekreftelses-e-post til ansatte når de sjekker ut fra fordelsregistreringen i Ansattselvbetjening. Denne funksjonen blir tilgjengelig 1. februar. Hvis du vil ha mer informasjon, kan du se [Konfigurere fordelsstyringsparametre per firma](hr-benefits-setup-parameters-per-company.md). |
| Ferdigheter som angis av en leder for de ansatte, kan godkjennes automatisk av en arbeidsflyt | Kommer snart. |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologioppdateringer for Microsoft Dataverse

I november 2020 endret Common Data Service navn til [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Se den [offisielle kunngjøringen](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) på Power Apps-bloggen for å få mer informasjon. Sammen med denne navneendringen er noe terminologi i Dataverse oppdatert. *Enhet* er nå for eksempel *tabell* og *felt* er nå *kolonne*. Hvis du vil ha mer informasjon, kan du se [Terminologioppdateringer](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

I denne versjonen har terminologien knyttet til Dynamics 365 Human Resources-integreringen med Dataverse, blitt oppdatert i hele programmet for å gjenspeile disse endringene. Skjemaet for **Common Data Service-integrering** er eksempelvis nå **Microsoft Dataverse-integrering**.

Hvis du vil lære mer om Dynamics 365 Human Resources-integrering med Microsoft Dataverse, kan du se [Konfigurere Microsoft Dataverse-integrering](./hr-admin-integration-common-data-service.md) og [Konfigurere virtuelle Microsoft Dataverse-tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]