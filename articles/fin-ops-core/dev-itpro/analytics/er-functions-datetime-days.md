---
title: DAYS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DAYS
author: NickSelin
ms.date: 12/04/2019
ms.topic: article
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
ms.openlocfilehash: 310359a29a506d69d1f34aaa710a82b0f2ea528e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746897"
---
# <a name="days-er-function"></a>DAYS ER-funksjon

[!include [banner](../includes/banner.md)]

`DAYS`-funksjonen returnerer en *Heltall*-verdi som representerer antall dager mellom en angitt dato og en annen angitt dato.

## <a name="syntax"></a>Syntaks

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumenter

`date 1`: *Dato*

En datoverdi som representerer startdatoen for beregningen av antall dager.

`date 2`: *Dato*

En datoverdi som representerer sluttdatoen for beregningen av antall dager.

## <a name="return-values"></a>Returverdier

*Heltall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

`DAYS` returnerer en positiv verdi når den første datoen er senere enn den andre datoen, returnerer **0** (null) når den første datoen er lik den andre datoen, og returnerer en negativ verdi når den første datoen er før den andre datoen.

## <a name="example"></a>Eksempel

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returnerer **-1**.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]