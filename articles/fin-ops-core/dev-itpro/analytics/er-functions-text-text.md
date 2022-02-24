---
title: TEXT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TEXT
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682901"
---
# <a name="text-er-function"></a>TEXT ER-funksjon

[!include [banner](../includes/banner.md)]

`TEXT`-funksjonen returnerer det angitte tallet som en *streng*-verdi etter at de er konvertert til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for gjeldende forekomst av programmet.

## <a name="syntax"></a>Syntaks

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltall* eller *Reell*

Et nummer som må konverteres til en tekststreng.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

For verdier for *reell*-typen begrenses strengkonverteringen til to desimalplasser.

## <a name="example"></a>Eksempel

Hvis de nasjonale innstillingene for Microsoft Dynamics 365 Finance-forekomstens server er definert som **EN-US**, returnerer `TEXT (NOW ())` gjeldende dato for programøkten, 17. desember 2015, som tekststrengen **"12/17/2015 07:59:23 AM"**. `TEXT (1/3)` returnerer **"0.33"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)
