---
title: FIRSTORNULL ER-funksjon
description: Dette emnet forklarer hvordan du bruker ER-funksjonen FIRSTORNULL.
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
ms.openlocfilehash: 18c8f79d7d6306d9973c5a3f129b9cde38d05d58502a2c83ac89a2bd10aaaeab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749715"
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