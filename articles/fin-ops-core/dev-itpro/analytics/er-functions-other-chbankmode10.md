---
title: CH_BANK_MOD_10-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen CH_BANK_MOD_10
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
ms.openlocfilehash: f658228e0c181bab9e07237adc330dbcb13c95c6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288116"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10-funksjon

[!include [banner](../includes/banner.md)]

`CH_BANK_MOD_10`-funksjonen returnerer en *streng*-verdi som representerer en kreditorreferanse som et MOD10-uttrykk, basert på sifrene i det angitte fakturanummeret.

## <a name="syntax"></a>Syntaks

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
