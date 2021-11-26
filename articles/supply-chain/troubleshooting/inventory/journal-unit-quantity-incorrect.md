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
ms.openlocfilehash: 074be71d7b6ec1acab6307a79e397c2a2a045c39
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778431"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Enheten og enhetsantallet fungerer ikke riktig i lagerjournalen

## <a name="symptoms"></a>Symptomer

Ett eller begge av følgende problemer kan oppstå når du arbeider med enheter og antall i en lagerjournal:

- Du ser ikke enheter eller enhetsantall i lagerjournalen mens en omregningsenhet er definert for det frigitte produktet, og du kan ikke endre enheten i lagerjournalen.
- Du ser feltene **Antall** og **Enhet** i lagerjournalen, men ikke feltet **Enhetsantall**. Hvis du endrer enheten, angir et antall og posterer journalen, viser journalen fortsatt den opprinnelige måleenheten for dette antallet.

## <a name="resolution"></a>Løsning

Følg fremgangsmåten nedenfor for å løse problemet.

1. I arbeidsområdet **Funksjonsbehandling** må du kontrollere at funksjonen *Bruke måleenhet og enhetsantall i lagerjournaler* er aktivert. Denne funksjonen legger til feltene **Enhet** og **Enhetsantall** i journalen. (Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard.)
1. Etter at funksjonen er aktivert, bruker du feltene **Antall**, **Enhetsantall** og **Enhet** på følgende måte:

    - **Antall** – Angi antallet ved å bruke standardenheten som er definert for det frigitte produktet. Selve standardenheten vises imidlertid ikke her. Hvis det defineres en omregning mellom standardenheten og enheten som er valgt i **Enhet**-feltet, oppdateres **Antall**-feltet automatisk basert på valgene i feltene **Enhetsantall** og **Enhet**.
    - **Enhetsantall** – Angi antallet ved å bruke enheten som er valgt i **Enhet**-feltet.
    - **Enhet** – Velg enheten som skal brukes på verdien i **Enhetsantall**-feltet.
