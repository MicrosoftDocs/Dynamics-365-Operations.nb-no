---
title: CONVERTCURRENCY ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen CONVERTCURRENCY.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: ac9a1cbb1c0a4b381a4e268f563c6ab0dd9c8053
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275520"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY ER-funksjonen

[!include [banner](../includes/banner.md)]

`CONVERTCURRENCY`-funksjonen returnerer en *reell* verdi som representerer resultatet av å konvertere det angitte pengebeløpet fra den angitte kildevalutaen til den angitte målvalutaen ved å bruke innstillingene for det aktuelle firmaet på den angitte datoen.

## <a name="syntax"></a>Syntaks

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumenter

`amount`: *Heltall* eller *Reell*

En numerisk verdi som representerer pengebeløpet som må konverteres.

`source currency`: *Streng*

Koden for kildevalutaen.

`target currency`: *Streng*

Koden for målvalutaen.

`date`: *Dato*

En *dato*-verdi som representerer datoen som brukes til å bestemme valutakursen for konverteringen.

`company`: *Streng*

En *streng*-verdi som representerer koden til et selskap som leverer innstillingene som brukes for konverteringen.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="example"></a>Eksempel

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returnerer tilsvarende én euro i amerikanske dollar på gjeldende øktdato, basert på innstillingene for **DEMF**-firmaet.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
