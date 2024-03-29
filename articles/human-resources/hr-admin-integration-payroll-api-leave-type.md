---
title: Permisjonstype
description: Denne artikkelen inneholder informasjon og en eksempelspørring for permisjonstype-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893793"
---
# <a name="leave-type"></a>Permisjonstype


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver permisjonstype-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>Beskrivelse

Denne enheten gir informasjon for en gitt permisjonstype.

Fysisk navn: mshr_essleavetypeentity.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Type-ID for permisjon**</br>mshr_leavetypeid</br>*Streng* | Skrivebeskyttet | Type-ID for permisjon. |
| **Beskrivelse**</br>mshr_description</br>*Streng* | Skrivebeskyttet | En beskrivelse av permisjonstypen. |
| **Kategori**</br>mshr_category</br>*mshr_LeaveTypeCategory-alternativsett* | Skrivebeskyttet | Kategori for permisjonstype. |
| **Årsakskode kreves**</br>mshr_isreasoncoderequired</br>*mshr_NoYes-alternativsett* | Skrivebeskyttet | Definerer om det kreves en årsakskode for permisjonstypen. |
| **Permisjonsenhet**</br>mshr_leaveamountunit</br>*mshr_LeaveAmountUnit-alternativsett* | Skrivebeskyttet | Enheten for denne permisjonstypen. |
| **Aktiver halv dag**</br>mshr_enablehalfdaydefinition</br>*mshr_NoYes-alternativsett* | Definerer om halv dag er aktivert for permisjonstypen. |
| **Dataområde-ID**</br>mshr_dataareaid_id</br>*Streng* | Skrivebeskyttet | Angir den juridiske enheten (firmaet). |
| **Permisjonstypeenhet**</br>mshr_essleavetypeentityid</br>*GUID* | Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer permisjonstypen. |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Svar**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
