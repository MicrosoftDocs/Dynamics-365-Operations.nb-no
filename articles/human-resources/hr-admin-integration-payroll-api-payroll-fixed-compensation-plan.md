---
title: Fast kompensasjonsplan for lønn
description: Dette emnet inneholder informasjon og en eksempelspørring for enheten Fast kompensasjonsplan for lønn i Dynamics 365 Human Resources.
author: jcart
manager: tfehr
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882049"
---
# <a name="payroll-fixed-compensation-plan"></a>Fast kompensasjonsplan for lønn

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet inneholder informasjon og en eksempelspørring for enheten Fast kompensasjonsplan for lønn i Dynamics 365 Human Resources.

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
| **Stillings-ID**<br>mshr_positionid<br>*Streng* | Skrivebeskyttet <br>Obligatorisk | Posterings-ID som er knyttet til den ansatte og fast kompensasjonsplanregistrering. |
| **Valuta.**<br>mshr_currency<br>*Streng* | Skrivebeskyttet <br>Obligatorisk |Valutaen som er definert for den faste kompensasjonsplanen   |
| **Personalnummer**<br>mshr_personnelnumber<br>*Streng* | Skrivebeskyttet<br>Obligatorisk |Det unike personalnummeret til den ansatte.  |

**Forespørsel**

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
