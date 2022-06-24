---
title: ADDDAYS ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen ADDDAYS.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 7cf2031c042ae93512cc85afe6a1b51558f6c8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858748"
---
# <a name="adddays-er-function"></a>ADDDAYS ER-funksjonen

[!include [banner](../includes/banner.md)]

`ADDDAYS`-funksjonen returnerer en *DateTime*-verdi som er det angitte antallet dager før eller etter en angitt startdato.

## <a name="syntax"></a>Syntaks

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumenter

`datetime`: *DateTime*

En dato/klokkeslett-verdi som representerer startdatoen.

`days`: *Heltall*

Antall dager før eller etter `datetime`.

## <a name="return-values"></a>Returverdier

*DateTime*

Den resulterende dato/klokkeslett-verdien.

## <a name="usage-notes"></a>Bruksnotater

En positiv verdi for `days` gir en fremtidig dato. En negativ verdi gir en tidligere dato.

## <a name="example-1"></a>Eksempel 1

`ADDDAYS (NOW(), 7)` returnerer datoen og klokkeslettet sju dager i fremtiden.

## <a name="example-2"></a>Eksempel 2

`ADDDAYS (NOW(), -3)` returnerer datoen og klokkeslettet tre dager tidligere.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]