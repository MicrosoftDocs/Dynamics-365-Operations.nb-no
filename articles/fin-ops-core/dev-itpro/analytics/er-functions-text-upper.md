---
title: UPPER ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen UPPER.
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: bdea427dda5f09a3903378012679e9dd3fa86be9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275349"
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
