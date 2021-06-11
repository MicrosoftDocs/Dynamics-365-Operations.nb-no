---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 21 januar 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 21. januar 2021.
author: marcelbf
ms.date: 01/21/2021
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
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 81586fbe996d526e9581bc052c93feafbbc42fc1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054889"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 21 januar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.3866.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Platform update 10.0.16(40) | -- | [Plattformoppdateringer for versjon 10.0.16 av Finance and Operations-apper (februar 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| Utvidede arbeidsflytforespørsler og -godkjenninger | [Forbedringer i arbeidsflyten for organisasjons- og personalstyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| ACA-samsvarsoppdateringer for skjema 1095-C, skjema 1095-B og elektronisk rapportering i eldre fordeler | -- | -- | 
| Fordelsbehandling støtter nå ACA-samsvarsrapportering for USA-baserte juridiske enheter | -- | [Generere ACA-rapporter i fordelsbehandling](hr-benefits-management-aca-reports.md) |
| Fordelsbehandling har nå enheter for fordelssatslag og dobbelt nivå for fordelssats eksponert  | -- | -- |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem |  beskrivelse |
| --- | --- | --- |
| 533079 | Navigasjonsfeil "Skjemaet ble kalt ved en feil" når vi prøver å se på fradrag. | Korrigerte feil da du så på fordelsfradrag med visningen **Per dato**. |
| 543641 | Postnummeret fylles ikke ut ved elektronisk rapportering.  | Korrigerte en intern feil der postnummeret ikke ble vist i elektroniske ACA-rapporter for fordelsstyring når dekningskoden er M til Q. |
| 542815 | Personlig kontaktskjerm i Ansattselvbetjening lar ansatte se andres personlige kontakter. | Korrigerte feil der **Rediger**-skjemaet for personlige kontakter i Ansattselvbetjening ikke begrenser spørringen nok til å garantere at bare én enkelt personlig kontakt hentes, slik at en bruker kan bruke hurtigtaster til å vise andres kontakter. |
| 536157 | Kan ikke åpne siden **Microsoft Dataverse-integrering** i Systemadministrasjon på grunn av kallet IsVirtualEntityPackageInstalled(). | Problemet forhindrer at siden for **Microsoft Dataverse-integrering** lastes i Human Resources. |
| 533079 | Navigasjonsfeil "Skjemaet ble kalt ved en feil" når vi prøver å se på fradrag. | Korrigerte feil som oppstod i **Fradrag**-skjemaet for fordelsbehandling ved visning **Per dato**. |
| 537264 | **Personlig informasjon**-hurtigfanen mangler fra kandidatpost. | Personlig informasjon for kandidaten er nå tilgjengelig på kandidatposten. |
| 537267 | **Yrkeserfaring** vises ikke på interne kandidatposter. | Hurtigfanen **Yrkeserfaring** vises nå på interne kandidatposter. Tidligere, hvis kandidaten var intern, ble **Yrkeserfaring** erstattet med **Ansettelseshistorikk**, som er kandidatens ansettelseshistorikk i organisasjonen. Begge gjelder og må vises for interne kandidater. |
| 537067 | **Kan kontakte arbeidsgiver** vises ikke. | **Kan kontakte arbeidsgiver**-kontrollen ble lagt til i ruten **Rediger yrkeserfaring** for en kandidatpost. |
| 525957 | **Kandidatstatus** oppdateres ikke for interne kandidater når overføringen er fullført. | Når en overføring er fullført (**Endre stilling**- eller **Fortsett**-knappen er valgt på siden **Overfør arbeider til en ny posisjonstilordning**), må **Status** for kandidatposten endres til **Ansatt**. |
| 537051 | Valutasymboler for indiske rupi og tyrkiske lire synkroniseres ikke riktig til Dataverse | Symboler for indiske rupi og tyrkiske lire synkroniseres nå ikke riktig til Dataverse. |
| 534846 | Rekrutteringstabeller må aktiveres for dataadministrasjon. | De nye tabellene som opprettes for rekrutteringsforespørsler og kandidater, aktiveres nå for dataadministrasjon. Dette gjør at endringssporing kan aktiveres for tabellene, slik at OData-endringssporingen aktiveres i de virtuelle Dataverse-tabellene. |
| 533474 | Reparerte manglende referanse til Microsoft.SqlServer.XEvent.dll. | Samlingsbelastningsunntak for Microsoft.SqlServer.XEvent.dll blokkerte virtuelle Dataverse-tabeller fra å bli konfigurert i noen miljøer. |
| 481122 | Arbeidsområdet **Personer** som viser avsluttede stillinger. | Avsluttede stillinger ble vist som åpne stillinger i arbeidsområdet **Personer**. Avsluttede stillinger vises ikke lenger. | 
| 541978 | Legg til primær e-postadresse i BaseWorker-enhet. | Denne endringen ble lagt til arbeiderens primære e-postadresse i HcmWorkerBaseEntity. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)<br>[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md) |
| Integrasjon med LinkedIn Talent Hub | [Integrasjon med LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrere med LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| Visning av permisjon for ledere på tvers av firmaer | [Visning av ansattpermisjon for ledere på tvers av firmaer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere permisjons- og fraværsparametere](./hr-leave-and-absence-parameters.md) |
|Gi ekstra innsikt i permisjonssaldoer| [Gi ekstra innsikt i permisjonssaldoer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Administrere ansattpermisjon](./hr-leave-and-absence-manage-employee-leave.md) |
| Ledere kan sende inn rekrutteringsforespørsler for stillinger | [Ledere kan sende inn en rekrutteringsforespørsel for åpne stillinger](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Legg til en rekrutteringsforespørsel](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Forbedret kandidatprofil i Personalstyring | [Forbedret kandidatprofil i personalstyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Legg til eller rediger en kandidatprofil](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Aktiver forenklede integreringer med rekrutteringsleverandører | [Aktiver forenklede integreringer med rekrutteringsleverandører](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Rekruttere jobbkandidater](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Kommer snart
| Funksjon | Detaljer |
| --- | --- |
| E-postbekreftelse for fordelsregistreringer | Denne funksjonen vil gi et alternativ for å sende en bekreftelses-e-post til ansatte når de sjekker ut fra fordelsregistreringen i Ansattselvbetjening. Hvis du vil ha mer informasjon, kan du se [Konfigurere fordelsstyringsparametre per firma](hr-benefits-setup-parameters-per-company.md). |
| Ferdigheter som angis av en leder for de ansatte, kan godkjennes automatisk av en arbeidsflyt | Kommer snart. |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologioppdateringer for Microsoft Dataverse

I november 2020 endret Common Data Service navn til [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Se den [offisielle kunngjøringen](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) på Power Apps-bloggen for å få mer informasjon. Sammen med denne navneendringen er noe terminologi i Dataverse oppdatert. *Enhet* er nå for eksempel *tabell* og *felt* er nå *kolonne*. Hvis du vil ha mer informasjon, kan du se [Terminologioppdateringer](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

I denne versjonen har terminologien knyttet til Dynamics 365 Human Resources-integreringen med Dataverse, blitt oppdatert i hele programmet for å gjenspeile disse endringene. Skjemaet for **Common Data Service-integrering** er eksempelvis nå **Microsoft Dataverse-integrering**.

Hvis du vil lære mer om Dynamics 365 Human Resources-integrering med Microsoft Dataverse, kan du se [Konfigurere Microsoft Dataverse-integrering](./hr-admin-integration-common-data-service.md) og [Konfigurere virtuelle Microsoft Dataverse-tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2020 for Dynamics 365 Human Resources](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]