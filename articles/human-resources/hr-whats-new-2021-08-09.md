---
title: Hva er nytt eller endret i Dynamics 365 Human Resources, 9. august 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 9. august 2021.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c43ed654a07834ce31a1425762f29c53aa2a020
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689277"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources, 9. august 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Microsoft Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4393.

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem | beskrivelse |
| --- | --- | --- |
| 558385 | Standard utpekt person blir ikke valgt når alternativet **Velg utpekte personer automatisk** er aktivert for standard utvalgte personer. | Dette problemet er nå løst. Flere standard utvalgte personer velges automatisk i kvalifiserte planer når alternativet **Velg utpekte personer automatisk** på siden **Delte parametere for Human Resources** er aktivert. |
| 589617 | På siden **Fridager** er saldoene for **Tilgjengelig for kjøp** og **Tilgjengelig for salg** tomme når tilgang er begrenset til et bestemt firma. | Dette problemet er nå løst. Siden **Fridager** viser de korrekte saldoene for **Tilgjengelig for kjøp** og **Tilgjengelig for salg** når brukeren er begrenset til et bestemt firma. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om hvordan du aktiverer eller deaktiverer funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)|
| Aktivere fraværsbehandling for å administrere permisjon | [Aktivere fraværsbehandling for å administrere permisjon](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | I denne versjonen oppdaterer vi visningen av arbeidsområdet for fraværsadministrasjon. Hvis du vil ha mer informasjon, kan du se [Konfigurer fraværsbehandlingsrollen](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Konfigurere vedleggskrav per permisjonstype | [Konfigurere vedleggskrav per permisjonstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurere permisjons- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Konfigurer permisjonsenheter per permisjonstype | [Konfigurer permisjonsenheter per permisjonstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurere permisjons- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gjør det mulig for ansatte å merkes som klare til betaling | [Gjør det mulig for ansatte å merkes som klare til betaling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til betaling](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Kommer snart

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funksjon | Detaljer |
| --- | --- |
| Platform update 10.0.21 (45) | Utrullingen av plattformoppdatering 10.0.21 er planlagt å begynne med serviceversjon 4. oktober 2021. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.21 av økonomi- og driftsapper (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
