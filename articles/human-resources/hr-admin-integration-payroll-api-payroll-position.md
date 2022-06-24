---
title: Lønnsdetaljer for stillinger
description: Denne artikkelen inneholder informasjon og en eksempelspørring for lønnsdetaljene for Stillinger-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: ac36b0386312e1631528b8ab5976db2cb3924caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904137"
---
# <a name="payroll-position"></a>Lønnsstilling


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Lønnsstillinger-enheten i Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollpositionentity.

### <a name="description"></a>beskrivelse

Denne enheten gir stillingsrelatert informasjon for en gitt ansatt.

Fysisk navn: mshr_payrollpositionentity.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | Beskrivelse |
| --- | --- | --- |
| **Stillings-ID**</br>mshr_positionid</br>*Streng* | Skrivebeskyttet | ID-en for stillingen. |
| **ID for lønnssyklus**</br>mshr_paycycleid</br>*Streng* | Skrivebeskyttet | Lønnssyklusen som er definert for stillingen. |
| **Årlige vanlige timer**</br>annualregularhours</br>*Desimal* | Skrivebeskyttet | Årlige faste timer definert i stillingen. |
| **Betalt av juridisk enhet**</br>paidbylegalentity</br>*Streng* | Skrivebeskyttet | Den juridiske enheten som er definert i stillingen, og som er ansvarlig for utstedelse av betaling. |
| **Gyldig til**</br>validto</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen stillingsdetaljene er gyldige til. |
| **Gyldig fra**</br>validfrom</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen stillingsdetaljene er gyldige fra. |
| **Primærfelt**</br>mshr_primaryfield</br>*Streng* | Systemgenerert | Primærfeltet. |
| **Enhets-ID for lønnsstillingsdetaljer**</br>payrollpositiondetailsentityid</br>*Guid* | Obligatorisk</br>Systemgenerert. | En systemgenerert globalt unik identifikator (GUID)-verdi som identifiserer stillingen entydig. |

## <a name="relations"></a>Relasjoner

| Egenskapsverdi | Relatert enhet | Navigasjonsegenskap | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Gjelder ikke |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Gjelder ikke |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
