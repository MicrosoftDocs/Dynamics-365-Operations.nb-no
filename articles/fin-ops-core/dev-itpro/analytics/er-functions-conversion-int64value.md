---
title: INT64VALUE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INT64VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042694"
---
# <a name="INT64VALUE">INT64VALUE ER-funksjon</a>

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
