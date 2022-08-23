---
title: ER-funksjonen WEEKNUM
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen WEEKNUM.
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268154"
---
# <a name="weeknum-er-function"></a>ER-funksjonen WEEKNUM

[!include [banner](../includes/banner.md)]

`WEEKNUM`-funksjonen returnerer en *[Heltall](er-formula-supported-data-types-primitive.md#integer)*-verdi som representerer uken i året som inkluderer en angitt *[Dato](er-formula-supported-data-types-primitive.md#date)*-verdi. Beregningen er basert på kulturavhengige regler som definerer en kalenderuke og den første dagen i uken.

## <a name="syntax"></a>Syntaks

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumenter</a>

`date`: *Dato*

En datoverdi som representerer datoen som skal brukes for beregningen av uken i året.

`culture`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Kulturen som skal brukes til beregningen. Du kan bruke kulturkoder som støttes i henhold til .NET [-standarder](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Returverdier

*Heltall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Uken i året beregnes basert på [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)-standarden, hvis denne standarden er vedtatt av et land eller område som de nasjonale standardene er angitt for ved kjøretid. Hvis ikke er beregningen basert på land-/områdespesifikke nasjonale standarder.

Hvis en ustøttet [kultur](#arguments)-kode angis som et argumentet for funksjonen `WEEKNUM` ved kjøretid, vises et unntak. Hvis den tomme strengen angis som en kulturkode, brukes den engelske landsnøytrale kalenderen til å beregne ukenummeret.

## <a name="examples"></a>Eksempler

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` returnerer **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` returnerer **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` returnerer **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` returnerer **21**.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
