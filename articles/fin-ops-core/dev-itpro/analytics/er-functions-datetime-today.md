---
title: TODAY ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 94ef15d1971287e8bf13944bc8f693b567950031
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411443"
---
# <a name=""></a><a name="TODAY">TODAY ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`TODAY`-funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programserveren.

## <a name="syntax"></a>Syntaks

```xpp
TODAY ()
```

## <a name="return-values"></a>Returverdier

*Dato*

Den resulterende datoverdien.

## <a name="example"></a>Eksempel

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer gjeldende dato for programserveren, 24. desember 2015, som strengen **"24-12-2015"**, basert på det angitte egendefinerte formatet.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)
