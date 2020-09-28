---
title: COUNT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen COUNT.
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
ms.openlocfilehash: c48483a6677aaeb36eac57a57cec71bf54c7991d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745351"
---
# <a name="count-er-function"></a>COUNT ER-funksjon

[!include [banner](../includes/banner.md)]

`COUNT`-funksjonen returnerer en *Heltall*-verdi som representerer antall poster i den angitte listen, hvis listen ikke er tom. Hvis listen er tom, returnerer denne funksjonen **0** (null).

## <a name="syntax"></a>Syntaks

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Heltall*

Den resulterende numeriske verdien.

## <a name="example"></a>Eksempel

`COUNT (SPLIT("abcd" , 3))` returnerer **2** fordi `SPLIT`-funksjonen som brukes i dette eksemplet, oppretter en liste som består av to poster.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
