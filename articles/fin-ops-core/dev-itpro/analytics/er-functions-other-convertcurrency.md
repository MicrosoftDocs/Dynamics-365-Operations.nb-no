---
title: CONVERTCURRENCY ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CONVERTCURRENCY.
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
ms.openlocfilehash: dc71ccedcdfc8a3dc9d7e087d29467bd3bbe72c3c5588872dbeaf3aa1dd35d2b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738606"
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