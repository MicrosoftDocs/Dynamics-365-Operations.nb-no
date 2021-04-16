---
title: TRIM ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TRIM
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 93b08792a7aab7245d0443da05e0330bf8b2d56e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746055"
---
# <a name="trim-er-function"></a>TRIM ER-funksjon

[!include [banner](../includes/banner.md)]

`TRIM`-funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at innledende og etterfølgende mellomrom er avkortet, og når flere mellomrom mellom ord er fjernet.

## <a name="syntax"></a>Syntaks

```vb
TRIM (text )
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]