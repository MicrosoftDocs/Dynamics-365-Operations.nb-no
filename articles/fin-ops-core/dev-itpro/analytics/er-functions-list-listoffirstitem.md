---
title: LISTOFFIRSTITEM ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen LISTOFFIRSTITEM.
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
ms.openlocfilehash: f4715becfb158826a2b5678aac6a58c987433192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881166"
---
# <a name="listoffirstitem-er-function"></a>LISTOFFIRSTITEM ER-funksjonen

[!include [banner](../includes/banner.md)]

`LISTOFFIRSTITEM` -funksjonen returnerer en *Postliste*-verdi som består av bare den første posten i den angitte listen.

## <a name="syntax"></a>Syntaks

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="example"></a>Eksempel

Uttrykket `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returnerer tekstverdien **"A"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]