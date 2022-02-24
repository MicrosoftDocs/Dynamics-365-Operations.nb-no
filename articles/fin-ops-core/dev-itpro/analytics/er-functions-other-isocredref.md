---
title: ISOCREDREF ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ISOCREDREF.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9a75cedcf543b318df2850df3e4a60bac2dc6b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680692"
---
# <a name="isocredref-er-function"></a>ISOCREDREF ER-funksjonen

[!include [banner](../includes/banner.md)]

`ISOCREDREF`-funksjonen returnerer en *streng*-verdi som representerer en ISO-kreditorreferanse (International Organization for Standardization) basert på sifrene og de alfabetiske symbolene i det angitte fakturanummeret.

## <a name="syntax"></a>Syntaks

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumenter

`invoice number digits`: *Streng*

En tekstverdi som representerer sifrene i et fakturanummer.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

> [!NOTE] 
> `invoice number digits`-argumentet må oversettes før det sendes til denne funksjonen for å eliminere symboler fra bokstaver som ikke er ISO-kompatible.

## <a name="example"></a>Eksempel

`ISOCredRef ("VEND-200002")` returnerer **"RF23VEND-200002"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)
