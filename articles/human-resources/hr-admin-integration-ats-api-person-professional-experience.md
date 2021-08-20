---
title: Persons yrkeserfaring
description: Dette emnet beskriver Persons yrkeserfaring-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: cc26e0ae1428811161b3573edec4aa47b46ae16dd8a69d44d2cdd77d49e68193
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763040"
---
# <a name="person-professional-experience"></a>Persons yrkeserfaring

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Persons yrkeserfaring-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>beskrivelse

Denne enheten beskriver yrkeserfaring eller arbeidshistorikk for en kandidat.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Persons yrkeserfaring-enhet**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik identifikator for enhetsposten. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk | Unik identifikatoren for personposten for kandidaten. |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity | Systemgenerert unik identifikator for personenhetsposten. |
| **Arbeidsgiverstilling**<br>mshr_employerposition<br>*Streng* | Lese/skrive<br>Obligatorisk | Stillingstittelen til kandidaten under ansettelse. |
| **Navn på arbeidsgiver**<br>mshr_employername<br>*Streng* | Lese/skrive<br>Obligatorisk | Navnet på arbeidsgiveren. |
| **Arbeidsgiverlokasjon**<br>mshr_employerlocation<br>*Streng* | Lese/skrive<br>Valgfri | Arbeidsgiverens lokasjon. Maksimumslengde: 60. Bestemt format er ikke definert eller nødvendig. |
| **Telefon**<br>mshr_phone<br>*Streng* | Lese/skrive<br>Valgfri | Arbeidsgiverens telefonnummer. |
| **URL-adresse**<br>mshr_url<br>*Streng* | Lese/skrive<br>Valgfri | URL-adressen til arbeidsgiverens webområde. |
| **Startdato**<br>mshr_startdate<br>*Datetime* | Lese/skrive<br>Obligatorisk | Startdatoen for kandidatens ansettelse. |
| **Sluttdato**<br>mshr_enddate<br>*Datetime* | Lese/skrive<br>Valgfri | Sluttdatoen for kandidatens ansettelse, eller null hvis kandidaten fremdeles er ansatt her. |
| **Tillat kontakt med arbeidsgiver**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno-alternativsett* | Lese/skrive<br>Valgfri | Angir om kandidaten tillater kontakt med den forrige arbeidsgiveren. |
| **Notater**<br>mshr_note<br>*Streng* | Lese/skrive<br>Valgfri | Merknader som skal brukes av rekrutteringsansvarlig eller ansettelsesansvarlig. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Felt som brukes som en primær identifikator for enhetsposten. Kombinasjon av partsnummer, startdato, arbeidsgiverstilling og arbeidsgivernavn. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]