---
title: Én av linjene er allerede ved en belastning
description: 'Denne siden forklarer hvorfor du kan ha mottatt feilen: "Én av linjene er allerede satt inn i en belastning. Kan ikke frigi til lageret", og hvordan du kan løse problemet.'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477250"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Én av linjene er allerede ved en belastning

## <a name="symptoms"></a>Symptomer

Du kan få følgende feilmelding når du arbeider med lastplanlegging og forsendelser:

> Én av linjene er allerede ved en belastning. Kan ikke frigi til lager.

Hvis du oppretter laster manuelt, eller hvis du definerer prosessen slik at laster allerede er opprettet før salgsordrelinjeposten inntreffer, antas det at den påfølgende frigivelsen utføres manuelt, og at ruten og vurderingen fra lasten skal brukes.

I et annet scenario vil du prøve å utføre en automatisk frigivelse av lageret, men bølgeprosessen kan ikke opprette arbeid. Derfor blir det fremdeles opprettet en åpen forsendelse eller last. Denne åpne forsendelsen eller lasten blokkerer deretter etterfølgende forsøk på å frigi ordren automatisk til du sletter den åpne forsendelsen eller lasten, eller manuelt behandler bølgen på nytt.

## <a name="resolution"></a>Løsning

Du kan frigi fra salgsordresiden eller automatisk frigivelse fra siden frigivelse av salgsordre, bare hvis det ikke finnes en last før frigivelsen til lageret. Lasten vil automatisk bli opprettet etter at bølgen er behandlet.
