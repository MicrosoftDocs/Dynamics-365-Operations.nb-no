---
title: DATETIMEVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETIMEVALUE.
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 7a9da0b9461926b1033d6a97b37d4b43a86d8dad
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485528"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE ER-funksjonen

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE`-funksjonen returnerer en *[DateTime](er-formula-supported-data-types-primitive.md#datetime)*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en dato/klokkeslett-verdi. Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenter

`text`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Tekst som representerer verdien som skal formateres.

`format`: *Streng*

Formatet til den gitte teksten. Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Streng*

Kulturen som brukes til formatering av den gitte teksten. Hvis du vil ha informasjon om de støttede språkene, kan du se [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Returverdier

*dato/klokkeslett*

Den resulterende dato/klokkeslett-verdien.

## <a name="usage-notes"></a>Bruksnotater

Når kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallkonteksten. Hvis `DATETIMEVALUE`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur. Standardverdi for `culture` er **EN-US**.

## <a name="example-1"></a>Eksempel 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returnerer **2:55:00 AM den 21. desember 2016**, basert på det spesifiserte egendefinerte formatet og standardprogrammets **EN-US**-kultur.

## <a name="example-2"></a>Eksempel 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returnerer **2:55:00 AM den 21. desember 2016**, basert på spesifisert egendefinert format og kultur.

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` vil imidlertid iverksette et unntak for å informere brukeren om at den angitte strengen ikke gjenkjennes som en gyldig dato/klokkeslett-verdi for den angitte kulturen.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
