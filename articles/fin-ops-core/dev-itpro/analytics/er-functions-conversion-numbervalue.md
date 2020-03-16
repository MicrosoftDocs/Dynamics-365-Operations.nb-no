---
title: NUMBERVALUE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMBERVALUE.
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
ms.openlocfilehash: 6eeb66f4206eb39141a5b2573fcb9d15428ae52a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042667"
---
# <a name="NUMBERVALUE">NUMBERVALUE ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`NUMBERVALUE`-funksjonen returnerer en *reell* verdi som er konvertert fra den angitte *streng*-verdien. Under konverteringen vurderes de angitte skilletegnene for desimal- og siffergruppering.

## <a name="syntax"></a>Syntaks

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstverdi som må konverteres til et *reelt* tall.

`decimal separator`: Streng

Et desimalskilletegn. Det brukes til å skille heltalls- og brøkdeler av et desimaltall.

`digit grouping separator`: *Streng*

Et skilletegn for siffergruppering. Det brukes som tusenskilletegn.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="example"></a>Eksempel

`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234.56**.

## <a name="additional-resources"></a>Tilleggsressurser

[Typekonverteringsfunksjoner](er-functions-category-type-conversion.md)
