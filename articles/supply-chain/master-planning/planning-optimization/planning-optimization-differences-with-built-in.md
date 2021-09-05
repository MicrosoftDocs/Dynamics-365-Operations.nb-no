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
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344960"
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
| Transportkalendere | Verdien i kolonnen **Transportkalender** på siden **Leveringsmåter** ignoreres. |

## <a name="additional-resources"></a>Tilleggsressurser

- [Analyse for tilpasning av planleggingsoptimalisering](planning-optimization-fit-analysis.md)
- [Parametere som ikke brukes av planleggingsoptimalisering](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
