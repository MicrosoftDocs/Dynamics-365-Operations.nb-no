---
title: EMPTYLIST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen EMPTYLIST.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fb991eb9ee08aeb418313eb782dbde7fa22b763
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042188"
---
# <a name="EMPTYLIST">EMPTYLIST ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`EMPTYLIST`-funksjonen returnerer en tom  *Postliste*-verdi ved hjelp av den angitte listen som en kilde for listestrukturen.

## <a name="syntax"></a>Syntaks

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="example"></a>Eksempel

`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny, tom liste som har samme struktur som listen som returneres av `SPLIT`- funksjonen som brukes.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
