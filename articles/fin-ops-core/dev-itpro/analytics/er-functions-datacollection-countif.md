---
title: COUNTIF ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen COUNTIF.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: bebb3d3b810e68fa6a0d3f4deb92b750b7c9a9f3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755306"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]