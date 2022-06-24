---
title: FA_BALANCE ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen FA_BALANCE.
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
ms.openlocfilehash: c3dd44f0d5ff143189b2c55c4df80847c2161231
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902690"
---
# <a name="fa_balance-er-function"></a>FA_BALANCE ER-funksjonen

[!include [banner](../includes/banner.md)]

`FA_BALANCE`-funksjonen returnerer en *Container (post)*-verdi som består av data for anleggsmiddelsaldoen for den angitte anleggsmiddelvaren, verdimodellkoden, rapporteringsåret og rapporteringsdatoen.

## <a name="syntax"></a>Syntaks

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumenter

`fixed asset code`: *Streng*

En *streng*-verdi som representerer koden for en anleggsmiddelvare som saldoen beregnes for.

`value model code`: *Streng*

En *streng*-verdi som representerer koden for en verdimodell som saldoen beregnes for.

`reporting year`: *Opplistingsverdi*

En opplistingsverdi for **AssetYear**-programmet som definerer en periode for saldoberegningen.

`reporting date`: *Dato*

En *dato*-verdi som definerer en dato for saldoberegningen.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example"></a>Eksempel

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returnerer den klargjorte databeholderen for saldoer for anleggsmidlet **COMP-000001** som har verdimodellen **Gjeldende** på den gjeldende datoen for programøkten.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]