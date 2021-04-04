---
title: REPLACE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen REPLACE.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
ms.topic: article
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
ms.openlocfilehash: c9f1abe397e05f816fcf226df76362d872819f57
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570270"
---
# <a name="replace-er-function"></a>REPLACE ER-funksjon

[!include [banner](../includes/banner.md)]

`REPLACE`-funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at hele eller deler av den er erstattet med en annen streng.

## <a name="syntax"></a>Syntaks

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen.

`pattern`: *Streng*

Hvis `regular expression flag`-argumentet er **USANN**, inneholder dette argumentet teksten som må erstattes.

Hvis `regular expression flag`-argumentet er **SANN**, inneholder dette argumentet et regulært uttrykk som definerer både et søkemønster og erstatningsteksten.

`replacement`: *Streng*

Hvis `regular expression flag`-argumentet er **USANN**, inneholder dette argumentet teksten som skal brukes som erstatning.

Hvis `regular expression flag`-argumentet er **SANN**, brukes ikke dette argumentet.

`regular expression flag`: *Boolsk*

En *boolsk* verdi som angir om et regulært uttrykk brukes til å utføre erstatningen.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Hvis `regular expression flag`-argumentet er **SANN**, returnerer denne funksjonen den angitte strengen etter at den er endret ved å bruke det vanlige uttrykket som er angitt av `pattern`-argumentet. Det vanlige uttrykket brukes til å søke etter tegn som skal erstattes.

Hvis argumentet `regular expression flag` er **USANN**, returnerer denne funksjonen den angitte strengen etter settet med tegn som er definert i `pattern` er erstattet av tegnene i argumentet `replacement`. 

## <a name="example-1"></a>Eksempel 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` bruker et vanlig uttrykk som fjerner alle ikke-numeriske symboler, og returnerer **"19234564971"**. 

## <a name="example-2"></a>Eksempel 2

`REPLACE ("abcdef", "cd", "GH", false)` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]