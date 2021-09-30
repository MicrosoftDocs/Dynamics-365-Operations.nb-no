---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 6. september 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 6. september 2021.
author: marcelbf
ms.date: 09/06/2021
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
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2add53b4b014cb65caacff03bf175078d2b70d8f
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485913"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 6. september 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Microsoft Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4443.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
|---|---|---|
| Aktivere fraværsbehandling for å administrere permisjon | [Aktivere fraværsbehandling for å administrere permisjon](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | I denne versjonen oppdaterer vi visningen av arbeidsområdet for fraværsadministrasjon. Hvis du vil ha mer informasjon, kan du se [Konfigurer fraværsbehandlingsrollen](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Konfigurere vedleggskrav per permisjonstype | [Konfigurere vedleggskrav per permisjonstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Konfigurere permisjons- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Konfigurer permisjonsenheter per permisjonstype | [Konfigurer permisjonsenheter per permisjonstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Konfigurere permisjons- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem | beskrivelse |
|---|---|---|
| 610128 | Feil ved publisering av data ved bruk av HcmDiscussionOverallCommentEntity | Når data publiseres fra en Excel-arbeidsbok til HcmDiscussionOverralCommentEntity-enheten, oppstår følgende feil: Finner ikke datakildeposten av typen HcmTopicOverrall. |
| 589073 | EEO-1-rapporten teller "Ikke spesifikk" og tomme verdier for **Kjønn**-feltet som Kvinne-verdi. | Hvis **Mann** ikke er angitt for **Kjønn**-feltet, genererer EEO-1-rapporten standardverdien **Kvinne**. |
| 589617 | Saldo fridager-kort, Tilgjengelig for kjøp- og Tilgjengelig for salg-saldoer vises ikke når brukerroller er begrenset til en bestemt juridisk enhet. | Hvis brukeren (ansattrollen) er begrenset til en bestemt juridisk enhet, vises ikke saldoene riktig på kortet **Avspaseringssaldoer** og i feltene **Tilgjengelig for kjøp** og **Tilgjengelig for salg**. |
| 604310 | Kategorien Fraværsbehandling bør være skjult når brukeren ikke har tilordnet fraværshierarki. | For en gitt juridisk enhet bør kategorien **Fraværsbehandling** være skjult i selvbetjeningsportalen med mindre parameteren for flere firmaer er aktivert, og minst ett fraværshierarki er tilknyttet brukeren. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om hvordan du aktiverer eller deaktiverer funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
|---|---|---|
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md) |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Gjør det mulig for ansatte å merkes som klare til betaling | [Gjør det mulig for ansatte å merkes som klare til betaling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til betaling](/dynamics365/human-resources/hr-compensation-payroll) |
| Egendefinerte felt i Rettighet |[Egendefinert felt-støtte i rettighetsbehandling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Bruke egendefinerte felt i rettighetsbehandling](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Kommer snart

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funksjon | Detaljer |
|---|---|
| Platform update 10.0.21 (45) | Utrullingen av plattformoppdatering 10.0.21 er planlagt å begynne med serviceversjon 4. oktober 2021. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.21 av Finance and Operations-apper (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Fordelsoppgave | Fordelsoppgave for visning av ansattes gjeldende fordelsvalg. Hvis du vil ha mer informasjon, kan du se [Fordelsoppgave](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) i lanseringsbølgedokument. |

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
