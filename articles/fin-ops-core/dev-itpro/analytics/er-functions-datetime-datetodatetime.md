---
title: DATETODATETIME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETODATETIME.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
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
ms.openlocfilehash: d30fdc9c7b6f277b8712b733cabdb0552db2a748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563588"
---
# <a name="datetodatetime-er-function"></a>DATETODATETIME ER-funksjonen

[!include [banner](../includes/banner.md)]

`DATETODATETIME`-funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt datoverdi til en dato/klokkeslett-verdi i Coordinated Universal Time (Greenwich middeltid \[GMT\]).

## <a name="syntax"></a>Syntaks

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumenter

`date`: *Dato*

En datoverdi som representerer datoen som skal konverteres.

## <a name="return-values"></a>Returverdier

*DateTime*

Den resulterende dato/klokkeslett-verdien.

## <a name="example-1"></a>Eksempel 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` returnerer datoen for gjeldende Microsoft Dynamics 365 Finance-økt, 24. desember 2015, som **12/24/2015 12:00:00 AM**. I dette eksemplet er **CompInfo** en ER-datakilde av typen **Finance and Operations/tabell** og refererer til CompanyInfo-tabellen.

## <a name="example-2"></a>Eksempel 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returnerer dato/klokkeslett-verdien **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]