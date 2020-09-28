---
title: ROUND ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUND.
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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744557"
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

Hvis verdien for `decimals`-parameteren er **0** (null), avrundes det angitte tallet til nærmeste heltall.

Hvis verdien for `decimals`-parameteren er mindre enn 0 (null), avrundes det angitte tallet til venstre for desimalpunktet.

## <a name="example-1"></a>Eksempel 1

`ROUND (1200.767, 2)` avrunder til to desimalplasser og returnerer **1200.77**.

## <a name="example-2"></a>Eksempel 2

`ROUND (1200.767, -3)` avrunder til nærmeste multiplum av 1 000, og returnerer **1000**.

## <a name="additional-resources"></a>Tilleggsressurser

[Matematiske funksjoner](er-functions-category-mathematical.md)
