---
title: Jobbfritaksstatus
description: I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053857"
---
# <a name="job-exempt-status"></a>Jobbfritaksstatus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.

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