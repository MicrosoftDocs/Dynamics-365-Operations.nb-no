---
title: Problemløserstrategi for produktkonfigurasjon
description: Denne artikkelen beskriver hvordan du kan bruke problemløserstrategien til å forbedre ytelsen til produktkonfigurasjon.
author: t-benebo
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b0b53da17bd106be60966d856d29d81a1e57f91
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065525"
---
# <a name="solver-strategy-for-product-configuration"></a>Problemløserstrategi for produktkonfigurasjon

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kan bruke problemløserstrategien til å forbedre ytelsen til produktkonfigurasjon.

Konseptet med problemløserstrategier ble først innført i Kumulativ oppdatering 7 (CU7) for Microsoft Dynamics AX 2012 R2. Det ble utvidet i Kumulativ oppdatering 8 (CU8) for Microsoft Dynamics AX 2012 R3 og økonomi- og driftsapper, Enterprise edition 7.3.

Problemløserstrategikonseptet består nå av følgende strategier:

- Standard
- Små domener først
- Ovenfra og nedover
- Z3

## <a name="solver-strategy"></a>Problemløserstrategi 

En produktkonfigurasjonsmodell kan formuleres som et [begrensningsbasert problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf). Microsoft Solver Foundation (MSF) inneholder to typer problemløserstrategier for å løse CSP-er som kan brukes fra produktkonfigurasjonsmodeller. Disse problemløserstrategiene er avhengige av [heuristikk](https://techterms.com/definition/heuristic), som brukes til å bestemme rekkefølgen som variablene i CSP-er blir vurdert når problemet løses. Heuristikk kan ha stor innvirkning på ytelsen når et problem eller en klasse med problemer løses.

Problemløserstrategien for produktkonfigurasjonsmodeller bestemmer hvilken problemløser som brukes med heuristikk. Strategien **Standard**, **Små domener først** og **Ovenfra og nedover** bruker de to problemløserne fra MSF, mens **Z3**-strategien bruker Z3-problemløseren. 

Studier av kundeimplementering har vist at en endring i problemløserstrategien for en produktkonfigurasjonsmodell kan redusere svartiden fra minutter til millisekunder. Derfor er det verdt å prøve forskjellige problemløserstrategier for å finne den mest effektive strategien for produktkonfigurasjonsmodellen din.

## <a name="change-the-settings-for-the-solver-strategy"></a>Endre innstillingene for problemløserstrategien

Du kan endre problemløserstrategien på siden **Produktkonfigurasjonsmodeller** i handlingsruten ved å velge **Modellegenskaper**. Deretter i **Rediger modelldetaljene**-dialogboksen velger du en problemløserstrategi.

[![Endre problemløserstrategien.](./media/solver-strategy.png)](./media/solver-strategy.png)

Det er for øyeblikket ingen logikk som automatisk oppdager hvilken problemløserstrategi som vil være den mest effektive strategien for restriksjonsbasert produktkonfigurasjon. Du må derfor prøve ut en og en problemløserstrategi.

Følgende tabell inneholder anbefalinger om problemløserstrategien som skal brukes i ulike scenarier.

| Problemløserstrategi      | Bruk strategien i dette scenariet |
|----------------------|-----------------------------------|
| Standard              | **Standard**-strategien er optimalisert til å løse modeller som bruker tabellbegrensninger. Kundeimplementeringsstudier har vist at denne strategien er den mest effektive strategien i scenarier der tabellbegrensninger brukes mye. |
| Små domener først | **Små domener først**- og **Ovenfra og nedover**-strategien henger nøye sammen. Kundeimplementeringsstudier har vist at **Ovenfra og nedover**-strategien overgår **Små domener først**-strategien. Men **Små domener først**-strategien bevares i produktet for bakoverkompatibilitet. Begge disse problemløserstrategiene har vist seg å være mer effektive på å løse modeller som inneholder flere aritmetiske uttrykk der det ikke brukes tabellbegrensninger. I noen tilfeller kan imidlertid **Standard**-strategien overgå disse to strategiene. Derfor må du huske å forsøke hver strategi. |
| Ovenfra og nedover             | **Små domener først**- og **Ovenfra og nedover**-strategien henger nøye sammen. Kundeimplementeringsstudier har vist at **Ovenfra og nedover**-strategien overgår **Små domener først**-strategien. Men **Små domener først**-strategien bevares i produktet for bakoverkompatibilitet. Begge disse problemløserstrategiene har vist seg å være mer effektive på å løse modeller som inneholder flere aritmetiske uttrykk der det ikke brukes tabellbegrensninger. I noen tilfeller kan imidlertid **Standard**-strategien overgå disse to strategiene. Derfor må du huske å forsøke hver strategi. |
| Z3                   | Det anbefales at du bruker **Z3**-strategien som standard problemløserstrategi. Hvis du er bekymret for ytelse og skalerbarhet, kan du evaluere de andre strategiene. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktkonfigurasjon](build-product-configuration-model.md)

[Heuristikk](https://techterms.com/definition/heuristic)

[Begrensningsbasert problem](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
