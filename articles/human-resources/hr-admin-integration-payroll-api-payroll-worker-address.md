---
title: Adresse til lønnsarbeider
description: Dette emnet inneholder informasjon og en eksempelspørring for Adresse til lønnsarbeider-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: bf3fc5f333333b9a832ecb9c185473e476ac231d
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559515"
---
# <a name="payroll-worker-address"></a>Adresse til lønnsarbeider

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Adresse til lønnsarbeider-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollworkeraddressentity.

### <a name="description"></a>beskrivelse

Denne enheten gir stedet for lønnsbostedet og lønnsarbeidsstedet for en angitt ansatt.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | Beskrivelse |
| --- | --- | --- |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Det unike personalnummeret til den ansatte. |
| **Plasserings-ID**</br>mshr_locationidbr>*Streng* | Skrivebeskyttet | ID-en for adressen. |
| **Bodde i adresse**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes-alternativsett](hr-admin-integration-payroll-api-no-yes.md)* | Skrivebeskyttet | En verdi som angir om adressen er der den ansatte bor. |
| **Arbeidet i adresse** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes-alternativsett](hr-admin-integration-payroll-api-no-yes.md)* | Skrivebeskyttet | En verdi som angir om adressen er der den ansatte arbeider. |
| **Land/område**</br>mshr_countryregionid</br>*Streng* | Skrivebeskyttet</br>Obligatorisk | Landet eller området definert for adressen. |
| **Postnummer**</br>mshr_zipcode<br>*Streng* | Skrivebeskyttet | Identifikasjonsnummeret som er definert for den ansatte. |
| **Gate**</br>mshr_street</br>*Streng* | Skrivebeskyttet | Gaten definert for adressen. |
| **Poststed**</br>mshr_city</br>*Streng* | Skrivebeskyttet | Poststedet definert for adressen. |
| **Delstat**</br>mshr_state</br>*Streng* | Skrivebeskyttet | Delstaten eller området definert for adressen. |
| **Kommune**</br>mshr_county</br>*Streng* | Skrivebeskyttet | Fylket definert for adressen. |
| **Gyldig fra**</br>mshr_postaladdressvalidfrom</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen som adressen gjelder fra. |
| **Gyldig til**</br>mshr_postaladdressvalidto</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Datoen som adressen gjelder til. |
| **Primærfelt**</br>mshr_primaryfield</br>*Streng* | Skrivebeskyttet | Primærfeltet. |
| **Adresse-ID for lønnsarbeider**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Systemgenerert | En systemgenerert globalt unik identifikator (GUID)-verdi som identifiserer adressen entydig. |

## <a name="relations"></a>Relasjoner

| Egenskapsverdi | Relatert enhet | Navigasjonsegenskap | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
