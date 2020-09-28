---
title: JSONVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen JSONVALUE.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 985a7e4f46756e595580d77ac904c883c305b04a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743813"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER-funksjonen

[!include [banner](../includes/banner.md)]

`JSONVALUE`-funksjonen analyserer data i JavaScript Object Notation (JSON)-format som brukes av den angitte banen, og henter en skalarverdi som har den angitte IDen. Den returnerer deretter den utpakkede skalerbare verdien som en *streng*-verdi.

## <a name="syntax"></a>Syntaks

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen som inneholder JSON-data.

`path`: *Streng*

Identifikatoren for en skalerbar verdi for JSON-data.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example"></a>Eksempel

Datakilden **JsonField** inneholder følgende data i JSON-format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. I dette tilfellet returnerer uttrykket `JSONVALUE (JsonField, "BuildNumber")` følgende verdi av *streng*-datatypen: **"7.3.1234.1"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)
