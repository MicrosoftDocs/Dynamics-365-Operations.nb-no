---
title: GETCURRENTCOMPANY ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen GETCURRENTCOMPANY.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b5f5f7d7c884000f59b93e10875f78289a879779
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280193"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER-funksjonen

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY`-funksjonen returnerer en *streng*-verdi som representerer koden for den juridiske enheten (firma) som en bruker er logget på nå.

## <a name="syntax"></a>Syntaks

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruker som er logget på firmaet **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
