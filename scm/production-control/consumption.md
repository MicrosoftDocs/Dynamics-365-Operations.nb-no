---
title: Beregne materialforbruk
description: Denne artikkelen inneholder informasjon om ulike alternativer som er knyttet til beregning av materialforbruk.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 2225707329c67a30d9234bef5282d49834ea042a
ms.lasthandoff: 03/31/2017


---

# <a name="calculate-material-consumption"></a>Beregne materialforbruk

Denne artikkelen inneholder informasjon om ulike alternativer som er knyttet til beregning av materialforbruk. 

Følgende alternativer som er knyttet til beregningen av materialforbruk, er tilgjengelige i fanen **Oppsett** og **Trinnforbruk** i hurtigfanen **Linjedetaljer** på **Stykkliste**-siden.

## <a name="variable-and-constant-consumption"></a>Variabelt og konstant forbruk
I den **forbruket er**, kan du velge om forbruk skal beregnes som et konstant antall eller et variabelt antall. Velg **konstant** Hvis et fast antall eller volum er nødvendig for produksjonen, uansett antall som produseres. Velg **Variabel**, som er standardinnstillingen, hvis den nødvendige mengden materiale i ferdigvarene er proporsjonal med antall ferdigvarer som produseres.

## <a name="calculating-consumption-from-a-formula"></a>Beregne forbruk med en formel
I **Formel**-feltet kan du definere forskjellige formler for beregning av materialforbruk. Hvis du bruker standardverdien **Standard**, beregnes ikke forbruket av en formel. Følgende formler fungerer sammen med feltet **Høyde**, **Bredde**, **Dybde**, **Tetthet** og **Konstant**:

-   Høyde \*konstant
-   Høyde \*bredde \*konstant
-   Høyde \*bredde \*dybde \*konstant
-   (Høyde \*bredde \*dybde / tetthet) \*Konstant

## <a name="rounding-up-and-multiples"></a>Avrunding opp og faktorer
Sammen gjør feltet **Avrundes opp** og **Faktorer** det mulig å runde opp materialforbruksverdien. Du kan for eksempel runde opp verdien i henhold til håndteringsenheten der råvarene plukkes for produksjon. Følgende alternativer er tilgjengelige i **Avrundes opp**-feltet: **Antall**, **Mål** og **Forbruk**.

### <a name="quantity"></a>Antall

Hvis du velger **Antall** som avrundingsmåte, må antallet være et multiplumstall av det angitte antallet. For eksempel hvis du må bruke hele tall, angir du **1** i **Faktorer**-feltet. Tall rundes deretter opp til et antall som kan deles med 1.

### <a name="measurement"></a>Mål

Vanligvis merker du av for **Mål** som avrundingsmåte når råvarene har bestemte dimensjoner. Et metallrør på 2 meter kreves for eksempel for en ferdigvare, og metallrørene kommer i 4,5 meters lengder. I dette tilfellet kan avrundingsmåten **Mål** brukes til å beregne hvor mange metallrør som kreves for å produsere et gitt antall enheter av ferdigvaren. For eksempel den **formelen** -feltet er satt til **høyde \*konstant**. Den **høyde** -feltet er satt til **2** for å angi lengden på tube som kreves for den ferdige varen. **Flere**-feltet settes til **4,5** for å angi at røret plukkes i lengder på 4,5 meter. Her er beregningen:

1.  Antallet som kreves for 10 stykker av ferdigvaren: 10 ÷ 2 = 5 stykker
2.  Totalt forbruk: 4,5 x 5 = 22,5 meter med metallrør

Det forutsettes av 0,5 meter rør kasseres for hvert rør som forbrukes.

### <a name="consumption"></a>Forbruk

Vanligvis merker du av for **Forbruk** som avrundingsmåte når råvarer må plukkes i hele antall av en bestemt håndteringsenhet av produktet. 2 liter maling brukes for eksempel til å produsere en stykk ferdigvare, og malingen plukkes i 25 liters spann. I dette tilfellet kan avrundingsmåten **Forbruk** brukes til å avrunde forbruk til hele tall for 25 liters spann. Her er beregningen av hvor mye maling som kreves hvis det skal produseres 180 stykker av ferdigvaren:

1.  Maling som kreves, unntatt svinn: 180 x 2 = 360 liter
2.  Antall spann: 360 ÷ 25 = 14,4, som rundes opp til 15
3.  Maling som kreves, inkludert svinn: 15 x 25 = 375 liter

## <a name="step-consumption"></a>Trinnforbruk
Trinnforbruk brukes til å beregne konstant forbruk i antallsintervaller. Hvis du velger **Trinnforbruk** i **Formel**-feltet i **Oppsett**-kategorien, kan du legge til informasjon om trinnene i kategorien **Trinnforbruk**. Det faste forbruksantallet kan defineres i intervaller av det produserte antallet. For eksempel er trinnforbruk definert som i følgende tabell.

| Fra serie | Antall |
|-------------|----------|
| 0,00        | 10,0000  |
| 100,00      | 20,0000  |
| 200,00      | 40,0000  |

Stykklisteantallet er 1, og produksjonsantallet er 110. Formelen for forbruket er av Fra serie (Antall) = Forbruk. Ettersom produksjonsantallet er 110, kommer det inn under "Fra 100-serien." Derfor er antallet 20.


