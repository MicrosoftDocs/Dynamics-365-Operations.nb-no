---
title: FIRSTORNULL ER-funksjon
description: Denne artikkelen forklarer hvordan du bruker ER-funksjonen FIRSTORNULL
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: bae2916371cd00810f559ff2006b2b238c8ad918
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900258"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER-funksjon

[!include [banner](../includes/banner.md)]

`FIRSTORNULL`-funksjonen returnerer den første posten i den angitte listen som en *Container (post)*-verdi, hvis denne posten ikke er tom. Hvis posten er tom, returnerer denne funksjonen en nullverdi for *Container (post)*.

## <a name="syntax"></a>Syntaks

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example"></a>Eksempel

Uttrykket `FIRSTORNULL(SPLIT("",1)).Value` returnerer en tom streng (**""**).

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]