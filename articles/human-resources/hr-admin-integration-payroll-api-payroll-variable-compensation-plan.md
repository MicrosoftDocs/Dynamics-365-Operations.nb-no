---
title: Variabel kompensasjonsplan for lønn
description: Dette emnet inneholder informasjon og en eksempelspørring for enheten Variabel kompensasjonsplan for lønn i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96a644bf129de6dd3f78098bcb6415d17058d6decbd7d904a99bb6f050d3a9e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730448"
---
# <a name="payroll-variable-compensation-plan"></a>Variabel kompensasjonsplan for lønn

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Variabel kompensasjonsplan for lønn-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>beskrivelse

Denne enheten gir den variable kompensasjonsplanen som er tilordnet for en gitt stilling av en ansatt.

Fysisk navn: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet</br>Obligatorisk |Det unike personalnummeret til den ansatte.  |
| **Belønningsdato**</br>mshr_awarddate</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet</br>Obligatorisk | Dato for belønningen. |
| **Belønningstype**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType-alternativsett](hr-admin-integration-payroll-api-award-type.md)* | Skrivebeskyttet</br>Obligatorisk | Belønningstypen som er definert for den variable kompensasjonsplanen. |
| **Valuta.**</br>mshr_unitcurrencycode</br>*Streng* | Skrivebeskyttet </br>Obligatorisk |Valutaen som er definert for den variable kompensasjonsplanen.   |
| **Fast kompensasjonsplan-ID**</br>mshr_fixedplanid</br>*Streng* | Skrivebeskyttet | Den faste kompensasjonsplanen som brukes som basis for beregningen av belønningen. |
| **Enhetsverdi**</br>mshr_awardamount</br>*Desimal* | Skrivebeskyttet | Verdien på enheten |
| **Prosesstype**</br>mshr_processtype</br>*[mshr_hrmCompProcessType-alternativsett](hr-admin-integration-payroll-api-process-type.md)* | Skrivebeskyttet | Prosesstypen. |
| **Variabel kompensasjonsplantype**</br>Streng</br>*mshr_typeid* | Skrivebeskyttet | Typen variabel kompensasjonsplan. |
| **ID for variabel kompensasjonsplan**</br>Streng</br>*mshr_planid* | Skrivebeskyttet | ID-en for den variable kompensasjonsplanen. |
| **Primærfelt**</br>mshr_primaryfield</br>*GUID* | Skrivebeskyttet</br>Systemgenerert. | |
| **Ansatt-ID**</br>mshr_fk_employee_id_value</br>*GUID* | Skrivebeskyttet</br>Obligatorisk</br>Sekundærnøkkel: mshr_Employee_id av mshr_payrollemployeeentity-enheten  | Ansatt-ID. |
| **Variabel kompensasjonsplan for lønn-enhet**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Obligatorisk</br>Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer kompensasjonsplanen. |


## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
