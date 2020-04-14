---
title: Common Data Service-enheter
description: Microsoft Dynamics 365 Human Resources bruker Common Data Service til å aktivere scenarioer for utvidbarhet og integrering.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166504"
---
# <a name="common-data-service-entities"></a>Common Data Service-enheter

Microsoft Dynamics 365 Human Resources bruker Common Data Service til å aktivere scenarioer for utvidbarhet og integrering.

Hvis du vil ha mer informasjon om Common Data Service, kan du se [Hva er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Følgende Human Resources-enheter er tilgjengelige i Common Data Service.

## <a name="benefit-entities"></a>Fordelsenheter

| Navn | Enhet |
| --- | --- |
| Fordelsberegningsfrekvens | cdm_benefitcalculationfrequency |
| Lønnsperiode i fordelsberegningsfrekvens | cdm_benefitcalculationfrequencypayperiod |
| Beregningssats for fordeler | cdm_benefitcalculationrate |
| Detaljer om beregningssats for fordeler | cdm_benefitcalculationratedetail |
| Fordelsalternativ | cdm_benefitoption |
| Fordelsplan | cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt) |
| Fordelstype | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Enheter for forretningsprosessoppgaver

| Navn | Enhet |
| --- | --- |
| Forretningsprosesskalender | cdm_businessprocesscalendar |
| Tilordning av forretningsprosessgruppe | cdm_businessprocessgroupassignment |
| Oppgavegruppe for forretningsprosessbibliotek | cdm_businessprocesslibrarytaskgroup |
| Forretningsprosessfase | cdm_businessprocessstage |
| Topptekst for sjekklistemal | cdm_businessprocesstemplateheader |
| Oppgave for sjekklistemal | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Kompensasjonsenheter

| Navn | Enhet |
| --- | --- |
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
| Fast kompensasjonshendelse | cdm_fixedcompensationevent |
| Overdragelsesregel | cdm_vestingrule |
| Fast kompensasjon for arbeider | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Organisasjonsenheter

| Navn | Enhet |
| --- | --- |
| Avdeling | cdm_department |
| Ansettelse | cdm_employment |
| Bedrift | cdm_company |
| Stilling | cdm_job |
| Jobbfunksjon | cdm_jobfunction |
| stilling | cdm_jobposition |
| Stillingstype | cdm_positiontype |
| Stillingstilordning | cdm_positionworkerassignmentmap |
| stillingsdimensjon | cdm_jobpositiondimension|
| Jobbtype | cdm_jobtype |
| Språk | cdm_language |
| Stillingstittel | cdm_title |

> [!NOTE]
> Finansdimensjoner for **Stillingstype**, **Stillingstilordning** og **Ansettelse** gir enveis integrering til Common Data Service. Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Common Data Service til Human Resources. 

## <a name="leave-and-absence-entities"></a>Permisjons- og fraværsenheter

| Navn | Entity |
| --- | --- |
| Banktransaksjon for permisjon | cdm_leavebanktransaction |
| Permisjonsregistrering | cdm_leaveenrollment |
| Permisjonsplan | cdm_leaveplan |
| Permisjonsforespørsel | cdm_leaverequest |
| Detaljer for fraværsforespørsel | cdm_leaverequestdetail |
| Permisjonstype | cdm_leavetype |
| Årsakskode for permisjonstype | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Lønnsenheter

| Navn | Enhet |
| --- | --- |
| Lønnssyklus | cdm_paycycle |
| Lønnsperiode | cdm_payperiod |
| Inntektskode for lønn | cdm_payrollearningcode |
| Bankkontobetaling | cdm_bankaccountdisbursement |
| Avgiftsområde | cdm_taxregion |

## <a name="worker-entities"></a>Arbeiderenheter

| Navn | Enhet |
| --- | --- |
| Arbeider | cdm_worker |
| Arbeideradresse | cdm_workeraddress |
| Arbeiderens personopplysninger | cdm_workerpersonaldetail |
| Personidentifikasjonsnummer for arbeider | cdm_workerpersonidentificationnumber |
| Personidentifikasjonstype for arbeider | cdm_workerpersonidentificationtype |
| Arbeidskalender | cdm_workcalendar |
| Arbeidskalenderdag | cdm_workcalendarday |
| Helligdag i arbeidskalender |cdm_workcalendarholiday |
| Ferielinje for arbeidskalender | cdm_workcalendarholidayline |
| Tidsintervall for arbeidskalender | cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt) |
| Bankkonto for arbeider | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>Enheter for arbeideroppsett

| Navn | Enhet |
| --- | --- |
| Veteranstatus | cdm_veteranstatus |
| Etnisk opprinnelse | cdm_ethnicorigin |
| Årsakskode | cdm_reasoncode |
| Utstedende byrå for personidentifikasjon | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Kompetanseenheter

| Navn | Enhet |
| --- | --- |
| Kompetansetype | cdm_skilltype |

## <a name="entity-relationship-models"></a>Enhetsrelasjonsmodeller

### <a name="worker"></a>Arbeider

![Arbeider](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Jobb og stilling

![Jobb og stilling](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Fordeler

![Fordeler](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensasjon

![Kompensasjon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Permisjon

![Permisjon](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbeidskalender

![Arbeidskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Se også

[Velge en dataintegreringsteknologi](hr-admin-integration-choose-technology.md)</br>
[Konfigurere Common Data Service-integrering](hr-admin-integration-common-data-service.md)
