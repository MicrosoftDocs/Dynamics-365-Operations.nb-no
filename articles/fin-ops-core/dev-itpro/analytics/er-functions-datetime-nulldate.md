---
title: NULLDATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NULLDATE.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746849"
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