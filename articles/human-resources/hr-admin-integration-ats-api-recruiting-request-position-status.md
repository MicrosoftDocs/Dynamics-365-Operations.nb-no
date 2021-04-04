---
title: Status for rekrutteringsforespørselsstilling
description: Dette emnet beskriver status for stillingen i en rekrutteringsforespørsel for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464724"
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