---
title: DATEFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATEFORMAT.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 1b3a0a2608328b233004034f7ab2ccfa833c17e3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890916"
---
# <a name="dateformat-er-function"></a>DATEFORMAT ER-funksjonen

[!include [banner](../includes/banner.md)]

`DATEFORMAT`-funksjonen returnerer en *Streng*-verdi som viser en gitt datoverdi som tekst i angitt format og i en valgfri angitt [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumenter

`date`: *Dato*

En datoverdi som representerer datoen som skal formateres.

`format`: *Streng*

Formatet til utdatastrengen.

> [!NOTE]
> Det skilles mellom små og store bokstaver i formatstrengen når du bruker et standardformat eller et egendefinert format. Den [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) formatangivelsen «d» returnerer for eksempel datoen ved hjelp av det korte datomønsteret, mens den standard formatangivelsen «D» returnerer ved hjelp av mønsteret med lang dato. Den [egendefinerte](/dotnet/standard/base-types/custom-date-and-time-format-strings) formatangivelsen «M» returnerer måneden fra 1 til og med 12, mens den egendefinerte formatangivelsen «m» returnerer minuttet fra 0 til og med 59.

`culture`: *Streng*

Kulturen som skal brukes til formatering.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende strengverdien.

## <a name="usage-notes"></a>Bruksnotater

Hvis kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallekonteksten. Hvis `DATEFORMAT`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur. Standardverdi for `culture` er **EN-US**.

## <a name="example-1"></a>Eksempel 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer gjeldende dato for programserveren, 24. desember 2015, som strengen **"24-12-2015"**, basert på det angitte egendefinerte formatet.

## <a name="example-2"></a>Eksempel 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer gjeldende programøktdato, 24. desember 2015, som strengen **"24-12-2015"**, basert på den valgte tyske kulturen og det angitte formatet.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]