---
title: FIRST ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen FIRST.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b06f07c4cfef5c74c22f60dfa37986ee88c544cf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275487"
---
# <a name="first-er-function"></a>FIRST ER-funksjon

[!include [banner](../includes/banner.md)]

`FIRST`-funksjonen returnerer den første posten i den angitte listen som en *Container (post)*-verdi, hvis denne listen ikke er tom. Hvis listen er tom, genererer denne funksjonen et unntak.

## <a name="syntax"></a>Syntaks

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example-1"></a>Eksempel 1

Uttrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstverdien **"A"**.

## <a name="example-2"></a>Eksempel 2

Uttrykket `FIRST(SPLIT("",1)).Value` genererer et unntak under kjøring.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
