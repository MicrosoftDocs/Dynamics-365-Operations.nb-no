---
title: CASE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CASE
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 97f5e821a635d5d31092a7b27f7ae3c2e603462186449bab5856955371a7f613
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756411"
---
# <a name="case-er-function"></a>CASE ER-funksjon

[!include [banner](../includes/banner.md)]

`CASE`-funksjonen evaluerer verdien til det angitte uttrykket mot de angitte alternative valgene, og returnerer resultatet av det første alternativet som tilsvarer verdien til det angitte uttrykket. Hvis ikke returnerer den et valgfritt standard resultat hvis et standard resultat er angitt som det siste argumentet i den kalte funksjonen som ikke innledes av et alternativ. Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene.

## <a name="syntax"></a>Syntaks

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumenter

`expression`: *Primitiv datatype* (boolsk, numerisk eller tekst)

Et gyldig uttrykk som returnerer en verdi av den primitive datatypen.

`option 1`: *Primitiv datatype* (boolsk, numerisk eller tekst)

Et gyldig uttrykk som returnerer en verdi av den samme primitive datatypen som `expression`-argumentet for den kalte funksjonen. Dette argumentet er obligatorisk.

`result 1`: *Hvilken som helst av datatypene som støttes*

Det returnerte resultatet som svarer til det forrige alternativet. Dette argumentet er obligatorisk.

`option N`: *Primitiv datatype* (boolsk, numerisk eller tekst)

Et gyldig uttrykk som returnerer en verdi av den samme primitive datatypen som `expression`-argumentet for den kalte funksjonen. Dette argumentet er valgfritt.

`result N`: *Hvilken som helst av datatypene som støttes*

Det returnerte resultatet som svarer til det forrige alternativet. Dette argumentet er valgfritt.

`default result`: *Hvilken som helst av datatypene som støttes*

Resultatet som skal returneres hvis det ikke finnes noen treff. Dette argumentet er valgfritt.

## <a name="return-values"></a>Returverdier

*Hvilken som helst av datatypene som støttes*

Resultatverdien for en hvilken som helst av de støttede datatypene.

## <a name="usage-notes"></a>Bruksnotater

Det oppstår et unntak under kjøring hvis det ikke finnes noen samsvar og et valgfritt standardresultat ikke er definert.

Alle resultater må angis ved hjelp av den samme datatypen. Et unntak er registrert ved utformingstid hvis datatypene for de konfigurerte resultatene ikke samsvarer.

Hvis den første resultatverdien og *N*-te resultatverdien er verdier for datatypen *Container (post)* eller *postliste*, har resultatet bare feltene som finnes i begge verdiene.

## <a name="example"></a>Eksempel

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returnerer strengen **"WINTER"** hvis gjeldende programøktdato er mellom oktober og desember. Ellers returneres en tom streng.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]