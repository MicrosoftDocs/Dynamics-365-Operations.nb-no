---
title: "Systemgruppering i en åpen arbeidsliste"
description: "Dette emnet beskriver hvordan du filtrerer den åpne arbeidslisten på en mobilenhet."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dbf0e49b1156c54cd37bbbe57ca564cdbc45fb2d
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017

---

# <a name="system-grouping-on-an-open-work-list"></a>Systemgruppering i en åpen arbeidsliste

[!include[banner](../includes/banner.md)]

Ved hjelp av et felt for systemgruppering, kan du filtrere en åpen arbeidslisten uten å måtte redigere menyelementet på mobilenheten.
Der det er aktuelt, fungerer systemgrupperinger for å filtrere en arbeidslisten i et enkelt arbeidshodefelt. Du kan ikke bruke systemgruppering til å filtrere på linjenivåfelter.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Definere systemgruppering i en åpen arbeidsliste
Bruk disse trinnene til å definere systemgruppering i en åpen arbeidsliste.

-   Velg **modus: indirekte** og **Aktivitetskode: Vis åpen arbeidsliste** fra et menyelement for mobilenhet. Følgende alternativer blir tilgjengelige: Disse alternativene er nødvendig for systemgruppring på en åpen arbeidsliste. 

| Alternativ        | beskrivelse   | 
| ------------- | ------------- |
| Tillat systemgruppering   | Aktiverer systemgruppering for et valgt menyelement for arbeidsliste.| 
| Systemgrupperingsfelt   | Bare tilgjengelig hvis **Tillat systemarbeid** er satt til **Ja**. Velg feltet som bestemmer hvordan plukkarbeid grupperes for arbeidere. Hvis du for eksempel felger **ShipmentId**-feltet vil arbeideren skanne forsendelses-IDen for å gruppere plukkarbeidet. Alt arbeid for forsendelsen tilordnes deretter til arbeideren. Dette feltet krever at du oppretter et menyelement for å bruke eksisterende arbeid som er gruppert av systemet. Bruk **Systemgrupperingsetikett**-feltet for å informere om hva som skal skannes. |
| Systemgrupperingsetikett   | Bare tilgjengelig hvis **Tillat systemarbeid** er satt til **Ja**. Angi informasjon til arbeideren om hva som skal skannes når plukkarbeid grupperes. Hvis du for eksempel bruker **ShipmentId**-feltet til å gruppere plukkarbeid etter forsendelse, kan du angi Forsendelses-ID i feltet. Dette feltet krever at du oppretter et menyelement for å bruke eksisterende arbeid som er gruppert av systemet. Du må også velge feltet du vil gruppere etter i **Systemgruppering**-feltet.|

