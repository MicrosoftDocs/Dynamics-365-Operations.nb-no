---
title: INDEX ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INDEX.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: e68f1690d6f852b0db560ef67a36fbde9e099715942a4b8a6e486d759af46682
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755785"
---
# <a name="index-er-function"></a>INDEX ER-funksjon

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

> [!NOTE]
> Fordi enbasert nummerering brukes for denne funksjonen, kan du angi verdien **1** for å returnere den første posten i den angitte listen.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="example-1"></a>Eksempel 1

Hvis du angir datakilden **DS** for typen *Beregnet felt*, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, returnerer uttrykket `DS.Value` tekstverdien **B** for den andre posten i denne postlisten. Uttrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstverdien **"B"**.

## <a name="example-2"></a>Eksempel 2

Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, genererer uttrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` et unntak under kjøring.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
