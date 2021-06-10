---
title: Rekrutteringsforespørsel
description: Dette emnet beskriver Rekrutteringsforespørsel-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: e56d956016fa43ac980ecc9118000f41569ca98a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059166"
---
# <a name="recruiting-request"></a>Rekrutteringsforespørsel

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Rekrutteringsforespørsel-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestentity

### <a name="description"></a>beskrivelse

Beskriver en forespørsel om å rekruttere for en jobb.

### <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for rekrutteringsforespørsel**<br>mshr_recruitingrequestid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | En brukerlesbar unik identifikator for forespørselen som vises i personalprogrammet. Nummerserie. |
| **ID for Rekrutteringsforespørsel-enhet**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | En systemgenerert GUID-verdi som entydig identifiserer rekrutteringsforespørselen. |
| **Dataområde-ID**<br>mshr_dataareaid<br>*Streng* | Lese/skrive<br>Valgfri<br> | Angir den juridiske enheten (firmaet) for rekrutteringsforespørselen. |
| **Verdi for dataområde-ID**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: cdm_companyid i cdm_company-enhet | Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet) for rekrutteringsforespørselen. |
| **Personalnummer for ansettelsessjef**<br>mshr_hiringmanagerpersonnelnumber<br>*Streng* | Lese/skrive<br>Valgfri | Personalnummeret til ansettelsesansvarlig som er knyttet til denne rekrutteringsforespørselen. |
| **ID-verdi for ansettelsesansvarlig**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmworkerbaseentityid i mshr_hcmworkerbaseentity-enhetentity | Systemgenerert GUID-verdi for å identifisere lederen som er knyttet til rekrutteringsforespørselen. |
| **Rekrutterers partsnummer**<br>mshr_recruiterpartynumber<br>*Streng* | Lese/skrive<br>Valgfri | Personnummeret (part) til rekrutteringspersonen som er valgt for forespørselen. |
| **Verdi for rekrutterings-ID**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity-enhet | Systemgenerert GUID-verdi for å identifisere rekruttereren som er knyttet til rekrutteringsforespørselen. |
| **Status**<br>mshr_status<br>Alternativsett for *RecruitingRequestStatus* | Lese/skrive<br>Obligatorisk<br> | Viser statusen for rekrutteringsforespørselen. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Obligatorisk | Beskriver forespørselen. |
| **ID for rekrutteringsforespørselssted**<br>mshr_recruitingrequestlocationid<br>*Streng* | Lese/skrive<br>Valgfri | Den brukerlesbare unike identifikatoren for jobblokasjonen som er knyttet til denne forespørselen. |
| **Verdi for rekrutteringslokasjons-ID**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmrecruitingrequestlocationentityid i mshr_hcmrecruitingrequestlocationentity-enhet | Systemgenerert GUID-verdi for å identifisere rekrutteringsforespørselslokasjonen som er valgt for rekruttereren. |
| **Kommentarer**<br>mshr_comments<br>*Streng* | Lese/skrive<br>Valgfri | Kommentarer om forespørselen som brukes av ansettelsesansvarlige og rekrutteringsansvarlige. |
| **Jobb-ID**<br>mshr_jobid<br>*Streng* | Skriv én gang<br>Obligatorisk |   Den brukerlesbare unike identifikatoren for jobben som deles av alle posisjoner som er knyttet til denne forespørselen. |
| **Verdi for jobb-ID**<br>_mshr_fk_job_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmjobentityid i mshr_hcmjobentity-enhet | Den systemgenererte unike identifikatoren for jobben som deles av alle posisjoner som er knyttet til rekrutteringsforespørselen. |
| **Tittel-ID**<br>mshr_titleid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Den brukerlesbare unike identifikatoren for jobbtittelen som er knyttet til denne forespørselen. |
| **Verdi for tittel-ID**<br>_mshr_fk_title_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmtitleid i mshr_hcmtitleentity-enhet | Den systemgenererte unike identifikatoren for jobbtittelen som er valgt for rekrutteringsforespørselen. |
| **Jobbfunksjons-ID**<br>mshr_jobfunctionid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_jobfunctionid i mshr_hcmjobfunctionentity-enhet | Den brukerlesbare unike identifikatoren for jobbfunksjonen som er knyttet til denne forespørselen. |
| **Standard fulltidsekvivalent**<br>mshr_defaultfulltimeequivalency<br>*Dobbel* | Skrivebeskyttet<br>Obligatorisk | Verdien for heltidsekvivalent for jobben, der 1.0 representerer en heltidsarbeider. |
| **Kategori for forskriftsmessig jobb**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory*-alternativsett | Skrivebeskyttet<br>Valgfri | EEO-jobbkategorien til jobbfunksjonen som er valgt for jobben. Gyldige verdier som er inkludert i alternativsettet HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory). |
| **Jobbtype-ID**<br>mshr_jobtypeid<br>*Streng* | Skrivebeskyttet<br>Valgfri | Typen jobb som er knyttet til stillingen. Jobbtypene er brukerdefinerte verdier som er tilgjengelige i mshr_hcmjobtypeentity-enheten. |
| **Verdi for jobbtype-ID**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmjobtypeentityid i mshr_hcmjobtypenentity-enhet | Den systemgenererte unike identifikatoren for jobbtypen som er knyttet til jobben for rekrutteringsforespørselen. |
| **Fritatt-status**<br>mshr_exemptstatus<br>*JobExemptStatus*-alternativsett | Skrivebeskyttet<br>Valgfri | FLSA-fritaksstatusen basert på jobbtypen. |
| **Beregnet startdato**<br>mshr_estimatedstartdate<br>*Dato* | Lese/skrive<br>Obligatorisk | Den estimerte datoen da en kandidat ville begynne å arbeide. |
| **Ekstern beskrivelse**<br>mshr_externaldescription<br>*Streng* | Lese/skrive<br>Valgfri | En kandidatbeskrivelse av jobb/stilling. | 
| **Kompensasjon, lav terskel**<br>mshr_compensationlowthreshold<br>*Dobbel* | Lese/skrive<br>Valgfri | Nedre grense for kompensasjonsnivået. |
| **Kontrollpunkt for kompensasjon**<br>mshr_compensationcontrolpoint<br>*Dobbel* | Lese/skrive<br>Valgfri | Kontrollpunkt for kompensasjonsnivået. |
| **Kompensasjon, høy terskel**<br>mshr_compensationhighthreshold<br>*Dobbel* | Lese/skrive<br>Valgfri | Øvre grense for kompensasjonsnivået. |
| **Kompensasjonsnivå**<br>mshr_compensationlevelid<br>*Streng* | Lese/skrive<br>Valgfri | Kompensasjonsnivået for jobben. En jobb kan defineres med flere kompensasjonsnivåer. Dette attributtet angir det valgte jobbkompensasjonsnivået for denne forespørselen. |
| **Jobbkompensasjons-ID**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmjobcompensationentityid i mshr_hcmjobcompensationentity-enhet | Systemgenerert unik identifikatoren for kompensasjonsnivået som er knyttet til jobben for rekrutteringsforespørselen. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
