---
title: ISEMPTY ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen ISEMPTY.
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
ms.openlocfilehash: 1d8c9a2195afbc76bc00f31778d087268b98279f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845532"
---
# <a name="isempty-er-function"></a>ISEMPTY ER-funksjon

[!include [banner](../includes/banner.md)]

`ISEMPTY`-funksjonen returnerer den *boolske* verdien **SANN** hvis den angitte listen ikke inneholder noen poster. Hvis ikke returneres den *boolske* verdien **USANN**.

## <a name="syntax"></a>Syntaks

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="example-1"></a>Eksempel 1

Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, genererer uttrykket `ISEMPTY(DS)` **USANN**.

## <a name="example-2"></a>Eksempel 2

Uttrykket `ISEMPTY (SPLIT ("",1))` returnerer **SANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]