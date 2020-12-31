---
title: SESSIONTODAY ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SESSIONTODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 87e8d5498c82d7c9ca6ee0a855f139dde77d75ab
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683825"
---
# <a name="sessiontoday-er-function"></a>SESSIONTODAY ER-funksjon

[!include [banner](../includes/banner.md)]

`SESSIONTODAY`-funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programøkt.

## <a name="syntax"></a>Syntaks

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Returverdier

*Dato*

Den resulterende datoverdien.

## <a name="example"></a>Eksempel

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer gjeldende programøktdato, 24. desember 2015, som strengen **"24-12-2015"**, basert på den valgte tyske kulturen og det angitte formatet.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)
