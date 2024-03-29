---
title: TRANSLATE ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen TRANSLATE.
author: kfend
ms.date: 04/02/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278449"
---
# <a name="translate-er-function"></a>TRANSLATE ER-funksjon

[!include [banner](../includes/banner.md)]

`TRANSLATE`-funksjonen returnerer en *Streng*-verdi som inneholder resultatet av tegnerstatningen av den angitte teksten i tegn i et annet angitt sett.

## <a name="syntax"></a>Syntaks

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen.

`pattern`: *Streng*

Teksten som må erstattes.

`replacement`: *Streng*

Teksten som skal brukes som erstatning.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

`TRANSLATE`-funksjonen erstatter ett tegn om gangen. Funksjonen erstatter det første tegnet i `text`-argumentet med det første tegnet i `pattern`-argumentet, og deretter det andre tegnet og følger den samme flyten til det er ferdig. Når et tegn fra argumentene `text` og `pattern` er likt, erstattes det med et tegn fra `replacement`-argumentet som er plassert i samme posisjon som tegnet fra `pattern`-argumentet. Hvis et tegn vises flere ganger i `pattern`-argumentet, brukes tilordningen av `replacement`-argumentet som tilsvarer den første forekomsten av dette tegnet.

## <a name="example-1"></a>Eksempel 1

`TRANSLATE ("abcdef", "cd", "GH")` erstatter tegnet **"c"** i den angitte teksten **"abcdef"** med tegnet **"G"** i `replacement`-teksten på grunn av følgende:
-   Tegnet **"c"** vises i `pattern`-teksten i første posisjon.
-   Den første posisjonen i `replacement`-teksten inneholder tegnet **"G"**.

## <a name="example-2"></a>Eksempel 2

`TRANSLATE ("abcdef", "ccd", "GH")` returnerer **"abGdef"**.

## <a name="example-3"></a>Eksempel 3

`TRANSLATE ("abccba", "abc", "123")` returnerer **"123321"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
