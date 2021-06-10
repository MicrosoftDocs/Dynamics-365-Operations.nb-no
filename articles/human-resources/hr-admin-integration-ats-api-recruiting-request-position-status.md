---
title: Status for rekrutteringsforespørselsstilling
description: Dette emnet beskriver status for stillingen i en rekrutteringsforespørsel for Dynamics 365 Human Resources.
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051887"
---
# <a name="recruiting-request-position-status"></a>Status for rekrutteringsforespørselsstilling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver status for stillingen i en rekrutteringsforespørsel for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestpositionstatus

Denne opplistingen gir alternativetsett for statusverdiene til hver stilling en rekrutteringsforespørsel i RecruitingRequestPosition-enheten.

| Verdi | Etikett | beskrivelse |
| --- | --- | --- |
| 200000000 | Åpen | Stillingen i rekrutteringsforespørselen er åpen for rekruttering. Dette viser ikke at det for øyeblikket ikke er noen aktiv stillingstilordning for stillingen. Det kan være en ansatt i stillingen når rekrutteringen gjøres. Den viser bare at stillingen er tilgjengelig for rekruttering i konteksten med rekrutteringsforespørselen. |
| 200000001 | Besatt | En arbeider er valgt for tilordning til stillingen. |
| 200000002 | Annullert | Forespørselen om rekruttering for denne stillingen er avbrutt. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]