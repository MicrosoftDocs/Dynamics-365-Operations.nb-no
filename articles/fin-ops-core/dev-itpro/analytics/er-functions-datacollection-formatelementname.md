---
title: FORMATELEMENTNAME ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen FORMATELEMENTNAME.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 0a733c3c70cede6395b3d7454d82ce4d999e7e9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851987"
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