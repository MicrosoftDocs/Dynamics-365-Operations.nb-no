---
title: Søkerintegreringsresultat
description: I dette emnet beskrives alternativetsettet for Applikasjonsintegrasjonsresultat for Dynamics 365 Human Resources.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467559"
---
# <a name="applicant-integration-result"></a>Søkerintegreringsresultat

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emnet beskrives alternativetsettet for Applikasjonsintegrasjonsresultat for Dynamics 365 Human Resources.

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