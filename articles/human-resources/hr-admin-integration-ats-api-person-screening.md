---
title: Personscreening
description: Dette emnet beskriver Personscreening-enheten for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5129348f928fd709a5fabe73917522799a2d47e0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066299"
---
# <a name="person-screening"></a>Personscreening


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Personscreening-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonscreeningentity

## <a name="description"></a>beskrivelse

Denne enheten beskriver screeninger en kandidat har bestått eller må bestå for ansettelse.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Enhets-ID for personens screening**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | Unik primær-ID for posten for personscreening. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk | Partnummeret (person) tilknyttet kandidaten. |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity | Systemgenerert unik identifikator for partsenhetsposten (person). |
| **ID for screeningtype**<br>mshr_screeningtypeid<br>*Streng* | Lese/skrive<br>Obligatorisk<br>Sekundærnøkkel: ScreeningType | IDen for screeningtype som er definert i Human Resources. |
| **Verdi for ID for screeningtype**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmscreeningtypeentityid i mshr_hcmscreeningtypeentity | Systemgenerert identifikator for skjermtypeposten i den tilknyttede enheten. |
| **Kreves innen**<br>mshr_requiredby<br>*Datetime* | Lese/skrive<br>Valgfri | Datoen som skjermbildet må fullføres innen. |
| **Status**<br>mshr_status<br>*mshr_hcmcompletionstatus-alternativsett*<br>Lese/skrive<br>Obligatorisk | Gir kandidatens status for screeningen. |
| **Fullføringsdato**<br>mshr_completeddate<br>*Datetime* | Lese/skrive<br>Valgfri | Datoen da screeningen ble fullført. |
| **Notater**<br>mshr_note<br>*Streng* | Lese/skrive<br>Valgfri | Merknader som skal brukes av ansettelsesansvarlige og rekrutteringspersoner. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
