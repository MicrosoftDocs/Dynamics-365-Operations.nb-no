---
title: FORMATELEMENTNAME ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen FORMATELEMENTNAME.
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 1c8c319075f8f39bec963df2c88d2d8d3beace43
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275445"
---
# <a name="formatelementname-er-function"></a>FORMATELEMENTNAME ER-funksjonen

[!include [banner](../includes/banner.md)]

`FORMATELEMENTNAME`-funksjonen returnerer en *streng*-verdi som representerer navnet på det gjeldende ER-formatets element.

## <a name="syntax"></a>Syntaks

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen kan kalles i ER-uttrykk som er konfigurert for egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** for en ER-formatkomponent fra **Tekst**-gruppen som ligger under **Felles\\Fil**- komponenten der **Samle inn utdatadetaljer** er slått på.

## <a name="example"></a>Eksempel

For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.

## <a name="additional-resources"></a>Tilleggsressurser

[Datainnsamlingsfunksjoner](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
