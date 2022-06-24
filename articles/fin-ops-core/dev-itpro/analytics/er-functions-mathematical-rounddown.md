---
title: ROUNDDOWN ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDDOWN.
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
ms.openlocfilehash: c651715a4a9c01f5c126ce16cd6238d86db5b144
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869351"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN ER-funksjon

[!include [banner](../includes/banner.md)]

`ROUNDDOWN`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet ned til angitt antall desimaler.

## <a name="syntax"></a>Syntaks

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenter

`number`: *Reell*

En numerisk verdi som må avrundes ned.

`decimals`: *Heltall*

En numerisk verdi som representerer antall desimaler.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid ned det angitte tallet (mot null).

## <a name="example-1"></a>Eksempel 1

`ROUNDDOWN (1200.767, 2)` avrunder ned til to desimalplasser og returnerer **1200.76**. 

## <a name="example-2"></a>Eksempel 2

`ROUNDDOWN (1700.767, -3)` avrunder ned til nærmeste multiplum av 1 000, og returnerer **1000**.

## <a name="additional-resources"></a>Tilleggsressurser

[Matematiske funksjoner](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]