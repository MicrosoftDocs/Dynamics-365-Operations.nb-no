---
title: Hva er nytt eller endret i Dynamics 365 Human Resources, 23. august 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 23. august 2021.
author: marcelbf
ms.date: 08/23/2021
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
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c9ee0206bd77a8a2ec42501d64e83077baef09
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441681"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources, 23. august 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Microsoft Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4419.

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem | beskrivelse |
| --- | --- | --- |
| 594066 | Kan ikke slette kontaktinformasjon | Når du velger å slette en kontaktinformasjonspost for en ansatt, blir en annen kontaktinformasjonspost enn den valgte posten slettet i stedet. |
| 611339 | Hvis du legger til en tilpasning, fører det til at bankkontoen ignorerer filteret og henter den første posten | Når du legger til en tilpasning, fører det til at bankkontolisten kjører en tilpasningsspørring etter at spørringen for datakilden er kjørt, noe som resulterer i at spørringen henter den øverste posten, uansett hvilken arbeider detaljene skal vises for. |
| 591806 | Oppgaver for forfallsdato som skal kobles inn, beregnes feil | Forfallsdatoer beregnes feil når følgende betingelser finnes: Kontrollistene som opprettes, bruker en kalender som bruker et utvidet tidsintervall (eksempel fra 2005 til 2050), og brukerens innstillinger benytter en annen tidssone enn normaltid. |   
| 592749 | Permisjonssaldoen er feil på **Ansattselvbetjening** | Hvis den ansatte er ansatt i mer enn én juridisk enhet og permisjonsvisning på tvers av firmaer er aktivert, kan permisjonssaldoen være feil. |
| 603133 | Uventet advarsel ved forespørsel om fritid | Når du ber om fri og fyller ut **Halvdags**-feltet før **Beløp**-feltet, fører det til en uventet advarsel. |
| 606546 | Merket felt vises ikke i Godkjent avspasering | Avmerkingsboksen for å velge flere godkjente permisjonsforespørsler, var ikke synlig. |
| 597059 | Arbeideren vises ikke i **permisjons- og fraværsfirmakalenderen** | En arbeider er ikke synlig i **permisjons- og fraværsfirmakalenderen** hvis det brukte datointervallet inkluderer en dag de har blitt avslått en permisjonsforespørsel for. |


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
| Platform update 10.0.21 (45) | Utrullingen av plattformoppdatering 10.0.21 er planlagt å begynne med serviceversjon 4. oktober 2021. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.21 av Finance and Operations-apper (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
