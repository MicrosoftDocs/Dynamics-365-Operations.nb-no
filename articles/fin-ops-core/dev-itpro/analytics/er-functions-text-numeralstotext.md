---
title: NUMERALSTOTEXT ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen NUMERALSTOTEXT.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 172693583699edfad7deeb16f8fc081abb6119d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287996"
---
# <a name="numeralstotext-er-function"></a>NUMERALSTOTEXT ER-funksjonen

[!include [banner](../includes/banner.md)]

`NUMERALSTOTEXT`-funksjonen returnerer det angitte tallet som en *Streng*-verdi etter at det er skrevet ut (det vil si konvertert til tekststrenger) på det angitte språket.

## <a name="syntax"></a>Syntaks

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltall* eller *Reell*

En numerisk verdi som angir nummeret som må staves.

`language`: *Streng*

En *streng*-verdi som representerer språkkoden.

`currency`: *Streng*

En *streng*-verdi som representerer valutakoden.

`print currency name flag`: *Boolsk*

En *boolsk* verdi som angir om et valutanavn må legges til den stavede teksten.

`decimal points`: *Heltall*

En *Heltall*-verdi som angir antall desimaler som den stavede teksten skal ha.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Språkkoden er valgfri. Hvis den er definert som en tom streng, brukes språkkoden for kjørekontekst. Standard språkkode er **EN-US**. Språkkoden for konteksten som kjører, er definert i en **Mappe** eller **Fil**-element i formatet elektronisk rapportering (ER) som kjører.

Valutakoden er valgfri. Hvis den er definert som en tom streng, brukes firmakoden for kjørekontekst.

> [!NOTE] 
> Argumentene `print currency name flag` og `decimal points` analyseres bare for følgende språkkoder: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** og **RU**. I tillegg analyseres `print currency name flag`-argumentet bare for firmaer der land- eller områdekonteksten støtter navn for valutanedgang.

## <a name="example-1"></a>Eksempel 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returnerer **"1234 og 56"**.

## <a name="example-2"></a>Eksempel 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` returnerer **"Sto dwadzieścia"**. 

## <a name="example-3"></a>Eksempel 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returnerer **"Сто двадцать евро 21 евроцент"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
