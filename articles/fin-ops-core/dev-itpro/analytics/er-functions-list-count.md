---
title: COUNT ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen COUNT.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 64c8be659b564d612f3127d46e54535c73ae21ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287256"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
