---
title: PADLEFT ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen PADLEFT.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: dac1f9142a381238bf116c4bce65958da8afc4db
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278896"
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
