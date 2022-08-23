---
title: PLIT ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen SPLIT.
author: kfend
ms.date: 04/01/2021
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
ms.openlocfilehash: e95ecaae46ee73899736b1d5729d7f9639fc6803
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274057"
---
# <a name="split-er-function"></a>PLIT ER-funksjonen

[!include [banner](../includes/banner.md)]

`SPLIT`-funksjonen deler den angitte inndatastrengen inn i delstrenger og returnerer resultatet som en ny *Postliste*-verdi.

## <a name="syntax-1"></a>Syntaks 1

```vb
SPLIT (input, length)
```

Denne syntaksen brukes til å dele opp den angitte inndatastrengen i delstrenger, der hver har den angitte lengden.

## <a name="syntax-2"></a>Syntaks 2

```vb
SPLIT (input, delimiter)
```

Denne syntaksen brukes til å dele opp den angitte inndatastrengen i delstrenger, basert på det angitte skilletegnet.

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Teksten som skal deles opp.

`length`: *Heltall*

Maksimumslengden på en enkelt delstreng.

`delimiter`: *Streng*

Et skilletegn som brukes til å skille delstrenger.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Poststrukturen for listen som returneres, består av **Verdi**-feltet for *Streng*-typen. Hver post i listen som returneres, inneholder genererte delstrenger i dette feltet.

Hvis `delimiter`-argumentet er tomt, består den nye listen som returneres, av én post som har **Verdi**-feltet av *Streng*-typen. Dette feltet viser inndatateksten.

Hvis `input`-argumentet er tomt, returneres det en ny, tom liste. Hvis enten `input` eller `delimiter`-argumentet ikke er angitt (null), iverksettes et programunntak.

## <a name="example-1"></a>Eksempel 1

`SPLIT ("abcd", 3)` returnerer en ny liste som består av to poster som har **Verdi**-feltet av *Streng* typen. **Verdi**-feltet i den første posten inneholder teksten **"abc"**, og **Verdi**-feltet i den andre posten inneholder teksten **"d"**.

## <a name="example-2"></a>Eksempel 2

`SPLIT ("XAb aBy", "aB")` returnerer en ny liste som består av tre poster som har **Verdi**-feltet av *Streng* typen. **Verdi**-feltet i den første posten inneholder teksten **"X"**, **Verdi**-feltet i den andre posten inneholder teksten **"&nbsp;"**, og **Verdi**-feltet i den tredje posten inneholder teksten **"y"**. 

## <a name="example-3"></a>Eksempel 3

Du kan bruke [INDEX](er-functions-list-index.md)-funksjonen til å få tilgang til individuelle elementer for den angitte inndatastrengen. Hvis du angir **MyList**-datakilden av **Beregnet felt**-typen og konfigurer den for `SPLIT("abc", 1)`-uttrykket, vil uttrykket `INDEX(MyList,2).Value` returnere teksten **"b"**.

## <a name="example-4"></a>Eksempel 4

[ENUMERATE](er-functions-list-enumerate.md)-funksjonen kan også hjelpe deg med å få tilgang til individuelle elementer for den angitte inndatastrengen. Hvis du først angir **MyList**-datakilden av **Beregnet felt**-typen og konfigurer `SPLIT("abc", 1)`-uttrykket for den og deretter angir **EnumeratedList**-datakilden av **Beregnet felt**-typen og konfigurer `ENUMERATE(MyList)`-uttrykket for den, returnerer uttrykket `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` teksten **"b"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
