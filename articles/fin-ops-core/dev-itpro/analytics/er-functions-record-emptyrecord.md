---
title: EMPTYRECORD ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen EMPTYRECORD.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d50b31fcbbb99050fca46b0a5ce10cc3fd243691
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684817"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER-funksjonen

[!include [banner](../includes/banner.md)]

`EMPTYRECORD`-funksjonen returnerer en nullverdi for *Container (post)*-verdi som har samme struktur som den angitte postlisten eller posten.

## <a name="syntax"></a>Syntaks

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste* eller *Container (post)*

Den gyldige banen til en datakilde for typen *Postliste* eller *Container (record)*.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="usage-notes"></a>Bruksnotater

> [!NOTE] 
> En null-post er en post der alle felt har en tom verdi. En tom verdi er **0** (null) for tall, en tom streng for strenger og så videre.

## <a name="example"></a>Eksempel

`EMPTYRECORD (SPLIT ("abc", 1))` returnerer en ny, tom post som har samme struktur som listen som returneres av `SPLIT`- funksjonen. Hvis du vil ha mer informasjon, kan du se [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Registreringsfunksjoner](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]