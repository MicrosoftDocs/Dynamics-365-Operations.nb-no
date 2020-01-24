---
title: NOT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NOT
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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916045"
---
# <a name="NOT">NOT ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`NOT`-funksjonen returnerer den omvendte logiske verdien til den angitte betingelsen som en *boolsk* verdi.

## <a name="syntax"></a>Syntaks

```
NOT (condition)
```

## <a name="arguments"></a>Argumenter

`condition`: *Boolsk*

Et gyldig betingelsesuttrykk som må tilbakeføres.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="example"></a>Eksempel

`NOT (TRUE)` returnerer **USANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)
