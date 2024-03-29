---
title: Konfigurer integrering med Finance
description: Denne artikkelen beskriver integreringen mellom Dynamics 365 Human Resources og Dynamics 365 Finance.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8be7cbf92c11036d334516116f0895c426380954
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875865"
---
# <a name="configure-integration-with-finance"></a>Konfigurer integrering med Finance


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Hvis du vil integrere Dynamics 365 Human Resources med Dynamics 365 Finance, kan du bruke Human Resources til Finance-malen i [Dataintegrator](/powerapps/administrator/data-integrator). Human Resources to Finance-malen gir dataflyt for jobber, stillinger og arbeidere. Malen gjør at data flyter fra Human Resources til Finance, men tillater ikke at data flyter fra Finance til Human Resources.

![Integrasjonsflyt fra Human Resources til Finance.](./media/hr-admin-integration-finance-flow.png)

Løsningen Human Resources til Finance tilbyr følgende typer datasynkronisering:

- Vedlikehold jobber i Human Resources og synkroniser dem fra Human Resources til Finance
- Vedlikehold stillinger og stillingstilordninger i Human Resources og synkroniser dem fra Human Resources til Finance
- Vedlikehold ansettelser i Human Resources og synkroniser dem fra Human Resources til Finance
- Vedlikehold arbeidere og arbeideradresser i Human Resources og synkroniser dem fra Human Resources til Finance

## <a name="system-requirements-for-human-resources"></a>Systemkrav for Human Resources

Integreringsløsningen krever følgende versjoner av Human Resources og Finance: 

- Dynamics 365 Human Resources den Dataverse
- Dynamics 365 Finance versjon 7.2 og nyere

## <a name="template-and-tasks"></a>Mal og oppgaver

Slik får du tilgang til Human Resources til Finance-malen.

1. Åpne [Administrasjonssenter for Power Apps](https://admin.powerapps.com/). 

2. Velg **Prosjekter**, og velg deretter **Nytt prosjekt** øverst i høyre hjørne. Opprett et nytt prosjekt for hver juridiske enhet du vil integrere i Finance.

3. Velg **Human Resources (Human Resources Dataverse til Finance)** for å synkronisere poster fra Human Resources til Finance.

Malene bruker følgende underliggende oppgaver til å synkronisere poster fra Human Resources til Finance:

- **Jobbfunksjoner til kompensasjon, jobbfunksjon**
- **Avdelinger til driftsenhet**
- **Jobbtyper til kompensasjonsjobbtype**
- **Jobber til jobber**
- **Jobber til jobbdetaljer**
- **Stillingstyper til stillingstype**
- **Jobbstillinger til basisstilling**
- **Jobbstillinger til stillingsdetaljer**
- **Jobbstillinger til stillingsvarigheter**
- **Jobbstillinger til stillingshierarkier**
- **Arbeidere til arbeider**
- **Ansettelser til ansettelse**
- **Ansettelser til ansettelsesdetalj**
- **Stillingstilordning til Stillingstilordninger**
- **Arbeideradresser til arbeiderpostadresse V2**

## <a name="template-mappings"></a>Maltilordninger

I følgende maltilordningstabeller inneholder navnet på oppgaven enhetene som brukes i hvert program. Kilden (Human Resources) vises til venstre, og målet (Finance) vises til høyre.

### <a name="job-functions-to-compensation-job-function"></a>Jobbfunksjoner til kompensasjon, jobbfunksjon

| Dataverse-tabell (kilde) | Finance-enhet (mål) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Funksjonsnavn)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>Avdelinger til driftsenhet

| Dataverse-tabell (kilde)           | Finance-enhet (mål) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Jobbtyper til kompensasjonsjobbtype

| Dataverse-tabell (kilde)   | Finance-enhet (mål) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Jobber til jobber

| Dataverse-tabell (kilde)                           | Finance-enhet (mål)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Jobber til jobbdetaljer

| Dataverse-tabell (kilde)                             | Finance-enhet (mål) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Jobbtype (Navn på jobbtype))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Jobbfunksjon (Navn på jobbfunksjon)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (Gyldig fra)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Gyldig til)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Tilsvarende standard fulltid)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Stillingstyper til stillingstype

| Dataverse-tabell (kilde)       | Finance-enhet (mål) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>Jobbstillinger til basisstilling

| Dataverse-tabell (kilde)           | Finance-enhet (mål) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Jobbstillingsnummer) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Jobbstillinger til stillingsdetaljer

| Dataverse-tabell (kilde)              | Finance-enhet (mål)       |
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

| Dataverse-tabell (kilde)             | Finance-enhet (mål) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Jobbstillingsnummer)   | POSITIONID (POSITIONID)                      |
| Calculated   Activation (Beregnet aktivering) | VALIDFROM (VALIDFROM)                        |
| Calculated   Retirement (Beregnet pensjon) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>Jobbstillinger til stillingshierarkier

| Dataverse-tabell (kilde)        | Finance-enhet (mål) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Jobbstillingsnummer)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (Gyldig fra)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Gyldig til)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Arbeidere til arbeider
| Dataverse-tabell (kilde)           | Finance-enhet (mål)       |
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

| Dataverse-tabell (kilde)                             | Finance-enhet (mål) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Ansettelser til ansettelsesdetalj

| Dataverse-tabell (kilde)                             | Finance-enhet (mål)   |
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

| Dataverse-tabell (kilde)                             | Finance-enhet (mål)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber (Jobbstillingsnummer)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (Gyldig fra)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Gyldig til)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Arbeideradresser til arbeiderpostadresse V2

| Dataverse-tabell (kilde)                             | Finance-enhet (mål)   |
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

Under integrasjonen fra Human Resources til Finance vil integreringen forsøke å finne poster basert på ID-en. Hvis postene samsvarer, blir dataene i Finance overskrevet med verdiene i Human Resources. Det kan imidlertid oppstå et problem hvis dette logisk sett er forskjellige poster, og den samme ID-en ble generert i Human Resources eller Finance basert på den respektive nummersekvensen.

Dette problemet kan oppstå med **Arbeider**, som bruker **Personalnummer** til å foreta samsvaret, og **Stillinger**. Jobber bruker ikke nummersekvenser. Resultatet er at hvis den samme jobb-ID-en finnes både i Human Resources og Finance, kommer Human Resources-informasjonen til å overskrive Dynamics 365 Finance-informasjonen. 

Hvis du vil forhindre problemer med dupliserte ID-er, kan du enten legge til et prefiks i [nummersekvensen](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) eller angi et startnummer i nummersekvensen som er utenfor rekkevidden til det andre systemet. 

Sted-ID-en som brukes for arbeideradresse, er ikke en del av nummerserien. Når du integrerer en arbeideradresse fra Human Resources til Finance, kan du opprette en duplikat adressepost hvis arbeidsadressen allerede finnes i Finance. 

Illustrasjonen nedenfor viser et eksempel på en tilordning av malen i Dataintegrator. 

![Tilordning av mal.](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
