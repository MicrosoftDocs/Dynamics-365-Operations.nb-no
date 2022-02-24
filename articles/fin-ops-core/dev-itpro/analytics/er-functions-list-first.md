---
title: FIRST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FIRST.
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
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679420"
---
# <a name="first-er-function"></a>FIRST ER-funksjon

[!include [banner](../includes/banner.md)]

`FIRST`-funksjonen returnerer den første posten i den angitte listen som en *Container (post)*-verdi, hvis denne listen ikke er tom. Hvis listen er tom, genererer denne funksjonen et unntak.

## <a name="syntax"></a>Syntaks

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example-1"></a>Eksempel 1

Uttrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstverdien **"A"**.

## <a name="example-2"></a>Eksempel 2

Uttrykket `FIRST(SPLIT("",1)).Value` genererer et unntak under kjøring.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
