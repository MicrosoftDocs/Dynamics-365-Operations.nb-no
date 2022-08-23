---
title: NULLDATETIME ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen NULLDATETIME.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 49b75a6cc1e2c1eee926ed8a235ae886d781ad3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287286"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME ER-funksjon

[!include [banner](../includes/banner.md)]

`NULLDATETIME`-funksjonen returnerer en *DateTime*-verdi som representerer **null** dato/klokkeslett-verdien (1. januar 1900) i Coordinated Universal Time (Greenwich middeltid \[GMT\]).

## <a name="syntax"></a>Syntaks

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Returverdier

*DateTime*

Den resulterende dato/klokkeslett-verdien.

## <a name="example"></a>Eksempel

`DATETIMEFORMAT( NULLDATETIME(), "O")` returnerer strengverdien **1900-01-01T00:00:00.0000000+00:00** når den kalles under en prosess som ble startet av en programbruker som har tidssoneverdien **(GMT) Coordinated Universal Time** i delen **Innstillinger for språk og land/område**.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
