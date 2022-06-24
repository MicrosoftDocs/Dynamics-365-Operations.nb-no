---
title: TRIM ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen TRIM
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: deadf89641771efa864e701af9dad57c5e62ea37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864665"
---
# <a name="trim-er-function"></a>TRIM ER-funksjon

[!include [banner](../includes/banner.md)]

`TRIM`-funksjonen returnerer den angitte tekststrengen som *Streng*-verdi etter at tegn for tabulator, vognretur, linjeskift og sideskift er erstattet med ett mellomromstegn, etter at innledende og etterfølgende mellomrom er avkortet, og etter at flere mellomrom mellom ord er fjernet.

## <a name="syntax"></a>Syntaks

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

I noen tilfeller vil du kanskje avkorte innledende og etterfølgende mellomrom, men foretrekker å beholde formateringen for den angitte teksten. Dette kan for eksempel være aktuelt når denne teksten representerer en adresse som kan angis i en tekstboks med flere linjer og inneholde formatering med linjeskift og vognretur. I dette tilfellet bruker du følgende uttrykk: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` der `text` er argumentet som refererer til den angitte tekststrengen.

## <a name="example-1"></a>Eksempel 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.

## <a name="example-2"></a>Eksempel 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` returnerer **"Eksempeltekst"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)

[REPLACE ER-funksjon](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
