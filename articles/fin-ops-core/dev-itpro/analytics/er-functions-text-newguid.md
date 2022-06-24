---
title: NEWGUID ER-funksjon
description: Denne artikkelen gir informasjon om hvordan du bruker ER-funksjonen NEWGUID.
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
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861823"
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
