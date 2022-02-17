---
title: Lønnsstillingsjobb
description: Dette emnet inneholder informasjon og en eksempelspørring for Lønnsstillingsjobb-enheten i Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
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
ms.openlocfilehash: 349479d9e77861b54d879bcfd93f7af0e38cff95
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069838"
---
# <a name="payroll-position-job"></a>Lønnsstillingsjobb


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Lønnsstillingsjobb-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>beskrivelse

Denne enheten gir relasjonen mellom stilling og jobb for en gitt fast kompensasjonsplan.

Fysisk navn: mshr_payrollpositionjobentity.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | Beskrivelse |
| --- | --- | --- |
| **Stillings-ID**</br>mshr_positionid</br>*Streng* | Skrivebeskyttet | ID-en for stillingen. |
| **Gyldig fra**</br>mshr_validto</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen som stillings- og jobbrelasjonen er gyldig fra. |
| **Gyldig til**</br>mshr_validto</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen som stillings- og jobbrelasjonen er gyldig til. |
| **Jobb-ID**</br>mshr_jobid</br>*Streng* | Skrivebeskyttet | ID-en for jobben. |
| **Primærfelt**</br>mshr_primaryfield</br>*Streng* | Systemgenerert | Primærfeltet. |
| **ID for Lønnsstillingsjobb-enhet**</br>mshr_payrollpositionjobentityid</br>*Guid* | Systemgenerert. | En systemgenerert globalt unik identifikator (GUID)-verdi som identifiserer stillingen entydig. |

## <a name="relations"></a>Relasjoner

| Egenskapsverdi | Relatert enhet | Navigasjonsegenskap | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Gjelder ikke |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Svar**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
