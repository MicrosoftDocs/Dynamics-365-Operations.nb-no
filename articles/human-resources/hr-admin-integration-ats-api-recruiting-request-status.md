---
title: Rekrutteringsforespørselsstatus
description: Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: d845179077fc2e04dfb3bd05eaa70b0a2a016121
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067107"
---
# <a name="recruiting-request-status"></a>Rekrutteringsforespørselsstatus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequeststatus

Denne opplistingen gir alternativsettet for statusverdiene for en RecruitingRequest.

| Verdi | Etikett | beskrivelse |
| --- | --- | --- |
| 200000000 | Utkast | Forespørselen er i utkast og er ikke klar for aktiv rekruttering. |
| 200000001 | Til gjennomgang | Forespørselen er sendt og rutes til godkjenning etter arbeidsflyt. Bare tilgjengelig når arbeidsflyten er aktivert. |
| 200000002 | Uavsluttet | Forespørselen venter på arbeidsflythandling. Bare tilgjengelig når arbeidsflyten er aktivert. |
| 200000003 | Annullert | Forespørselen har blitt avbrutt. Bare tilgjengelig når arbeidsflyten er aktivert. |
| 200000004 | Nektet | Forespørselen er avvist. Bare tilgjengelig når arbeidsflyten er aktivert. |
| 200000005 | Aktive | Alle arbeidsflyter fullføres og godkjennes, og forespørselen er klar for aktiv rekruttering. |
| 200000006 | Forseglet | Rekrutteringsforespørselen er lukket. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
