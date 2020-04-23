---
title: LISTJOIN ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249041"
---
# <a name=""></a><a name="LISTJOIN">LISTJOIN ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`LISTJOIN`-funksjonen returnerer en *Postliste*-verdi som representerer en ny sammenkoblet liste over poster som er opprettet fra de angitte argumentene.

## <a name="syntax"></a>Syntaks

```vb
LIST (list 1 [, list 2, …, list N])
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

I dette tilfellet returnerer uttrykket `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` en ny liste som inneholder to poster. Strukturen i denne listen består av et enkelt **Beløp**-felt av `Real`-typen, fordi dette feltet er det eneste feltet som vises i alle argumentene til den kalte funksjonen.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)