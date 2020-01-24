---
title: ORDERBY ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ORDERBY.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916206"
---
# <a name="ORDERBY">ORDERBY ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`ORDERBY`-funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er sortert i henhold til de angitte argumentene. Disse argumentene kan defineres som uttrykk.

## <a name="syntax"></a>Syntaks

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`expression 1`: *Felt*

Den gyldige banen til et felt i datakilden som `list`-argumentet for den kalte funksjonen refererer til. Det refererte feltet må være et felt av den primitive datatypen. Dette argumentet er obligatorisk.

`expression N`: *Felt*

Den gyldige banen til et felt i datakilden som `list`-argumentet for den kalte funksjonen refererer til. Det refererte feltet må være et felt av den primitive datatypen. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="example-1"></a>Eksempel 1

Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("C|B|A", "|")`, genererer uttrykket `FIRST( ORDERBY( DS, DS. Value)).Value` tekstverdien **"A"**.

## <a name="example-2"></a>Eksempel 2

Hvis **Leverandør** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `ORDERBY (Vendors, Vendors.'name()')` en liste over leverandører sortert etter navn i stigende rekkefølge.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
