---
title: ROUNDUP ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDUP.
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917057"
---
# <a name="ROUNDUP">ROUNDUP ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`ROUNDUP`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet opp til angitt antall desimaler.

## <a name="syntax"></a>Syntaks

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenter

`number`: *Reell*

En numerisk verdi som må avrundes opp.

`decimals`: *Heltall*

En numerisk verdi som representerer antall desimaler.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid opp det angitte tallet (bort fra null).

## <a name="example-1"></a>Eksempel 1

`ROUNDUP (1200.763, 2)` avrunder opp til to desimalplasser og returnerer **1200.77**.

## <a name="example-2"></a>Eksempel 2

`ROUNDUP (1200.767, -3)` avrunder opp til nærmeste multiplum av 1 000, og returnerer **2000**.

## <a name="additional-resources"></a>Tilleggsressurser

[Matematiske funksjoner](er-functions-category-mathematical.md)
