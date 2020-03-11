---
title: OR ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen OR
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
ms.openlocfilehash: 2a850b1cbe7224ab1a7b2bd39ac4667304781cbb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041682"
---
# <a name="OR">OR ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`OR`-funksjonen returnerer en *boolsk* verdi av **USANN** hvis alle de angitte betingelsene er usanne. Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis en angitt betingelse er sann.

## <a name="syntax"></a>Syntaks

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenter

`condition 1`: *Boolsk*

Et gyldig betingelsesuttrykk som må testes. Dette argumentet er obligatorisk.

`condition N`: *Boolsk*

Et gyldig betingelsesuttrykk som må testes. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="example"></a>Eksempel

`OR (1=2, "a"="a")` returnerer **SANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)
