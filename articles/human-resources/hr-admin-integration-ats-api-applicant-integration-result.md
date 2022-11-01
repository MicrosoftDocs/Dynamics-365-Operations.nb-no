---
title: Søkerintegreringsresultat
description: I denne artikkelen beskrives alternativetsettet for Applikasjonsintegrasjonsresultat for Dynamics 365 Human Resources.
author: jaredha
ms.date: 09/12/2022
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
ms.openlocfilehash: 86f3f75e538268644cea4f927f04c07aae115f00
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702235"
---
# <a name="applicant-integration-result"></a>Søkerintegreringsresultat


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikkelen beskrives alternativetsettet for Applikasjonsintegrasjonsresultat for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmapplicantintegrationresult

Denne opplistingen gir status for en kandidatpost.

| Verdi | Etikett | beskrivelse |
| --- | --- | --- |
| 200000000 | Ikke behandlet | Kandidaten er fortsatt under vurdering. |
| 200000001 | Ansatt | Kandidaten ble ansatt. |
| 200000002 | Ikke ansatt | Det ble gjort beslutning om å ikke ansette kandidaten. |
| 200000003 | Forkastet | Kandidaten ble avvist fra vurdering. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
