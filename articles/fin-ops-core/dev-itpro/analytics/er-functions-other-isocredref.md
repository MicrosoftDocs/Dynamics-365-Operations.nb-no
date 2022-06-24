---
title: ISOCREDREF ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen ISOCREDREF.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: dcbd53ec1939e6fb4bcd829bad01b353e823795a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896770"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]