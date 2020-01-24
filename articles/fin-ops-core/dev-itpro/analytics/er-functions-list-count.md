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
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916252"
---
# <a name="COUNT">COUNT ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`COUNT`-funksjonen returnerer en *Heltall*-verdi som representerer antall poster i den angitte listen, hvis listen ikke er tom. Hvis listen er tom, returnerer denne funksjonen **0** (null).

## <a name="syntax"></a>Syntaks

```
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
