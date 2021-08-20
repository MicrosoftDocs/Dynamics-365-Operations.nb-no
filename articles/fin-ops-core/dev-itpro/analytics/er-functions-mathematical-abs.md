---
title: ABS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ABS
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: db12ddddb087556414e81d646c4c87d273a77c133e49152091452d0731916e93
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776080"
---
# <a name="abs-er-function"></a>ABS ER-funksjon

[!include [banner](../includes/banner.md)]

`ABS`-funksjonen returnerer den absolutte (modulus) verdien til det angitte nummeret som en *reell* verdi. Altså returnes tallet uten fortegn.

## <a name="syntax"></a>Syntaks

```vb
ABS (number)
```

## <a name="arguments"></a>Argumenter

`number`: *Reell*

En numerisk verdi du vil bruke modulus til.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="example"></a>Eksempel

`ABS (-1)` returnerer **1**.

## <a name="additional-resources"></a>Tilleggsressurser

[Matematiske funksjoner](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]