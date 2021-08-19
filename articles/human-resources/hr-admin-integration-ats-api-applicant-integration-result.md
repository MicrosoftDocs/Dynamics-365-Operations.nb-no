---
title: Søkerintegreringsresultat
description: I dette emnet beskrives alternativetsettet for Applikasjonsintegrasjonsresultat for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f173e15d5524dfd4d63113760760b2534cc8769456df621415a11e4053cc6fb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725920"
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