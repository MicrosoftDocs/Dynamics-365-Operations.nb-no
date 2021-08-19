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
ms.openlocfilehash: d5f84a1a6ff794cdc8b4b81e8518983789a0b33f1708719906f6ad094d9c4285
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722637"
---
# <a name="payroll-position-job"></a>Lønnsstillingsjobb

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Lønnsstillingsjobb-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>beskrivelse

Denne enheten gir relasjonen mellom stilling og jobb for en gitt fast kompensasjonsplan.

Fysisk navn: mshr_payrollpositionjobentity.

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Jobb-ID**<br>mshr_jobid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk |ID-en for jobben. |
| **Gyldig fra**<br>mshr_validto<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet <br>Obligatorisk | Datoen som stillings- og jobbrelasjonen er gyldig fra. |
| **Gyldig til**<br>mshr_validto<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet <br>Obligatorisk | Datoen som stillings- og jobbrelasjonen er gyldig til.  |
| **Stillings-ID**<br>mshr_positionid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | ID-en for stillingen. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Obligatorisk<br>Systemgenerert |  |
| **ID-verdi for stillingsjobb**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_PayrollPositionJobEntity av mshr_payrollpositionjobentity |ID-en for jobben som er knyttet til stillingen.|
| **ID-verdi for fast kompensasjonsplan**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_FixedCompPlan_id av mshr_payrollfixedcompensationplanentity  | ID-en for den faste kompensasjonsplanen som er knyttet til stillingen. |
| **ID for Lønnsstillingsjobb-enhet**<br>mshr_payrollpositionjobentityid<br>*Guid* | Obligatorisk<br>Systemgenerert. | En systemgenerert GUID-verdi som entydig identifiserer jobben.  |

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
