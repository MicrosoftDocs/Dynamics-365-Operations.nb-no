---
title: UPPER ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen UPPER.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 3742f490fb87d156e3b3dcebabdcebb85ab76f5d0afd9a60806497d32e5746e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729812"
---
# <a name="upper-er-function"></a>UPPER ER-funksjon

[!include [banner](../includes/banner.md)]

`UPPER`-funksjonen returnerer den angitte tekststrengen som en *Streng*-verdi etter at den er konvertert til store bokstaver.

## <a name="syntax"></a>Syntaks

```vb
UPPER (text )
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`UPPER ("Sample")` returnerer **"SAMPLE"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]