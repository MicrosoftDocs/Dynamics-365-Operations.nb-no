---
title: ISVALIDCHARACTERISO7064 ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ISVALIDCHARACTERISO7064
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 21962952bb3bdd016831dc5e196af27c69ecc6db
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744077"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 ER-funksjon

[!include [banner](../includes/banner.md)]

`ISVALIDCHARACTERISO7064`-funksjonen returnerer den *boolske* verdien **SANN** hvis den angitte strengen representerer et gyldig internasjonalt bankkontonummer (IBAN). Hvis ikke returneres den *boolske* verdien **USANN**.

## <a name="syntax"></a>Syntaks

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstverdi som representerer et IBAN-nummer.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returnerer **SANN**. 

`ISVALIDCHARACTERISO7064 ("AT61")` returnerer **USANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)
