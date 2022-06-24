---
title: Lønnsansatt
description: Denne artikkelen inneholder informasjon og en eksempelspørring for Lønnsansatt-enheten i Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b07fbc76b997600b2c076c00a63d1f6d865326d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872217"
---
# <a name="payroll-employee"></a>Lønnsansatt


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Lønnsansatt-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollemployeeentity.

### <a name="description"></a>beskrivelse

Denne enheten gir informasjon om den ansatte. Du må definere [parameterne for lønnsintegrering](hr-admin-integration-payroll-api-parameters.md) før du bruker denne enheten.

>[!IMPORTANT] 
>Feltene **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** vil ikke lenger være tilgjengelige på denne enheten. Dette sikrer at det bare er én datoeffektiv datakilde som sikkerhetskopierer denne enheten.
>Disse feltene vil være tilgjengelige på **DirPersonNameHistoricalEntity**, som ble frigitt i platformoppdatering 43. Det finnes en OData-relasjon fra **PayrollEmployeeEntity** til **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for juridisk enhet**</br>mshr_legalentityid</br>*Streng* | Skrivebeskyttet | Angir den juridiske enheten (firmaet). |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Det unike personalnummeret til den ansatte. |
| **Startdato for ansettelse**</br>mshr_employmentstartdate</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Startdatoen for den ansattes ansettelse. |
| **Sluttdato for ansettelse**</br>mshr_employmentenddate</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet |Sluttdatoen for den ansattes ansettelse.  |
| **Fødselsdato**</br>mshr_birthdate</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Den ansattes fødselsdato. |
| **Kjønn**</br>mshr_gender</br>[mshr_hcmpersongender-alternativsett](hr-admin-integration-payroll-api-gender.md) | Skrivebeskyttet | Den ansattes kjønn. |
| **Ansettelsestype**</br>mshr_employmenttype</br>[mshr_hcmemploymenttype-alternativsett](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Skrivebeskyttet | Ansettelsestypen. |
| **ID for Identifikasjonstype**</br>mshr_identificationtypeid</br>*Streng* |Skrivebeskyttet | Identifikasjonstypen som er definert for den ansatte. |
| **Identifikasjonsnummer til**</br>mshr_identificationnumber</br>*Streng* | Skrivebeskyttet |Identifikasjonsnummeret som er definert for den ansatte. |
| **Klar til betaling**</br>mshr_readytopay</br>[mshr_noyes-alternativsett](hr-admin-integration-payroll-api-no-yes.md) | Skrivebeskyttet | Angir om den ansatte er merket som klar til å betale. |
| **Enhets-ID for lønnsansatt**</br>mshr_payrollemployeeentityid</br>*GUID* | Systemgenerert | En systemgenerert globalt unik identifikator (GUID)-verdi som identifiserer den ansatte entydig. |

## <a name="relations"></a>Relasjoner

|Egenskapsverdi | Relatert enhet | Navigasjonsegenskap | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Eksempelspørring for lønnsansatt

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Svar**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
