---
title: COUNTIF ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen COUNTIF.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: cc857a004d988a421c32722b1f69e86b7fefeb36
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743621"
---
# <a name="countif-er-function"></a>COUNTIF ER-funksjonen

[!include [banner](../includes/banner.md)]

`COUNTIF`-funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen. Betingelsen består av et nøkkelområde og en nøkkelverdi.

## <a name="syntax"></a>Syntaks

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>Argumenter

`condition range`: *Streng*

En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.

`condition value`: *Streng*

En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.

## <a name="return-values"></a>Returverdier

*Heltall*

Den resulterende numeriske verdien.

## <a name="usage-notes"></a>Bruksnotater

Egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** kan konfigureres for enten **Sekvens**-komponenten eller **XML-element**-komponenten for et ER-format som ligger under **Vanlige\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.

Denne funksjonen returnerer en **0**-verdi (null) når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.

I `condition range`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.

I `condition value`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.

## <a name="example"></a>Eksempel

For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.

## <a name="additional-resources"></a>Tilleggsressurser

[Datainnsamlingsfunksjoner](er-functions-category-data-collection.md)
