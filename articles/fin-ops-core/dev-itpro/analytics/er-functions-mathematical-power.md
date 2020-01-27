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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb768b400e3ddb99e7c8b05905d7a2dd9e4392de
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915907"
---
# <a name="POWER">POWER ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`POWER`-funksjonen returnerer en *reell* verdi som representerer resultatet av å heve det angitte positive tallet til den angitte potens.

## <a name="syntax"></a>Syntaks

```
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
