---
title: CHAR ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CHAR
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 63df7b1ac847e12cf429467dd444450552a59162
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744967"
---
# <a name="char-er-function"></a>CHAR ER-funksjon

[!include [banner](../includes/banner.md)]

`CHAR`-funksjonen returnerer en *streng*-verdi som viser et enkelt tegn som det angitte Unicode-nummeret refererer til.

## <a name="syntax"></a>Syntaks

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltall*

Et tall som svarer til et forventet enkelt tegn.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Strengen som denne funksjonen returnerer, avhenger av kodingen som er valgt i det overordnede **FIL**-formatelementet. Listen over støttede kodinger finner du her [Kodingsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Eksempel

`CHAR (255)` returnerer **"ÿ"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)
