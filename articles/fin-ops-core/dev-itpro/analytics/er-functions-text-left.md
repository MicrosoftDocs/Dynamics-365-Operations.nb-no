---
title: LEFT ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen LEFT
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 51842c56053f9de8ea7f65bcda71d606f42f8bf1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852640"
---
# <a name="left-er-function"></a>LEFT ER-funksjon

[!include [banner](../includes/banner.md)]

`LEFT`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra starten av den angitte strengen.

## <a name="syntax"></a>Syntaks

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *streng*-verdi som representerer den opprinnelige teksten.

`number`: *Heltall*

Antall tegn som må returneres fra begynnelsen av den opprinnelige teksten.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

`LEFT ("Sample", 3)` returnerer **"Sam"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]