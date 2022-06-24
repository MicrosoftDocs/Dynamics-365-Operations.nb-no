---
title: COUNT ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen COUNT.
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
ms.openlocfilehash: b848bd179806b676435c219f0eb983516f3d0bf9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895402"
---
# <a name="count-er-function"></a>COUNT ER-funksjon

[!include [banner](../includes/banner.md)]

`COUNT`-funksjonen returnerer en *Heltall*-verdi som representerer antall poster i den angitte listen, hvis listen ikke er tom. Hvis listen er tom, returnerer denne funksjonen **0** (null).

## <a name="syntax"></a>Syntaks

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Heltall*

Den resulterende numeriske verdien.

## <a name="example"></a>Eksempel

`COUNT (SPLIT("abcd" , 3))` returnerer **2** fordi `SPLIT`-funksjonen som brukes i dette eksemplet, oppretter en liste som består av to poster.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]