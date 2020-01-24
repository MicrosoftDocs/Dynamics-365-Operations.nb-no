---
title: TABLENAME2ID ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TABLENAME2ID
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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915815"
---
# <a name="TABLENAME2ID">TABLENAME2ID ER-funksjon</a>

[!include [banner](../includes/banner.md)]

`TABLENAME2ID`-funksjonen returnerer en numerisk representasjon av tabell-IDen for det angitte tabellnavnet som en  *heltall*-verdi.

## <a name="syntax"></a>Syntaks

```
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstverdi som representerer et gyldig tabellnavn.

## <a name="return-values"></a>Returverdier

*Heltall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Utføring av denne funksjonen kan ha forskjellige resultater i forskjellige forekomster av Microsoft Dynamics 365 Finance, selv om det samme firmanavnet brukes.

## <a name="example"></a>Eksempel

`TABLENAME2ID ("Intrastat")` returnerer **1510**.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)
