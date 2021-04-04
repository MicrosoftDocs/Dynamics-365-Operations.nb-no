---
title: ER-funksjonen ENDSWITH
description: Dette emnet gir generell informasjon om hvordan du bruker funksjonen ER-funksjonen ENDSWITH.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 2470bd8c75cf690d701957c4c79009659d61f7a5
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557541"
---
# <a name="endswith-er-function"></a>ER-funksjonen ENDSWITH

[!include [banner](../includes/banner.md)]

Funksjonen `ENDSWITH` bestemmer om de angitte inndataene slutter med den angitte teksten. Den returnerer den *boolske* verdien **SANN** hvis de angitte inndataene slutter med den angitte teksten. Hvis ikke returneres den *boolske* verdien **USANN**.

## <a name="syntax"></a>Syntaks

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige banen til et element for en datakilde for typen *Streng* eller en strengkonstant. Verdien avslutter kanskje det andre argumentet.

`start text`: *Streng*

Den gyldige banen for en datakilde for datatypen *Streng* eller en strengkonstant. Verdien finnes kanskje på slutten av det første argumentet.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen kan bare brukes til å angi et betingelsesuttrykk for funksjonen [FILTER](er-functions-list-filter.md) når den relevante tilordningen er konfigurert i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) for å få tilgang til [Microsoft Dataverse](../data-entities/data-integration-cds.md). Ellers opprettes det et unntak på utformingstidspunktet. Meldingen du mottar, anbefaler at du bruker funksjonen [WHERE](er-functions-list-where.md) i stedet for funksjonen `FILTER`.

## <a name="example-1"></a>Eksempel 1

Uttrykket `ENDSWITH ("abc", "d")` returnerer **USANN**, mens uttrykket `ENDSWITH ("abc", "C")` returnerer **SANN**.

## <a name="example-2"></a>Eksempel 2

Uttrykket `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returnerer **TRUE** hvis verdien for feltet **Adresse** for datakilden **modell** avsluttes med strengen **USA**. Hvis ikke returnes **USANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)
