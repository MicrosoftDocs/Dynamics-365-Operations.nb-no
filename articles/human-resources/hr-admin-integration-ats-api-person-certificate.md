---
title: Personsertifikat
description: Dette emnet beskriver Personsertifikat-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055202"
---
# <a name="person-certificate"></a>Personsertifikat

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Personsertifikat-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersoncertificateentity

## <a name="description"></a>beskrivelse

Denne enheten beskriver de profesjonelle sertifikatene til en kandidat.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Personsertifikat-enhet**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik identifikator for posten for personsertifikatenhet. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk | Parts-ID-en (person) til kanditaten. |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity | Systemgenerert unik identifikator for partsenhetsposten (person). |
| **ID for sertifikattype**<br>mshr_certificatetypeid<br>*Streng* | Lese/skrive<br>Obligatorisk |  IDen for sertifikattype som er definert i Human Resources. |
| **Verdi for ID for sertifikattype**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmcertificatetypeentityid i mshr_hcmcertificatetypeentity | Systemgenerert unik identifikator for sertifikattype i den tilknyttede enheten. |
| **Startdato**<br>mshr_startdate<br>*Datetime* | Lese/skrive<br>Obligatorisk | Datoen da sertifikatet ble utstedt. |
| **Sluttdato**<br>mshr_enddate<br>*Datetime* | Lese/skrive<br>Valgfri | Datoen da sertifikatet utløper. |
| **Notater**<br>mshr_notes<br>*Streng* | Lese/skrive<br>Valgfri | Merknader som skal brukes av ansettelsesansvarlige og rekrutteringspersoner. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk |  Felt som brukes som en identifikator for enhetsposten. Kombinasjon av partnummer, ID for sertifikattype og startdato. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]