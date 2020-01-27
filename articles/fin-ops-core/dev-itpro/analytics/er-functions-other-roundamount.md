---
title: ROUNDAMOUNT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDAMOUNT.
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
ms.openlocfilehash: c68933352da1f9c7dc5dad76e8635981f8a89fce
ms.sourcegitcommit: 9291e6dc0de076a16684980e528c5aa98845bb34
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2918985"
---
# <a name="ROUNDAMOUNT">ROUNDAMOUNT ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`ROUNDAMOUNT`-funksjonen returnerer en *reell* verdi som resultatet av avrunding av det angitte beløpet til nærmeste multiplum av et annet nummer i henhold til den angitte avrundingsregelen.

## <a name="syntax"></a>Syntaks

```
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Argumenter

`number`: *Int* eller *Real*

En numerisk verdi som må avrundes.

`decimals`: *Int* eller *Real*

Tallet som verdien for `number`-parameteren må avrundes til et multiplum av.

`round rule`: *Opplistingsverdi*

En opplistingsverdi for **RoundOffType**-opplistingen som definerer avrundingsregelen. Denne opplistingen har følgende verdier:

- Normal (ordinær)
- Nedover (RoundDown)
- Avrundingsmetode (RoundUp)

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien er et multiplum av verdien som er angitt av `decimals`-parameteren, og er nærmest verdien som er angitt av `number`-parameteren.

## <a name="usage-notes"></a>Bruksnotater

Når `number`-parameteren er null, returnerer denne funksjonen alltid null.

Når `decimals`-parameteren er null, runder denne funksjonen av til standard avrundingsverdi. Når `round rule`-parameteren er satt til **RoundOffType.Ordinary**, er standard avrundingsverdi **0,01**. Hvis ikke er standard avrundingsverdi **1,0**.

Når `round rule`-parameteren er satt til **RoundOffType.Ordinary**, runder denne funksjonen av til det nærmeste avrundingsbeløpet.

Når `round rule`-parameteren er satt til **RoundOffType.RoundDown**, runder denne funksjonen av mot null til nærmeste avrundingsbeløpet.

Når `round rule`-parameteren er satt til **RoundOffType.RoundUp**, runder denne funksjonen bort fra null til nærmeste avrundingsbeløpet.

Når `round rule`-parameteren er satt til **RoundOffType.Ordinary**, oppfører denne funksjonen seg som [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-funksjonen og [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X + +-funksjonen.

## <a name="remarks"></a>Kommentarer

Hvis du vil avrunde en numerisk verdi til et angitt antall desimaler, bruker du [ROUND](er-functions-mathematical-round.md)-funksjonen.

## <a name="example"></a>Eksempel

Hvis **model.RoundOff**-parameteren er satt til **RoundOffType.Ordinary**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35. 

Hvis **model.RoundOff**-parameteren er satt til **RoundOffType.RoundDown**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35. 

Hvis **model.RoundOff**-parameteren er satt til **RoundOffType.RoundUp**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)

[Matematiske funksjoner](er-functions-category-mathematical.md)
