---
title: Liste over ER-funksjoner i den logiske kategorien
description: Denne artikkelen inneholder informasjon om de logiske funksjonene som støttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2361fa0df3fe60813e75c772134299ad948f3582
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888198"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Liste over ER-funksjoner i den logiske kategorien

[!include [banner](../includes/banner.md)]

Logiske funksjoner for elektronisk rapportering (ER) kan brukes til å arbeide med logiske verdier for å utføre mer enn én sammenligning i ett enkelt uttrykk eller teste flere betingelser. Denne artikkelen inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon | Beskrivelse |
|----------|-------------|
| [Og](er-functions-logical-and.md)                       | Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis alle de angitte betingelsene er sanne. Hvis ikke returneres den *boolske* verdien **USANN**. |
| [Sak](er-functions-logical-case.md)                     | Denne funksjonen evaluerer verdien til det angitte uttrykket mot de angitte alternative valgene, og returnerer resultatet av det første alternativet som tilsvarer verdien til det angitte uttrykket. Hvis ikke returnerer den et valgfritt standard resultat hvis et standard resultat er angitt som det siste argumentet i den kalte funksjonen som ikke innledes av et alternativ. Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene. |
| [Inneholder](er-functions-logical-contains.md)             | Denne funksjonen bestemmer om de angitte inndataene inneholder den angitte teksten. Den returnerer den *boolske* verdien **SANN** hvis de angitte inndataene inneholder den angitte teksten. Hvis ikke returneres den *boolske* verdien **USANN**. |
| [EndsWith](er-functions-logical-endswith.md)             | Denne funksjonen bestemmer om de angitte inndataene slutter med den angitte teksten. Den returnerer den *boolske* verdien **SANN** hvis de angitte inndataene slutter med den angitte teksten. Hvis ikke returneres den *boolske* verdien **USANN**. |
| [Hvis](er-functions-logical-if.md)                         | Denne funksjonen returnerer den første verdien hvis den angitte betingelsen er oppfylt. Hvis ikke returneres den andre verdien som er angitt. Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene. |
| [Ikke](er-functions-logical-not.md)                       | Denne funksjonen returnerer den omvendte logiske verdien til den angitte betingelsen som en *boolsk* verdi. |
| [Or](er-functions-logical-or.md)                         | Denne funksjonen returnerer en *boolsk* verdi av **USANN** hvis alle de angitte betingelsene er usanne. Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis en angitt betingelse er sann. |
| [StartsWith](er-functions-logical-startswith.md)         | Denne funksjonen bestemmer om de angitte inndataene starter med den angitte teksten. Den returnerer den *boolske* verdien **SANN** hvis de angitte inndataene starter med den angitte teksten. Hvis ikke returneres den *boolske* verdien **USANN**. |
| [ValueIn](er-functions-logical-valuein.md)               | Denne funksjonen bestemmer om de angitte inndataene samsvarer med en verdi for et angitt element i den angitte listen. Den returnerer en *boolsk* verdi av **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen. Hvis ikke returneres den *boolske* verdien **USANN**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Denne funksjonen bestemmer om de angitte inndataene av typen *Int64* eller *Integer* samsvarer med en verdi for et angitt element i den angitte listen. Den returnerer en *boolsk* verdi av **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen. Hvis ikke returneres den *boolske* verdien **USANN**. |


## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]