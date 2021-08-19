---
title: FIRST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FIRST.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f108676c2ff8801fddc0a72be3f75d212582efe6b5d96f7515354739eb446532
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740996"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]