---
title: IF ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen IF.
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
ms.openlocfilehash: 066cffaebc415305a2481e3bf0f0a5f4e108fabc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844565"
---
# <a name="if-er-function"></a>IF ER-funksjon

[!include [banner](../includes/banner.md)]

`IF`-funksjonen returnerer den første verdien hvis den angitte betingelsen er oppfylt. Hvis ikke returneres den andre verdien som er angitt. Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene.

## <a name="syntax"></a>Syntaks

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumenter

`condition`: *Boolsk*

Et gyldig betingelsesuttrykk som må testes.

`first value`: *Hvilken som helst av datatypene som støttes*

Resultatet som returneres hvis betingelsen oppfylles.

`second value`: *Hvilken som helst av datatypene som støttes*

Resultatet som returneres hvis betingelsen ikke oppfylles.

## <a name="return-values"></a>Returverdier

*Hvilken som helst av datatypene som støttes*

Resultatverdien for en hvilken som helst av de støttede datatypene.

## <a name="usage-notes"></a>Bruksnotater

Argumentene `first value` og `second value` må angis ved hjelp av den samme datatypen. Et unntak er registrert ved utformingstid hvis datatypene for de konfigurerte verdiene ikke samsvarer.

Hvis den første og andre verdien er verdier for datatypen *Container (post)* eller *Postliste*, har resultatet bare feltene som finnes i begge verdiene.

## <a name="example"></a>Eksempel

`IF (1=2, "condition is met", "condition is not met")` returnerer strengen **"betingelsen er ikke oppfylt"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]