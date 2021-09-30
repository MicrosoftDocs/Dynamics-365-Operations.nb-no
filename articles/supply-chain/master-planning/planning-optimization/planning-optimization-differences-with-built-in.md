---
title: Forskjeller mellom innebygd hovedplanlegging og planleggingsoptimalisering
description: Dette emnet viser funksjoner som Planleggingsoptimalisering ennå ikke støtter, og som ikke er oppført på siden Analyse for tilpasning av planleggingsoptimalisering.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 63f3bc6cb7563ee6ff719272a0795efffcb40bc8
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500202"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Forskjeller mellom innebygd hovedplanlegging og planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Resultatet av planleggingsoptimalisering kan være forskjellig fra den innebygde hovedplanleggingsmotoren. Forskjellen kan også skyldes ventende funksjoner. Dette emnet viser funksjoner som Planleggingsoptimalisering ennå ikke støtter, og som ikke er oppført på siden **[Analyse for tilpasning av planleggingsoptimalisering](planning-optimization-fit-analysis.md)**.

| Funksjon | Gjeldende virkemåte i Planleggingsoptimalisering |
|---|---|
| Produkter med faktisk vekt | Produkter med faktisk vekt betraktes som vanlige produkter.|
| Utvidbare dimensjoner | Utvidbare dimensjoner er tomme i planlagte bestillinger selv om det er merket av for **Dekningsplanlegg etter dimensjon** på siden **Lagringsdimensjonsgrupper** eller **Sporingsdimensjonsgrupper**. |
| Filtrerte produksjonsutkjøringer | Hvis du vil ha mer informasjon, kan du se [Produksjonsplanlegging – filtre](production-planning.md#filters). |
| Prognoseplanlegging | Prognoseplanlegging støttes ikke. Vi anbefaler at du bruker hovedplanlegging der en prognosemodell er tilordnet hovedplanen. |
| Nummersekvenser for planlagte ordrer | Nummerserier for planlagte ordrer støttes ikke. Planlagte bestillingsnumre genereres på servicesiden. |
| Planlegg kopiering, sletting av plan og opprydding av planversjon | <p>Følgende elementer er deaktivert under **Hovedplanlegging \> Hovedplanlegging \> Vedlikehold planer** i navigasjonsruten:</p><ul><li>Planlegg kopi</li><li>Slett plan</li><li>Planlegg versjonsopprydding</li></ul> |
| Returordrer | Returordrer tas ikke hensyn til. |
| Planleggingsrelaterte funksjoner | Hvis du vil ha mer informasjon, kan du se [Planlegging med uendelig kapasitet](infinite-capacity-planning.md#limitations). |
| Fullføring av sikkerhetslager | Planleggingsoptimalisering bruker alltid *Dagens dato + leveringstid* for feltet **Fyll opp minimum** på siden **Varedekning**. Dette hindrer uønskede planlagte ordrer og andre problemer fordi hvis leveringstiden ikke er inkludert for sikkerhetslager, vil planlagte bestillinger som opprettes for den gjeldende lagerbeholdningen, alltid bli forsinket på grunn av leveringstiden. |
| Utligning av sikkerhetslager og nettobehov | Kravtypen *Sikkerhetslager* er ikke inkludert og vises ikke på siden **Nettobehov**. Sikkerhetslager representerer ikke etterspørsel og har ikke en tilknyttet behovsdato. I stedet definerer det en begrensning for hvor mye lager som må finnes til enhver tid. Det tas imidlertid fremdeles hensyn til **Minimum**-feltverdien ved beregning av planlagte bestillinger under hovedplanleggingen. Vi foreslår at du undersøker kolonnen **Akkumulert antall** på **Nettobehov**-siden for å se at denne verdien ble tatt hensyn til. |
| Transportkalendere | Verdien i kolonnen **Transportkalender** på siden **Leveringsmåter** ignoreres. |

## <a name="additional-resources"></a>Tilleggsressurser

- [Analyse for tilpasning av planleggingsoptimalisering](planning-optimization-fit-analysis.md)
- [Parametere som ikke brukes av planleggingsoptimalisering](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
