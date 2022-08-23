---
title: LIST ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen LIST
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 7a5f27baa248ec84c75725cf32a1f482841424c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277640"
---
# <a name="list-er-function"></a>LIST ER-funksjon

[!include [banner](../includes/banner.md)]

`LIST`-funksjonen returnerer en *Postliste*-verdi som består av en ny postliste som er opprettet fra de angitte argumentene.

## <a name="syntax"></a>Syntaks

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumenter

`record 1`: *Container (post)*

En referanse til en datakilde for *Post*-datatypen. Dette argumentet er obligatorisk.

`record N`: *Container (post)*

En referanse til en datakilde for *Post*-datatypen. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Strukturen i listen som opprettes, inneholder bare feltene som vises i strukturen for hver post som nevnes i argumentene.

## <a name="example"></a>Eksempel

Du angir datakilde **Post 1** av *Container*-typen. Denne datakilden inneholder følgende nestede felt av typen *Beregnet felt*:

- **Kode:** Dette feltet inneholder et uttrykk som returnerer en verdi av *streng*-typen.
- **Beløp:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Reell*-typen.

Du angir deretter datakilde **Post 2** av *Container*-typen. Denne datakilden inneholder følgende nestede felt av typen *Beregnet felt*:

- **Beløp:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Reell*-typen.
- **IsValid:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Boolsk*-typen.

I dette tilfellet returnerer uttrykket `LIST('Record 1', 'Record 2')` en ny liste som inneholder to poster. Strukturen i denne listen består av et enkelt **Beløp**-felt av *Reell*-typen, fordi dette feltet er det eneste feltet som vises i alle argumentene til den kalte funksjonen.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
