---
title: SESSIONTODAY ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen SESSIONTODAY.
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
ms.openlocfilehash: 0eeb4fcc449b565774cc79b767a2d157557d5b98
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274897"
---
# <a name="sessiontoday-er-function"></a>SESSIONTODAY ER-funksjon

[!include [banner](../includes/banner.md)]

`SESSIONTODAY`-funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programøkt.

## <a name="syntax"></a>Syntaks

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Returverdier

*Dato*

Den resulterende datoverdien.

## <a name="example"></a>Eksempel

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer gjeldende programøktdato, 24. desember 2015, som strengen **"24-12-2015"**, basert på den valgte tyske kulturen og det angitte formatet.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
