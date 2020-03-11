---
title: INDEX ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INDEX.
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
ms.openlocfilehash: 45e95751e3adfe6aa208daaba774a349216e1f1f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042073"
---
# <a name="INDEX">INDEX ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`INDEX`-funksjonen returnerer en *Container (post)*-verdi som er valgt ved hjelp av den angitte numeriske indeksen i den angitte listen. Det oppstår et unntak hvis indeksen er utenfor området til postene i den angitte listen.

## <a name="syntax"></a>Syntaks

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`index`: *Heltall*

En numerisk indeks som angir plasseringen til den ønskede posten i den angitte listen.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example-1"></a>Eksempel 1

Hvis du angir datakilden **DS** for typen *Beregnet felt*, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, returnerer uttrykket `DS.Value` tekstverdien **B** for den andre posten i denne postlisten. Uttrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstverdien **"B"**.

## <a name="example-2"></a>Eksempel 2

Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, genererer uttrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` et unntak under kjøring.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
