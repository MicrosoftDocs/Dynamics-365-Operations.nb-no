---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (08. juli 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 7/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8fe7bc33407bd5781d565f854c0f096766da5fc9
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555394"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (8. juli 2020)

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3382. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="database-logging"></a>Databaselogging

Med databaseloggføring kan du bestemme hvilke tabeller og felt som skal overvåkes. Du kan også fastslå hvilke hendelser som skal utløse endringssporing. Du kan bruke funksjonen for databaselogging for å se endringene over tid. Hvis du vil ha mer informasjon, se [Konfigurere og administrere databaselogging](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurere navnet på ansattselvbetjening

I **Parametere for Personale** kan du nå endre navnet på **Ansattselvbetjening**-arbeidsområdet til **Selvbetjening**. Hvis du vil ha mer informasjon, se [Endre navn på arbeidsområde for selvbetjening for ansatte](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Fordelsstyring åpner registreringstilgang utenfor perioden

Denne versjonen retter opp en feil der ansatte kan få tilgang til fordeler ved å åpne registrering utenfor registreringsperioden eller uten en levetidshendelse. Hvis du trenger demonstrasjon av åpen registrering i Ansattselvbetjening, må du derfor justere datoene for åpen registrering til i dag (eller tidligere) for å gjøre den tilgjengelig. Du kan endre denne innstillingen under **Fordelsbehandling > Regler og alternativperioder**.

## <a name="email-employee-enrollment-confirmation"></a>E-postbekreftelse på ansattregistrering

Du kan nå sende e-postmeldinger til ansatte etter at de har fullført sine fordelsvalg. Du kan enten sende en standardmelding eller bruke en organisasjonse-postmal. Disse innstillingene er under **Personalparametere > Fordelsbehandling**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Avbrutt permisjon vises fortsatt i kommende fridager i Personer-arbeidsområdet (441358)

Avbrutt permisjon vises ikke lenger i kommende fritid på permisjonskortene i **Personer**-arbeidsområdet.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Kan ikke bruke egenskapen for avdelingsenhet i PositionV2-enheten (456486)

Du kan nå legge til en avdeling uten å opprette en duplikat relasjon.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity bør bare bruke beregnet felt for pensjonsplaner (459779)

Når du eksporterer **PayrollWorkerEnrolledBenefitDetailEntity**-enheten, bestemmer eksporten om den skal bruke et beregnet felt basert på en rentetabell eller bruke **ContributionAmountCur**-feltet i backing-tabellen. Logikken som brukes av dataenheten, bruker pristabellen i situasjoner der programmet vanligvis ikke gjør det. Denne logikken gjør at enheten eksporterer for å returnere en nullverdi for denne kolonnen, fordi det ikke er noen pristabell for beregning, og produktet tillater ikke at kunden angir en.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Forvirrende oversettelser i tsjekkisk språk i Personaladministrasjon og Ansattselvbetjening (400276)

Denne versjonen korrigerer oversettelsene for **Firmakatalog**, **Neste registrerte kurs**, **Jobb** og **Stilling**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>WorkCalendarEmployment-tabellen har ikke de opprettede og endrede systemfeltene aktivert (460171)

Opprettede og endrede systemfelt er nå aktivert i tabellen **WorkCalendarEmployment** i Human Resources.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Nullreferanseunntak for ansettelse og tillegging av informasjon for fremtidige ansatte (455475)

Denne versjonen korrigerer en feil (nullreferanse) i strømlinjeformet ansattregistrering når du ansetter en person ved hjelp av alternativet for **Ansett og legg til detaljer**.

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a>Endringer som er gjort i arbeiderenheten i Common Data Service, gjenspeiles ikke i Human Resources (455652)

Endringer som er gjort i følgende felt i **Arbeider**-enheten i Common Data Service, vises nå i Human Resources:

- **Fungerer hjemmefra**
- **Ansiennitetsdato**
- **Jubileumsdato**
- **Opprinnelig ansettelsesdato**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Riktig kompensasjonsnivå går ikke til standarden basert på jobben som er tilordnet til stillingen (394136)

Med denne endringen går det riktige kompensasjonsnivået til standarden basert på **Gyldig dato**-poster for **Stillingsdetaljer** og **Startdatoen** for **Kompensasjonsplantilordningen**.

## <a name="in-preview"></a>I forhåndsvisning

## <a name="mandatory-fields"></a>Obligatorisk felt 

Du kan nå endre feltene ved hjelp av tilpasningsfunksjonene i Human Resources. Denne funksjonen krever **Lagrede visninger**.

## <a name="human-resources-application-in-teams"></a>Human Resources-søknad i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. For mer informasjon, se [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF)-enheter for Fordelsbehandling
 
Enheter for fordelsstyring frigis. DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling. En mal for fordelsbehandling vil være tilgjengelig for å flytte data. Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.

## <a name="buy-and-sell-leave"></a>Kjøp og selg permisjon 

Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon. Denne prosessen behandles ofte manuelt. Denne funksjonen automatiserer behandling av policyer og forespørsler for personalavdelingen. Den strømlinjeformer permisjonsstyringsprosessen og bidrar til å eliminere feil. Hvis du vil ha mer informasjon, kan du se:

- [Administrere policyer for kjøp og salg av permisjon](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kjøp og selg permisjon](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Permisjonsavsetning for ett enkelt firma eller én enkelt plan

Kunder kan behandle avsetninger for ett enkelt firma eller en enkel permisjons- og fraværsplan. Denne muligheten gir klarhet for avsetningsprosessen for kunder med forskjellige policyer for fraværsår eller permisjonsavsetning. Hvis du vil ha mer informasjon, se [Avsett permisjon per firma eller per permisjonsplan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

## <a name="add-attachments-to-time-off-requests"></a>Legge til vedlegg i fraværsforespørsler

Muligheten til å legge til vedlegg i godkjente permisjonsforespørsler er viktig i det gjeldende COVID-19-miljøet. Ansatte kan nå legge til disse vedleggene. De har også mer innsikt i hvordan det gjøres oppdateringer for permisjonsforespørsler. Hvis du vil ha mer informasjon, kan du se [Legge til et vedlegg i en eksisterende forespørsel](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Legge til årsakskode for avsetningsuspensjoner 

Årsakskoder er lagt til i avsetningssuspensjonen.

## <a name="carry-forward-rules"></a>Overføringsregler 

Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres. Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Avbryte permisjonsavsetning for angitte permisjonstyper

Du kan opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales. Fravær som ikke betales, kan være en type, men behøver ikke å være det. Du kan stoppe enhver permisjon basert på en annen permisjonstype.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhet tilgjengelig for avsetningssuspensjoner 

En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.

## <a name="coming-soon"></a>Kommer snart

## <a name="checklist-entities-included-in-common-data-service"></a>Sjekklisteenheter inkludert i Common Data Service

Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Common Data Service.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)
