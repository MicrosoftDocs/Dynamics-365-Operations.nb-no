---
title: NULLCONTAINER ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NULLCONTAINER.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746513"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER-funksjonen

[!include [banner](../includes/banner.md)]

`NULLCONTAINER`-funksjonen returnerer en nullverdi for *Container (post)*-verdi som har samme struktur som den angitte postlisten eller posten.

## <a name="syntax"></a>Syntaks

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste* eller *Container (post)*

Den gyldige banen til en datakilde for typen *Postliste* eller *Container (record)*.

## <a name="return-values"></a>Returverdier

*Container (post)*

Den resulterende postvedien.

## <a name="usage-notes"></a>Bruksnotater

> [!NOTE] 
> Denne funksjonen er foreldet. Bruk `EMPTYRECORD`-funksjonen i stedet. Hvis du vil ha mer informasjon, kan du se [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Eksempel

`NULLCONTAINER (SPLIT ("abc", 1))` returnerer en ny, tom post som har samme struktur som listen som returneres av `SPLIT`- funksjonen. Hvis du vil ha mer informasjon, kan du se [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Registreringsfunksjoner](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]