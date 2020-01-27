---
title: MID ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen MID
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915608"
---
# <a name="MID">MID ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`MID`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra den angitte strengen, og begynner fra den angitte posisjonen.

## <a name="syntax"></a>Syntaks

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *streng*-verdi som angir teksten det skal returneres tegn fra.

`starting position`: *Heltall*

En *Heltall*-verdi som angir plasseringen til det første tegnet som må returneres fra den angitte teksten.

`number of characters`: *Heltall*

En *Heltall*-verdi som angir antall tegn som må returneres, som begynner fra den angitte startposisjonen.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Hvis verdien for `starting position`-argumentet er mindre enn 0 (null), telles tegnene som returneres, fra den første plasseringen i den angitte strengen.

Hvis verdien for `starting position`-argumentet overskrider lengden på den angitte strengen, returneres en tom streng.

## <a name="example"></a>Eksempel

`MID ("Sample", 2, 3)` returnerer **"amp"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)
