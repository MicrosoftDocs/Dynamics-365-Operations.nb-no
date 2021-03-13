---
title: Attesttype
description: Dette emnet beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125719"
---
# <a name="certificate-type"></a>Attesttype

Dette emnet beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.

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

