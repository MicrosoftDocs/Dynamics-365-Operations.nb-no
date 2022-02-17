---
title: Budsjettmidler tilgjengelig
description: Dette emnet introduserer funksjonen for tilgjengelige budsjettmidler og gir informasjon som kan hjelpe deg med å konfigurere budsjettkontroll for å optimalisere administrasjon av organisasjonens finansressurser.
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891320"
---
# <a name="budget-funds-available"></a>Budsjettmidler tilgjengelig

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet introduserer funksjonen for tilgjengelige budsjettmidler og gir informasjon som kan hjelpe deg med å konfigurere budsjettkontroll for å optimalisere administrasjon av organisasjonens finansressurser.

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