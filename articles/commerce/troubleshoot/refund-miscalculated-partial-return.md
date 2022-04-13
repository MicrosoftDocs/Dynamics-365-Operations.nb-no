---
title: Refunderbare tillegg beregnes på grunnlag av returnert antall
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe deg når kasserere ser feil refunderbare tillegg i salgsstedet (POS) for antallet returnerte varer.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/28/2022
ms.locfileid: "8490217"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Refunderbare tillegg beregnes på grunnlag av returnert antall

[!include [banner](../../includes/banner.md)]

Dette emnet gir feilsøkingsveiledning som kan hjelpe deg når kasserere ser feil refunderbare tillegg i salgsstedet (POS) for antallet returnerte varer.

## <a name="description"></a>Beskrivelse

En kunde returnerer et delvist antall av varene som ble kjøpt inn for en salgsordre som har refunderbare tillegg på linjenivå. I stedet for å vise en delvis refundering, vises imidlertid POS alle gebyrer som refunderbare.

En kunde kjøper for eksempel et antall på fem varer for USD 5 per vare, for totale tillegg på USD 25. Kunden returnerer deretter tre av de fem varene. Kassereren blir imidlertid forevist et refunderbart tillegg på USD 25 gebyr på salgsstedet i stedet for det forventede refunderbare tillegget på USD 15 for de tre varene som ble returnert.

## <a name="resolution"></a>Oppløsning

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Aktiver funksjonen Aktiver refunderingsgebyrer basert på det refunderte antallet

Per Microsoft Dynamics 365 Commerce versjon 10.0.26 kan du bruke funksjonen **Aktiver refunderingsgebyrer basert på det refunderte antallet** til å beregne refunderbare tillegg på linjenivå basert på antall returnerte varer.

Følg denne fremgangsmåten for å aktivere funksjonen **Aktiver refunderingsgebyrer basert på det refunderte antallet** i Commerce Headquarters.

1. Åpne arbeidsområdet **Funksjonsbehandling** (**Systemadministrator \> Arbeidsområder \> Funksjonsbehandling**).
1. I listen over tilgjengelige funksjoner søker du etter og velger funksjonen **Aktiver refunderingsgebyrer basert på det refunderte antallet**.
1. Velg **Aktiver nå** i høyre rute.
