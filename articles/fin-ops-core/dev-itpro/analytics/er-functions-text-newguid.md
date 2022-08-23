---
title: NEWGUID ER-funksjon
description: Denne artikkelen gir informasjon om hvordan du bruker ER-funksjonen NEWGUID.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274780"
---
# <a name="newguid-er-function"></a>NEWGUID ER-funksjon

[!include [banner](../includes/banner.md)]

Funksjonen `NEWGUID` genererer en ny, globalt unik identifikator (PST) og returnerer den som en *[GUID](er-formula-supported-data-types-primitive.md#guid)*-verdi.

## <a name="syntax"></a>Syntaks

```vb
NEWGUID ()
```

## <a name="return-values"></a>Returverdier

*GUID*

Den resulterende GUID-verdien.

## <a name="example"></a>Eksempel

`NEWGUID()` returnerer alltid en ny *GUID*-verdi, for eksempel **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
