---
title: NOW ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NOW
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
ms.openlocfilehash: e8c411e1ce9656ffa35986f1ceef712c9def1e6b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743525"
---
# <a name="now-er-function"></a>NOW ER-funksjon

[!include [banner](../includes/banner.md)]

`NOW`-funksjonen returnerer en *DateTime*-verdi som representerer gjeldende dato og klokkeslett for programserveren.

## <a name="syntax"></a>Syntaks

```vb
NOW ()
```

## <a name="return-values"></a>Returverdier

*DateTime*

Den resulterende dato/klokkeslett-verdien.

## <a name="example"></a>Eksempel

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returnerer gjeldende dato/klokkeslett-verdi for programserveren, 24. desember 2015, som **"24-12-2015"**, basert på det angitte egendefinerte formatet.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)
