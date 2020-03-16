---
title: REVERSE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen REVERSE.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a6134ae7eb1a8044cf906f2a8d02eb153522a6cf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041935"
---
# <a name="REVERSE">REVERSE ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`REVERSE`-funksjonen returnerer den angitte listen som en *postliste*-verdi i reversert sorteringsrekkefølge.

## <a name="syntax"></a>Syntaks

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="example-1"></a>Eksempel 1

Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("C|B|A", "|")`, genererer uttrykket `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` tekstverdien **"C"**.

## <a name="example-2"></a>Eksempel 2

Hvis **Leverandør** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` en liste over leverandører sortert etter navn i synkende rekkefølge.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
