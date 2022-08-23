---
title: CASE ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen CASE
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 702648e14abe980d246b92b0fe512bba07717e45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274867"
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
