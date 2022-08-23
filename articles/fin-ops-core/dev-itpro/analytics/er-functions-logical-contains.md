---
title: ER-funksjonen CONTAINS
description: Denne artikkelen gir generell informasjon om hvordan du bruker funksjonen ER-funksjonen CONTAINS.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0b2831f8aec4847279953ebcea583c9218d214a7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273136"
---
# <a name="contains-er-function"></a>ER-funksjonen CONTAINS

[!include [banner](../includes/banner.md)]

Funksjonen `CONTAINS` bestemmer om de angitte inndataene inneholder den angitte teksten. Den returnerer den *boolske* verdien **SANN** hvis de angitte inndataene inneholder den angitte teksten. Hvis ikke returneres den *boolske* verdien **USANN**.

## <a name="syntax"></a>Syntaks

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige banen til et element for en datakilde for typen *Streng* eller en strengkonstant. Verdien kan inneholde det andre argumentet.

`search text`: *Streng*

Den gyldige banen for en datakilde for datatypen *Streng* eller en strengkonstant. Verdien finnes kanskje i det første argumentet.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="usage-notes"></a>Bruksnotater

Denne funksjonen kan bare brukes til å angi et betingelsesuttrykk for funksjonen [FILTER](er-functions-list-filter.md) når den relevante tilordningen er konfigurert i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) for å få tilgang til [Microsoft Dataverse](/power-platform/admin/data-integrator). Ellers opprettes det et unntak på utformingstidspunktet. Meldingen du mottar, anbefaler at du bruker funksjonen [WHERE](er-functions-list-where.md) i stedet for funksjonen `FILTER`.

## <a name="example-1"></a>Eksempel 1

Uttrykket `CONTAINS ("abc", "d")` returnerer **USANN**, mens uttrykket `CONTAINS ("abc", "C")` returnerer **SANN**.

## <a name="example-2"></a>Eksempel 2

Uttrykket `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returnerer **SANN** hvis verdien til feltet **Adresse** i datakilden **modell** inneholder strengen **DEU**. Hvis ikke returnes **USANN**.

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)
