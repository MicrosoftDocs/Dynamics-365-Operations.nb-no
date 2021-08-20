---
title: DATEVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATEVALUE.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 7c2db02e95c0e744c863381cff779b92679e7a396d7edb7bf90d3bffc0229619
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747599"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER-funksjonen

[!include [banner](../includes/banner.md)]

`DATEVALUE`-funksjonen returnerer en *dato*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en datoverdi. Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Tekst som representerer verdien som skal formateres.

`format`: *Streng*

Formatet til den gitte teksten.

`culture`: *Streng*

Kulturen som brukes til formatering av den gitte teksten.

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