---
title: Beregninger i produktkonfigurasjonsmodell
description: Denne artikkelen beskriver hvordan du oppretter beregninger for attributter i en produktkonfigurasjonsmodell
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35057a4fc59732fea24e4d953cafed633a936ec1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878939"
---
# <a name="product-configuration-model-calculations"></a>Beregninger i produktkonfigurasjonsmodell

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter beregninger for attributter i en produktkonfigurasjonsmodell.

## <a name="prerequisites"></a>Forutsetninger

Beregninger brukes til å beregne konfigurasjonsverdiene for et produkt i en produktkonfigurasjonsmodell. Før du kan sette opp beregninger, må den relaterte produktkonfigurasjonsmodellen finnes. Hvis du vil ha en oversikt over oppsettsprosessen for konfigurasjonsmodeller og de relaterte oppgavene, kan du se [Definer en produktkonfigurasjonsmodell](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Opprett en beregning

En beregning består av et uttrykk og et målattributt. Hvis du vil ha mer informasjon, kan du se [Vanlige spørsmål om beregninger for produktkonfigurasjonsmodeller](calculate-product-configuration-models.md).

Følg denne fremgangsmåten for å opprette en beregning for en eksisterende produktmodell.

1. Gå til **Behandling av produktinformasjon \> Felles \> Produktkonfigurasjonsmodeller**.
1. Åpne en produktkonfigurasjonsmodell, og velg deretter **Rediger**.
1. På **Beregninger**-hurtigfanen velger du **Legg til** for å legge til en beregning, og deretter angir du følgende felter:

    - **Navn** – Angi et navn for beregningen.
    - **Beskrivelse** – Angi en beskrivelse av beregningen.
    - **Målattributt** – Velg attributtet som du gjør beregningen for.

1. Velg **Rediger uttrykk**.
1. I dialogboksen **Angi en beregning** legger du til de nødvendige attributtene, operatorene og verdiene i uttrykket. Hvis du vil ha mer informasjon om hvordan du kan arbeide med disse elementene, kan du se [Uttrykksbegrensninger og tabellbegrensninger i produktkonfigurasjonsmodeller](expression-constraints-table-constraints-product-configuration-models.md).
1. Når uttrykket er klart, velger du **OK**.

## <a name="calculation-examples"></a>Beregningseksempler

Denne delen gir noen eksempler som viser hvordan beregninger fungerer.

### <a name="example-1"></a>Eksempel 1

Målattributtet er boolsk, og beregningen bruker følgende betingede uttrykk:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Dette uttrykket returnerer verdien *Sann* til målattributtet hvis `decimalAttribute2` er større enn eller lik `decimalAttribute1`. Hvis ikke returneres den boolske verdien *Usann*.

### <a name="example-2"></a>Eksempel 2

I dette eksemplet brukes tekstattributtet `textFixedList` som målattributtet. Dette attributtet inneholder følgende faste liste.

| Verdi | Problemløserverdi |
|---|---|
| A | 1a |
| T | 2b |
| K | 2c |

Følgende skjermbilde viser hvordan innstillingene for dette attributtet kan se ut i systemet.

![Attributtytypeinnstillinger for eksempel 2.](media/model-calculations-example2.png "Attributtytypeinnstillinger for eksempel 2")

Attributtet brukes i følgende betingede setning:

`If[integerAttribute < 150, 0, 2]`

Hvis `integerAttribute` er mindre enn 150, returneres tekstverdien til den første posten i den faste listen, *A*. Ellers returneres tekstverdien til den tredje posten i den faste listen, *C*.

> [!NOTE]
> Den faste listen tilsvarer en nullbasert opplisting, og du får tilgang til verdiene via den aktuelle heltallsverdien. Derfor sammenlignes den første faste listeverdien (*A*) med *0*, den andre verdien (*B*) sammenlignes med *1*, og den tredje verdien (*C*) sammenlignes med *2*.

### <a name="example-3"></a>Eksempel 3

I dette eksemplet brukes måltattributtet `textFixedList` fra forrige eksempel. Det bruker også et annet tekstattributt, `textAttribute`, som inneholder følgende faste liste.

| Verdi | Problemløserverdi |
|---|---|
| AA | 1aa |
| BB | 2bb |

Følgende skjermbilde viser hvordan innstillingene for dette attributtet kan se ut i systemet.

![Attributtytypeinnstillinger for eksempel 3.](media/model-calculations-example3.png "Attributtytypeinnstillinger for eksempel 3")

Verdien for `textFixedList`-attributtet beregnes ved hjelp av følgende betingede setning:

`If[textAttribute == "1aa", 0, 2]`

Hvis `textAttribute`-verdien har en løserverdi som er lik *1aa*, returnerer dette uttrykket tekstverdien til den første posten i den faste `textFixedList`-listen, *A*. Ellers returneres tekstverdien til den tredje posten i den faste `textFixedList`-listen, *C*.

> [!NOTE]
> - Den betingede setningen må bruke løserverdien til attributtet.
> - Bare tekstattributter i en fast liste kan brukes i beregninger.

## <a name="see-also"></a>Se også

- [Vanlige spørsmål om beregninger for produktkonfigurasjonsmodeller](calculate-product-configuration-models.md)
- [Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell](tasks/add-expression-constraint-product-configuration-model.md)
- [Oversikt over produktkonfigurasjonsmodeller](product-configuration-models.md)
