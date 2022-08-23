---
title: CONCATENATE ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen CONCATENATE
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
ms.openlocfilehash: 230bbbac5df7824c3ef7d0550cc45dbf6c374858
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267292"
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
