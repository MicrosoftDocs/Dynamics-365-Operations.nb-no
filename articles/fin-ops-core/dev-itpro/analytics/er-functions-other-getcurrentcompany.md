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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915999"
---
# <a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY`-funksjonen returnerer en *streng*-verdi som representerer koden for den juridiske enheten (firma) som en bruker er logget på nå.

## <a name="syntax"></a>Syntaks

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruker som er logget på firmaet **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)
