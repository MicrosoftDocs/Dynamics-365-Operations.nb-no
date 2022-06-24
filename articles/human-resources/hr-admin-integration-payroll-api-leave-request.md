---
title: Permisjonsforespørsel
description: Denne artikkelen inneholder informasjon og en eksempelspørring for permisjonsforespørsel-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899679"
---
# <a name="leave-request"></a>Permisjonsforespørsel


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver permisjonsforespørsel-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>Beskrivelse

Denne enheten gir informasjon om en permisjonsforespørsel.

Fysisk navn: mshr_essleaverequestentity.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Forespørsels-ID**</br>mshr_requestid</br>*Streng* | Skrivebeskyttet | Forespørsels-ID-en. |
| **Type-ID for permisjon**</br>mshr_leavetypeid</br>*Streng* | Skrivebeskyttet | Type-ID for permisjon. |
| **Dato**</br>mshr_leavedate</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen for permisjonsforespørselen. |
| **Beløp**</br>mshr_amount</br>*Desimal* | Skrivebeskyttet | Permisjonsforespørselsbeløpet. |
| **Halvdagstype**</br>mshr_halfdaydefinition</br>*mshr_LeaveHalfDayDefinition-alternativsett* | Skrivebeskyttet | Typen halvdags permisjon. |
| **Kommentar**</br>mshr_comment</br>*Streng* | Skrivebeskyttet | Kommentar for forespørselen. |
| **Status**</br>mshr_status</br>*mshr_status-alternativsett* | Skrivebeskyttet | Statusen for forespørselen. |
| **Dato**</br>mshr_requestdate</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen for forespørselen. |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Det unike personalnummeret til den ansatte. |
| **Årsakskode-ID**</br>mshr_reasoncodeid</br>*Streng* | Skrivebeskyttet | Årsakskode-ID-en. |
| **Dataområde-ID**</br>mshr_dataareaid</br>*Streng* | Skrivebeskyttet | Angir den juridiske enheten (firmaet). |
| **Primærfelt**</br>mshr_primaryfield</br>*GUID* | Skrivebeskyttet</br>Systemgenerert | |
| **Permisjonstypeenhet**</br>mshr_essleaverequestentityid</br>*GUID* | Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer permisjonsforespørselen. |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Svar**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
