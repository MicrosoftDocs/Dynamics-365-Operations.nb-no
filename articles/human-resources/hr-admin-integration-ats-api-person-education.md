---
title: Personutdanning
description: Denne artikkelen beskriver Personutdanning-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0fbbb467852d2aeb070c7732c9aa3108fd504de0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893910"
---
# <a name="person-education"></a>Personutdanning


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Personutdanning-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersoneducationentity

## <a name="description"></a>beskrivelse

Denne enheten inneholder utdanningshistorikken til personen som er kandidaten. Utdanningen er knyttet til personens post, som gjør det mulig å knytte utdannelsen til andre roller som opprettes for personen, i tillegg til kandidatposten (arbeider, oppdragstaker og så videre).

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Enhets-ID for personens utdannelse**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik identifikator for enhetsposten for personutdannelsen. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk | Den unike identifikatoren for partposten (personen) for kandidaten. |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity | Den systemgenererte unike identifikatoren for personposten til kandidaten. |
| **Studiepoenggrunnlag**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis-alternativsett* | Lese/skrive<br>Valgfri | Studiepoenggrunnlaget for utdanningsgraden. |
| **Fullførte vekttall**<br>mshr_creditscompleted<br>*Desimal* | Lese/skrive<br>Valgfri | Antallet studiepoeng som er oppnådd for utdannelsen. |
| **Opptjente vekttall**<br>mshr_creditsearned<br>*Desimal* | Lese/skrive<br>Valgfri | Antallet studiepoeng som er oppnådd for utdannelsesposten for en pågående grad. |
| **Studiepoeng som kreves**<br>mshr_creditsneeded<br>*Desimal* | Lese/skrive<br>Valgfri | Antallet studiepoeng som kreves for en utdannelse som pågår. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Valgfri | En beskrivelse av kandidatens utdannelse. |
| **ID for utdannelsesnivå**<br>mshr_educationlevelid<br>*Streng* | Lese/skrive<br>Valgfri | IDen for utdannelsesnivået. | 
| **Verdien på ID-en for utdannelsesnivået**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmeducationdegreeentityid i mshr_hcmeducationdegreeentity-enhet | Systemgenerert identifikator for posten for utdannelsesgrad. Denne IDen angir utdannelsesgradene og -nivåene som er definert for organisasjonen. |
| **ID for utdannelsesdisiplin**<br>mshr_educationdisciplineid<br>*Streng* | Lese/skrive<br>Obligatorisk<br>Sekundærnøkkel: EducationDiscipline | IDen for utdannelsesdisiplinen. |
| **Verdi for ID for utdannelsesdisiplin**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmeducationdisciplineentityid i mshr_hcmeducationdisciplineentity-enhet | Den systemgenererte unike identifikatoren for utdannelsesdisiplinen for utdannelsesposten. |
| **Vektlegging på videregående**<br>mshr_secondaryemphasis<br>*Streng* | Lese/skrive<br>Valgfri | Vektlegging for oppnådd grad for videregående. |
| **ID for utdanningsinstitusjon**<br>mshr_educationinstitutionid<br>*Streng* | Lese/skrive<br>Valgfri | IDen til den vedlagte utdanningsinstitusjonen. |
| **Verdi for ID for utdanningsinstitusjon**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmeducationinstitutionentityid i mshr_hcmeducationinstitutionentity | Systemgenerert identifikator for utdanningsinstitusjonen. |
| **Startdato**<br>mshr_startdate<br>*Datetime* | Lese/skrive<br>Valgfri | Startdatoen for utdannelsen for oppnådd grad. |
| **Sluttdato**<br>mshr_enddate<br>*Datetime* | Lese/skrive<br>Obligatorisk | Datoen da kvalifikasjonsbevis ble utstedt. |
| **Varighet**<br>mshr_duration<br>*Desimal* | Lese/skrive<br>Valgfri | Varigheten for utdannelsesposten. |
| **Varighetsenhet**<br>mshr_durationunit<br>*mshr_periodunit-alternativsett* | Lese/skrive<br>Valgfri | Tidsenhet knyttet til varigheten til utdannelsesposten. |
| **Gjennomsnittskarakter**<br>mshr_gradepointaverage<br>*Desimal* | Lese/skrive<br>Valgfri | Den oppnådde gjennomsnittskarakteren for graden. |
| **Karakterskala**<br>mshr_gradescale<br>*Streng* | Lese/skrive<br>Valgfri | Skalaen som brukes for gjennomsnittskarakteren for graden. |
| **Notater**<br>mshr_notes<br>*Streng* | Lese/skrive<br>Valgfri | Merknader som skal brukes av rekrutteringsansvarlig eller ansettelsesansvarlig. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Felt som brukes som en annen primær identifikator for enhetsposten. Kombinasjon av partsnummer, ID for utdanningsdisiplin, ID for utdanningsinstitusjon og ID for utdannelsesnivå. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
