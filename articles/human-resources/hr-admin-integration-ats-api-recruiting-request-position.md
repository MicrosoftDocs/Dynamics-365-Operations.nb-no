---
title: Rekrutteringsforespørselsstilling
description: Denne artikkelen beskriver Rekrutteringsforespørselsstilling-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0996532edf09ea5159e143d92fb2a93c4d6f826d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904253"
---
# <a name="recruiting-request-position"></a>Rekrutteringsforespørselsstilling


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Rekrutteringsforespørselsstilling-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>beskrivelse

Beskriver stillingen eller stillingene som skal fylles ut for en rekrutteringsforespørsel. Det er valgfritt å legge til en stilling i rekrutteringsforespørselen. Egenskapene til stillingen er skrivebeskyttet, fordi stillingsegenskapene i rekrutteringsforespørselen ikke må skille seg fra de som er i hovedoppføringen for stillingen. Hvis egenskapene må endres, bør det gjøres i hovedoppføringen for stillingen før du legger til stillingen i rekrutteringsforespørselen.

### <a name="json-representation"></a>JSON-representasjon
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Rekrutteringsforespørselsstilling-enhet**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk |    Systemgenerert ID for posten for rekrutteringsforespørselsstilling. |
| **ID for rekrutteringsforespørsel**<br>mshr_recruitingrequestid<br>*Streng* | Skriv én gang<br>Obligatorisk | Den brukerlesbare unike identifikatoren for rekrutteringsforespørselen. |
| **ID for rekrutteringsforespørselsverdi**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmrecruitingrequestentityid i mshr_hcmrecruitingrequestentity-enhet | Systemgenerert ID for rekrutteringsforespørselen som stillingen er tilordnet. |
| **Stillings-ID**<br>mshr_positionid<br>*Streng* | Skriv én gang<br>Obligatorisk | Den brukerlesbare unike identifikatoren for stillingen. |
| **Stillings-ID-verdi**<br>_mshr_fk_position_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmpositionv2entityid i mshr_hcmpositionv2entity-enheten | Systemgenerert identifikator for stillingen. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Stillingsbeskrivelsen. |
| **ID for stillingstype**<br>mshr_positiontypeid<br>*Streng* | Skrivebeskyttet<br>Valgfri | Den brukerlesbare unike identifikatoren for stillingstypen for denne stillingen. |
| **Verdi for stillingstype-ID**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmpositiontypeentityid i mshr_hcmpositiontypeentity-enhet | En systemgenerert unik ID for stillingstypen for denne stillingen. |
| **Status**<br>mshr_status<br>*RecruitingRequestPositionStatus*-slternativsett | Lese/skrive<br>Obligatorisk | Status for stillingen for rekrutteringsforespørselen. |
| **Avdelingsnummer**<br>mshr_departmentnumber<br>*Streng* | Skrivebeskyttet<br>Valgfri<br> | Avdelingsnummeret for stillingen. |
| **Verdi for avdelings-ID**<br>_mshr_fk_department_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_omdepartmententityid i mshr_omdepartmententity-enhet | Systemgenerert unik identifikator for avdelingen for stillingen. |
| **ID for Rapporter til stilling**<br>mshr_reportstopositionid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Den brukerlesbare IDen for stillingen som de rekrutterte stillingene rapporterer til i organisasjonshierarkiet. |
| **Verdi for ID for Rapporter til stilling**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmpositionv2entityid i mshr_hcmpositionv2entity-enheten | Den systemgenererte IDen for stillingen som den rekrutterte stillingen rapporterer til. |
| **Rapporter til-personalnummer**<br>mshr_reportstopersonnelnumber<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Arbeider-IDen til den ansatte som kandidaten skal rapportere til. |
| **Verdi for ID for Rapporter til arbeider**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmworkerbaseentityid i mshr_hcmworkerbaseentity-enhetentity | Systemgenererte ID for den ansatte som kandidaten skal rapportere til. |
| **Finansdimensjon**<br>mshr_financialdimension<br>*Streng* | Skrivebeskyttet<br>Valgfri | Finansdimensjonen (for eksempel kostsenter) som er tilordnet stillingen. Finansdimensjonen tilordnes for hver stilling per juridisk enhet. Kostsentre som er definert i dimensjoner, er tilgjengelige via mshr_dimattributeomcostcenterentity-enheten. |
| **Dataområde-ID**<br>mshr_dataareaid<br>*Streng* | Lese/skrive<br>Valgfri | Angir den juridiske enheten (firmaet) for rekrutteringsforespørselsstillingen. |
| **Verdi for dataområde-ID**<br>_mshr_dataareaid_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: cdm_companyid i cdm_company-enhet | Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet) for rekrutteringsforespørselsstillingen. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Sammenslåing av rekrutteringsforespørselsverdi og stillings-ID som en annen metode for å identifisere posten entydig. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
