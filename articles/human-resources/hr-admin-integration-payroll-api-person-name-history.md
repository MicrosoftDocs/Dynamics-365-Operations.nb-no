---
title: Historikk for personnavn
description: Dette emnet inneholder informasjon og en eksempelspørring for historikk for personnavn-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 418047a0643ee29b89763dbe2b030753f405b575
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559669"
---
# <a name="person-name-history"></a>Historikk for personnavn

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver historikk for personnavn-enheten i Dynamics 365 Human Resources.

Fysisk navn: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Beskrivelse

Denne enheten gir informasjon om navnhistorikken for en angitt person.

> [!IMPORTANT] 
> Feltene **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** vil ikke lenger være tilgjengelige på Lønnsansatt-enheten. De har blitt fjernet for å sikre at det bare er én datoeffektiv datakilde som sikkerhetskopierer denne enheten.

## <a name="properties"></a>Egenskaper

| Egenskap</br>**Fysisk navn**</br>**_Type_** | Bruk | Beskrivelse |
| --- | --- | --- |
| **Fornavn**</br>mshr_firstname</br>*Streng* | Skrivebeskyttet | Fornavnet. |
| **Prefiks for etternavn**</br>mshr_lastnameprefix</br>*Streng*) | Skrivebeskyttet | Prefiks for etternavn. |
| **Etternavn**</br>mshr_lastname</br>*Streng*) | Skrivebeskyttet | Etternavnet. |
| **Mellomnavn**</br>mshr_middlename</br>*Streng*) | Skrivebeskyttet | Mellomnavnet. |
| **Gyldig til**</br>mshr_validto</br>*Streng*) | Skrivebeskyttet | Datoen som navnet gjelder til. |
| **Partsnummer**</br>mshr_partynumber</br>*Streng* | Skrivebeskyttet | En brukerlesbar, systemgenerert unik identifikator for personen. |
| **Primærfelt**</br>mshr_primaryfield</br>*Streng* | Skrivebeskyttet | Den unike ID-en til posten. |
| **Enhets-ID for personnavnhistorikk**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Systemgenerert | En systemgenerert globalt unik identifikator (GUID)-verdi som identifiserer posten entydig. |

## <a name="relations"></a>Relasjoner

| Egenskapsverdi | Relatert enhet | Navigasjonsegenskap | Samlingstype |
| --- | --- | --- | --- |
| Gjelder ikke | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Gjelder ikke | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Eksempelspørring for lønnsansatt

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Svar**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
