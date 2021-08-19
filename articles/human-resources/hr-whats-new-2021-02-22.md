---
title: Nyheter eller endringer i Dynamics 365 Human Resources 22. februar 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 22. februar 2021.
author: marcelbf
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 379a902489bdccdfa3490a830cc3b0bbf7639e7f0b62079a3ff3a999b0a7c412
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721565"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Nyheter eller endringer i Dynamics 365 Human Resources 22. februar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.3988.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Dynamics 365 Human Resources-app for Microsoft Teams | [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)<br>[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem |  beskrivelse |
| --- | --- | --- |
| 529994 | Endring av feltet **Kjent som** i skjemaet **Arbeider** utløser ikke en Dataverse-oppdatering | Løste et problem der Dataverse ikke oppdateres når feltet **Kjent som** oppdateres i skjemaet **Arbeider**. |
| 532651 | PBI-rapporten om kompensasjon bruker ikke valutaomregning ved beregning av metrikk for alle firmaer | Løste et problem der PBI-rapporten Kompensasjonsanalyse ikke gjorde valutaomregning riktig. |
| 552226 | Behandling av livshendelser lukker og åpner planer på nytt flere ganger for enkelthendelser  | Løste et problem der en ansatt er i flere juridiske enheter og en livshendelse forekommer, genererer en livshendelsespost for hver juridiske enhet den ansatte er i. Ved behandling av livshendelser må du velge den juridiske enheten som skal behandles. Behandlingslogikken begrenser seg imidlertid ikke til denne juridiske enheten. I stedet behandler den for alle juridiske enheter, og lukker og åpner planene på nytt i den valgte juridiske enheten. Denne handlingen er en livshendelse som behandler flere ganger i samme juridiske enhet, noe som resulterer i flere lukkinger/gjenåpninger av hver plan som berøres av livshendelsen. |
| 518064 | Bare én avhengig av valgte kvalifiserte planer når mer enn én er merket som standardvalg | Løste et problem der flere standardvalg ikke velges automatisk i kvalifiserte planer. Du kan nå angi primær mottaker for en personlig kontakt. Den primære mottakeren er oppført som 100 % i kvalifiserte planer når det er flere mottakere. |
| 552365 | BOYD-eksportjobber (ta med din egen database) mislykkes etter oppgradering til plattformoppdatering 40 | Reparerte et problem der BYOD-eksporter mislyktes etter at platformoppdatering 40 er brukt i miljøet. |
| 547123 | Begrens antall oppgaver det spørres om i gjøremålslisten på instrumentbordet | Antall oppgaver som vises i gjøremålslisten, er nå begrenset til 15 for å rette opp et ytelsesproblem som forårsakes av et stort antall oppgaver som prøver å laste. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Visning av permisjon for ledere på tvers av firmaer | [Visning av ansattpermisjon for ledere på tvers av firmaer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere permisjons- og fraværsparametere](./hr-leave-and-absence-parameters.md) |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Du kan hindre at ansatte redigerer kontaktdetaljer for virksomhet. | [Begrense at ansatte redigerer kontaktdetaljer for virksomhet.](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Begrense redigering av personlige opplysninger](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| Ferdigheter som angis av en leder for de ansatte, kan godkjennes automatisk av en arbeidsflyt | Kommer snart. |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologioppdateringer for Microsoft Dataverse

I november 2020 endret Common Data Service navn til [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Se den [offisielle kunngjøringen](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) på Power Apps-bloggen for å få mer informasjon. Med denne navneendringen er deler av terminologien i Dataverse oppdatert. *Enhet* er nå for eksempel *tabell* og *felt* er nå *kolonne*. Hvis du vil ha mer informasjon, kan du se [Terminologioppdateringer](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

I denne versjonen har terminologien knyttet til Dynamics 365 Human Resources-integreringen med Dataverse, blitt oppdatert i hele programmet for å gjenspeile disse endringene. Skjemaet for **Common Data Service-integrering** er eksempelvis nå **Microsoft Dataverse-integrering**.

Hvis du vil lære mer om Dynamics 365 Human Resources-integrering med Microsoft Dataverse, kan du se [Konfigurere Microsoft Dataverse-integrering](./hr-admin-integration-common-data-service.md) og [Konfigurere virtuelle Microsoft Dataverse-tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Oppdateringer av tjenestedistribusjon

Fra og med versjonen fra 22. februar 2021 blir distribusjonen av regionale tjenester justert. Justeringene vil inkludere rotasjon av rekkefølgen globale områder mottar oppdateringer for Human Resources-tjenesten, og endringer i ventetiden mellom oppdateringsstadier. Disse endringene gir oss mer i tråd med SDP (Safe Deployment Practices) for å forbedre serviceforsikring, kvalitet og støtte.

Vi vil fortsette å følge distribusjonsfrekvensen på to uker. Kundene kan imidlertid legge merke til at oppdateringer vanligvis brukes i Human Resources-miljøet på en annen dag i syklusen for to uker enn i tidligere versjoner.

Hvis du vil ha mer informasjon om serviceoppdateringsprosessen, kan du se [Oppdateringsprosess](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]