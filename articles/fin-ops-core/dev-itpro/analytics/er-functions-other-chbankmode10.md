---
title: CH_BANK_MOD_10-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CH_BANK_MOD_10
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
ms.openlocfilehash: 42a345fc48b0d87b353308060903a6b5156c0e62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915884"
---
# <a name="CH_BANK_MOD_10">CH_BANK_MOD_10-funksjon</a>

[!include [banner](../includes/banner.md)]

`CH_BANK_MOD_10`-funksjonen returnerer en *streng*-verdi som representerer en kreditorreferanse som et MOD10-uttrykk, basert på sifrene i det angitte fakturanummeret.

## <a name="syntax"></a>Syntaks

```
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumenter

`invoice number digits`: *Streng*

En tekstverdi som representerer sifrene i et fakturanummer.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`CH_BANK_MOD_10 ("VEND-200002")` returnerer **3**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)
