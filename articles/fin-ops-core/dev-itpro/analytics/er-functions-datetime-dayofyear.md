---
title: DAYOFYEAR ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DAYOFYEAR.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746921"
---
# <a name="dayofyear-er-function"></a>DAYOFYEAR ER-funksjonen

[!include [banner](../includes/banner.md)]

`DAYOFYEAR`-funksjonen returnerer en *Heltall*-verdi som representerer antall dager mellom 1. januar og den angitte datoen.

## <a name="syntax"></a>Syntaks

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumenter

`date`: *Dato*

En datoverdi som representerer datoen som skal brukes for beregningen av antall dager.

## <a name="return-values"></a>Returverdier

*Heltall*

Den resulterende numeriske verdien.

## <a name="example-1"></a>Eksempel 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returnerer **61**.

## <a name="example-2"></a>Eksempel 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returnerer **1**.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]