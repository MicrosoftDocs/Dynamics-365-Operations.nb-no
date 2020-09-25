---
title: GETCURRENTCOMPANY ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GETCURRENTCOMPANY.
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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744133"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER-funksjonen

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY`-funksjonen returnerer en *streng*-verdi som representerer koden for den juridiske enheten (firma) som en bruker er logget på nå.

## <a name="syntax"></a>Syntaks

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruker som er logget på firmaet **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)
