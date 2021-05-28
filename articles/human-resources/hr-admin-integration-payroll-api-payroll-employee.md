---
title: Lønnsansatt
description: Dette emnet inneholder informasjon og en eksempelspørring for Lønnsansatt-enheten i Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0cd37a7323c0dd0dc6e60ff0495f827e9a8582c1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019376"
---
# <a name="payroll-employee"></a>Lønnsansatt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet inneholder informasjon og en eksempelspørring for Lønnsansatt-enheten i Dynamics 365 Human Resources.

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Personalnummer**<br>mshr_personnelnumber<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Det unike personalnummeret til den ansatte. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Obligatorisk<br>Systemgenerert |  |
| **Etternavn**<br>mshr_lastname<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Ansattes etternavn. |
| **ID for juridisk enhet**<br>mshr_legalentityID<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Angir den juridiske enheten (firmaet). |
| **Gyldig fra**<br>mshr_namevalidfrom<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet <br>Obligatorisk | Datoen som ansattinformasjonen er gyldig fra.  |
| **Kjønn**<br>mshr_gender<br>*Int32* | Skrivebeskyttet<br>Obligatorisk | Den ansattes kjønn. |
| **Enhets-ID for lønnsansatt**<br>mshr_payrollemployeeentityid<br>*GUID* | Obligatorisk<br>Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer den ansatte. |
| **Startdato for ansettelse**<br>mshr_employmentstartdate<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet<br>Obligatorisk | Startdatoen for den ansattes ansettelse. |
| **ID for Identifikasjonstype**<br>mshr_identificationtypeid<br>*Streng* |Skrivebeskyttet<br>Obligatorisk | Identifikasjonstypen som er definert for den ansatte. |
| **Sluttdato for ansettelse**<br>mshr_employmentenddate<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet<br>Obligatorisk |Sluttdatoen for den ansattes ansettelse.  |
| **Dataområde-ID**<br>mshr_dataareaid_id<br>*GUID* | Obligatorisk <br>Systemgenerert | Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet). |
| **Gyldig til**<br>mshr_namevalidto<br>*Motregning av dato/klokkeslett* |  Skrivebeskyttet<br>Obligatorisk | Datoen som ansattinformasjonen er gyldig til. |
| **Fødselsdato**<br>mshr_birthdate<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet <br>Obligatorisk | Den ansattes fødselsdato. |
| **Identifikasjonsnummer til**<br>mshr_identificationnumber<br>*Streng* | Skrivebeskyttet <br>Obligatorisk |Identifikasjonsnummeret som er definert for den ansatte.  |
| **Fornavn**<br>mshr_firstname<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Ansattes fornavn. |
| **Mellomnavn**<br>mshr_middlename<br>*Streng* | Skrivebeskyttet<br>Obligatorisk |Ansattes mellomnavn.  |

## <a name="example-query-for-payroll-employee"></a>Eksempelspørring for lønnsansatt

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Svar**

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
