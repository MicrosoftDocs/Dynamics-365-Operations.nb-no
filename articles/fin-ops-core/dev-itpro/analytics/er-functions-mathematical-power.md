---
title: POWER ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen POWER.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274004"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
