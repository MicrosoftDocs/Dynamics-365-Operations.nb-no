---
title: GUIDVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GUIDVALUE.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915700"
---
# <a name="GUIDVALUE">GUIDVALUE ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`GUIDVALUE`-funksjonen konverterer de angitte inndataene for *Streng*-datatypen til et dataelement av *GUID*-typen.

## <a name="syntax"></a>Syntaks

```
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
