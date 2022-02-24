---
title: Hva er nytt eller endret i Dynamics 365 Talent (3. desember 2019)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528699"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (3. desember 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2646. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Arbeidsområde for funksjonsbehandling

Arbeidsområdet **Funksjonsbehandling** inneholder en liste over funksjoner som leveres i hver utgivelse. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem. Hvis du vil ha mer informasjon om funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager. Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden. Så snart du ser nye funksjoner i arbeidsområdet for **funksjonsbehandling**, kan du aktivere dem. Det kan hende at noen funksjoner er aktivert som standard.
 
Noen ganger vil en integrert funksjon være aktivert som standard og kan ikke deaktiveres (for eksempel arbeidsområdet **Funksjonsbehandling**).
 
Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer. Arbeidsområdet for **funksjonsbehandling** angir når en forhåndsvisningsfunksjon blir obligatorisk. Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene. De kan ikke deaktivere obligatoriske funksjoner. Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Legge til automatisk planlegging av opprydding i logg for satsvis jobb (332528)

Med denne endringen kjøres **Logg for satsvis jobb** hver natt og fjerner loggelementer for satsvis jobb som er eldre enn 30 dager.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent svarer ikke i arbeiderhandlinger når identifikasjonsnummerlengden ikke samsvarer med identifikasjonstypen (390971)

Denne versjonen korrigerer problemet når identifikasjonsnummerlengden ikke samsvarer med definisjonen i identifikasjonstypen. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Fast kompensasjon oppdaterer ikke nivået med endringer i stillingsdetaljer (348085)

I denne ukens utgivelse bestemmer **kompensasjons startdato** jobben som er knyttet til stillingen på det tidspunktet når du oppretter en ny fast kompensasjonspost for en ansatt.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Arbeidere, ansatte og leverandører-listene viser arbeidertype som begge når de bare skal være arbeider eller oppdragstaker (384473)

Denne endringen gjenspeiler nøyaktig hvilken type arbeider som er angitt (oppdragstaker eller ansatt).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>E-postvarsler for nye ansettelseshandlinger inneholder ikke navneinformasjon på grunn av sikkerhetspolicyer (383402)

Denne endringen korrigerer informasjonen som vises i feltene for fornavn eller etternavn i plassholderne for arbeidsflyt når avansert sikkerhet er aktivert.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Systemet tillater to heldags permisjonsforespørsler for samme dag (379284)

Med denne endringen kan du ikke utstede to permisjonsforespørsler for samme dag. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Adresseendringslisten skal sorteres etter ikrafttredelsesdato (352798)

Med denne endringen er adresseendringslisten nå sortert etter **ikrafttredelsesdato**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Permisjonsforespørsler bør tillate slettinger fra Common Data Service til Talent (376999)

Med denne endringen kan utkast til og avlyste permisjonsforespørsler slettes fra Common Data Service og så fjernet fra Talent.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Sletting av inntekstskoder er tillatt når den samme inntektskoden er tilordnet en ansatt (371792)

I denne versjonen må du først fjerne inntektskoden fra den ansatte før du sletter inntektskoden fra systemet.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Arbeidsflyt for permisjon og fravær med to godkjenningsstadier mislykkes å fullføre (391116)

Med denne endringen fortsetter arbeidsflyten for permisjon og fravær gjennom alle trinn når mer enn én godkjenningsfase er konfigurert for forespørselen.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Utstedelsesdatoen synkroniseres ikke til Common Data Service når oppdatert eller angitt i Talent (397361)

Denne endringen korrigerer et problem der utstedelsesdatoen for **Personidentifikasjon**-poster ikke ble synkronisert til Common Data Service fra Talent.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Sirkelreferansefeil for hierarki utstedt ved tilordning av en leder til en stilling (386659)

Denne endringen korrigerer et unikt scenario der en sirkelreferansefeil vises når du tilordner en ny leder til en stilling.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service-enheter som nå støtter egendefinerte felt

Følgende Common Data Service-enheter støtter nå egendefinerte felt:

| Navn | Enhet |
| --- | --- |
| Bankkontobetaling | cdm_bankaccountdisbursement |
| Fordelsberegningsfrekvens | cdm_benefitcalculationfrequency |
| Lønnsperiode i fordelsberegningsfrekvens | cdm_benefitcalculationfrequencypayperiod |
| Beregningssats for fordeler | cdm_benefitcalculationrate |
| Detaljer om beregningssats for fordeler | cdm_benefitcalculationratedetail |
| Fordelsalternativ | cdm_benefitoption |
| Fordelsplan | cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt) |
| Fordelstype | cdm_benefittype |
| Forretningsprosesskalender | cdm_businessprocesscalendar |
| Tilordning av forretningsprosessgruppe | cdm_businessprocessgroupassignment |
| Oppgavegruppe for forretningsprosessbibliotek | cdm_businessprocesslibrarytaskgroup |
| Forretningsprosessfase | cdm_businessprocessstage |
| Topptekst for sjekklistemal | cdm_businessprocesstemplateheader |
| Oppgave for sjekklistemal | cdm_businessprocesstemplatetask |
| Bedrift | cdm_company |
| Fast plan for kompensasjon | cdm_compensationfixedplan |
| Kompensasjonsrutenett | cdm_compensationgrid |
| Kompensasjonsnivå | cdm_compensationlevel |
| Kompensasjon, lønnsfrekvens | cdm_compensationpayfrequency |
| Oppsett av referansepunkt for kompensasjon | cdm_compensationreferencepointsetup |
| Oppsettslinje for referansepunkt for kompensasjon | cdm_compensationreferencepointsetupline |
| Kompensasjonsområde | cdm_compensationregion |
| Kompensasjonsstruktur | cdm_compensationstructure |
| Variabel kompensasjonsplan | cdm_compensationvariableplan |
| Nivå for variabel kompensasjonsplan | cdm_compensationvariableplanlevel |
| Type variabel kompensasjonsplan | cdm_compensationvariableplantype |
| Avdeling | cdm_department |
| Ansettelse | cdm_employment |
| Etnisk opprinnelse | cdm_ethnicorigin |
| Fast kompensasjonshendelse | cdm_fixedcompensationevent |
| Stilling | cdm_job |
| Jobbfunksjon | cdm_jobfunction |
| Jobbstilling | cdm_jobposition |
| Jobbtype | cdm_jobtype |
| Språk | cdm_language |
| Permisjonsbanktransaksjon | cdm_leavebanktransaction |
| Permisjonsregistrering | cdm_leaveenrollment |
| Permisjonsplan | cdm_leaveplan |
| Permisjonsforespørsel | cdm_leaverequest |
| Detaljer for fraværsforespørsel | cdm_leaverequestdetail |
| Permisjonstype | cdm_leavetype |
| Årsakskode for permisjonstype | cdm_leavetypereasoncode |
| Lønnssyklus | cdm_paycycle |
| Lønnsperiode | cdm_payperiod |
| Inntektskode for lønn | cdm_payrollearningcode |
| Utstedende byrå for personidentifikasjon | cdm_personidentificationissuingagency |
| Stillingstype | cdm_positiontype |
| Stillingstilordning | cdm_positionworkerassignmentmap |
| Årsakskode | cdm_reasoncode |
| Kompetansetype | cdm_skilltype |
| Avgiftsområde | cdm_taxregion |
| Overdragelsesregel | cdm_vestingrule |
| Veteranstatus | cdm_veteranstatus |
| Arbeidskalender | cdm_workcalendar |
| Arbeidskalenderdag | cdm_workcalendarday |
| Helligdag i arbeidskalender |cdm_workcalendarholiday |
| Ferielinje for arbeidskalender | cdm_workcalendarholidayline |
| Tidsintervall for arbeidskalender | cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt) |
| Arbeider | cdm_worker |
| Arbeideradresse | cdm_workeraddress |
| Bankkonto for arbeider | cdm_workerbankaccount |
| Fast kompensasjon for arbeider | cdm_workerfixedcompensation |
| Arbeiderens personopplysninger | cdm_workerpersonaldetail |
| Personidentifikasjonsnummer for arbeider | cdm_workerpersonidentificationnumber |
| Personidentifikasjonstype for arbeider | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>I forhåndsvisning

Forhåndsvisningsfunksjoner er bare tilgjengelige i **Sandkasse**-miljøer.

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.
