---
title: Variabel kompensasjonsplan for lønn
description: Dette emnet inneholder informasjon og en eksempelspørring for enheten Variabel kompensasjonsplan for lønn i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5cc9e02ff2dd49e2eb0c8131fcff2eca4b9c3b1
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533654"
---
# <a name="payroll-variable-compensation-plan"></a>Variabel kompensasjonsplan for lønn


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Variabel kompensasjonsplan for lønn-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>beskrivelse

Denne enheten gir den variable kompensasjonsplanen som er tilordnet for en gitt stilling av en ansatt.

Fysisk navn: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Det unike personalnummeret til den ansatte.  |
| **Belønningsdato**</br>mshr_awarddate</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Dato for belønningen. |
| **Belønningstype**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType-alternativsett](hr-admin-integration-payroll-api-award-type.md)* | Skrivebeskyttet | Belønningstypen som er definert for den variable kompensasjonsplanen. |
| **Valuta.**</br>mshr_unitcurrencycode</br>*Streng* | Skrivebeskyttet |Valutaen som er definert for den variable kompensasjonsplanen.   |
| **Fast kompensasjonsplan-ID**</br>mshr_fixedplanid</br>*Streng* | Skrivebeskyttet | Den faste kompensasjonsplanen som brukes som basis for beregningen av belønningen. |
| **Enhetsverdi**</br>mshr_awardamount</br>*Desimal* | Skrivebeskyttet | Verdien på enheten |
| **Prosesstype**</br>mshr_processtype</br>*[mshr_hrmCompProcessType-alternativsett](hr-admin-integration-payroll-api-process-type.md)* | Skrivebeskyttet | Prosesstypen. |
| **Variabel kompensasjonsplantype**</br>Streng</br>*mshr_typeid* | Skrivebeskyttet | Typen variabel kompensasjonsplan. |
| **ID for variabel kompensasjonsplan**</br>Streng</br>*mshr_planid* | Skrivebeskyttet | ID-en for den variable kompensasjonsplanen. |
| **Antall enheter**</br>Desimal</br>*mshr_numberofunits* | Skrivebeskyttet | Antall enheter av belønningen. |
| **Primærfelt**</br>mshr_primaryfield</br>*GUID* | Skrivebeskyttet</br>Systemgenerert. | |
| **Variabel kompensasjonsplan for lønn-enhet**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer kompensasjonsplanen. |

## <a name="relations"></a>Relasjoner 

|Egenskapsverdi | Relatert enhet | Navigasjonsegenskap | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
