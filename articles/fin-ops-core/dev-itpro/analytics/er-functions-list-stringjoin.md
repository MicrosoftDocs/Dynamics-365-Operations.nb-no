---
title: STRINGJOIN ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen STRINGJOIN.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 651cc261e6a33b1a824feb94afa767e439196e249bb13b0fc4886dc72bfdd184
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776104"
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