---
title: FA_BALANCE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FA_BALANCE.
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
ms.openlocfilehash: 6a969e3a484208388fd82d7a714bee27b7fe64a9
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744173"
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
