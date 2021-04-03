---
title: PADLEFT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen PADLEFT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562691"
---
# <a name="padleft-er-function"></a>PADLEFT ER-funksjonen

[!include [banner](../includes/banner.md)]

`PADLEFT`-funksjonen returnerer en *Streng*-verdi med den angitte lengden der begynnelsen av den angitte strengen fylles ut med de angitte tegnene.

## <a name="syntax"></a>Syntaks

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *streng*-verdi som representerer den opprinnelige teksten.

`length`: *Heltall*

En *Heltall*-verdi som representerer det endelige antallet tegn i den utfylte strengen.

`padding chars`: *Streng*

Tegnene som skal brukes til utfylling.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`PADLEFT ("1234", 10, "`&nbsp;`")` returnerer tekststrengen **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]