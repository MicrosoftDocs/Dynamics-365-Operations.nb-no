---
title: Jobbfritaksstatus
description: I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464458"
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