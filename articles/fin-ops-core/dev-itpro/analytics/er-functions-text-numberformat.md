---
title: NUMBERFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMBERFORMAT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a431414044846bf4e79e6b9f0e5b27281ea8f46
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744413"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER-funksjonen

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT`-funksjonen returnerer en *Streng*-verdi som viser det angitte tallet i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

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
