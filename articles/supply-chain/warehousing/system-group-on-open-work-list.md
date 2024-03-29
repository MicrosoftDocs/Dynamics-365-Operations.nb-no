---
title: Systemgruppering i en åpen arbeidsliste
description: Denne artikkelen beskriver hvordan du filtrerer den åpne arbeidslisten på en mobilenhet.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42e5862392cff57886c36bcbe138e13a8ce7ef23
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849104"
---
# <a name="system-grouping-on-an-open-work-list"></a>Systemgruppering i en åpen arbeidsliste

[!include [banner](../includes/banner.md)]

Ved hjelp av et felt for systemgruppering, kan du filtrere en åpen arbeidslisten uten å måtte redigere menyelementet på mobilenheten.
Der det er aktuelt, fungerer systemgrupperinger for å filtrere en arbeidslisten i et enkelt arbeidshodefelt. Du kan ikke bruke systemgruppering til å filtrere på linjenivåfelter.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Definere systemgruppering i en åpen arbeidsliste
Bruk disse trinnene til å definere systemgruppering i en åpen arbeidsliste.

-   Velg **modus: indirekte** og **Aktivitetskode: Vis åpen arbeidsliste** fra et menyelement for mobilenhet. Følgende alternativer blir tilgjengelige: Disse alternativene er nødvendig for systemgruppring på en åpen arbeidsliste. 

|        Alternativ         |                                                                                                                                                                                                                                                                         beskrivelse                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tillat systemgruppering |                                                                                                                                                                                                                                                 Aktiverer systemgruppering for et valgt menyelement for arbeidsliste.                                                                                                                                                                                                                                                  |
| Systemgrupperingsfelt | Bare tilgjengelig hvis <strong>Tillat systemarbeid</strong> er satt til <strong>Ja</strong>. Velg feltet som bestemmer hvordan plukkarbeid grupperes for arbeidere. Hvis du for eksempel felger <strong>ShipmentId</strong>-feltet vil arbeideren skanne forsendelses-IDen for å gruppere plukkarbeidet. Alt arbeid for forsendelsen tilordnes deretter til arbeideren. Dette feltet krever at du oppretter et menyelement for å bruke eksisterende arbeid som er gruppert av systemet. Bruk <strong>Systemgrupperingsetikett</strong>-feltet for å informere om hva som skal skannes. |
| Systemgrupperingsetikett |                       Bare tilgjengelig hvis <strong>Tillat systemarbeid</strong> er satt til <strong>Ja</strong>. Angi informasjon til arbeideren om hva som skal skannes når plukkarbeid grupperes. Hvis du for eksempel bruker <strong>ShipmentId</strong>-feltet til å gruppere plukkarbeid etter forsendelse, kan du angi Forsendelses-ID i feltet. Dette feltet krever at du oppretter et menyelement for å bruke eksisterende arbeid som er gruppert av systemet. Du må også velge feltet du vil gruppere etter i <strong>Systemgruppering</strong>-feltet.                       |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]