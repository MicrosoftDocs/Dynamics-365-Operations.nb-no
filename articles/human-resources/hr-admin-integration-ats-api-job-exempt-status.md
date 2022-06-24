---
title: Jobbfritaksstatus
description: Denne artikkelen beskriver alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894679"
---
# <a name="job-exempt-status"></a>Jobbfritaksstatus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.

Fysisk navn: cdm_jobexemptstatus

Denne opplistingen spesifiserer alternativsettet for fritaksstatusverdier for FLSA-jobb. Dette finnes i det eksisterende cdm_jobexemptstatus-alternativsett.

| Verdi | Etikett | beskrivelse |
| --- | --- | --- |
| 200000000 | Avgiftsfri | Jobben har en fritaksstatus basert på FLSA-retningslinjene. |
| 200000001 | NonExempt | Jobben har en ikke-fritaksstatus basert på FLSA-retningslinjene. |
| 200000002 | Gjelder ikke | FLSA-statusretningslinjer gjelder ikke for jobben. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
