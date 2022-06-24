---
title: ROUNDUP ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDUP.
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
ms.openlocfilehash: ec4fdce6f072c5c3d87b139c8f64bd63a8a3eccd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855652"
---
# <a name="roundup-er-function"></a>ROUNDUP ER-funksjon

[!include [banner](../includes/banner.md)]

`ROUNDUP`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet opp til angitt antall desimaler.

## <a name="syntax"></a>Syntaks

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenter

`number`: *Reell*

En numerisk verdi som må avrundes opp.

`decimals`: *Heltall*

En numerisk verdi som representerer antall desimaler.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid opp det angitte tallet (bort fra null).

## <a name="example-1"></a>Eksempel 1

`ROUNDUP (1200.763, 2)` avrunder opp til to desimalplasser og returnerer **1200.77**.

## <a name="example-2"></a>Eksempel 2

`ROUNDUP (1200.767, -3)` avrunder opp til nærmeste multiplum av 1 000, og returnerer **2000**.

## <a name="additional-resources"></a>Tilleggsressurser

[Matematiske funksjoner](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]