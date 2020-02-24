---
title: Konfigurere integrasjon med Finance
description: Denne artikkelen beskriver funksjonaliteten som er tilgjengelig for integrering fra Dynamics 365 Human Resources og Dynamics 365 Finance.
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
ms.openlocfilehash: 2e7070f627654c9eb889f3e0ee27e37681db0502
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010043"
---
# <a name="configure-integration-with-finance"></a>Konfigurere integrasjon med Finance

Denne artikkelen beskriver funksjonaliteten som er tilgjengelig for integrering fra Dynamics 365 Human Resources og Dynamics 365 Finance. Malen for Human Resources til Finance som er tilgjengelig med [Dataintegrator](https://docs.microsoft.com/powerapps/administrator/data-integrator), muliggjør flyt av data for jobber, stillinger og arbeidere. Dataene flyter fra Human Resources til Finance. Malen gir deg ikke muligheten til å bruke data til å flyte bakover fra Finance til Human Resources. 

![Integrasjonsflyt fra Human Resources til Finance](./media/TalentFinOpsFlow.png)

Løsningen Human Resources til Finance tilbyr følgende typer datasynkronisering. 

- Vedlikehold jobber i Human Resources og synkroniser dem fra Human Resources til Finance.
- Vedlikehold stillinger og stillingstilordninger i Human Resources og synkroniser dem fra Human Resources til Finance.
- Vedlikehold ansettelser i Human Resources og synkroniser dem fra Human Resources til Finance.
- Vedlikehold arbeidere og arbeideradresser i Human Resources og synkroniser dem fra Human Resources til Finance.

## <a name="system-requirements-for-human-resources"></a>Systemkrav for Human Resources
Integreringsløsningen krever følgende versjoner av Human Resources og Finance: 
- Dynamics 365 Human Resources på Common Data Service.
- Dynamics 365 Finance versjon 7.2 og senere.

## <a name="template-and-tasks"></a>Mal og oppgaver

Gjør følgende for å få tilgang til malen.
1. Åpne [Administrasjonssenter for Power Apps](https://admin.powerapps.com/). 
1. Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler. Det må opprettes et nytt prosjekt for hver juridiske enhet du vil integrere i Finance.

Følgende mal brukes til å synkronisere poster fra Human Resources til Finance.

- **Navnet på malen i Dataintegrasjon:** Human Resources (Human Resources Common Data Service til Finance)

  > [!NOTE]
  > Navnet på oppgaven inneholder enhetene som brukes i hvert program. Kilden (Human Resources) vises til venstre, og målet (Finance and Operations) vises til høyre.

Følgende underliggende oppgaver brukes til å synkronisere poster fra Human Resources til Finance.
- Jobbfunksjoner til kompensasjon, jobbfunksjon
- Avdelinger til driftsenhet
- Jobbtyper til kompensasjonsjobbtype
- Jobber til jobber
- Jobber til jobbdetaljer
- Stillingstyper til stillingstype
- Jobbstillinger til basisstilling
- Jobbstillinger til stillingsdetaljer
- Jobbstillinger til stillingsvarigheter
- Jobbstillinger til stillingshierarkier
- Arbeidere til arbeider
- Ansettelser til ansettelse
- Ansettelser til ansettelsesdetalj
- Stillingstilordning til Stillingstilordninger
- Arbeideradresser til arbeiderpostadresse V2

## <a name="template-mappings"></a>Maltilordninger

### <a name="job-functions-to-compensation-job-function"></a>Jobbfunksjoner til kompensasjon, jobbfunksjon

| Common Data Service-enhet (kilde)                 | Finance and Operations-enhet (mål) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Funksjonsnavn)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>Avdelinger til driftsenhet

| Common Data Service-enhet (kilde)                           | Finance and Operations-enhet (mål) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Jobbtyper til kompensasjonsjobbtype

| Common Data Service-enhet (kilde)                   | Finance and Operations-enhet (mål) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Jobber til jobber

| Common Data Service-enhet (kilde)                                           | Finance and Operations-enhet (mål)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Jobber til jobbdetaljer

| Common Data Service-enhet (kilde)                                             | Finance and Operations-enhet (mål) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Jobbtype (Navn på jobbtype))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Jobbfunksjon (Navn på jobbfunksjon)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (Gyldig fra)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Gyldig til)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Tilsvarende standard fulltid)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Stillingstyper til stillingstype

| Common Data Service-enhet (kilde)                       | Finance and Operations-enhet (mål) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>Jobbstillinger til basisstilling

| Common Data Service-enhet (kilde)                           | Finance and Operations-enhet (mål) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Jobbstillingsnummer) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Jobbstillinger til stillingsdetaljer

| Common Data Service-enhet (kilde)                                                      | Finance and Operations-enhet (mål)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (Jobbstillingsnummer)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (Jobb (Navn))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (Avdeling (Avdelingsnummer)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (Stillingstype (Navn))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (Tilgjengelig for tilordning)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (Gyldig fra)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (Gyldig til)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Tilsvarende fulltid)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Jobbstillinger til stillingsvarigheter

| Common Data Service-enhet (kilde)                             | Finance and Operations-enhet (mål) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Jobbstillingsnummer)   | POSITIONID (POSITIONID)                      |
| Calculated   Activation (Beregnet aktivering) | VALIDFROM (VALIDFROM)                        |
| Calculated   Retirement (Beregnet pensjon) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hiearchies"></a>Jobbstillinger til stillingshierarkier

| Common Data Service-enhet (kilde)                                                                           | Finance and Operations-enhet (mål) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Jobbstillingsnummer)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (Gyldig fra)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Gyldig til)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Arbeidere til arbeider
| Common Data Service-enhet (kilde)                           | Finance and Operations-enhet (mål)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Ansettelser til ansettelse

| Common Data Service-enhet (kilde)                                             | Finance and Operations-enhet (mål) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Ansettelser til ansettelsesdetalj

| Common Data Service-enhet (kilde)                                             | Finance and Operations-enhet (mål)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (Gyldig fra)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Gyldig til)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Stillingstilordning til Stillingstilordninger

| Common Data Service-enhet (kilde)                                             | Finance and Operations-enhet (mål)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber (Jobbstillingsnummer)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (Gyldig fra)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Gyldig til)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Arbeideradresser til arbeiderpostadresse V2

| Common Data Service-enhet (kilde)                                             | Finance and Operations-enhet (mål)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Integreringshensyn
Når du integrerer data fra Human Resources til Finance, vil integreringen forsøke å finne poster basert på ID-en. Hvis det oppstår et treff, blir dataene i Finance overskrevet med verdiene i Human Resources. Det kan imidlertid oppstå et problem hvis dette logisk sett er forskjellige poster, og den samme ID-en ble generert i Human Resources eller Finance basert på den respektive nummersekvensen.

Områder der dette kan forekomme, er arbeider, som bruker personalnummer til å foreta samsvaret, og stillinger. Jobber bruker ikke nummersekvenser. Som et resultet, hvis den samme jobb-ID-en finnes både i Human Resources og Finance, vil Human Resources-informasjonen overskrive Dynamics 365 Finance-informasjonen. 

Hvis du vil forhindre problemer med dupliserte ID-er, kan du enten legge til et prefiks i [nummersekvensen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json) eller angi et startnummer i nummersekvensen som er utenfor rekkevidden til det andre systemet. 

Sted-ID-en som brukes for arbeideradresse, er ikke en del av nummerserien. Når du integrerer en arbeideradresse fra Human Resources til Finance, kan du opprette en duplikat adressepost hvis arbeidsadressen allerede finnes i Finance. 

Illustrasjonen nedenfor viser et eksempel på en tilordning av malen i Dataintegrator. 

![Tilordning av mal](./media/IntegrationMapping.png)


