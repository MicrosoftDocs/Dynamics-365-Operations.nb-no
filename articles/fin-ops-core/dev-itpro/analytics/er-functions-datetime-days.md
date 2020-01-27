---
title: DAYS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DAYS
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916298"
---
# <a name="DAYS">DAYS ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`DAYS`-funksjonen returnerer en *Heltall*-verdi som representerer antall dager mellom en angitt dato og en annen angitt dato.

## <a name="syntax"></a>Syntaks

```
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
