---
title: Kompensasjon, lønnsfrekvens
description: Dette emnet inneholder informasjon og en eksempelspørring for enheten Kompensasjon, lønnsfrekvens i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 171b7fb7b361bd1fe2e7e637cd555c88a81a8bcf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066149"
---
# <a name="compensation-pay-frequency"></a>Kompensasjon, lønnsfrekvens


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver enheten Kompensasjon, lønnsfrekvens i Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Beskrivelse

Denne enheten gir informasjon om lønnssatskonverteringen for en angitt lønnsfrekvens for kompensasjon.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | Beskrivelse |
| --- | --- | --- |
| **Årlig lønnssatskonvertering**</br>mshr_annualconversionfactor</br>*Desimal* | Skrivebeskyttet | Den årlige konverteringsfaktoren for betalingsfrekvensen. |
| **Beskrivelse**</br>mshr_description</br>*Streng* | Skrivebeskyttet | Beskrivelsen av omregningssatsen. |
| **Lønnssatskonvertering per time**</br>mshr_hourlyconversionfactor</br>*Desimal* | Skrivebeskyttet | Konverteringsfaktoren per time for betalingsfrekvensen. |
| **Månedlig lønnssatskonvertering**</br>mshr_monthlyconversionfactor</br>*Desimal* | Skrivebeskyttet | Den månedlige konverteringsfaktoren for betalingsfrekvensen. |
| **Konvertering av lønnssats**</br>mshr_payrateconversion</br>*Streng* | Skrivebeskyttet | En unik streng for å identifisere omregningssatsen. |
| **Periode**</br>mshr_period</br>*periodealternativsett* | Skrivebeskyttet | Hovedperioden for den gitte lønnssatskonverteringen. |
| **Ukentlig lønnssatskonvertering**</br>mshr_weeklyconversionfactor</br>*Desimal* | Skrivebeskyttet | Den ukentlige konverteringsfaktoren for betalingsfrekvensen. |
| **Dataområde-ID**</br>mshr_dataareaid</br>*Streng* | Skrivebeskyttet | Den juridiske enheten (firmaet). |
| **Enhets-ID for Kompensasjon, lønnsfrekvens**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Systemgenerert | En systemgenerert globalt unik identifikator (GUID)-verdi som identifiserer posten entydig. |

## <a name="example-query-for-payroll-employee"></a>Eksempelspørring for lønnsansatt

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Svar**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
