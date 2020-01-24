---
title: FIRST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FIRST.
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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917356"
---
# <a name="FIRST">FIRST ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`FIRST`-funksjonen returnerer den første posten i den angitte listen som en *Container (post)*-verdi, hvis denne listen ikke er tom. Hvis listen er tom, genererer denne funksjonen et unntak.

## <a name="syntax"></a>Syntaks

```
FIRST (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example-1"></a>Eksempel 1

Uttrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstverdien **"A"**.

## <a name="example-2"></a>Eksempel 2

Uttrykket `FIRST(SPLIT("",1)).Value` genererer et unntak under kjøring.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
