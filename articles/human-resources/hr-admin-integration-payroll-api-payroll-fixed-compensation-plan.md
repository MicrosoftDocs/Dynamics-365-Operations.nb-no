---
title: Fast kompensasjonsplan for lønn
description: Denne artikkelen inneholder informasjon og en eksempelspørring for enheten Fast kompensasjonsplan for lønn i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 83fa8aeb38cc44191242cf029022939cefb22cb8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909853"
---
# <a name="payroll-fixed-compensation-plan"></a>Fast kompensasjonsplan for lønn


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Fast kompensasjonsplan for lønn-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>beskrivelse

Denne enheten gir den faste kompensasjonsplanen som er tilordnet for en gitt stilling av en ansatt.

Fysisk navn: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Plan-ID**</br>mshr_planid</br>*Streng* | Skrivebeskyttet | Angir kompensasjonsplanen.  |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Det unike personalnummeret til den ansatte. |
| **Lønnssats**</br>mshr_payrate</br>*Desimal* | Skrivebeskyttet | Lønnssats som er definert i den faste kompensasjonsplanen. |
| **Stillings-ID**</br>mshr_positionid</br>*Streng* | Skrivebeskyttet | Stillings-ID som er knyttet til den ansatte og fast kompensasjonsplanregistrering. |
| **Gyldig fra**</br>mshr_validfrom</br>*Motregning av dato/klokkeslett* |  Skrivebeskyttet | Datoen som den ansattes faste kompensasjon er gyldig fra.  |
| **Gyldig til**</br>mshr_validto</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen som den ansattes faste kompensasjon er gyldig til. |
| **Lønnsfrekvens**</br>mshr_payfrequency</br>*Streng* | Skrivebeskyttet | IDen for [lønnsfrekvensen for kompensasjon](hr-admin-integration-payroll-api-compensation-pay-frequency.md) for den angitte lønnssatsen. |
| **Valuta**</br>mshr_currency</br>*Streng* | Skrivebeskyttet | Valutaen som er definert for den faste kompensasjonsplanen. |
| **Fast kompensasjonsplan for lønn-enhet**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer kompensasjonsplanen. |

## <a name="relations"></a>Relasjoner

|Egenskapsverdi | Relatert enhet | Navigasjonsegenskap | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
