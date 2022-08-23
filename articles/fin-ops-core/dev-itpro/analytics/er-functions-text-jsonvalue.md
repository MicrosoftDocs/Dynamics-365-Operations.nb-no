---
title: JSONVALUE ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen JSONVALUE.
author: kfend
ms.date: 10/25/2021
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
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267971"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER-funksjonen

[!include [banner](../includes/banner.md)]

`JSONVALUE`-funksjonen analyserer data i JavaScript Object Notation (JSON)-format som brukes av den angitte banen, og henter en skalarverdi som har den angitte IDen. Den returnerer deretter den utpakkede skalerbare verdien som en *streng*-verdi.

## <a name="syntax"></a>Syntaks

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen som inneholder JSON-data.

`path`: *Streng*

Identifikatoren for en skalerbar verdi for JSON-data. Bruk en skråstrek (/) for å skille navnene på relaterte JSON-noder. Bruk parentesnotasjon (\[\]) for å angi indeksen for en bestemt verdi i en JSON-matrise. Legg merke til at nullbasert nummerering brukes for denne indeksen.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example-1"></a>Eksempel 1

Datakilden **JsonField** inneholder følgende data i JSON-format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. I dette tilfellet returnerer uttrykket `JSONVALUE (JsonField, "BuildNumber")` følgende verdi av *streng*-datatypen: **"7.3.1234.1"**.

## <a name="example-2"></a>Eksempel 2

**JsonField**-datakilden for typen *Beregnet felt* inneholder følgende uttrykk: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Dette uttrykket konfigurert til å returnere en [*Streng*](er-formula-supported-data-types-primitive.md#string)-verdi som representerer følgende data i JSON-format.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

I dette tilfellet returnerer uttrykket `JSONVALUE(json, "workers/[1]/emails/[0]")` følgende verdi av *streng*-datatypen: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
