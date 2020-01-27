---
title: SESSIONNOW ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SESSIONNOW.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916275"
---
# <a name="">SESSIONNOW ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`SESSIONNOW`-funksjonen returnerer en *DateTime*-verdi som representerer gjeldende dato og klokkeslett for programøkt.

## <a name="syntax"></a>Syntaks

```
SESSIONNOW ()
```

## <a name="return-values"></a>Returverdier

*DateTime*

Den resulterende dato/klokkeslett-verdien.

## <a name="example"></a>Eksempel

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer gjeldende dato/klokkeslett-verdi for programøkt, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen og det angitte formatet.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)
