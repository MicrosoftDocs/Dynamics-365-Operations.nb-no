---
title: CHAR ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen CHAR
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
ms.openlocfilehash: 1fb1d25c2624894e7bb0fa34b7bc48905a9289a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881497"
---
# <a name="char-er-function"></a>CHAR ER-funksjon

[!include [banner](../includes/banner.md)]

`CHAR`-funksjonen returnerer en *streng*-verdi som viser et enkelt tegn som det angitte Unicode-nummeret refererer til.

## <a name="syntax"></a>Syntaks

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltall*

Et tall som svarer til et forventet enkelt tegn.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Strengen som denne funksjonen returnerer, avhenger av kodingen som er valgt i det overordnede **FIL**-formatelementet. Listen over støttede kodinger finner du her [Kodingsklasse](/dotnet/api/system.text.encoding).

## <a name="example"></a>Eksempel

`CHAR (255)` returnerer **"ÿ"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]