---
title: NUMBERFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMBERFORMAT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890389"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER-funksjonen

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT`-funksjonen returnerer en *Streng*-verdi som viser det angitte tallet i angitt format og i en valgfri angitt [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-numeric-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltall* eller *Reell*

En numerisk verdi som angir nummeret som må formateres.

`format` : *Streng*

En *streng*-verdi som representerer formatet.

`culture`: *Streng*

En *streng*-verdi som representerer kulturen som skal brukes til formatering.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Hvis kulturen ikke er definert som et argument for den kalte funksjonen, vil konteksten som denne funksjonen kjøres i, bestemme kulturen som brukes til å formatere tall.

## <a name="example-1"></a>Eksempel 1

For **EN-US**-kulturen returnerer `NUMBERFORMAT (0.45, "p")` **"45.00 %"**, og `NUMBERFORMAT (10.45, "#")` returnerer **"10"**.

## <a name="example-2"></a>Eksempel 2

`NUMBERFORMAT (10/3, "F2", "de")` returnerer **3,33**, mens `NUMBERFORMAT (10/3, "F2", "en-us")` returnerer **3.33**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]