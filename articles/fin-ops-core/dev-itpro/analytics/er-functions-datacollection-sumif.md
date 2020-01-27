---
title: SUMIF ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SUMIF.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 579b14c713bc5f9831c5e012d16bb3b6f97b1035
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916436"
---
# <a name="SUMIF">SUMIF ER-funksjonen</a>

[!include [banner](../includes/banner.md)]

`SUMIF`-funksjonen returnerer en *reell* verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen. Betingelsen består av et nøkkelområde og en nøkkelverdi.

## <a name="syntax"></a>Syntaks

```
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>Argumenter

`key name for summing`: *Streng*

En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for ER-formatkomponenten som verdien for bindingen må brukes til summeringsformål for.

Egenskapen **Navn på innsamlet datanøkkel** kan konfigureres for enten en **Sekvens**-komponenten eller en **XML-element** -komponenten for et ER-format som ligger under **Vanlig\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.

## <a name="return-values"></a>Returverdier

*Kommatall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen returnerer en **0**-verdi (null) når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.

I `condition range`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.

I `condition value`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.

## <a name="example"></a>Eksempel

For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.

## <a name="additional-resources"></a>Tilleggsressurser

[Datainnsamlingsfunksjoner](er-functions-category-data-collection.md)
