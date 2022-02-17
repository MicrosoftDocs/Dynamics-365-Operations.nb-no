---
title: Permisjonssaldo
description: Dette emnet inneholder informasjon og en eksempelspørring for permisjonssaldo-enheten i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d26d9624ae8d99b208f77d12137262983499c51
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064822"
---
# <a name="leave-balance"></a>Permisjonssaldo


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver permisjonssaldo-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>beskrivelse

Denne enheten gir permisjonssaldo per permisjonstype for en angitt ansatt.

Fysisk navn: mshr_essleavebalanceentities.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Det unike personalnummeret til den ansatte. |
| **Gjeldende saldo**</br>mshr_balanceavailable</br>*Desimal* | Skrivebeskyttet | Den ansattes gjeldende saldo. |
| **Type**</br>mshr_balanceavailable</br>*Streng* | Skrivebeskyttet | Type-ID for permisjon. |
| **Avsetningssats**</br>mshr_accrualratedescription</br> | Skrivebeskyttet | Avsetningsraten. |
| **Siste overføringsbeløp**</br>mshr_lastcarryforwardamount</br>*Desimal* | Skrivebeskyttet | Siste overføring-beløp. |
| **Tatt dette året**</br>mshr_takenthisyear</br>*Desimal* | Skrivebeskyttet | Permisjonsbeløpet som ble tatt i år. |
| **Totalt i inneværende år**</br>mshr_totalthisyear</br>*Desimal* | Skrivebeskyttet | Det totale beløpet for dette året. |
| **Dataområde-ID**</br>mshr_dataareaid_id</br>*Streng* | Skrivebeskyttet | Angir den juridiske enheten (firmaet). |
| **Primærfelt**</br>mshr_primaryfield</br>*GUID* | Skrivebeskyttet</br>Systemgenerert | |
| **Type-ID for permisjon**</br>_mshr_fk_leavetype_id_value</br>*GUID* | Skrivebeskyttet</br>Sekundærnøkkel:mshr_essleavetypeentityid of mshr_essleavetypeentity entity  | Type-ID for permisjon |
| **Permisjonssaldo-enhet**</br>mshr_essleavebalanceentityid</br>*GUID* | Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer saldoen. |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
