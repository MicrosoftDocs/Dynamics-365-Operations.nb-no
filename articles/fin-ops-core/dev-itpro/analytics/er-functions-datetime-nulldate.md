---
title: NULLDATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NULLDATE.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 657766a838fbcd32c6b8bb0ba1f728e9dbbac92e103c219f3eeeab7ecd8c747d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749758"
---
# <a name="nulldate-er-function"></a>NULLDATE ER-funksjon

[!include [banner](../includes/banner.md)]

`NULLDATE`-funksjonen returnerer en *dato*-verdi som representerer **null**-datoen (1. januar 1900).

## <a name="syntax"></a>Syntaks

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Returverdier

*Dato*

Den resulterende datoverdien.

## <a name="example-1"></a>Eksempel 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returnerer **null**-datoen, 1. januar 1900, som **"1900-01-01"**, basert på det angitte egendefinerte formatet.

## <a name="example-2"></a>Eksempel 2

Uttrykket `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returnerer **Sann** når verdien i **DocumentDate**-feltet er lik **null**-datoen. I dette eksemplet er **Faktura** en ER-datakilde av typen **Finans/tabell-post** og refererer til CustInvoiceJour-tabellen.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]