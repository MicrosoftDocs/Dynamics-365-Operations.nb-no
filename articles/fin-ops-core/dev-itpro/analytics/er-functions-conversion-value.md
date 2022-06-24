---
title: VALUE ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen VALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: e96d274962ad79969a3158f7e352d3c72bd4072c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892987"
---
# <a name="value-er-function"></a>VALUE ER-funksjonen

[!include [banner](../includes/banner.md)]

`VALUE`-funksjonen returnerer en *reell* verdi som er konvertert fra den angitte strengen.

## <a name="syntax"></a>Syntaks

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En strengverdi som må konverteres til en numerisk verdi.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Komma og punktum-tegn (.) regnes som desimalskilletegn, og en foranstilt bindestrek (-) brukes som negativt fortegn. Det oppstår et unntak under kjøring hvis den angitte strengen inneholder andre ikke-numeriske tegn.

## <a name="example-1"></a>Eksempel 1

`VALUE ("1 234,56")` iverksetter et unntak.

## <a name="example-2"></a>Eksempel 2

`VALUE ("1234,56")` returnerer **1234.56**.

## <a name="additional-resources"></a>Tilleggsressurser

[Typekonverteringsfunksjoner](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]