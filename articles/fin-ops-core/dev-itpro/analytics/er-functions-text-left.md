---
title: LEFT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LEFT
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 5d0056dbe46b20432aacb35a971895b987fdbf1b8ebc0d2679bb1e52eb3c4cc2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762482"
---
# <a name="left-er-function"></a>LEFT ER-funksjon

[!include [banner](../includes/banner.md)]

`LEFT`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra starten av den angitte strengen.

## <a name="syntax"></a>Syntaks

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *streng*-verdi som representerer den opprinnelige teksten.

`number`: *Heltall*

Antall tegn som må returneres fra begynnelsen av den opprinnelige teksten.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`LEFT ("Sample", 3)` returnerer **"Sam"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]