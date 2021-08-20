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
ms.openlocfilehash: 898ca7b33e39ec33990fecc4c3a7229620fbfddd5ce8ad14423af38047187e55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761980"
---
# <a name="payroll-worker-address"></a>Adresse til lønnsarbeider

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Adresse til lønnsarbeider-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollworkeraddressentity.

### <a name="description"></a>beskrivelse

Denne enheten gir stedet for lønnsbostedet og lønnsarbeidsstedet for en angitt ansatt.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Poststed**</br>mshr_city</br>*Streng* | Skrivebeskyttet</br>Obligatorisk | Poststedet definert for adressen.   |
| **Personalnummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet</br>Obligatorisk | Det unike personalnummeret til den ansatte.  |
| **Land/område**</br>mshr_countryregionid</br>*Streng* | Skrivebeskyttet</br>Obligatorisk | Landet eller området definert for adressen.  |
| **Gyldig fra**</br>mshr_postaladdressvalidfrom</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet </br>Obligatorisk | Datoen som adressen gjelder fra. |
| **Arbeidet i adresse** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes-alternativsett](hr-admin-integration-payroll-api-no-yes.md)* | Skrivebeskyttet</br>Obligatorisk | Angir om adressen er der den ansatte arbeider. |
| **Kommune**</br>mshr_county</br>*Streng* | Skrivebeskyttet</br>Obligatorisk | Landet definert for adressen.  |
| **Adresse-ID for lønnsarbeider**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Obligatorisk</br>Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer adressen.  |
| **Primærfelt**</br>mshr_primaryfield</br>*Streng* | Skrivebeskyttet</br>Obligatorisk |  |
| **Gate**</br>mshr_street</br>*Streng* | Skrivebeskyttet</br>Obligatorisk | Gaten definert for adressen. |
| **Gyldig til**</br>mshr_postaladdressvalidto</br>*Motregning av dato/klokkeslett* | Skrivebeskyttet </br>Obligatorisk | Datoen som adressen gjelder til.  |
| **Plasserings-ID**</br>mshr_locationidbr>*Streng* | Skrivebeskyttet <br>Obligatorisk | ID-en for adressen.  |
| **Postnummer**</br>mshr_zipcode<br>*Streng* | Skrivebeskyttet <br>Obligatorisk |Identifikasjonsnummeret som er definert for den ansatte.  |
| **Bodde i adresse**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes-alternativsett](hr-admin-integration-payroll-api-no-yes.md)* | Skrivebeskyttet</br>Obligatorisk | Angir om adressen er der den ansatte bor. |
| **Delstat**</br>mshr_state</br>*Streng* | Skrivebeskyttet</br>Obligatorisk | Delstaten definert for adressen.  |

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
