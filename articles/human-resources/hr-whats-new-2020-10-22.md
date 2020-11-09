---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 22. oktober 2020
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: jcart1106
manager: tfehr
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5c66d8695ee0ff41e81c699a5d5a37075470059
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107542"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 22. oktober 2020

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources. Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.3680.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Platform update 10.0.14(38) | -- | [Plattformoppdateringer for versjon 10.0.14 av Finance and Operations-apper (november 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| Forbedringer i arbeidsflyt for organisasjons- og personalstyring | [Forbedringer i arbeidsflyten for organisasjons- og personalstyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer| Problem  | beskrivelse|
| --- | --- | --- |
| 437922 | Import av FMLA-timer ved hjelp av DMF-enheten resulterer i en skrivebeskyttelsesfeil. | Bruk av FMLA-timer-enheten til å importere timer knyttet til en FMLA-sak mislyktes. Vi har lagt til logikk for å sikre at timene som importeres, ikke overskrider timene som gjenstår for saken. |
| 512019 | Feil **Siste overføring** -beløp. | Hvis du på **Fridager** -siden endrer **Per dato** til den første dagen i den neste regnskapsperioden, vises et feil **Siste overføring** -beløp for typen **Årlig permisjon**. Nå vises det riktig beløp. |
| 458639 | Enhten for **arbeiderkontakter** støtter ikke endringssporingsmodus. | Vi har oppdatert **Arbeiderkontakter** -enheten slik at du kan bruke den i BYOD-scenarioer.|
| 505347 | Opplæringsledere kan sende en permisjonsforespørsel for en ansatt når funksjonen for strømlinjeformet arbeider var aktivert. | Andre roller enn personalassistent eller personalsjef kan ikke sende fraværsforespørsler for ansatte. |
| 513490 | Logging for fordelsadministrasjon: Legg til logging for planer uten dekningsalternativer. | Vi har aktivert resultater av logging for **Plan uten dekningsalternativer**. De vises nå i tabellen **Prosessresultater** , og de blir sortert riktig slik at de vises øverst. |
| 517021 | Kan ikke velge flere planer med samme **Plantype** -kode hvis **Plantype** har én registrering per type. | Vi endret begrensningene for å velge planer der bare én registrering er tillatt. Begrensningene er nå på **plantypekode** -nivå i stedet for **plantype**. Denne endringen tillater planer som HSA og FSA, som begge er samme type, men du kan gi dem en separat **plantypekode**. På denne måten kan du velge begge for den samme registreringsperioden. |
| 444791 | Kan ikke vise kompensasjon i Ansattselvbetjening når **Begrens tilgang** er aktivert i kompensasjonsplanen. | På **Kompensasjon** -kortet i ansattselvbetjeningen viste det gjeldende kompensasjonsbeløpet og økningsprosenten "0" hvis den ansatte ble registrert i en plan med **Begrenset tilgang** aktivert og tilordnet til bestemte roller. Vi har løst dette problemet, slik at ansatte og ledere alltid kan se kompensasjonsdetaljer for seg selv og deres direkte underordnede. |
| 457542 | Oppdatering av kursdetaljer etter at kurset er lukket, oppdaterer ikke også den samme informasjonen for den ansatte som tok kurset. | Ansattinformasjonen oppdateres nå på riktig måte når du endrer kursdetaljer etter at et kurs er lukket og åpnet på nytt. |
| 515342 | Kan ikke sette inn data via **CDSLeaveRequestDetailEntity**. Firma blir ikke funnet eller finnes ikke. | Du kan nå bruke **CDSLeaveRequestDetailEntity** til å sette inn data. |
| 514743 | Feil i skjemaet **E-postparameter** når du bruker Microsoft Exchange. | Meldingen "Kan ikke laste inn filer eller samling..." vises på siden **E-postparametere** når e-postleverandøren var satt til **Exchange**. Denne korrigeringen tillater også at siden **E-postparametere** lastes inn og lagres som forventet. |


## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md) |
| Utvidede arbeidsflytforespørsler og -godkjenninger | [Forbedringer i arbeidsflyten for organisasjons- og personalstyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuelle enheter i Common Data Service for Human Resources | [Utvide Dynamics 365 Human Resources-kjernedata i Common Data Service](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Konfigurere virtuelle enheter for Common Data Service](hr-admin-integration-common-data-service-virtual-entities.md) |
| Integrasjon med LinkedIn Talent Hub | [Integrasjon med LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrere med LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Egendefinerte koblinger i Lederselvbetjening | [Egendefinerte koblinger i Lederselvbetjening](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Egendefinerte koblinger i Lederselvbetjening](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>Kommer snart

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2020 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)
