---
title: Dataverse-tabeller
description: Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838589"
---
# <a name="dataverse-tables"></a>Dataverse-tabeller


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources bruker Dataverse til å aktivere scenarioer for utvidbarhet og integrering.

> [!NOTE]
> Human Resources-enheter tilsvarer Dataverse-tabeller. Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Følgende Dataverse-tabeller er tilgjengelige på Human Resources-enheter.

Hvis du vil ha mer informasjon om de kjente problemene, kan du se [Problemsøk i Lifecycle Services (LCS)](/dev-itpro/lifecycle-services/issue-search-lcs).

## <a name="benefit-tables"></a>Fordelstabeller

| Navn | Tabell | Kjente problemer  | Status |
| --- | --- |    --------|----------  |
| Beregningsfrekvens for fordeler | cdm_benefitcalculationfrequency |     |     |
| Lønnsperiode i fordelsberegningsfrekvens | cdm_benefitcalculationfrequencypayperiod |     |     |
| Beregningssats for fordeler | cdm_benefitcalculationrate |    |     |
| Detaljer om beregningssats for fordeler | cdm_benefitcalculationratedetail |753225 | Løst  |
| Fordelsalternativ | cdm_benefitoption |    |     |
| Fordelsplan | cdm_benefitplan (ikke aktivert for støtte for egendefinerte felt) |    |     |
| Fordelstype | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>Tabeller for forretningsprosessoppgaver

| Navn | Tabell |Kjente problemer  | Status |
| --- | --- |   --------|----------   |
| Forretningsprosesskalender | cdm_businessprocesscalendar | 751867 | Løst |
| Tilordning av forretningsprosessgruppe | cdm_businessprocessgroupassignment | 751869  751863 | Aktive|
| Oppgavegruppe for forretningsprosessbibliotek | cdm_businessprocesslibrarytaskgroup |751866 | Forseglet |
| Forretningsprosessfase | cdm_businessprocessstage |      |     |
| Topptekst for sjekklistemal | cdm_businessprocesstemplateheader |     |     |
| Oppgave for sjekklistemal | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>Kompensasjonstabeller

| Navn | Tabell |Kjente problemer  | Status |
| --- | --- | ----------      | -------    |
| Fast kompensasjonsplan | cdm_compensationfixedplan |754453 | Forseglet |
| Kompensasjonsrutenett | cdm_compensationgrid |             |     |
| Kompensasjonsnivå | cdm_compensationlevel |           |     |
| Kompensasjon, lønnsfrekvens | cdm_compensationpayfrequency |                  |     |
| Oppsett av referansepunkt for kompensasjon | cdm_compensationreferencepointsetup |               |     |
| Oppsettslinje for referansepunkt for kompensasjon | cdm_compensationreferencepointsetupline |             |     |
| Kompensasjonsområde | cdm_compensationregion |                   |     |
| Kompensasjonsstruktur | cdm_compensationstructure |    754456        | Forseglet    |
| Variabel kompensasjonsplan | cdm_compensationvariableplan |               |     |
| Nivå for variabel kompensasjonsplan | cdm_compensationvariableplanlevel |                |     |
| Type variabel kompensasjonsplan | cdm_compensationvariableplantype |               |     |
| Fast kompensasjonshendelse | cdm_fixedcompensationevent |               |     |
| Overdragelsesregel | cdm_vestingrule |              |     |
| Fast kompensasjon for arbeider | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>Organisasjonstabeller

| Navn | Tabell |Kjente problemer  | Status |
| --- | --- | ----------      | -------    |
| Avdeling | cdm_department |  752194    | Forseglet    |
| Ansettelse | cdm_employment | 762414  |  Forseglet  |
| Selskap | cdm_company |  |     |
| Stilling | cdm_job |  |     |
| Jobbfunksjon | cdm_jobfunction |        |     |
| stilling | cdm_jobposition | 752214      | Forseglet    |
| Stillingstype | cdm_positiontype |            |     |
| Stillingstilordning | cdm_positionworkerassignmentmap | 752224    |  Forseglet   |
| stillingsdimensjon | cdm_jobpositiondimension|       |     |
| Jobbtype | cdm_jobtype |      |     |
| Språk | cdm_language |        |     |
| Stillingstittel | cdm_title |       |     |

> [!NOTE]
> Finansdimensjoner for **Stillingstype**, **Stillingstilordning** og **Ansettelse** gir enveis integrering til Dataverse. Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Dataverse til Human Resources. 

## <a name="leave-and-absence-tables"></a>Tabeller for permisjon og fravær

| Navn | Tabell | Kjente problemer  | Status |
| --- | --- |   ----------      | -------    |
| Banktransaksjon for permisjon | cdm_leavebanktransaction |  752252    |    Løst |
| Permisjonsregistrering | cdm_leaveenrollment |  752934    |Forseglet     |
| Permisjonsplan | cdm_leaveplan |   752232   |   Forseglet  |
| Permisjonsforespørsel | cdm_leaverequest | 753207     | Forseglet    |
| Detaljer for fraværsforespørsel | cdm_leaverequestdetail | 753207     |   Forseglet  |
| Permisjonstype | cdm_leavetype |      |     |
| Årsakskode for permisjonstype | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>Integreringen for dobbel skriving ved hjelp av Dataverse-tabeller for permisjon og fravær er bare tilgjengelig når funksjonen **Konfigurer flere permisjonstyper på én enkelt permisjonsplan** er aktivert i Microsoft Dynamics 365 Finance ved hjelp av **Funksjonsbehandling**. 

## <a name="payroll-tables"></a>Lønnstabeller

| Navn | Tabell |Kjente problemer  | Status |
| --- | --- |  ----------      | -------    |
| Lønnssyklus | cdm_paycycle |    |     |
| Lønnsperiode | cdm_payperiod |          |     |
| Inntektskode for lønn | cdm_payrollearningcode |   754458        |   Forseglet  |
| Bankkontobetaling | cdm_bankaccountdisbursement |    751904     |   Forseglet  |
| Avgiftsområde | cdm_taxregion |          |     |

## <a name="worker-tables"></a>Arbeidertabeller

| Navn | Tabell |Kjente problemer  | Status |
| --- | --- |----------      | -------    |
| Worker | cdm_worker |    751906    |    Forseglet |
| Arbeideradresse | cdm_workeraddress |   754465     |Forseglet     |
| Arbeiderens personopplysninger | cdm_workerpersonaldetail |   751906     |   Forseglet  |
| Personidentifikasjonsnummer for arbeider | cdm_workerpersonidentificationnumber |  766704      |   Forseglet  |
| Personidentifikasjonstype for arbeider | cdm_workerpersonidentificationtype |        |     |
| Arbeidskalender | cdm_workcalendar |        |     |
| Arbeidskalenderdag | cdm_workcalendarday |        |     |
| Helligdag i arbeidskalender |cdm_workcalendarholiday |        |     |
| Ferielinje for arbeidskalender | cdm_workcalendarholidayline |        |     |
| Tidsintervall for arbeidskalender | cdm_workcalendartimeinterval (ikke aktivert for støtte for egendefinerte felt) |        |     |
| Bankkonto for arbeider | cdm_workerbankaccount |        |     |

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
