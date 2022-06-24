---
title: GUIDVALUE ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen GUIDVALUE.
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
ms.openlocfilehash: f3899d983f7c790ff2e3dc74dd91c44fc54e44d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898747"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE ER-funksjonen

[!include [banner](../includes/banner.md)]

`GUIDVALUE`-funksjonen konverterer de angitte inndataene for *Streng*-datatypen til et dataelement av *GUID*-typen.

## <a name="syntax"></a>Syntaks

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen.

## <a name="return-values"></a>Returverdier

*GUID*

Den resulterende GUID-verdien (globalt unik identifikator).

## <a name="usage-notes"></a>Bruksnotater

For å konvertere i motsatt retning (det vil si å konvertere angitt inndata av *GUID*-datatypen til et dataelement av *String*-datatypen), kan du bruke funksjonen [TEXT](er-functions-text-text.md).

## <a name="example"></a>Eksempel

Du definerer de følgende datakildene i modelltilordningen:

- En **myID**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- En **Brukere**-datakilde av *Tabellposter*-typen som refererer til tabellen UserInfo

Du kan deretter bruke et uttrykk, for eksempel `FILTER (Users, Users.objectId = myID)`, til å filtrere UserInfo-tabellen etter **objectId**-feltet for *GUID*-datatypen.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]