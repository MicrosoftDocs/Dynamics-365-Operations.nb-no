---
title: Sertifikattype
description: Denne artikkelen beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: bfe7f06176098a504f8d2ad1c1431a6f60fe059c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886196"
---
# <a name="certificate-type"></a>Sertifikattype


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmcertificatetypeentity

## <a name="description"></a>beskrivelse

Denne enheten definerer listen over profesjonelle sertifikattyper som er definert i Human Resources. Enheten er ikke spesifikk for en juridisk enhet (firma).

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Sertifikattype-enhet**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk 
Systemgenerert | Unik primær identifikator for sertifikattypen. |
| **Sertifikattype**<br>mshr_certificatetype<br>*Streng* | Lese/skrive<br>Obligatorisk | Unik brukerlesbare identifikator for sertifikattypen. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Obligatorisk | Beskrivelse av sertifikattypen. |
| **Krever fornying**<br>mshr_requirerenewal<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Valgfri | Angir om det kreves fornyelse for sertifikatet. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
