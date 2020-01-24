---
title: RIGHT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen RIGHT.
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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916735"
---
# <a name="RIGHT">RIGHT ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`RIGHT`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra slutten av den angitte strengen.

## <a name="syntax"></a>Syntaks

```
RIGHT (text, number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *streng*-verdi som representerer den opprinnelige teksten.

`number`: *Heltall*

Antall tegn som må returneres fra slutten av den opprinnelige teksten.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`RIGHT ("Sample", 3)` returnerer **"ple"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)
