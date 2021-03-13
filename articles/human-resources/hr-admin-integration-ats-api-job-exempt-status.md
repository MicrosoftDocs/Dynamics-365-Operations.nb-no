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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125575"
---
# <a name="job-exempt-status"></a>Jobbfritaksstatus

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
