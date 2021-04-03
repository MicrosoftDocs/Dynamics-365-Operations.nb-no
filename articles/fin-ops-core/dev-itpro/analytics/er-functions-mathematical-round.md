---
title: ROUND ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUND.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
ms.topic: article
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
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570404"
---
# <a name="round-er-function"></a>ROUND ER-funksjon

[!include [banner](../includes/banner.md)]

`ROUND`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er avrundet til angitt antall desimaler.

## <a name="syntax"></a>Syntaks

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Argumenter

`number`: *Reell*

En numerisk verdi som må avrundes.

`decimals`: *Heltall*

En numerisk verdi som representerer antall desimaler.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Hvis verdien for `decimals`-parameteren er større enn 0 (null), avrundes det angitte tallet til så mange desimalplasser.

Hvis verdien for `decimals`-parameteren er **0** (null), avrundes det angitte tallet til nærmeste jevne heltall.

Hvis verdien for `decimals`-parameteren er mindre enn 0 (null), avrundes det angitte tallet til venstre for desimalpunktet.

## <a name="example-1"></a>Eksempel 1

`ROUND (1200.767, 2)` avrunder til to desimalplasser og returnerer **1200,77**.

## <a name="example-2"></a>Eksempel 2

`ROUND (1200.767, -3)` avrunder til nærmeste multiplum av 1 000, og returnerer **1000**.

## <a name="example-3"></a>Eksempel 3

`ROUND (1200.5, 0)` avrunder til nærmeste jevne heltall og returnerer **1200**, mens `ROUND (1201.5, 0)` gjør det samme og returnerer **1202**.

## <a name="additional-resources"></a>Tilleggsressurser

[Matematiske funksjoner](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]