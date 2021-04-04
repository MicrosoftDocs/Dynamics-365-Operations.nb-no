---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 2. desember 2020
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 2. desember 2020.
author: marcelbf
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 89c5dbab58679dfe36f5eec0d6c5724f81c18523
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463460"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 2. desember 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.3788.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Ledere kan sende inn rekrutteringsforespørsler for stillinger | [Ledere kan sende inn en rekrutteringsforespørsel for åpne stillinger](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Legg til en rekrutteringsforespørsel](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Forbedret kandidatprofil i Personalstyring | [Forbedret kandidatprofil i personalstyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Legg til eller rediger en kandidatprofil](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Aktiver forenklede integreringer med rekrutteringsleverandører | [Aktiver forenklede integreringer med rekrutteringsleverandører](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Rekruttere jobbkandidater](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| Egendefinerte koblinger i Lederselvbetjening | [Egendefinerte koblinger i Lederselvbetjening](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Egendefinerte koblinger i Lederselvbetjening](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem | beskrivelse |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult bør inkludere DateTime som ble brukt i behandling. | BenefitEligibity-behandlingsresultatet inneholder nå datetimestamp for siste behandling, som manglet tidligere. |
| 526903 | Fordelsregistrering mislykkes for planer med avhengigheter når **Velg utpekte personer automatisk** er aktivert i **delte parametere for Human Resources**. | Løste problemet der fordelsregistreringen mislyktes for utpekte personer når alternativet **Velg utpekte personer automatisk** ble aktivert for standard utpekte personer. |
| 521922 | Parameteren **Vis fravær uten detaljer** viser detaljer om fridagerforespørsler i fraværskalenderen for team. | Permisjonstypen, permisjonstypefargen og dagsdetaljer ble vist i fraværskalenderen for team når **Vis fravær uten detaljer** er satt til **Ja** i **Parametere for permisjon og fravær**. Dette er tatt hånd om, og nå kan ikke permisjonstypen vises, og standardfarge for permisjonstype (mørk blå) brukes for alle permisjonstyper i fraværskalenderen for team. |
| 527316 | Tittelendringer for jobb-, stillings- og arbeidervarslinger synkroniseres ikke. | En tittelrelasjon ble tidligere lagt til jobb-, plasserings- og arbeiderenhetene. Synkroniseringen for denne relasjonen fungerer for synkroniseringen fra Human Resources til Dataverse, men fungerte ikke for varslinger fra Dataverse. Dette er tatt hånd om. |
| 512275 | Fjern fargealternativene fra **Parametere for permisjon og fravær**. | Nå som farger defineres på permisjonstypen, er ikke lenger fargeralternativene nødvendige i **Parametere for permisjon og fravær**, så de ble fjernet. |
| 437112 | Villedende feilmeldingstekst under tilordning av ansattplassering. | Oppdaterte feilmeldingen under ansettelse av en arbeider og forsøk på å tilordne arbeideren til en stilling som ikke er aktiv. Oppdatert meldingen **Den angitte stillingen er ikke aktiv på ansettelsesstartdatoen. Kontroller varigheten for denne stillingen.** |
| 527816 | Ytelsesproblemer med **Fridager**-siden. | Ytelsen er forbedret på **Fridager**-siden. |
| 523158 | BenefitPeriodMigrationUpgrade og BenefitPlanMigrationUpgrade kjører ikke. | Løste problemer med fordelsoverføringsjobber relatert til at **Periode** og **Planlegg** ikke kjørte riktig. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md) |
| Utvidede arbeidsflytforespørsler og -godkjenninger | [Forbedringer i arbeidsflyten for organisasjons- og personalstyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integrasjon med LinkedIn Talent Hub | [Integrasjon med LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrere med LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|Visning av permisjon for ledere på tvers av firmaer | [Visning av ansattpermisjon for ledere på tvers av firmaer](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere permisjons- og fraværsparametere](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Gi ekstra innsikt i permisjonssaldoer| [Gi ekstra innsikt i permisjonssaldoer](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Administrere ansattpermisjon](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Ledere kan sende inn rekrutteringsforespørsler for stillinger | [Ledere kan sende inn en rekrutteringsforespørsel for åpne stillinger](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Legg til en rekrutteringsforespørsel](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Forbedret kandidatprofil i Personalstyring | [Forbedret kandidatprofil i personalstyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Legg til eller rediger en kandidatprofil](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Aktiver forenklede integreringer med rekrutteringsleverandører | [Aktiver forenklede integreringer med rekrutteringsleverandører](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Rekruttere jobbkandidater](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Kommer snart

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2020 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]