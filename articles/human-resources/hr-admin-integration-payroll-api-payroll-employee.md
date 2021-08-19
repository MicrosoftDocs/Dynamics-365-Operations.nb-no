---
title: Lønnsansatt
description: Dette emnet inneholder informasjon og en eksempelspørring for Lønnsansatt-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 20e74e97f98d0bc0fd454d54cbf969d4f1b46c7c98b2949b0ed8cfe671312dd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768197"
---
# <a name="payroll-employee"></a>Lønnsansatt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Lønnsansatt-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollemployeeentity.

### <a name="description"></a>beskrivelse

Denne enheten gir informasjon om den ansatte. Du må definere [parameterne for lønnsintegrering](hr-admin-integration-payroll-api-parameters.md) før du bruker denne enheten.

>[!IMPORTANT] 
>Feltene **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** vil ikke lenger være tilgjengelige på denne enheten. Dette sikrer at det bare er én datoeffektiv datakilde som sikkerhetskopierer denne enheten.
>Disse feltene vil være tilgjengelige på **DirPersonNameHistoricalEntity**, som ble frigitt i platformoppdatering 43. Det finnes en OData-relasjon fra **PayrollEmployeeEntity** til **DirPersonNameHistoricalEntity** i **Person**-feltet. 

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Personalnummer**<br>mshr_personnelnumber<br>*Streng* | Skrivebeskyttet | Det unike personalnummeret til den ansatte. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Systemgenerert |  |
| **ID for juridisk enhet**<br>mshr_legalentityID<br>*Streng* | Skrivebeskyttet | Angir den juridiske enheten (firmaet). |
| **Kjønn**<br>mshr_gender<br>[mshr_hcmpersongender-alternativsett](hr-admin-integration-payroll-api-gender.md) | Skrivebeskyttet | Den ansattes kjønn. |
| **Enhets-ID for lønnsansatt**<br>mshr_payrollemployeeentityid<br>*GUID* | Obligatorisk<br>Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer den ansatte. |
| **Startdato for ansettelse**<br>mshr_employmentstartdate<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Startdatoen for den ansattes ansettelse. |
| **ID for Identifikasjonstype**<br>mshr_identificationtypeid<br>*Streng* |Skrivebeskyttet | Identifikasjonstypen som er definert for den ansatte. |
| **Sluttdato for ansettelse**<br>mshr_employmentenddate<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet |Sluttdatoen for den ansattes ansettelse.  |
| **Dataområde-ID**<br>mshr_dataareaid_id<br>*GUID* | Skrivebeskyttet <br>Systemgenerert | Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet). |
| **Gyldig til**<br>mshr_namevalidto<br>*Motregning av dato/klokkeslett* |  Skrivebeskyttet | Datoen som ansattinformasjonen er gyldig til. |
| **Fødselsdato**<br>mshr_birthdate<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet | Den ansattes fødselsdato. |
| **Identifikasjonsnummer til**<br>mshr_identificationnumber<br>*Streng* | Skrivebeskyttet |Identifikasjonsnummeret som er definert for den ansatte.  |

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
## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
