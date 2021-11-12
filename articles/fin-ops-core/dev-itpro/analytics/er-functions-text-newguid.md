---
title: NEWGUID ER-funksjon
description: Dette emnet gir informasjon om hvordan du bruker ER-funksjonen NEWGUID.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647950"
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
