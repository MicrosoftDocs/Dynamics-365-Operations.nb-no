---
title: WHERE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen WHERE.
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
ms.openlocfilehash: 392cf7acebd7ad95bcc0f5d4b7a67500a412a795
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041842"
---
# <a name="WHERE">WHERE ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`WHERE`-funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er filtrert i henhold til den angitte betingelsen.

## <a name="syntax"></a>Syntaks

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`condition`: *Boolsk*

Et gyldig betingelsesuttrykk som brukes til å filtrere poster i den angitte listen.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen er ulik [FILTER](er-functions-list-filter.md)-funksjonen fordi den angitte betingelsen brukes på en ER-datakilde av typen *Postposte* som finnes i minnet.

Hvis argumentene som er konfigurert for denne funksjonen (`list` og `condition`), tillater at denne forespørselen skal oversettes til det direkte SQL-kallet, utløses en varselmelding ved utformingstid. Denne meldingen informerer brukeren om at ytelsen kan forbedres hvis [FILTER](er-functions-list-filter.md)-funksjonen brukes i stedet for `WHERE`.

## <a name="example-1"></a>Eksempel 1

Hvis **Leverandør** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `WHERE (Vendors, Vendors.VendGroup = "40")` en liste over bare leverandører som tilhører leverandørgruppe 40.

## <a name="example-2"></a>Eksempel 2

Hvis du angir datakilden **DS** for typen *Beregnet felt*, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, returnerer uttrykket `WHERE( DS, DS.Value = "B")` en liste med bare én post som inneholder teksten **"B"** i **Verdi**-feltet.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
