---
title: LISTJOIN ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen LISTJOIN.
author: NickSelin
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba7b4b52f5403232d3a32a6b2907c20de29c80d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877132"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER-funksjonen

[!include [banner](../includes/banner.md)]

`LISTJOIN`-funksjonen returnerer en *Postliste*-verdi som representerer en ny sammenkoblet liste over poster som er opprettet fra de angitte argumentene.

## <a name="syntax"></a>Syntaks

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumenter

`list 1`: *Postliste*

En referanse til en datakilde for *Postliste*-datatypen. Dette argumentet er obligatorisk.

`list N`: *Postliste*

En referanse til en datakilde for *Postliste*-datatypen. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Strukturen i listen som opprettes, inneholder bare feltene som vises i strukturen for hver postliste som det er referert til i argumentene.

## <a name="example"></a>Eksempel

Du angir datakilden **Post 1** av `Container`-typen. Denne datakilden inneholder følgende nestede felt av typen `Calculated field`:

- **Kode** Dette feltet inneholder et uttrykk som returnerer en verdi av `String`-typen.
- **Beløp** Dette feltet inneholder et uttrykk som returnerer en verdi av `Real`-typen.

Du angir deretter datakilden **Post 2** av `Container`-typen. Denne datakilden inneholder følgende nestede felt av typen `Calculated field`:

- **Beløp** Dette feltet inneholder et uttrykk som returnerer en verdi av `Real`-typen.
- **IsValid** Dette feltet inneholder et uttrykk som returnerer en verdi av `Boolean`-typen.

![Siden ER-utforming av modelltilordning.](./media/er-functions-list-listjoin-image1.gif)

I dette tilfellet returnerer uttrykket `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` en ny liste som inneholder to poster.

![Utformingsside for ER-modelltilordning med to poster.](./media/er-functions-list-listjoin-image2.gif)

Strukturen i denne listen består av et enkelt **Beløp**-felt av `Real`-typen, fordi dette feltet er det eneste feltet som vises i alle argumentene til den kalte funksjonen.

![Beløpsfelt på siden ER-utforming av modelltilordning.](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)

[Feilsøke datakilder for et utført ER-format for å analysere dataflyt og transformasjon](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
