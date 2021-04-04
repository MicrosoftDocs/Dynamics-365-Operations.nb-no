---
title: PLIT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLIT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: 806a0995f0c138f4e80396bb993bc6f41bc7c827
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567348"
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

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]