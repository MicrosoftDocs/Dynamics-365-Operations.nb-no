---
title: TABLENAME2ID ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen TABLENAME2ID
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: b5deea69d5c43be599ccf02c0344ba8d662a6e0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886856"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER-funksjon

[!include [banner](../includes/banner.md)]

`TABLENAME2ID`-funksjonen returnerer en numerisk representasjon av tabell-IDen for det angitte tabellnavnet som en  *heltall*-verdi.

## <a name="syntax"></a>Syntaks

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstverdi som representerer et gyldig tabellnavn.

## <a name="return-values"></a>Returverdier

*Heltall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Utføring av denne funksjonen kan ha forskjellige resultater i forskjellige forekomster av Microsoft Dynamics 365 Finance, selv om det samme firmanavnet brukes.

## <a name="example"></a>Eksempel

`TABLENAME2ID ("Intrastat")` returnerer **1510**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]