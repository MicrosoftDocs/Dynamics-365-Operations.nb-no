---
title: Budsjettmidler tilgjengelig
description: Denne artikkelen introduserer funksjonen for tilgjengelige budsjettmidler og gir informasjon som kan hjelpe deg med å konfigurere budsjettkontroll for å optimalisere administrasjon av organisasjonens finansressurser.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: b6f94931ba3514c1c66d80b64846d882861d555c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898247"
---
# <a name="budget-funds-available"></a>Budsjettmidler tilgjengelig

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen introduserer funksjonen for tilgjengelige budsjettmidler og gir informasjon som kan hjelpe deg med å konfigurere budsjettkontroll for å optimalisere administrasjon av organisasjonens finansressurser.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Utvidet beregningsfunksjon for tilgjengelige budsjettmidler

Ved hjelp av funksjonen **Bare spor beløp i beregning for tilgjengelige budsjettmidler** kan du spore de underliggende budsjettkontrolltabellene for dokumenttyper og -delstater, basert på innstillingene på siden **Definer budsjettkontrollparametere**.

Noen alternativer for budsjettkontrollkonfigurasjon må ha bestemte innstillinger for at funksjonen skal fungere riktig. Disse alternativene velges eller tømmes i kategorien **Budsjettmidler tilgjengelig** på siden **Definer budsjettkontrollparametere**. Tabellen nedenfor viser innstillingene som kreves for funksjonen for tilgjengelig budsjettmidler.

| Hvis dette alternativet velges | Dette alternativet må også velges |
| ------------------------- | -------------------------------- |
| Budsjettreservasjoner for forhåndsdisposisjoner | Budsjettreservasjoner for disposisjoner *og* Faktiske utgifter |
| Budsjettreservasjoner for disposisjoner | Faktiske utgifter |
| Budsjettreservasjoner for disposisjoner med dokumenter av typen Innkjøpsrekvisisjon | Budsjettreservasjoner for forhåndsdisposisjoner |

Denne funksjonen påvirker bare nye dokumenter. Beløp for eksisterende dokumenter vil fortsatt spores og vises i forespørselen om budsjettkontrollstatistikk til en innstilling for tilgjengelige budsjettmidler endres og den nye budsjettkontrollkonfigurasjonen er aktivert. På dette tidspunktet fjernes budsjettsporingsdata for dokumenter som ble fjernet fra beregningen av tilgjengelige budsjettmidler.

Vi anbefaler at du lar alternativet **Uposterte faktiske utgifter** være fjernet. Hvis det er merket av for den, vil en tidkrevende budsjettkontrollberegning bli utført på uposterte dokumenter, for eksempel ventende leverandørfakturaer.
