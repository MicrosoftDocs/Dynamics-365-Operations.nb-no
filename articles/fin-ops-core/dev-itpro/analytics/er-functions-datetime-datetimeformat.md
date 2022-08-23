---
title: DATETIMEFORMAT ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen DATETIMEFORMAT.
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: e21b676046b6279826a728657fcc0d2a00a38b76
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287376"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER-funksjonen

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT`-funksjonen returnerer en *[Streng](er-formula-supported-data-types-primitive.md#string)*-verdi som viser en gitt dato/klokkeslett-verdi som tekst i angitt format og i en valgfri angitt [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Argumenter

`datetime`: *[DateTime](er-formula-supported-data-types-primitive.md#datetime)*

En dato/klokkeslett-verdi som representerer dato og klokkeslett til-formatet.

`format`: *Streng*

Formatet til utdatastrengen. Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> Det skilles mellom små og store bokstaver i formatstrengen når du bruker et standardformat eller et egendefinert format. Den [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) formatangivelsen «d» returnerer for eksempel datoen ved hjelp av det korte datomønsteret, mens den standard formatangivelsen «D» returnerer ved hjelp av mønsteret med lang dato. Den [egendefinerte](/dotnet/standard/base-types/custom-date-and-time-format-strings) formatangivelsen «M» returnerer måneden fra 1 til og med 12, mens den egendefinerte formatangivelsen «m» returnerer minuttet fra 0 til og med 59.

`culture`: *Streng*

Kulturen som skal brukes til formatering. Hvis du vil ha informasjon om de støttede språkene, kan du se [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende strengverdien.

## <a name="usage-notes"></a>Bruksnotater

Hvis kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallekonteksten. Hvis `DATETIMEFORMAT`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur. Standardverdi for `culture` er **EN-US**.

Når `DATETIMEFORMAT`-funksjonen konverterer en gitt dato/klokkeslett-verdi, vurderes innstillingen for tidssone for programbrukeren som kjører ER-formatet som funksjonen kalles i konteksten til.

## <a name="example-1"></a>Eksempel 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returnerer gjeldende dato/klokkeslett-verdi for programserveren, 24. desember 2015, som **"24-12-2015"**, basert på det angitte egendefinerte formatet.

## <a name="example-2"></a>Eksempel 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer gjeldende dato/klokkeslett-verdi for programøkt, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen og det angitte formatet.

## <a name="example-3"></a>Eksempel 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returnerer strengverdien **2019-11-12T 08:00:00.0000000-08:00** når funksjonen kalles under en prosess som ble startet av en programbruker som har tidssoneverdien **(GMT-08:00) Stillehavskysten (USA og Canada)** i delen **Innstillinger for språk og land/område**.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
