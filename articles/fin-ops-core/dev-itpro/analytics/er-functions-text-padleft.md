---
title: PADLEFT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen PADLEFT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 28306b2e5fb1febce49ab55240c6d84ff240282a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916781"
---
# <a name="PADLEFT">PADLEFT ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`PADLEFT`-funksjonen returnerer en*Streng*-verdi med den angitte lengden der begynnelsen av den angitte strengen fylles ut med de angitte tegnene.

## <a name="syntax"></a>Syntaks

```
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *streng*-verdi som representerer den opprinnelige teksten.

`length`: *Heltall*

En *Heltall*-verdi som representerer det endelige antallet tegn i den utfylte strengen.

`padding chars`: *Streng*

Tegnene som skal brukes til utfylling.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`PADLEFT ("1234", 10, "`&nbsp;`")` returnerer tekststrengen **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)
