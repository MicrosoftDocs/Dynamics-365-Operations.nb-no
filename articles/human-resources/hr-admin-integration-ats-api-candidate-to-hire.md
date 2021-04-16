---
title: Ansettelseskandidat
description: Dette emnet beskriver Kandidaten for ansettelse-enheten i Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f0ddf7bd403c926b231f9e010280083d1638b3ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795051"
---
# <a name="candidate-to-hire"></a>Ansettelseskandidat

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Kandidaten for ansettelse-enheten i Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmcandidatetohireentity

## <a name="description"></a>beskrivelse

Denne enheten gir kandidatdetaljer som brukes til å opprette en arbeider i Dynamics 365 Human Resources. Den brukes til å lese alle kandidatposter og opprette interne og eksterne kandidatposter, slik at du kan opprette personlige opplysninger for den nye kandidaten.

Når du oppretter en ekstern kandidatpost som skal være en ny personpost i systemet, må du ikke definere et partsnummer (person) som du posterer en ny kandidatpost. Den nye personenhetsposten opprettes med den nye kandidatposten.

Når du oppretter en intern kandidatpost (en kandidat til en stilling som allerede har en ansattpost i firmaet), definerer du partsnummeret til posten (personen) som allerede eksisterer for personen for mshr_partynumber-egenskapen i kandidatposten i stedet for å definere personlige opplysninger (som navn, kjønn eller fødselsdato) som kan brukes til å opprette en ny personpost.

## <a name="json-representation"></a>JSON-representasjon

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Kandidat for ansettelse-enhet**<br>mshr_hcmcandidatetohireentityid<br>Guid | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | En systemgenerert unik identifikator for enhetsposten. |
| **Kandidat-ID**<br>mshr_candidateid<br>Streng | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | En unik identifikator for enheten. |
| **Partsnummer**<br>mshr_partynumber<br>Streng | Skrivebeskyttet<br>Obligatorisk | Partnummeret (person) for kandidatens personpost. |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>Guid | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid av mshr_direpersonentity | Den systemgenererte unike identifikatoren for partposten (personen) for kandidaten. |
| **Partstype**<br>mshr_partytype<br>mshr_dirpartytype-alternativsett | Skrivebeskyttet<br>Obligatorisk | Partstypen for posten, som definert i alternativsettet mshr_dirpartytype. For denne enheten vil typen alltid være "Person". |
| **ID for rekrutteringsforespørsel**<br>mshr_recruitingrequestid<br>Streng | Skriv én gang<br>Valgfri | Referanser til rekrutteringsforespørselen denne kandidaten oppfyller. |
| **ID for rekrutteringsforespørselsverdi**<br>_mshr_fk_recruitingrequest_id_value<br>Guid | Lese/skrive<br>Valgfri<br>Sekundærnøkkel: mshr_hcmrecruitingrequestentityid i mshr_hcmrecruitingrequestentity | Den systemgenererte unike identifikatoren for rekrutteringsforespørselen kandidaten oppfyller. |
| **Stillings-ID**<br>mshr_positionid<br>Streng | Lese/skrive<br>Valgfri | IDen for stillingen som kandidaten vurderes for. |
| **Stillings-ID-verdi**<br>_mshr_fk_position_if_value<br>Guid | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmpositionv2entityid i mshr_hcmpositionv2entity | Systemgenerert identifikator for stillingen som kandidaten vurderes for. |
| **Fornavn**<br>mshr_firstname<br>Streng | Lese/skrive<br>Obligatorisk | Kandidatens fornavn. |
| **Mellomnavn**<br>mshr_middlename<br>Streng | Lese/skrive<br>Valgfri | Kandidatens mellomnavn. |
| **Prefiks for etternavn**<br>mshr_lastnameprefix<br>Streng | Lese/skrive<br>Valgfri | Prefiks for etternavn til kandidat. |
| **Etternavn**<br>mshr_lastname<br>Streng | Lese/skrive<br>Valgfri | Kandidatens etternavn. |
| **Kjønn**<br>mshr_gender<br>mshr_hcmpersongender-alternativsett | Lese/skrive<br>Valgfri | Kandidatens kjønn. |
| **Fødselsdato**<br>mshr_birthdate<br>Dato/klokkeslett | Lese/skrive<br>Valgfri | Kandidatens fødselsdato. |
| **Kode for statsborgerskap**<br>mshr_citizenshipcountrycode<br>Streng | Lese/skrive<br>Valgfri | Angir landet der kandidaten har statsborgerskap. Gyldige landskoder er mshr_logisticaddresscountryregionentity. |
| **ID for veteranstatus**<br>mshr_veteranstatusid<br>Streng | Lese/skrive<br>Valgfri | Viser veteranstatusen for kandidaten. |
| **Verdi for ID for veteranstatus**<br>_mshr_fk_veteranstatus_id_value<br>Guid | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmveteranstatusentityid i mshr_hcmveteranstatusentity | Systemgenerert unik identifikator for enhetsposten for veteranstatus. |
| **Startdato for militærtjeneste**<br>mshr_militaryservicestartdate<br>Dato/klokkeslett | Lese/skrive<br>Valgfri | Startdatoen for kandidatens militærtjeneste. |
| **Sluttdato for militærtjeneste**<br>mshr_militaryserviceenddate<br>Dato/klokkeslett | Lese/skrive<br>Valgfri | Sluttdatoen for kandidatens militærtjeneste. |
| **Er ufør veteran**<br>mshr_isdisabledveteran<br>mshr_noyes-alternativsettet | Lese/skrive<br>Valgfri | Viser om kandidaten har deaktivert veteranstatus. |
| **Tilgjengelighetsdato**<br>mshr_availabilitydate<br>Dato/klokkeslett | Lese/skrive<br>Valgfri | Den tidligste datoen kandidaten er tilgjengelig for jobb. |
| **Er villig til å flytte**<br>mshr_iswillingtorelocate<br>mshr_noyes-alternativsettet | Lese/skrive<br>Valgfri | Viser om kandidaten er villig til å flytte for stillingen. |
| **Kommentarer**<br>mshr_comments<br>Streng | Lese/skrive<br>Valgfri | Kommentarer som skal brukes av rekrutteringsansvarlig eller ansettelsesansvarlig. |
| **Applikasjonsintegrasjonsresultat**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult-alternativsett | Lese/skrive<br>Obligatorisk | Statusen for kandidaten i ansettelsesprosessen knyttet til integreringen. |
| **Årsakskode-ID for ikke ansett**<br>mshr_donothirereasoncodeid<br>Streng | Lese/skrive<br>Valgfri | Du kan velge å angi en årsakskode når statusen (applikasjonsintegrasjonsresultat) er satt til "Ikke ansatt". |
| **Verdi for årsakskode-ID**<br>_mshr_fk_reasoncode_id_value<br>Guid | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmreasoncodeentityid i mshr_hcmreasoncodeentity-enhet | Systemgenerert unik identifikator for årsakskoden **Ikke ansett**. |
| **Dataområde-ID**<br>mshr_dataareaid<br>Streng | Lese/skrive<br>Valgfri |  Angir den juridiske enheten (firmaet). |
| **Verdi for dataområde-ID**<br>_mshr_dataareaid_id_value<br>Guid | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: cdm_companyid i cdm_company-enhet | Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet). |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]