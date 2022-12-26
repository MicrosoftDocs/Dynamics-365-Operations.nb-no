---
title: Konfigurer integrering med Dataverse-tabeller
description: Denne artikkelen beskriver integreringen mellom Microsoft Dynamics 365 Human Resources og Dataverse.
author: anschmidt
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63c25020b7026a76ecc6e2c3563f8299627ec8a8
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838629"
---
# <a name="configure-integration-with-dataverse-tables"></a>Konfigurer integrering med Dataverse-tabeller

>[!Important]
>Funksjonaliteten som er nevnt i denne artikkelen, er for øyeblikket tilgjengelig for kunder på Dynamics 365 Human Resources i Finance and Operations-infrastrukturen. 


Hvis du vil integrere Microsoft Dynamics 365 Human Resources med Dataverse, kan du bruke [dataintegratoren](/powerapps/administrator/data-integrator). Med Human Resources-til-Dataverse-malen kan data for jobber, stillinger, arbeidere og andre flyte fra Human Resources til Dataverse og fra Dataverse til Human Resources ved å opprette en skrive i begge systemene.

## <a name="system-requirements-for-human-resources"></a>Systemkrav for Human Resources

Integreringsløsningen krever følgende versjoner av Human Resources og Dynamics 365 Finance: 

- Dynamics 365 Finance versjon 7.2 og nyere
- Dynamics CRM-miljø der det er opprettet en database, og Dynamics 365-apper er tillatt

## <a name="template-and-tasks"></a>Mal og oppgaver

Følg denne fremgangsmåten for å få til gang til Human Resources-til-Finance-malen.

1. Åpne [Administrasjonssenter for Power Apps](https://admin.powerapps.com/). 
2. Velg **Dynamics 365-apper** under miljøet, og velg deretter **Appkilde** på verktøylinjen.
3. Hvis du vil installere malen, kan du søke etter Dobbel skriving i Human Resources, eller gå direkte til følgende adresse: <https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite>.
3. Når installasjonen er fullført, åpner du Dynamics 365 Finance.
4. Åpne arbeidsområdet **Databehandling**. 
5. Velg **Dobbel skriving**. 
6. Følg fremgangsmåten for å koble miljøet til minst ett firma i organisasjonen. 
7. Når du er ferdig med å konfigurere en kobling til Dataverse-miljøet, velger du **Bruk løsning**. Løsningen brukes, og tildelingene installeres i integratorappen.

## <a name="template-mappings"></a>Maltilordninger

I følgende maltildelingstabeller angir navnet på oppgaven at enhetene brukes i hvert program. Finance er til venstre, og Dataverse er til høyre.

### <a name="bank-account-disbursements-dual-write-to-bank-account-disbursement"></a>Bankkontobetalinger (dobbel skriving) til bankkontoutbetaling

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATIONID        | cdm\_bankaccountid.cdm\_accountidentification        |
| BELØP                         | cdm\_amount                                         |
| PRIORITET                       | cdm\_disbursementpriority                           |
| PERSONALNUMMER                | cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber    |
| REST                      | cdm\_isremainder                                    |

### <a name="benefit-calculation-rate-detail-dual-write-to-benefit-calculation-rate-detail"></a>Detaljer om beregningssats for fordeler (dobbel skriving) til Detaljer om beregningssats for fordeler

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| CONTRIBUTIONMETHOD             | cdm\_contributionmethod                             |
| GYLDIG                      | cdm\_effective                                      |
| EMPLOYERCONTRIBUTION           | cdm\_employercontribution                           |
| UTLØP                     | cdm\_expiration                                     |
| WORKERDEDUCTION                | cdm\_workerdeduction                                |
| NAVN                           | cdm\_calculationrateid.cdm\_name                     |

### <a name="benefit-calculation-rate-header-to-benefit-calculation-rate"></a>Hode for beregningssats for fordel til Beregningssats for fordeler

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| NAVN                           | cdm\_name                                           |
| TIERTYPE                       | cdm\_tiertype                                       |

### <a name="benefit-option-to-benefit-option"></a>Fordelsalternativ til Fordelsalternativ

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| ALLOWBENEFICIARYDESIGNATIONS   | cdm\_allowbeneficiarydesignations                   |
| ALLOWDEPENDENTCOVERAGE         | cdm\_allowdependentcoverage                         |
| BENEFITOPTIONID                | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| ISWAIVE                        | cdm\_iswaived                                       |

### <a name="benefit-type-to-benefit-type"></a>Fordelstype til fordelstype

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BENEFITTYPEID                  | cdm\_name                                           |
| CONCURRENTENROLLMENT           | cdm\_concurrentenrollment                           |
| BESKRIVELSE                    | cdm\_description                                    |
| PAYROLLCATEGORY                | cdm\_payrollcategory                                |

### <a name="business-calendar-to-business-process-calendar"></a>Forretningskalender til forretningsprosesskalender

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| NAVN                           | cdm\_calendarname                                   |
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| ISOPENMONDAY                   | cdm\_ismondayopen                                   |
| ISOPENTUESDAY                  | cdm\_istuesdayopen                                  |
| ISOPENWEDNESDAY                | cdm\_iswednesdayopen                                |
| ISOPENTHURSDAY                 | cdm\_isthursdayopen                                 |
| ISOPENFRIDAY                   | cdm\_isfridayopen                                   |
| ISOPENSATURDAY                 | cdm\_issaturdayopen                                 |
| ISOPENSUNDAY                   | cdm\_issundayopen                                   |

### <a name="business-process-to-business-process-header"></a>Forretningsprosess til forretningsprosesshode

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processid                                      |
| PROCESSTYPE                    | cdm\_processtype                                    |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| NAVN                           | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| STATUS                         | cdm\_status                                         |
| TARGETDATE                     | cdm\_targetdate                                     |
| STARTDATETIME                  | cdm\_startdatetime                                  |
| ENDDATETIME                    | cdm\_enddatetime                                    |
| RESOLVEDBYPERSONNELNUMBER      | cdm\_resolvedbyid.cdm\_workernumber                  |
| PROCESSOWNERPERSONNELNUMBER    | cdm\_processownerid.cdm\_workernumber                |
| SOURCETEMPLATENAME             | cdm\_sourcetemplateid.cdm\_name                      |
| SOURCETEMPLATEPROCESSTYPE      | cdm\_sourcetemplateid.cdm\_businessprocesstype       |
| SOURCETEMPLATEGENERICSUBTYPE   | cdm\_sourcetemplateid.cdm\_genericsubtype            |

### <a name="business-process-library-task-group-to-business-process-library-task-group"></a>Oppgavegruppe for forretningsprosessbibliotek til oppgavegruppe for forretningsprosessbibliotek

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_processtype                                    |
| NAVN                           | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |

### <a name="business-process-stage-to-business-process-stage"></a>Forretningsprosesstadium til forretningsprosesstadium

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| NAVN                           | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| SEQUENCENUMBER                 | cdm\_sequencenumber                                 |

### <a name="business-process-task-to-business-process-task"></a>Forretningsprosessoppgave til forretningsprosessoppgave

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| DUEDATE                        | cdm\_duedate                                        |
| TASKID                         | cdm\_taskid                                         |
| INSTRUKSJONER                   | cdm\_instructions                                   |
| COMPLETIONDATETIME             | cdm\_completiondatetime                             |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| NAVN                           | cdm\_name                                           |
| STATUS                         | cdm\_status                                         |
| RESOLVEDBY\_PERSONNELNUMBER     | cdm\_resolvedbyid.cdm\_workernumber                  |
| TEMPLATETASKID                 | cdm\_templatetaskid.cdm\_taskid                      |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedposition.cdm\_jobpositionnumber         |

### <a name="business-process-template-to-checklist-template-header"></a>Forretningsprosessmal til kontrollistemalhode

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| NAVN                           | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| CALENDARID                     | cdm\_businessprocesscalendarid.cdm\_name             |
| PERSONALNUMMER                | cdm\_processownerid.cdm\_workernumber                |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="business-process-template-task-to-checklist-template-task"></a>Oppgave for forretningsprosessmal til kontrollistemaloppgave

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| TASKID                         | cdm\_taskid                                         |
| NAVN                           | cdm\_name                                           |
| TEMPLATEHEADER\_PROCESSTYPE     | cdm\_businessprocesstemplateheaderid.cdm\_businessprocesstype |
| TEMPLATEHEADER\_GENERICSUBTYPE  | cdm\_businessprocesstemplateheaderid.cdm\_genericsubtype |
| TEMPLATEHEADER\_NAME            | cdm\_businessprocesstemplateheaderid.cdm\_name       |
| BESKRIVELSE                    | cdm\_description                                    |
| DUEDATEOFFSETDAYS              | cdm\_duedateoffsetdays                              |
| MENUITEMTYPE                   | cdm\_tasklinktype                                   |
| MENUITEM                       | cdm\_tasklink                                       |
| CONTACTPERSON\_PERSONNELNUMBER  | cdm\_contactpersonid.cdm\_workernumber               |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedpositionid.cdm\_jobpositionnumber       |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| INSTRUKSJONER                   | cdm\_instructions                                   |

### <a name="calculation-frequency-to-benefit-calculation-frequency"></a>Beregningsfrekvens til Beregningsfrekvens for fordeler

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| FREQUENCY                      | cdm\_name                                           |
| FREQUENCYCONTROL               | cdm\_frequencycontrol                               |
| ISIMMUTABLE                    | cdm\_isimmutable                                    |

### <a name="calculation-frequency-pay-period-to-benefit-calculation-frequency-pay-period"></a>Lønnsperiode i beregningsfrekvens til Lønnsperiode i fordelsberegningsfrekvens

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| CALCULATIONFREQUENCYID         | cdm\_benefitcalculationfrequencyid.cdm\_name         |
| PERIODSTARTDATE                | cdm\_payperiodid.cdm\_periodstartdate                |
| PAYCYCLEID                     | cdm\_payperiodid.cdm\_paycycleid.cdm\_name            |

### <a name="calendar-to-work-calendar"></a>Kalender til arbeidskalender

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| CALENDARNAME                   | cdm\_description                                    |
| WORKCALENDARHOLIDAYID          | cdm\_workcalendarholidayid.cdm\_name                 |

### <a name="compensation-fixed-action-table-to-fixed-compensation-event"></a>Kompensasjon, fast handlingstabell til Fast kompensasjonshendelse

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| HANDLING                         | cdm\_name                                           |
| AKTIV                         | cdm\_isactive                                       |
| BESKRIVELSE                    | cdm\_description                                    |
| TYPE                           | cdm\_eventtype                                      |

### <a name="compensation-fixed-plan-to-compensation-fixed-plan"></a>Fast kompensasjonsplan til fast kompensasjonsplan

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PLAN                           | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| TYPE                           | cdm\_type                                           |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VALUTA                       | cdm\_transactioncurrencyid.isocurrencycode          |
| PAYFREQUENCY                   | cdm\_payfrequency.cdm\_name                          |
| HIRERULE                       | cdm\_hirerule                                       |
| OUTOFRANGETOLERANCE            | cdm\_outofrangetolerance                            |
| RECOMMENDATIONALLOWED          | cdm\_recommendationallowed                          |
| COMPENSATIONSTRUCTURE          | cdm\_compensationgrid.cdm\_name                      |
| REFPOINTSETUPID                | cdm\_referencepointsetupline.cdm\_referencepointsetupid.cdm\_name |
| CONTROLPOINT                   | cdm\_referencepointsetupline.cdm\_name               |

### <a name="compensation-grids-to-compensation-grid"></a>Kompensasjonsrutenett til kompensasjonsrutenett

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| GRIDID                         | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| REFERENCESETUP                 | cdm\_referencepointsetupid.cdm\_name                 |
| TYPE                           | cdm\_type                                           |
| VALUTA                       | cdm\_transactioncurrencyid.isocurrencycode          |

### <a name="compensation-job-function-to-job-function"></a>Kompensasjon, jobbfunksjon til jobbfunksjon

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| JOBFUNCTIONID                  | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |

### <a name="compensation-job-type-to-job-type"></a>Kompensasjonsjobbtype til jobbtype

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| JOBTYPEID                      | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| EXEMPTSTATUS                   | cdm\_exemptstatus                                   |

### <a name="compensation-pay-frequency-to-compensation-pay-frequency"></a>Kompensasjon, lønnsfrekvens til kompensasjon, lønnsfrekvens

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PAYRATECONVERSION              | cdm\_name                                           |
| PERIODE                         | cdm\_period                                         |
| BESKRIVELSE                    | cdm\_description                                    |
| ANNUALCONVERSIONFACTOR         | cdm\_annualconversionfactor                         |
| HOURLYCONVERSIONFACTOR         | cdm\_hourlyconversionfactor                         |
| MONTHLYCONVERSIONFACTOR        | cdm\_monthlyconversionfactor                        |
| WEEKLYCONVERSIONFACTOR         | cdm\_weeklyconversionfactor                         |

### <a name="compensation-regions-to-compensation-region"></a>Kompensasjonsområder til kompensasjonsområde

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| LOKASJON                       | cdm\_name                                           |

### <a name="compensation-variable-plan-v2-to-compensation-variable-plan"></a>Variabel plan for kompensasjon V2 til variabel kompensasjonsplan

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| VARIABLEAWARDBASIS             | cdm\_awardbasis                                     |
| AWARDBASISCALCULATION          | cdm\_awardbasiscalculation                          |
| CALCULATIONTYPE                | cdm\_calculationtype                                |
| BESKRIVELSE                    | cdm\_description                                    |
| ENABLEENROLLMENT               | cdm\_enableenrollment                               |
| ENABLELEVELS                   | cdm\_enablelevels                                   |
| ENABLERECOMMENDATION           | cdm\_enablerecommendation                           |
| HIRERULE                       | cdm\_hirerule                                       |
| LEVERAGE100PERCENT             | cdm\_leverage100percent                             |
| LEVERAGEMAXIMUM                | cdm\_leveragemaximum                                |
| LEVERAGEMINIMUM                | cdm\_leverageminimum                                |
| LEVERAGEOVEROBJECTIVE          | cdm\_leverageoverobjective                          |
| LEVERAGEUNDEROBJECTIVE         | cdm\_leverageunderobjective                         |
| PERCENTOFBASIS                 | cdm\_percentofbasis                                 |
| PLANID                         | cdm\_name                                           |
| VARIABLECOMPENSATIONTYPE       | cdm\_variablecompensationtypeid.cdm\_name            |
| UNITCURRENCYCODE               | transactioncurrencyid.isocurrencycode              |
| UNITRELATIONSHIP               | cdm\_unitrelationship                               |
| UNITVALUE                      | cdm\_unitvalue                                      |
| NUMBEROFUNITSREAL              | cdm\_numberofunits                                  |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VESTINGRULE                    | cdm\_vestingruleid.cdm\_name                         |
| LEVERAGETOLERANCEMAX           | cdm\_leveragetolerancemax                           |
| LEVERAGETOLERANCEMIN           | cdm\_leveragetolerancemin                           |

### <a name="compensation-variable-type-to-compensation-variable-plan-type"></a>Kompensasjon, variabel type til type variabel kompensasjonsplan

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| TYPE                           | cdm\_awardtype                                      |
| VARIABLECOMPENSATIONTYPE       | cdm\_name                                           |

### <a name="compensation-vesting-rules-to-vesting-rule"></a>Kompensasjon, overdragelsesregler til overdragelsesregel

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| NOTAT                           | cdm\_notes                                          |
| VESTINGRULE                    | cdm\_name                                           |

### <a name="department-v2-to-department"></a>Avdeling V2 til avdeling

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| OPERATINGUNITNUMBER            | cdm\_departmentnumber                               |
| NAVN                           | cdm\_name                                           |
| SEARCHNAME                     | cdm\_description                                    |
| PARTYTYPE                      | cdm\_partytype                                      |

### <a name="dual-write-tax-region-to-tax-region"></a>Avgiftsområde for dobbel skriving til avgiftsområde

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BY                           | cdm\_city                                           |
| COUNTRYORREGION                | cdm\_countryorregion                                |
| KOMMUNE                         | cdm\_county                                         |
| DELSTAT                          | cdm\_stateorprovince                                |
| TAXREGIONNAME                  | cdm\_name                                           |

### <a name="dual-write-worker-identification-to-worker-person-identification-number"></a>Arbeideridentifikasjonsnummer for personidentifikasjonsnummer for arbeider

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| ENTRYTYPE                      | cdm\_entrytype                                      |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| IDENTIFICATIONNUMBER           | cdm\_identificationnumber                           |
| IDENTIFICATIONTYPEID           | cdm\_identificationtypeid.cdm\_name                  |
| ISPRIMARY                      | cdm\_isprimary                                      |
| ISSUEDATE                      | cdm\_issuedate                                      |
| ISSUINGAGENCYID                | cdm\_issuingagencyid.cdm\_name                       |
| WORKERNUMBER                   | cdm\_workerid.cdm\_workernumber                      |

### <a name="compensation-structure-to-compensation-structure"></a>Kompensasjonsstruktur til kompensasjonsstruktur

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BELØP                         | cdm\_amount                                         |
| RUTENETT                           | cdm\_compensationgridid.cdm\_name                    |
| LEVELID                        | cdm\_compensationlevelid.cdm\_name                   |
| REFERENCEPOINTLINENUMBER       | cdm\_referencepointid.cdm\_linenumber                |
| REFERENCESETUP                 | cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name |
| REFERENCEPOINT                 | cdm\_referencepointid.cdm\_name                      |

### <a name="earning-code-to-payroll-earning-code"></a>Inntektskode til inntektskode for lønn

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| EARNINGCODE                    | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| INCLUDEINPAYMENTTYPE           | cdm\_includeinpaymenttype                           |
| QUANTITYUNIT                   | cdm\_quantityunit                                   |
| TRACKFMLAHOURS                 | cdm\_trackfmlahours                                 |
| ISPRODUCTIVE                   | cdm\_isproductive                                   |

### <a name="employee-fixed-compensation-to-worker-fixed-compensation"></a>Fast kompensasjon for ansatt til fast kompensasjon for arbeider

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| TYPE                           | cdm\_compensationtype                               |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| LINENUMBER                     | cdm\_linenumber                                     |
| PAYFREQUENCY                   | cdm\_payfrequencyid.cdm\_name                        |
| PAYRATE                        | cdm\_payrate                                        |
| PLAN                           | cdm\_planid.cdm\_name                                |
| POSITIONID                     | cdm\_positionid.cdm\_jobpositionnumber               |
| PROCESSTYPE                    | cdm\_processtype                                    |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| HANDLING                         | cdm\_eventid.cdm\_name                               |
| TRINN                           | cdm\_referencepointsetuplineid.cdm\_name             |
| REFPOINTSETUPID                | cdm\_referencepointsetuplineid.cdm\_referencepointsetupid.cdm\_name |

### <a name="employment-per-company-to-employment"></a>Ansettelse per firma til ansettelse

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| EMPLOYMENTENDDATE              | cdm\_employmentenddate                              |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| EMPLOYMENTSTARTDATE            | cdm\_employmentstartdate                            |
| WORKERTYPE                     | cdm\_workertype                                     |
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| ADJUSTEDWORKERSTARTDATE        | cdm\_adjustedworkerstartdate                        |
| EMPLOYERNOTICEAMOUNT           | cdm\_employernoticeamount                           |
| EMPLOYERUNITOFNOTICE           | cdm\_employerunitofnotice                           |
| WORKERUNITOFNOTICE             | cdm\_workerunitofnotice                             |
| WORKERNOTICEAMOUNT             | cdm\_workernoticeamount                             |
| LASTDATEWORKED                 | cdm\_lastdateworked                                 |
| PROBATIONENDDATE               | cdm\_probationenddate                               |
| TRANSITIONDATE                 | cdm\_transitiondate                                 |
| TRANSITIONREASONCODENAME       | cdm\_transitionreasoncode.cdm\_name                  |
| WORKERSTARTDATE                | cdm\_workerstartdate                                |
| VALIDTO                        | cdm\_validto                                        |
| VALIDFROM                      | cdm\_validfrom                                      |

### <a name="ethnic-origins-to-ethnic-origin"></a>Etnisk opprinnelse til etnisk opprinnelse

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| ETHNICORIGINID                 | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |

### <a name="group-assignment-to-business-process-group-assignment"></a>Gruppetildeling til tildeling av forretningsprosessgruppe

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| NAVN                           | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="identification-type-to-worker-person-identification-type"></a>Identifikasjonstype til personidentifikasjonstype for arbeider

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| IDENTIFICATIONTYPEID           | cdm\_name                                           |
| ALLOWEDVALUES                  | cdm\_allowedvalues                                  |
| FIXEDLENGTH                    | cdm\_fixedlength                                    |
| IDENTIFICATIONNUMBERFORMAT     | cdm\_identificationnumberformat                     |

### <a name="issuing-agency-to-person-identification-issuing-agency"></a>Utstedende byrå til utstedende byrå for personidentifikasjon

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| E-POST                          | cdm\_email                                          |
| DIREKTENUMMER                      | cdm\_extension                                      |
| FAKS                            | cdm\_fax                                            |
| ISSUINGAGENCY                  | cdm\_name                                           |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| NAVN                           | cdm\_description                                    |
| PERSONSØKER                          | cdm\_pager                                          |
| SMS                            | cdm\_sms                                            |
| TELEFON                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telex                                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |

### <a name="job-positions-dual-write-to-job-position"></a>Dobbelskriving for standard stillingsdimensjoner til stilling

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONID                     | cdm\_jobpositionnumber                              |
| AKTIVERING                     | cdm\_activation                                     |
| AVAILABLEFORASSIGNMENT         | cdm\_availableforassignment                         |
| COMPENSATIONREGIONID           | cdm\_compensationregionid.cdm\_name                  |
| DEPARTMENTID                   | cdm\_departmentid.cdm\_departmentnumber              |
| BESKRIVELSE                    | cdm\_description                                    |
| FULLTIMEEQUIVALENT             | cdm\_fulltimeequivalent                             |
| JOBID                          | cdm\_jobid.cdm\_name                                 |
| PARENTPOSITIONID               | cdm\_parentjobpositionid.cdm\_jobpositionnumber      |
| POSITIONTYPEID                 | cdm\_positiontypeid.cdm\_name                        |
| AVGANGVEDPENSJON                     | cdm\_retirement                                     |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |

### <a name="jobs-dual-write-to-job"></a>Dobbel skriving for jobb til jobb

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| JOBID                          | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| JOBDESCRIPTION                 | cdm\_jobdescription                                 |
| ALLOWUNLIMITEDPOSITIONS        | cdm\_allowunlimitedpositions                        |
| MAXIMUMNUMBEROFPOSITIONS       | cdm\_maximumnumberofpositions                       |
| JOBFUNCTIONID                  | cdm\_jobfunctionid.cdm\_name                         |
| JOBTYPEID                      | cdm\_jobtypeid.cdm\_name                             |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| DEFAULTFULLTIMEEQUIVALENCY     | cdm\_defaultfulltimeequivalent                      |

### <a name="language-codes-to-language"></a>Språkkoder til språk

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| LANGUAGECODEID                 | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |

### <a name="leave-and-absence-bank-transaction-v2-to-leave-bank-transaction"></a>Banktransaksjon for permisjon og fravær V2 til banktransaksjon for permisjon

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BELØP                         | cdm\_amount                                         |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TRANSACTIONDATE                | cdm\_transactiondate                                |
| TRANSACTIONNUMBER              | cdm\_transactionnumber                              |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| TRANSACTIONTYPE                | cdm\_transactiontype                                |

### <a name="leave-and-absence-enrollment-v2-to-leave-enrollment"></a>Permisjons- og fraværsregistrering V2 til permisjonsregistrering

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| CUSTOMDATE                     | cdm\_customdate                                     |
| ACCRUALSTARTDATE               | cdm\_accrualstartdate                               |
| ACCRUALDATEBASIS               | cdm\_accrualdatebasis                               |
| ISACCRUALSUSPENDED             | cdm\_isaccrualsuspended                             |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TIERBASIS                      | cdm\_tierbasis                                      |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="leave-and-absence-plan-v2-to-leave-plan"></a>Permisjons- og fraværsplan V2 til permisjonsplan

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| ACCRUALFREQUENCY               | cdm\_accrualfrequency                               |
| NAVN                           | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| STARTDATE                      | cdm\_startdate                                      |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-and-absence-type-to-leave-type"></a>Permisjons- og fraværstype til permisjonstype

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| TYPE                           | cdm\_type                                           |
| EARNINGCODEID                  | cdm\_earningcodeid.cdm\_name                         |

### <a name="leave-and-absence-type-reason-code-to-leave-type-reason-code"></a>Årsakskode for permisjons- og fraværstype til årsakskode for permisjonstype

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| LEAVETYPE                      | cdm\_typeid.cdm\_type                                |
| REASONCODEID                   | cdm\_reasoncodeid.cdm\_name                          |

### <a name="leave-time-off-request-detail-to-leave-request-detail"></a>Detaljer om be om permisjonsfridager til detaljer for fraværsforespørsel

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BELØP                         | cdm\_amount                                         |
| LEAVEDATE                      | cdm\_leavedate                                      |
| REQUESTID                      | cdm\_leaverequestid.cdm\_leaverequestnumber          |
| TYPE                           | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-time-off-request-header-to-leave-request"></a>Overskrift for be om permisjonsfridager til permisjonsforespørsel

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| REQUESTID                      | cdm\_leaverequestnumber                             |
| REQUESTDATE                    | cdm\_requestdate                                    |
| STATUS                         | cdm\_status                                         |
| KOMMENTAR                        | cdm\_comment                                        |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="levels-to-compensation-level"></a>Nivåer til kompensasjonsnivå

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| TYPE                           | cdm\_type                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| NIVÅ                          | cdm\_name                                           |

### <a name="onboarding-process-header-to-onboard-process-header"></a>Topptekst i jobbintroduksjonsprosess til inkludert prosesshode

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ONBOARDEDEMPLOYEEPERSONNELNUMBER | cdm\_onboardedemployeeid.cdm\_workernumber           |
| EMPLOYMENTPERSONNELNUMBER      | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| LEGALENTITYID                  | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |
| EMPLOYMENTSTARTDATE            | cdm\_employmentid.cdm\_employmentstartdate           |

### <a name="pay-cycle-to-pay-cycle"></a>Lønnssyklus til lønnssyklus

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| PAYCYCLEFREQUENCY              | cdm\_frequency                                      |

### <a name="pay-period-to-pay-period"></a>Lønnsperiode til lønnsperiode

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| COMMENTS                       | cdm\_description                                    |
| DEFAULTPAYMENTDATE             | cdm\_defaultpaymentdate                             |
| PAYCYCLEID                     | cdm\_paycycleid.cdm\_name                            |
| PERIODENDDATE                  | cdm\_periodenddate                                  |
| PERIODSTARTDATE                | cdm\_periodstartdate                                |
| STATUS                         | cdm\_status                                         |

### <a name="payroll-details-for-positions-to-payroll-position-detail"></a>Lønnsdetaljer for stillinger til lønnsstillingsdetalj

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_paycycle.cdm\_name                              |
| POSITIONID                     | cdm\_position.cdm\_jobpositionnumber                 |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| ANNUALREGULARHOURS             | cdm\_annualregularhours                             |
| PAIDBYLEGALENTITY              | cdm\_paidby.cdm\_companycode                         |

### <a name="position-default-dimensions-dual-write-to-job-position-dimension"></a>Dobbelskriving for standard stillingsdimensjoner til stillingsdimensjon

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |

### <a name="position-type-to-position-type"></a>Stillingstype til stillingstype

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONTYPEID                 | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| KLASSIFISERING                 | cdm\_classification                                 |

### <a name="position-worker-assignments-v2-to-position-worker-assignment"></a>Stillingstildelinger V2 til stillingstildeling

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| IsPrimaryPosition              | cdm\_isprimaryposition                              |

### <a name="reason-codes-to-reason-code"></a>Årsakskoder til årsakskode

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| REASONCODEID                   | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| ISABSENCEAPPLICABLE            | cdm\_isabsenceapplicable                            |
| ISAPPLICATIONAPPLICABLE        | cdm\_isapplicationapplicable                        |
| ISCOMPENSATIONAPPLICABLE       | cdm\_iscompensationapplicable                       |
| ISCREATENEWPOSITIONAPPLICABLE  | cdm\_iscreatenewpositionapplicable                  |
| ISEDITPOSITIONAPPLICABLE       | cdm\_iseditpositionapplicable                       |
| ISHIREAPPLICABLE               | cdm\_ishireapplicable                               |
| ISSKILLMAPPINGAPPLICABLE       | cdm\_isskillmappingapplicable                       |
| ISTERMINATIONAPPLICABLE        | cdm\_isterminationapplicable                        |
| ISTRANSFERAPPLICABLE           | cdm\_istransferapplicable                           |

### <a name="reference-point-setup-line-dual-write-to-compensation-reference-point-setup-line"></a>Linje i referansepunktoppsett (dobbel skriving) til oppsettslinje for referansepunkt for kompensasjon

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| BESKRIVELSE                    | cdm\_description                                    |
| LINENUM                        | cdm\_linenumber                                     |
| REFPOINTID                     | cdm\_name                                           |
| REFPOINTSETUPID                | cdm\_referencepointsetupid.cdm\_name                 |

### <a name="reference-point-setups-to-compensation-reference-point-setup"></a>Referansepunktoppsett til oppsett av referansepunkt for kompensasjon

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| REFERENCESETUP                 | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| TYPE                           | cdm\_compensationtype                               |

### <a name="skill-types-to-skill-type"></a>Kompetansetyper til kompetansetype

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| SKILLTYPE                      | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |

### <a name="titles-to-title"></a>Titler til tittel

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| TITLEID                        | cdm\_name                                           |

### <a name="variable-compensation-level-v2-to-compensation-variable-plan-level"></a>Variabelt kompensasjonsnivå V2 til nivå for variabel kompensasjonsplan

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| AWARDAMOUNT                    | cdm\_awardamount                                    |
| AWARDPERCENT                   | cdm\_awardpercent                                   |
| AWARDUNITSREAL                 | cdm\_awardunits                                     |
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| PLANID                         | cdm\_compensationvariableplanid.cdm\_name            |

### <a name="veteran-status-to-veteran-status"></a>Veteranstatus til veteranstatus

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| VETERANSTATUSID                | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |
| ISPROTECTEDVETERAN             | cdm\_isprotectedveteran                             |

### <a name="work-calendar-enrollments-to-work-calendar-enrollment"></a>Registreringer i arbeidskalender til registrering i arbeidskalender

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_employmentid.cdm\_employmentstartdate           |
| PERSONALNUMMER                | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| CALENDARID                     | cdm\_workcalendarid.cdm\_name                        |
| COMPANYID                      | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |

### <a name="work-calendar-holiday-to-work-calendar-holiday"></a>Helligdag i arbeidskalender til helligdag i arbeidskalender

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| ID                             | cdm\_name                                           |
| BESKRIVELSE                    | cdm\_description                                    |

### <a name="work-calendar-holiday-line-to-work-calendar-holiday-line"></a>Ferielinje for arbeidskalender til ferielinje for arbeidskalender

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| HOLIDAYID                      | cdm\_workcalendarholidayid.cdm\_name                 |
| NAVN                           | cdm\_name                                           |
| HOLIDAYDATE                    | cdm\_holidaydate                                    |

### <a name="worker-to-worker"></a>Arbeider til arbeider

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONALNUMMER                | cdm\_workernumber                                   |
| FIRSTNAME                      | cdm\_firstname                                      |
| MIDDLENAME                     | cdm\_middlename                                     |
| LASTNAME                       | cdm\_lastname                                       |
| WORKERTYPE                     | cdm\_type                                           |
| WORKERSTATUS                   | cdm\_status                                         |
| PRIMARYCONTACTEMAIL            | cdm\_primaryemailaddress                            |
| PRIMARYCONTACTPHONE            | cdm\_primarytelephone                               |
| PRIMARYCONTACTFACEBOOK         | cdm\_facebookidentity                               |
| PRIMARYCONTACTTWITTER          | cdm\_twitteridentity                                |
| PRIMARYCONTACTLINKEDIN         | cdm\_linkedinidentity                               |
| PRIMARYCONTACTURL              | cdm\_websiteurl                                     |
| GENDER                         | cdm\_gender                                         |
| FØDSELSDATO                      | cdm\_birthdate                                      |
| NAVN                           | cdm\_fullname                                       |

### <a name="worker-bank-accounts-to-worker-bank-account"></a>Bankkontoer for arbeider til bankkonto for arbeider

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATION          | cdm\_accountidentification                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONID         | cdm\_countryorregion                                |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSDISTRICTNAME            | cdm\_districtname                                   |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| BANKACCOUNTNUMBER              | cdm\_bankaccountnumber                              |
| BANKACCOUNTTYPE                | cdm\_bankaccounttype                                |
| E-POST                          | cdm\_email                                          |
| DIREKTENUMMER                      | cdm\_extension                                      |
| FAKS                            | cdm\_fax                                            |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| ROUTINGNUMBER                  | cdm\_routingnumber                                  |
| TELEFON                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telexnumber                                    |
| BANKIBAN                       | cdm\_iban                                           |
| SWIFTNO                        | cdm\_swiftcode                                      |
| BANKLOCATIONCODE               | cdm\_banklocationcode                               |
| BRANCHNAME                     | cdm\_branchname                                     |
| BRANCHNUMBER                   | cdm\_branchnumber                                   |
| ROUTINGNUMBERTYPE              | cdm\_routingnumbertype                              |
| ACCOUNTHOLDER                  | cdm\_accountholder                                  |
| NAMEOFPERSON                   | cdm\_nameofperson                                   |
| NAVN                           | cdm\_description                                    |
| ADDRESSSTREET                  | cdm\_line1                                          |
| ADDRESSSTREETNUMBER            | cdm\_line2                                          |

### <a name="worker-personal-details-to-worker-personal-detail"></a>Arbeiderens personopplysninger til arbeiderens personopplysninger

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| FØDSELSDATO                      | cdm\_birthdate                                      |
| PERSONBIRTHCITY                | cdm\_birthcity                                      |
| GENDER                         | cdm\_gender                                         |
| EXPATRIATEENDDATE              | cdm\_expatriateenddate                              |
| EXPATRIATESTARTDATE            | cdm\_expatriatestartdate                            |
| DISABLEDVETERAN                | cdm\_isdisabledveteran                              |
| DECEASEDDATE                   | cdm\_deceaseddate                                   |
| DISABLEDVERIFICATIONDATE       | cdm\_disabledveteranverificationdate                |
| UTDANNING                      | cdm\_education                                      |
| ETHNICORIGINID                 | cdm\_ethnicoriginid.cdm\_name                        |
| ISDISABLED                     | cdm\_isdisabled                                     |
| ISFULLTIMESTUDENT              | cdm\_isfulltimestudent                              |
| ISEXPATRIATERULINGAPPLICABLE   | cdm\_isexpatriaterulingapplicable                   |
| MARITALSTATUS                  | cdm\_maritalstatus                                  |
| MILITARYSERVICESTARTDATE       | cdm\_militaryservicestartdate                       |
| MILITARYSERVICEENDDATE         | cdm\_militaryserviceenddate                         |
| NUMBEROFDEPENDENTS             | cdm\_numberofdependents                             |
| NATIVELANGUAGEID               | cdm\_nativelanguageidid.cdm\_name                    |
| NATIONALITYCOUNTRYREGION       | cdm\_nationalitycountryregion                       |
| PERSONBIRTHCOUNTRYREGION       | cdm\_birthcountryregion                             |
| FATHERBIRTHCOUNTRYREGION       | cdm\_fatherbirthcountryregion                       |
| MOTHERBIRTHCOUNTRYREGION       | cdm\_motherbirthcountryregion                       |
| CITIZENSHIPCOUNTRYREGION       | cdm\_citizenshipcountryregion                       |
| VETERANSTATUSID                | cdm\_veteranstatusid.cdm\_name                       |

### <a name="worker-postal-addresses-dual-write-to-worker-address"></a>Dobbel skriving for postadresser til arbeideradresse

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| ADDRESSLOCATIONID              | cdm\_addressnumber                                  |
| ADDRESSLOCATIONROLES           | cdm\_addresstype                                    |
| GYLDIG                      | cdm\_effectivedate                                  |
| UTLØP                     | cdm\_expirationdate                                 |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSSTREETNUMBER            | cdm\_streetnumber                                   |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSCOUNTYID                | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_description                                    |
| ADDRESSLATITUDE                | cdm\_latitude                                       |
| ADDRESSLONGITUDE               | cdm\_longitude                                      |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ISPRIMARY                      | cdm\_ispreferred                                    |

### <a name="working-time-to-work-calendar-time-interval"></a>Driftstid til tidsintervall for arbeidskalender

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| ENDTIME                        | cdm\_endtime                                        |
| STARTTIME                      | cdm\_starttime                                      |
| WORKCALENDARDATE               | cdm\_workcalendardayid.cdm\_calendardate             |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKCALENDARID                 | cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name  |

### <a name="working-times-to-work-calendar-day"></a>Driftstider til arbeidskalenderdag

| Finance-enhet                 | Dataverse-tabell                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARDATE                   | cdm\_calendardate                                   |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKINGDAYDEFINITION           | cdm\_status                                         |

## <a name="integration-considerations"></a>Integreringshensyn

- Alle endringer som gjøres i data i ett av systemene, vil være underlagt validering av det andre systemet. Hvis det oppstår en feil, skrives ikke data i noen av systemene. 
- Alle skrivinger er underlagt standarddata (hvis egendefinert logikk forekommer i Finance).
- Integratorappen for dobbel skriving bruker integreringsnøkler til å tildele mellom de to systemene. Noen ganger er det vanskelig å velge riktig integreringsnøkkel, spesielt hvis flere integreringsnøkler oppfyller kravene. Hvis du vil ha hjelp til dette valget, viser følgende tabell de foreslåtte integreringsnøklene for tildelingene.

| Dataverse-tabell                          | Integreringsnøkler |
|------------------------------------------|------------------|
| Bankkontobetaling                | cdm\_bankaccountid.cdm\_accountidentification, cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Beregningsfrekvens for fordeler            | cdm\_name |
| Lønnsperiode i fordelsberegningsfrekvens | cdm\_payperiodid.cdm\_periodstartdate, cdm\_payperiodid.cdm\_paycycleid.cdm\_name, cdm\_benefitcalculationfrequencyid.cdm\_name |
| Beregningssats for fordeler                 | cdm\_name |
| Detaljer om beregningssats for fordeler          | cdm\_workerdeduction, cdm\_effective, cdm\_calculationrateid.cdm\_name |
| Fordelsalternativ                           | cdm\_name |
| Fordelstype                             | cdm\_name |
| Forretningsprosesskalender                | cdm\_name |
| Tilordning av forretningsprosessgruppe        | cdm\_name |
| Forretningsprosesshode                  | cdm\_processid |
| Oppgavegruppe for forretningsprosessbibliotek      | cdm\_processtype, cdm\_name |
| Forretningsprosessfase                   | cdm\_name, cdm\_businessprocesstype, cdm\_companyid.cdm\_companycode |
| Oppgave i forretningsprosess                    | cdm\_taskid |
| Forretningsenhet                            | |
| Topptekst for sjekklistemal                | cdm\_businessprocesstype, cdm\_name, cdm\_genericsubtype |
| Oppgave for sjekklistemal                  | cdm\_taskid |
| Selskap                                  | cdm\_companycode |
| Fast kompensasjonsplan                  | cdm\_name, cdm\_company.cdm\_companycode |
| Kompensasjonsrutenett                        | cdm\_name, cdm\_companyid.cdm\_companycode |
| Kompensasjonsnivå                       | cdm\_name |
| Kompensasjon, lønnsfrekvens               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Oppsett av referansepunkt for kompensasjon       | cdm\_name, cdm\_companyid.cdm\_companycode |
| Oppsettslinje for referansepunkt for kompensasjon  | cdm\_name, cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode |
| Kompensasjonsområde                      | cdm\_name |
| Kompensasjonsstruktur                   | cdm\_compensationlevelid.cdm\_name, cdm\_referencepointid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_compensationgridid.cdm\_name, cdm\_compensationgridid.cdm\_companyid.cdm\_companycode |
| Variabel kompensasjonsplan               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Nivå for variabel kompensasjonsplan         | cdm\_companyid.cdm\_companycode, cdm\_compensationvariableplanid.cdm\_name, cdm\_compensationvariableplanid.cdm\_companyid.cdm\_companycode, cdm\_compensationlevelid.cdm\_name |
| Type variabel kompensasjonsplan          | cdm\_name, cdm\_companyid.cdm\_companycode |
| Valuta.                                 | isocurrencycode |
| Avdeling                               | cdm\_departmentnumber |
| Ansettelse                               | cdm\_employmentstartdate, cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Etnisk opprinnelse                            | cdm\_name |
| Fast kompensasjonshendelse                 | cdm\_name, cdm\_companyid.cdm\_companycode |
| Stilling                                      | cdm\_name |
| Jobbfunksjon                             | cdm\_name |
| stilling                             | cdm\_jobpositionnumber |
| stillingsdimensjon                   | cdm\_jobpositionid.cdm\_jobpositionnumber, cdm\_companyid.cdm\_companycode |
| Jobbtype                                 | cdm\_name |
| Språk                                 | cdm\_name |
| Banktransaksjon for permisjon                   | cdm\_transactiondate, cdm\_transactiontype, cdm\_transactionnumber, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| Permisjonsregistrering                         | cdm\_startdate, cdm\_leaveplanid.cdm\_name, cdm\_leaveplanid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| Permisjonsplan                               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Permisjonsforespørsel                            | cdm\_leaverequestnumber, cdm\_companyid.cdm\_companycode |
| Detaljer for fraværsforespørsel                     | cdm\_leavedate, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_leaverequestid.cdm\_leaverequestnumber, cdm\_leaverequestid.cdm\_companyid.cdm\_companycode |
| Permisjonstype                               | cdm\_type, cdm\_companyid.cdm\_companycode |
| Årsakskode for permisjonstype                   | cdm\_reasoncodeid.cdm\_name, cdm\_typeid.cdm\_type, cdm\_typeid.cdm\_companyid.cdm\_companycode |
| Inkludert prosesshode                   | cdm\_processheaderid.cdm\_processid |
| Organisasjon                             | |
| Lønnssyklus                                | cdm\_name |
| Lønnsperiode                               | cdm\_periodstartdate, cdm\_paycycleid.cdm\_name, cdm\_periodenddate |
| Inntektskode for lønn                     | cdm\_name |
| Lønnsstillingsdetalj                  | cdm\_validfrom, cdm\_validto, cdm\_position.cdm\_jobpositionnumber |
| Utstedende byrå for personidentifikasjon     | cdm\_name |
| Stillingstype                            | cdm\_name |
| Stillingstilordning               | cdm\_validfrom, cdm\_jobpositionid.cdm\_jobpositionnumber |
| Årsakskode                              | cdm\_name |
| Kompetansetype                               | cdm\_name |
| Avgiftsområde                               | cdm\_stateorprovince, cdm\_name, cdm\_countryorregion, cdm\_county, cdm\_city |
| Team                                     | azureactivedirectoryobjectid, membershiptype |
| Tittel                                    | cdm\_name |
| Bruker                                     | azureactivedirectoryobjectid |
| Overdragelsesregel                             | cdm\_name, cdm\_companyid.cdm\_companycode |
| Veteranstatus                           | cdm\_name |
| Arbeidskalender                            | cdm\_name, cdm\_companyid.cdm\_companycode |
| Arbeidskalenderdag                        | cdm\_calendardate, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Registrering i arbeidskalender                 | cdm\_employmentid.cdm\_employmentstartdate, cdm\_employmentid.cdm\_workerid.cdm\_workernumber, cdm\_employmentid.cdm\_companyid.cdm\_companycode |
| Helligdag i arbeidskalender                    | cdm\_name |
| Ferielinje for arbeidskalender               | cdm\_holidaydate, cdm\_workcalendarholidayid.cdm\_name |
| Tidsintervall for arbeidskalender              | cdm\_starttime, cdm\_workcalendardayid.cdm\_calendardate, cdm\_workcalendardayid.cdm\_companyid.cdm\_companycode, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Worker                                   | cdm\_workernumber |
| Arbeideradresse                           | cdm\_addressnumber, cdm\_addresstype, cdm\_workerid.cdm\_workernumber |
| Bankkonto for arbeider                      | cdm\_accountidentification, cdm\_workerid.cdm\_workernumber |
| Fast kompensasjon for arbeider                | cdm\_linenumber, cdm\_effectivedate, cdm\_companyid.cdm\_companycode, cdm\_positionid.cdm\_jobpositionnumber, cdm\_workerid.cdm\_workernumber, cdm\_eventid.cdm\_name, cdm\_eventid.cdm\_companyid.cdm\_companycode, cdm\_planid.cdm\_name, cdm\_planid.cdm\_company.cdm\_companycode |
| Personidentifikasjonsnummer for arbeider      | cdm\_identificationnumber, cdm\_workerid.cdm\_workernumber, cdm\_identificationtypeid.cdm\_name |
| Personidentifikasjonstype for arbeider        | cdm\_name |
| Arbeiderens personopplysninger                   | cdm\_workerid.cdm\_workernumber |
