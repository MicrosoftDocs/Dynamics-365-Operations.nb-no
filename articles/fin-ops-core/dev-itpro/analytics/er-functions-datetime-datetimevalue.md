---
title: DATETIMEVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETIMEVALUE.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: de601ad08b85797a4241ef74ecb3eba37eda37ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917540"
---
# <a name="DATETIMEVALUE">DATETIMEVALUE ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE`-funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en dato/klokkeslett-verdi. Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaks 1

```
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaks 2

```
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Tekst som representerer verdien som skal formateres.

`format`: *Streng*

Formatet til den gitte teksten.

`culture`: *Streng*

Kulturen som brukes til formatering av den gitte teksten.

## <a name="return-values"></a>Returverdier

*DateTime*

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
