---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (6. oktober 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 6. oktober 2020.
author: jcart1106
manager: tfehr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 036b43d8730b52bddc93c0fc3b47d9d62649e898
ms.sourcegitcommit: 2190be6c205d7d9e43bdb99b9190cc0112f9f093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5152179"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (6. oktober 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources. Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.3636.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjon er vanligvis tilgjengelig i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Ekstra innsikt i permisjonskalendere | [Gi ekstra innsikt i permisjonskalender-visninger](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Vise team- og firmakalender](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

>[!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem | beskrivelse |
| --- | --- | --- |
| 448806 | **Standard identifikasjonstype** eksporteres som **RecId** i HCM-parametere | Denne endringen i parameterene for Human Resources-enheten legger til en ekstra kolonne som viser **standard identifikasjonstype**. |
| 492923 | Oppgaveopptak lagres ikke i Lifecycle Services (LCS) | Du kan nå lagre oppgaveopptak i LCS. |
| 429950 | Fast kompensasjon utløper ikke riktig ved endring av plassering | Når du endrer posisjonen til en arbeider på siden **Overføring av arbeider**, ble sluttkompensasjonsdatoen angitt én dag før slutten av stillingen. Sluttdatoen for kompensasjon er den samme som stillingens sluttdato. |
| 467214 | **Lønnsbasert analyse** vises bare hvis **Navn på konverteringer av lønnssats** er satt til **Årlig** | Lønnsbaserte lønnssatser med et annet navn enn **Årlig** vises ikke i kompensasjonsanalyse. Med denne oppdateringen bruker kompensasjonsanalyse nå alle konverteringer av lønnssats. Når du kjører rapportene etter **Hver time** eller **Lønn**, blir konverteringer av lønnssats som bruker en annen periode enn hver time, inkludert i **Lønn**-filteret. Bare lønnssatser med en periode på **Hver time**, er inkludert i **Hver time**-filteret. |
| 482464 | Når du viser **Gjennomganger**, endres ikke **Detaljer**-visningen til rutenettvisning etter at du har brukt et filter | Når du har brukt et filter, vises gjennomgangsrutenettet som forventet. |
| 483184 | Human Resources genererer ikke permisjonsavsetninger når du velger **Basis for lag** som den **justerte startdatoen** i **Permisjonsregistrering**-posten |Den **justerte startdatoen** fylles ut og brukes ved generering av permisjoner.  |
| 509731 | Fritidsforespørsel for fremtidig fratrådt arbeider fører til feil hvis de brukes for fridager etter avslutningsdato | Fritidsforespørsler kan nå sendes til ansatte med en fremtidig avslutningsdato så lenge forespørselen er før avslutningsdatoen. |
| 510716 | Kompensasjonsanalyse inkluderer både mannlige og kvinnelige ansatte for **Gjennomsnittlig timelønn for menn** | I kompensasjonsanalyse inkluderte **Gjennomsnittlig timelønn for menn** på den **demografiske analysen av kompensasjon** gjennomsnittslønn for kvinner. Nå inneholder den bare dette for mannlige ansatte. |
| 511348 | Selvbetjeningsfordeler skal bare vise fordelsplaner som er gyldige fra i dag til slutten av fordelsperioden | Utløpte fordelsplaner ble vist for ansatte på siden for **fordelsregistrering**. Denne korrigeringen fjerner disse planene. |
| 512706 | Angi følgende felt til skrivebeskyttet:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Knappene **Legg til** og **Fjern** for dimensjonsdetaljer ble ikke aktivert riktig etter at handlingen ble fullført. Denne oppdateringen til **Detalj for stillingshandling** gjør feltene ikke-redigerbare etter at handlingen er fullført. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md) |
| Utvidede arbeidsflytforespørsler og -godkjenninger | [Forbedringer i arbeidsflyten for organisasjons- og personalstyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuelle enheter i Dataverse for Human Resources | [Utvide Dynamics 365 Human Resources-kjernedata i Dataverse](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Konfigurere virtuelle enheter for Dataverse](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Kommer snart

Følgende nye funksjoner er planlagt for fremtidig frigivelser:

- **Sjekklisteenheter inkludert i Dataverse**: Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Dataverse.

- **Årsakskoder for fordelsstyring**: Årsakskoder for fordelsstyring kombineres snart med eksisterende årsakskoder i Human Resources. Hvis du har opprettet årsakskoder i fordelsstyringen som er over 15 tegn, må du endre navnet på årsakskoden i skjemaet **Årsakskoder** for Fordelsbehandling slik at det består av 15 tegn eller mindre. Når du har oppdatert navnet, vises årsakskoden under det eksisterende årsakskodeskjemaet i Personaladministrasjon. Denne endringen vil være tilgjengelig i fremtiden, og vil ikke påvirke eksisterende funksjonalitet.

- **Egendefinerte koblinger i Lederselvbetjening**: For å støtte ledere utvider vi funksjoner i Lederselvbetjening. Vi legger til muligheten for å legge til egendefinerte koblinger i kategorien **Mitt team**. Denne funksjonen ligner på funksjonen for egendefinerte koblinger i kategorien **Min informasjon** i ansattselvbetjening. Hvis du vil ha mer informasjon, se [Egendefinerte koblinger i Lederselvbetjening](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2019-frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Tilleggsressurser

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2020 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)
