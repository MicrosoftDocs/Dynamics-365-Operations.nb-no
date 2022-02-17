---
title: Dataverse-tabeller
description: Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6774fad3543d80d04faacf5960c8037f1734f084
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066831"
---
# <a name="dataverse-tables"></a>Dataverse-tabeller


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.

> [!NOTE]
> Human Resources-enheter tilsvarer Dataverse-tabeller. Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Følgende Dataverse-tabeller er tilgjengelige på Human Resources-enheter.

## <a name="benefit-tables"></a>Fordelstabeller

| Navn | Tabell |
| --- | --- |
| Beregningsfrekvens for fordeler | cdm_benefitcalculationfrequency |
| Lønnsperiode i fordelsberegningsfrekvens | cdm_benefitcalculationfrequencypayperiod |
| Beregningssats for fordeler | cdm_benefitcalculationrate |
| Detaljer om beregningssats for fordeler | cdm_benefitcalculationratedetail |
| Fordelsalternativ | cdm_benefitoption |
| Fordelsplan | cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt) |
| Fordelstype | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Tabeller for forretningsprosessoppgaver

| Navn | Tabell |
| --- | --- |
| Forretningsprosesskalender | cdm_businessprocesscalendar |
| Tilordning av forretningsprosessgruppe | cdm_businessprocessgroupassignment |
| Oppgavegruppe for forretningsprosessbibliotek | cdm_businessprocesslibrarytaskgroup |
| Forretningsprosessfase | cdm_businessprocessstage |
| Topptekst for sjekklistemal | cdm_businessprocesstemplateheader |
| Oppgave for sjekklistemal | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Kompensasjonstabeller

| Navn | Tabell |
| --- | --- |
| Fast kompensasjonsplan | cdm_compensationfixedplan |
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

## <a name="organization-tables"></a>Organisasjonstabeller

| Navn | Tabell |
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
> Finansdimensjoner for **Stillingstype**, **Stillingstilordning** og **Ansettelse** gir enveis integrering til Dataverse. Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Dataverse til Human Resources. 

## <a name="leave-and-absence-tables"></a>Tabeller for permisjon og fravær

| Navn | Tabell |
| --- | --- |
| Banktransaksjon for permisjon | cdm_leavebanktransaction |
| Permisjonsregistrering | cdm_leaveenrollment |
| Permisjonsplan | cdm_leaveplan |
| Permisjonsforespørsel | cdm_leaverequest |
| Detaljer for fraværsforespørsel | cdm_leaverequestdetail |
| Permisjonstype | cdm_leavetype |
| Årsakskode for permisjonstype | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Lønnstabeller

| Navn | Tabell |
| --- | --- |
| Lønnssyklus | cdm_paycycle |
| Lønnsperiode | cdm_payperiod |
| Inntektskode for lønn | cdm_payrollearningcode |
| Bankkontobetaling | cdm_bankaccountdisbursement |
| Avgiftsområde | cdm_taxregion |

## <a name="worker-tables"></a>Arbeidertabeller

| Navn | Tabell |
| --- | --- |
| Worker | cdm_worker |
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

## <a name="worker-setup-tables"></a>Tabeller for arbeideroppsett

| Navn | Tabell |
| --- | --- |
| Veteranstatus | cdm_veteranstatus |
| Etnisk opprinnelse | cdm_ethnicorigin |
| Årsakskode | cdm_reasoncode |
| Utstedende byrå for personidentifikasjon | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Kompetansetabeller

| Navn | Tabell |
| --- | --- |
| Kompetansetype | cdm_skilltype |

## <a name="table-relationship-models"></a>Tabellrelasjonsmodeller

### <a name="worker"></a>Worker

![Arbeider.](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Jobb og stilling

![Jobb og stilling.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Fordeler

![Fordeler.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensasjon

![Kompensasjon.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Ferie

![Ferie.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbeidskalender

![Arbeidskalender.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Se også

[Velg en dataintegreringsteknologi](hr-admin-integration-choose-technology.md)<br>
[Konfigurere Dataverse-integrering](hr-admin-integration-common-data-service.md)<br>
[Konfigurere virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Vanlige spørsmål om virtuelle tabeller for Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologioppdateringer](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
