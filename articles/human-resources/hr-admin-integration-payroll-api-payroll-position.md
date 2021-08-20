---
title: Lønnsdetaljer for stillinger
description: Dette emnet inneholder informasjon og en eksempelspørring for lønnsdetaljene for Stillinger-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 05e9d6441cf99dce3f4663b9d5ba57e2b386e8c2f3060f75550270083f3b98b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741459"
---
# <a name="payroll-position"></a>Lønnsstilling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Lønnsstillinger-enheten i Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollpositionentity.

### <a name="description"></a>beskrivelse

Denne enheten gir stillingsrelatert informasjon for en gitt ansatt.

Fysisk navn: 

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Årlige vanlige timer**<br>annualregularhours<br>*Desimal* | Skrivebeskyttet<br>Obligatorisk | Årlige faste timer definert i stillingen.  |
| **Enhets-ID for lønnsstillingsdetaljer**<br>payrollpositiondetailsentityid<br>*Guid* | Obligatorisk<br>Systemgenerert. | En systemgenerert GUID-verdi som entydig identifiserer stillingen.  |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Obligatorisk<br>Systemgenerert |  |
| **ID-verdi for stillingsjobb**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_PayrollPositionJobEntity av mshr_payrollpositionjobentity |ID-en for jobben som er knyttet til stillingen.|
| **ID-verdi for fast kompensasjonsplan**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_FixedCompPlan_id av mshr_payrollfixedcompensationplanentity  | ID-en for den faste kompensasjonsplanen som er knyttet til stillingen. |
| **ID for lønnssyklus**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Lønnssyklusen som er definert for stillingen. |
| **Betalt av juridisk enhet**<br>paidbylegalentity<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Den juridiske enheten som er definert i stillingen som er ansvarlig for utstedelse av betaling. |
| **Stillings-ID**<br>mshr_positionid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | ID-en for stillingen. |
| **Gyldig til**<br>validto<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet<br>Obligatorisk |Datoen stillingsdetaljene er gyldige fra.  |
| **Gyldig fra**<br>validfrom<br>*Motregning av dato/klokkeslett* | Skrivebeskyttet<br>Obligatorisk |Datoen stillingsdetaljene er gyldige til.  |

## <a name="example-query"></a>Eksempelspørring

**Forespørsel**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
