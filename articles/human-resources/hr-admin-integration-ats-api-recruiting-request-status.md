---
title: Rekrutteringsforespørselsstatus
description: Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125960"
---
# <a name="recruiting-request-status"></a>Rekrutteringsforespørselsstatus

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