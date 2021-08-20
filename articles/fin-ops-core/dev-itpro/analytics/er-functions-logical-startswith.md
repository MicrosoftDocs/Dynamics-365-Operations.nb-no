---
title: ER-funksjonen STARTSWITH
description: Dette emnet gir generell informasjon om hvordan du bruker funksjonen ER-funksjonen STARTSWITH.
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: b378f501ccf812cfa0ae09e7cfbfdcf4c8a24ab8747b8ffe6044769df14a3057
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762230"
---
# <a name="startswith-er-function"></a>ER-funksjonen STARTSWITH

[!include [banner](../includes/banner.md)]

Funksjonen `STARTSWITH` bestemmer om de angitte inndataene starter med den angitte teksten. Den returnerer den *boolske* verdien **SANN** hvis de angitte inndataene starter med den angitte teksten. Hvis ikke returneres den *boolske* verdien **USANN**.

## <a name="syntax"></a>Syntaks

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige banen til et element for en datakilde for typen *Streng* eller en strengkonstant. Verdien starter kanskje det andre argumentet.

`start text`: *Streng*

Den gyldige banen for en datakilde for datatypen *Streng* eller en strengkonstant. Verdien finnes kanskje på starten av det første argumentet.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen kan bare brukes til å angi et betingelsesuttrykk for funksjonen [FILTER](er-functions-list-filter.md) når den relevante tilordningen er konfigurert i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) for å få tilgang til [Microsoft Dataverse](/power-platform/admin/data-integrator). Ellers opprettes det et unntak på utformingstidspunktet. Meldingen du mottar, anbefaler at du bruker funksjonen [WHERE](er-functions-list-where.md) i stedet for funksjonen `FILTER`.

## <a name="example-1"></a>Eksempel 1

Uttrykket `STARTSWITH ("abc", "d")` returnerer **USANN**, mens uttrykket `STARTSWITH ("abc", "A")` returnerer **SANN**.

## <a name="example-2"></a>Eksempel 2

Uttrykket `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returnerer **TRUE** hvis verdien for feltet **Adresse** for datakilden **modell** startes med strengen **123 Coffee Street**. Hvis ikke returnes **USANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)
