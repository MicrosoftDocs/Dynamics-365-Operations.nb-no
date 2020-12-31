---
title: POWER ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen POWER.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683335"
---
# <a name="power-er-function"></a>POWER ER-funksjonen

[!include [banner](../includes/banner.md)]

`POWER`-funksjonen returnerer en *reell* verdi som representerer resultatet av å heve det angitte positive tallet til den angitte potens.

## <a name="syntax"></a>Syntaks

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumenter

`number`: *Reell* eller *Heltall*

En numerisk verdi som må heves til den angitte potens.

`power`: *Reell* eller *Heltall*

En numerisk verdi som representerer den bestemte potensen.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="example-1"></a>Eksempel 1

`POWER (10, 2)` returnerer **100**.

## <a name="example-2"></a>Eksempel 2

`POWER (4, 0.5)` returnerer **2**.

## <a name="additional-resources"></a>Tilleggsressurser

[Matematiske funksjoner](er-functions-category-mathematical.md)
