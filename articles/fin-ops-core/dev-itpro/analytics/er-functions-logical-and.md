---
title: AND ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen AND
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ccb7feb1d0f6836e7e8001870034900f6a1f598
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687080"
---
# <a name="and-er-function"></a>AND ER-funksjon

[!include [banner](../includes/banner.md)]

`AND`-funksjonen returnerer en *boolsk* verdi av **SANN** hvis alle de angitte betingelsene er sanne. Hvis ikke returneres den *boolske* verdien **USANN**.

## <a name="syntax"></a>Syntaks

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenter

`condition 1`: *Boolsk*

Et gyldig betingelsesuttrykk som må testes. Dette argumentet er obligatorisk.

`condition N`: *Boolsk*

Et gyldig betingelsesuttrykk som må testes. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="usage-notes"></a>Bruksnotater

I argumentene til logiske funksjoner kan du bruke datakildereferanser, tall- og tekstverdier, boolske verdier, sammenligningsoperatorer og andre funksjoner for elektronisk rapportering (ER). Alle argumentene må imidlertid evalueres til en *boolsk* verdi som er **SANN** eller **USANN**.

## <a name="example"></a>Eksempel

`AND (1=1, "a"="a")` returnerer **SANN**.

`AND (1=2, "a"="a")` returnerer **USANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)
