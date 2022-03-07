---
title: Personidentifikasjonsnummer
description: Dette emnet beskriver Personidentifikasjonsnummer-enheten for Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 054547c4f33e50d2dc0fa275559ba6ed44c27971
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125407"
---
# <a name="person-identification-number"></a>Personidentifikasjonsnummer

Dette emnet beskriver Personidentifikasjonsnummer-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>beskrivelse

Denne enheten beskriver identifikasjonsnumrene for kandidaten. Den gjør det mulig for API-forbrukeren å skrive identifikasjonsnumre, for eksempel personnummer eller passnummer, til kandidatposten. Identifikasjonsnumrene vises på arbeiderposten, men ikke på kandidatposten. Et integreringsprogram kan skrive verdiene til Human Resources-databasen, men tallene vises ikke i Human Resources før kandidatens arbeidspost er opprettet.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Personidentifikasjonsnummer-enhet**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | Unik primær-ID for posten for personidentifikasjonsnummeret. |
| **Oppføringstype**<br>mshr_entrytype<br>*Streng* | Lese/skrive<br>Valgfri | Fri verdi som kan brukes til å referere til oppføringstypen for identifikasjonsnummeret. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelsen av identifikasjonsnummeret. |
| **Utløpsdato**<br>mshr_expirationdate<br>*Datetime* | Lese/skrive<br>Valgfri | Datoen da identifikasjonsnummeret eller det tilknyttede dokumentet utløper. |
| **Er primær**<br>mshr_isprimary<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Valgfri | Definerer om identifikasjonsnummeret er primærposten for personen for denne identifikasjonstypen. |
| **Identifikasjonsnummer**<br>mshr_identificationnumber<br>*Streng* | Lese/skrive<br>Obligatorisk | Identifikasjonsnummeret. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk | Den unike identifikatoren for parten (personen) som eier identifikasjonsnummeret. |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity-enhet | Den unike ID-en til parten (personen). |
| **ID for Identifikasjonstype**<br>mshr_identificationtypeid<br>*Streng* | Lese/skrive<br>Obligatorisk | Typen identifikasjonsnummer. |
| **Verdi for ID for Identifikasjonstype**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmidentificationtypeentityid i mshr_hcmidentificationtypeentity-enhet | Systemgenerert unik ID for identifikasjonstypen. |
| **ID for utstedende byrå**<br>mshr_issuingagencyid<br>*Streng* | Lese/skrive<br>Valgfri | Byrået eller organisasjonen som utsteder identifikasjonsnummeret. |
| **Verdi for ID for utstedende byrå**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmissuingagencyentityid i mshr_hcmissuingagencyentity-enhet | Systemgenerert unik ID for byrået som utsteder identifikasjonsnummeret. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Felt som brukes som en identifikator for enhetsposten. Kombinasjon av partnummer, identifikasjonstype-ID og identifikasjonsnummer. |
| **Utstedelsesdato**<br>mshr_issuedate<br>*Dato* | Lese/skrive<br>Valgfri | Datoen da identifikasjonsnummeret ble utstedt. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

