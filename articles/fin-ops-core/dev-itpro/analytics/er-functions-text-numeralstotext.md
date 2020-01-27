---
title: NUMERALSTOTEXT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMERALSTOTEXT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 459123a66dae7a3d87a22b042e1be6585959ac15
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915631"
---
# <a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`NUMERALSTOTEXT`-funksjonen returnerer det angitte tallet som en *Streng*-verdi etter at det er skrevet ut (det vil si konvertert til tekststrenger) på det angitte språket.

## <a name="syntax"></a>Syntaks

```
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
