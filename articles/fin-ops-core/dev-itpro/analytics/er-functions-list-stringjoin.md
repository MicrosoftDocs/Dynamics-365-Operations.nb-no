---
title: STRINGJOIN ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen STRINGJOIN.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6510c271ac5e01d841722fdf2c5fd8c7deaf8caf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271651"
---
# <a name="stringjoin-er-function"></a>STRINGJOIN ER-funksjonen

[!include [banner](../includes/banner.md)]

`STRINGJOIN`-funksjonen returnerer en *Streng*-verdi som består av sammenkoblede verdier for det angitte feltet fra den angitte listen. Verdiene kan skilles med det angitte skilletegnet.

## <a name="syntax"></a>Syntaks

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`field`: *Felt*

Den gyldige banen til et felt av *Streng*-datatypen i den angitte listen.

`delimiter`: *Streng*

Et skilletegn som brukes til å skille delstrenger.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

Hvis du angir `SPLIT("abc" , 1)` som datakilde **DS**, returnerer uttrykket `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
