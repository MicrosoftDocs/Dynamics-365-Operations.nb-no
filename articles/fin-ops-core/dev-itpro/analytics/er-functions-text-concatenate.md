---
title: CONCATENATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CONCATENATE.
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
ms.openlocfilehash: 04c7b32e2a9578f8864570a552817ec3ce28fa43
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041187"
---
# <a name="CONCATENATE">CONCATENATE ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`CONCATENATE`-funksjonen returnerer alle de angitte tekststrengene som en *streng*-verdi etter at de er føyd sammen til én streng.

## <a name="syntax"></a>Syntaks

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumenter

`text 1`: *Streng*

En referanse til en datakilde for *Streng*-datatypen. Dette argumentet er obligatorisk.

`text N`: *Streng*

En referanse til en datakilde for *Streng*-datatypen. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.

## <a name="usage-notes"></a>Bruksnotater

Uttrykket `"abc" & "def"` returnerer også **"abcdef"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)
