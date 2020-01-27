---
title: Konvertering for måleenhet per produktvariant
description: Dette emnet forklarer hvordan konverteringer av måleenheter kan defineres for produktvarianter.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935105"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Konvertering for måleenhet per produktvariant

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan konverteringer av måleenheter kan defineres for produktvarianter. Det inneholder et eksempel på oppsettet.

Denne funksjonen gjør det mulig for firmaer å definere ulik enhetsomregning mellom variantene av samme produkt. Eksemplet nedenfor brukes i dette emnet. Et firma selger t-skjorter i størrelsene Liten, Middels, Stor og Ekstra stor. T-skjorten er definert som et produkt, og de ulike størrelsene er definert som varianter av produktet. T-skjortene pakkes i bokser, og det kan være fem t-skjorter i en boks, bortsett fra ekstra stor-størrelsen der det bare er plass til fire t-skjorter. Firmaet ønsker å spore de ulike variantene av t-skjorter i enheten **Stykker**, men selger t-skjortene i enheten **Boks**. Konverteringen mellom lagerenheten og salgsenheten er 1 boks = 5 stykker, med unntak av varianten ekstra stor, der konverteringen er 1 boks = 4 stykker.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Definere et produkt for enhetsomregning per variant

Produktvarianter kan bare opprettes for produkter av undertypen **Produkt**: **Produktstandard**. Hvis du vil ha mer informasjon, kan du se [Opprette en produktstandard](tasks/create-product-master.md).

Funksjonen er ikke aktivert for produkter som er angitt for Faktisk vekt-prosesser. 

Når produktstandarden med frigitte produktvarianter er opprettet, kan enhetsomregninger per varianter defineres. Du finner menyelementet for å åpne enhetskonverteringssiden i forbindelse med et produkt eller en produktvariant på følgende sider.

-   **Produktdetaljer**-siden
-   **Detaljer om frigitte produkter**-siden
-   **Frigitte produktvarianter**-siden

Når du åpner **Enhetsomregning**-siden i konteksten av en produktstandard eller frigitt produktvariant, kan du velge om du vil definere enhetsomregning for produktet eller for en produktvariant. Det gjør du ved å velge enten **Produktvariant** eller **Produkt** i **Opprett konvertering for**-feltet.

### <a name="product-variant"></a>Produktvariant

Hvis du velger **Produktvariant**, kan du velge hvilken variant du vil definere enhetsomregning for i **Produktvariant**-feltet.

### <a name="product"></a>Produkt

Hvis du velger **Produkt**, kan du definere en enhetsomregning for produktstandarden. Denne enhetsomregningen vil gjelde for alle produktvarianter uten definert enhetsomregning.

### <a name="example"></a>Eksempel

Produktstandarden **t-skjorte** har fire frigitte produktvarianter: liten, middels, stor og ekstra stor. T-skjortene er pakket i bokser, og det kan være fem t-skjorter i en boks, bortsett fra ekstra stor-størrelsen der det bare er plass til fire t-skjorter.

Først må du åpne **Enhetsomregning**-siden fra siden Frigi produktdetaljer for **t-skjorte.**

På **Enhetsomregning**-siden definerer du enhetsomregning for den frigitte produktvarianten ekstra stor.

| **Felt**             | **Innstilling**             |
|-----------------------|-------------------------|
| Opprett konvertering for | Produktvariant         |
| Produktvariant       | T-skjorte : : Ekstra stor : : |
| Fra enhet             | Bokser                   |
| Omregningsfaktor                | 4                       |
| Til enhet               | Stykker                  |

De frigitte produktvariantene liten, middels og stor har samme enhetsomregning mellom enheten Boks og Stykker, som betyr at du kan definere enhetsomregning for disse produktvariantene i produktstandarden.

| **Felt**             | **Innstilling** |
|-----------------------|-------------|
| Opprett konvertering for | Produkt     |
| Produkt               | T-skjorte     |
| Fra enhet             | Bokser       |
| Omregningsfaktor                | 5           |
| Til enhet               | Stykker      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Bruke Excel til å oppdatere enhetsomregningene

Hvis et produkt har mange produktvarianter med forskjellige enhetsomregninger, er det lurt å eksportere enhetskonverteringene fra **Enhetsomregning**-siden til et Excel-regneark, oppdatere konverteringene og deretter publisere dem tilbake til Supply Chain Mangement.

Alternativet for å eksportere til Excel og publisere endringene tilbake til Supply Chain Mangement, aktiveres fra **Åpne i Microsoft office**-menyelementet i handlingsruten på **Enhetsomregning**-siden.
