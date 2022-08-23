---
title: SESSIONNOW ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen SESSIONNOW.
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
ms.openlocfilehash: 1cf092d55728f23cb10070324abc4458004946c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272630"
---
# <a name="sessionnow-er-function"></a>SESSIONNOW ER-funksjon

[!include [banner](../includes/banner.md)]

`SESSIONNOW`-funksjonen returnerer en *DateTime*-verdi som representerer gjeldende dato og klokkeslett for programøkt.

## <a name="syntax"></a>Syntaks

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>Returverdier

*DateTime*

Den resulterende dato/klokkeslett-verdien.

## <a name="example"></a>Eksempel

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer gjeldende dato/klokkeslett-verdi for programøkt, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen og det angitte formatet.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
