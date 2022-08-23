---
title: WHERE ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen WHERE.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b3f8b01bffd0c530e5095531fc184c960744e751
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273166"
---
# <a name="where-er-function"></a>WHERE ER-funksjonen

[!include [banner](../includes/banner.md)]

`WHERE`-funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er filtrert i henhold til den angitte betingelsen.

## <a name="syntax"></a>Syntaks

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`condition`: *Boolsk*

Et gyldig betingelsesuttrykk som brukes til å filtrere poster i den angitte listen.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen er ulik [FILTER](er-functions-list-filter.md)-funksjonen fordi den angitte betingelsen brukes på en ER-datakilde av typen *Postposte* som finnes i minnet.

Hvis argumentene som er konfigurert for denne funksjonen (`list` og `condition`), tillater at denne forespørselen skal oversettes til det direkte SQL-kallet, utløses en varselmelding ved utformingstid. Denne meldingen informerer brukeren om at ytelsen kan forbedres hvis [FILTER](er-functions-list-filter.md)-funksjonen brukes i stedet for `WHERE`.

## <a name="example-1"></a>Eksempel 1

Hvis **Leverandør** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `WHERE (Vendors, Vendors.VendGroup = "40")` en liste over bare leverandører som tilhører leverandørgruppe 40.

## <a name="example-2"></a>Eksempel 2

Hvis du angir datakilden **DS** for typen *Beregnet felt*, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, returnerer uttrykket `WHERE( DS, DS.Value = "B")` en liste med bare én post som inneholder teksten **"B"** i **Verdi**-feltet.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
