---
title: MID ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen MID
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: ca5dbfb6de3057ad2c4a6dcc7ecce3d0ddc69595
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867647"
---
# <a name="mid-er-function"></a>MID ER-funksjon

[!include [banner](../includes/banner.md)]

`MID`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra den angitte strengen, og begynner fra den angitte posisjonen.

## <a name="syntax"></a>Syntaks

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *streng*-verdi som angir teksten det skal returneres tegn fra.

`starting position`: *Heltall*

En *Heltall*-verdi som angir plasseringen til det første tegnet som må returneres fra den angitte teksten.

`number of characters`: *Heltall*

En *Heltall*-verdi som angir antall tegn som må returneres, som begynner fra den angitte startposisjonen.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Hvis verdien for `starting position`-argumentet er mindre enn 0 (null), telles tegnene som returneres, fra den første plasseringen i den angitte strengen.

Hvis verdien for `starting position`-argumentet overskrider lengden på den angitte strengen, returneres en tom streng.

## <a name="example"></a>Eksempel

`MID ("Sample", 2, 3)` returnerer **"amp"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]