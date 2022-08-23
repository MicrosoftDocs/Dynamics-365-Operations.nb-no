---
title: DATEVALUE ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen DATEVALUE.
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
ms.openlocfilehash: 290a4665d3527c0f0954c46cb0a0a14677b93218
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268706"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER-funksjonen

[!include [banner](../includes/banner.md)]

`DATEVALUE`-funksjonen returnerer en *[dato](er-formula-supported-data-types-primitive.md#date)*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en datoverdi. Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenter

`text`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Tekst som representerer verdien som skal formateres.

`format`: *Streng*

Formatet til den gitte teksten. Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Streng*

Kulturen som brukes til formatering av den gitte teksten. Hvis du vil ha informasjon om de støttede språkene, kan du se [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Returverdier

*Dato*

Den resulterende datoverdien.

## <a name="usage-notes"></a>Bruksnotater

Når kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallkonteksten. Hvis `DATEVALUE`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur. Standardverdi for `culture` er **EN-US**.

## <a name="example-1"></a>Eksempel 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returnerer datoverdien **21. desember 2016**, basert på det spesifiserte egendefinerte formatet og standardprogrammets **EN-US**-kultur.

## <a name="example-2"></a>Eksempel 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returnerer datoverdien **21. januar 2016**, basert på angitt egendefinert format og kultur.

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` vil imidlertid iverksette et unntak for å informere brukeren om at den angitte strengen ikke gjenkjennes som en gyldig dato for den angitte kulturen.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
