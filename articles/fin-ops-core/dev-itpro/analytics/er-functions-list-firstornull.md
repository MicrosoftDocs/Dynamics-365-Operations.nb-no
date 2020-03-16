---
title: FIRSTORNULL ER-funksjon
description: Dette emnet forklarer hvordan du bruker ER-funksjonen FIRSTORNULL.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 86c8a0ae21ffeb6268efbbd198f7c709c2ad54f6
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042119"
---
# <a name="FIRSTORNULL">FIRSTORNULL ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`FIRSTORNULL`-funksjonen returnerer den første posten i den angitte listen som en *Container (post)*-verdi, hvis denne posten ikke er tom. Hvis posten er tom, returnerer denne funksjonen en nullverdi for *Container (post)*.

## <a name="syntax"></a>Syntaks

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example"></a>Eksempel

Uttrykket `FIRSTORNULL(SPLIT("",1)).Value` returnerer en tom streng (**""**).

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
