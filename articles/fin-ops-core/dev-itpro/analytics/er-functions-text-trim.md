---
title: TRIM ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen TRIM
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273106"
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
