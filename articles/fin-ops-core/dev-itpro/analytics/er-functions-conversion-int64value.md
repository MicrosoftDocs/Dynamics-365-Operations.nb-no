---
title: INT64VALUE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INT64VALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755402"
---
# <a name="int64value-er-function"></a>INT64VALUE ER-funksjon

[!include [banner](../includes/banner.md)]

`INT64VALUE`-funksjonen returnerer en *Int64*-verdi som representerer den angitte strengen.

## <a name="syntax-1"></a>Syntaks 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstverdi som må konverteres til et *Int64*-tall.

`number`: *Reell* eller *Heltall*

En numerisk *Reell* eller *Heltall*-verdi som må konverteres til et *Int64*-tall.

## <a name="return-values"></a>Returverdier

*Int64*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Desimaler avrundes.

## <a name="example-1"></a>Eksempel 1

`INT64VALUE ("22565422744")` returnerer *Int64*-verdien **22565422744**.

## <a name="example-2"></a>Eksempel 2

`INT64VALUE ( VALUE("22565422744.77"))` returnerer *Int64*-verdien **22565422744**.

## <a name="additional-resources"></a>Tilleggsressurser

[Typekonverteringsfunksjoner](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]