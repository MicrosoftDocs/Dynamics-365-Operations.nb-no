---
title: FA_SUM ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FA_SUM
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
ms.openlocfilehash: 32eb07689598a3b6c852f272b480106670b88cd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916988"
---
# <a name="FA_SUM">FA_SUM ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`FA_SUM`-funksjonen returnerer en *Container (post)*-verdi som består av data for anleggsmiddelbeløpene for den angitte anleggsmiddelvaren, verdimodellkoden, rapporteringsåret og datoperioden.

## <a name="syntax"></a>Syntaks

```
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumenter

`fixed asset code`: *Streng*

En *streng*-verdi som representerer koden for en anleggsmiddelvare som saldoen beregnes for.

`value model code`: *Streng*

En *streng*-verdi som representerer koden for en verdimodell som saldoen beregnes for.

`start date`: *Dato*

En *dato*-verdi som representerer startdatoen for en periode som anleggsmiddelbeløpene beregnes for.

`end date`: *Dato*

En *dato*-verdi som representerer sluttdatoen for en periode som anleggsmiddelbeløpene beregnes for.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example"></a>Eksempel

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returnerer databeholderen for anleggsmiddel **COMP-000001** som er klargjort for den **gjeldende**-verdimodellen, og for en periode fra **Dato1** til **Dato2**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)
