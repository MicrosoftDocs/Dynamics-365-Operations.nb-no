---
title: CONCATENATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CONCATENATE.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569611"
---
# <a name="concatenate-er-function"></a>CONCATENATE ER-funksjon

[!include [banner](../includes/banner.md)]

`CONCATENATE`-funksjonen returnerer alle de angitte tekststrengene som en *streng*-verdi etter at de er føyd sammen til én streng.

## <a name="syntax"></a>Syntaks

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumenter

`text 1`: *Streng*

En referanse til en datakilde for *Streng*-datatypen. Dette argumentet er obligatorisk.

`text N`: *Streng*

En referanse til en datakilde for *Streng*-datatypen. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.

## <a name="usage-notes"></a>Bruksnotater

Uttrykket `"abc" & "def"` returnerer også **"abcdef"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]