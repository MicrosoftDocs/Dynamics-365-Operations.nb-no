---
title: INTVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INTVALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 5d54543a6f9878feb3482c1c1e6c1f1f468718489fbc46aded84a5a84bdfb04e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745946"
---
# <a name="intvalue-er-function"></a>INTVALUE ER-funksjonen

[!include [banner](../includes/banner.md)]

`INTVALUE`-funksjonen returnerer en *Int*-verdi som representerer den angitte strengen.

## <a name="syntax-1"></a>Syntaks 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstverdi som må konverteres til et *Int*-tall.

`number`: *Reell* eller *Heltall*

En numerisk *Reell* eller *Heltall*-verdi som må konverteres til et *Int*-tall.

## <a name="return-values"></a>Returverdier

*Int*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Desimaler avrundes.

## <a name="example-1"></a>Eksempel 1

`INTVALUE ("100.77")` returnerer *Int*-verdien **100**.

## <a name="example-2"></a>Eksempel 2

`INTVALUE (-100.77)` returnerer *Int*-verdien **-100**.

## <a name="additional-resources"></a>Tilleggsressurser

[Typekonverteringsfunksjoner](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]