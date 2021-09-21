---
title: Enheten og enhetsantallet fungerer ikke riktig i lagerjournalen
description: Enheten og enhetsantallet fungerer ikke riktig i lagerjournalen
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477181"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Enheten og enhetsantallet fungerer ikke riktig i lagerjournalen

## <a name="symptoms"></a>Symptomer

Ett eller begge av følgende problemer kan oppstå når du arbeider med enheter og antall i en lagerjournal:

- Du ser ikke enheter eller enhetsantall i lagerjournalen mens en omregningsenhet er definert for det frigitte produktet, og du kan ikke endre enheten i lagerjournalen.
- Du ser feltene **Antall** og **Enhet** i lagerjournalen, men ikke feltet **Enhetsantall**. Hvis du endrer enheten, angir et antall og posterer journalen, viser journalen fortsatt den opprinnelige måleenheten for dette antallet.

## <a name="resolution"></a>Løsning

Følg fremgangsmåten nedenfor for å løse problemet.

1. I arbeidsområdet **Funksjonsbehandling** må du kontrollere at funksjonen *Bruke måleenhet og enhetsantall i lagerjournaler* er aktivert. Denne funksjonen legger til feltene **Enhet** og **Enhetsantall** i journalen.
1. Etter at funksjonen er aktivert, bruker du feltene **Antall**, **Enhetsantall** og **Enhet** på følgende måte:

    - **Antall** – Angi antallet ved å bruke standardenheten som er definert for det frigitte produktet. Selve standardenheten vises imidlertid ikke her. Hvis det defineres en omregning mellom standardenheten og enheten som er valgt i **Enhet**-feltet, oppdateres **Antall**-feltet automatisk basert på valgene i feltene **Enhetsantall** og **Enhet**.
    - **Enhetsantall** – Angi antallet ved å bruke enheten som er valgt i **Enhet**-feltet.
    - **Enhet** – Velg enheten som skal brukes på verdien i **Enhetsantall**-feltet.
