---
title: NOT ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen NOT
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da30e9a0092f594da7cef7b425e2b89af7bda491
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890492"
---
# <a name="not-er-function"></a>NOT ER-funksjon

[!include [banner](../includes/banner.md)]

`NOT`-funksjonen returnerer den omvendte logiske verdien til den angitte betingelsen som en *boolsk* verdi.

## <a name="syntax"></a>Syntaks

```vb
NOT (condition)
```

## <a name="arguments"></a>Argumenter

`condition`: *Boolsk*

Et gyldig betingelsesuttrykk som må tilbakeføres.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="example"></a>Eksempel

`NOT (TRUE)` returnerer **USANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]