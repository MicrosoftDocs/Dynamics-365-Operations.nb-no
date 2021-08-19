---
title: Fast kompensasjonsplan for lønn
description: Dette emnet inneholder informasjon og en eksempelspørring for enheten Fast kompensasjonsplan for lønn i Dynamics 365 Human Resources.
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
ms.openlocfilehash: f1e5345d9f27106bdf3a3a60cb0480a9b072e340c01236e4d48c5e2ae592ddbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738397"
---
# <a name="payroll-fixed-compensation-plan"></a>Fast kompensasjonsplan for lønn

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Fast kompensasjonsplan for lønn-enheten for Dynamics 365 Human Resources.

### <a name="description"></a>beskrivelse

Denne enheten gir den faste kompensasjonsplanen som er tilordnet for en gitt stilling av en ansatt.

Fysisk navn: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Ansatt-ID**<br>mshr_fk_employee_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_Employee_id av mshr_payrollemployeeentity-enheten  | Ansatt-ID |
| **Lønnssats**<br>mshr_payrate<br>*Desimal* | Skrivebeskyttet<br>Obligatorisk | Lønnssats som er definert i den faste kompensasjonsplanen. |
| **Plan-ID**<br>mshr_planid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk |Angir kompensasjonsplanen.  |
| **Gyldig fra**<br>mshr_validfrom<br>*Motregning av dato/klokkeslett* |  Skrivebeskyttet<br>Obligatorisk |Datoen som den ansattes faste kompensasjon er gyldig fra.  |
| **Fast kompensasjonsplan for lønn-enhet**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Obligatorisk<br>Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer kompensasjonsplanen. |
| **Lønnsfrekvens**<br>mshr_payfrequency<br>*Streng* | Skrivebeskyttet<br>Obligatorisk |Frekvensen den ansatte får betalt.  |
| **Gyldig til**<br>mshr_validto<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet <br>Obligatorisk | Datoen som den ansattes faste kompensasjon er gyldig til. |
| **Stillings-ID**<br>mshr_positionid<br>*Streng* | Skrivebeskyttet <br>Obligatorisk | Stillings-ID som er knyttet til den ansatte og fast kompensasjonsplanregistrering. |
| **Valuta.**<br>mshr_currency<br>*Streng* | Skrivebeskyttet <br>Obligatorisk |Valutaen som er definert for den faste kompensasjonsplanen   |
| **Personalnummer**<br>mshr_personnelnumber<br>*Streng* | Skrivebeskyttet<br>Obligatorisk |Det unike personalnummeret til den ansatte.  |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
