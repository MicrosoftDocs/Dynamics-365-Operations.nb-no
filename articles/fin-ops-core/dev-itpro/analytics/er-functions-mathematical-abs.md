---
title: ABS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ABS
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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917103"
---
# <a name="ABS">ABS ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`ABS`-funksjonen returnerer den absolutte (modulus) verdien til det angitte nummeret som en *reell* verdi. Altså returnes tallet uten fortegn.

## <a name="syntax"></a>Syntaks

```
ABS (number)
```

## <a name="arguments"></a>Argumenter

`number`: *Reell*

En numerisk verdi du vil bruke modulus til.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="example"></a>Eksempel

`ABS (-1)` returnerer **1**.

## <a name="additional-resources"></a>Tilleggsressurser

[Matematiske funksjoner](er-functions-category-mathematical.md)
