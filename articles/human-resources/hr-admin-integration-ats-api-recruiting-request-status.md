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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059190"
---
# <a name="recruiting-request-status"></a>Rekrutteringsforespørselsstatus

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