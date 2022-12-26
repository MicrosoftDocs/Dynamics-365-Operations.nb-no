---
title: Personscreening
description: Denne artikkelen beskriver Personscreening-enheten for Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/05/2022
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
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831897"
---
# <a name="person-screening"></a>Personscreening


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Personscreening-enheten for Dynamics 365 Human Resources.

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
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | Beskrivelse |
| --- | --- | --- |
| **Notater**<br>mshr_note<br>*Streng* | Lese/skrive<br>Valgfri | Merknader som skal brukes av ansettelsesansvarlige og rekrutteringspersoner. |
| **Kreves innen**<br>mshr_requiredby<br>*Datetime* | Lese/skrive<br>Valgfri | Datoen som skjermbildet må fullføres innen. |
| **Status**<br>mshr_status<br>*mshr_hcmcompletionstatus-alternativsett*|Lese/skrive<br>Obligatorisk | Gir kandidatens status for screeningen. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk | Partnummeret (person) tilknyttet kandidaten. |
| **ID for screeningtype**<br>mshr_screeningtypeid<br>*Streng* | Lese/skrive<br>Obligatorisk<br>Sekundærnøkkel: ScreeningType | IDen for screeningtype som er definert i Human Resources. |
| **Verdi for ID for screeningtype**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmscreeningtypeentityid i mshr_hcmscreeningtypeentity | Systemgenerert identifikator for skjermtypeposten i den tilknyttede enheten. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* |  Skrivebeskyttet<br>Obligatorisk | Felt som brukes som en identifikator for enhetsposten. |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity | Systemgenerert unik identifikator for partsenhetsposten (person). |
| **Enhets-ID for personens screening**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert| Unik primær-ID for posten for personscreening. |
| **Fullføringsdato**<br>mshr_completeddate<br>*Datetime* | Lese/skrive<br>Valgfri | Datoen da screeningen ble fullført. |


## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
