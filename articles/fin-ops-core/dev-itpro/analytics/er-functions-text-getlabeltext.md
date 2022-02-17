---
title: GETLABELTEXT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GETLABELTEXT.
author: NickSelin
ms.date: 01/04/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 911567a94b80c2b762a37e83d37fc500132edb18
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075638"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER-funksjonen

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

`GETLABELTEXT`-funksjonen søker etter en bestemt etikett for å returnere en *[Streng](er-formula-supported-data-types-primitive.md#string)*-verdi som representerer oversettelsen av den spesifiserte etiketten på det spesifiserte språket.

## <a name="syntax"></a>Syntaks

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumenter

### <a name="label-id"></a>Etikett-ID

`label id`: *Streng* eller *Etikett-ID*

Gyldig ID for en av følgende etikettyper:

- [ER-etikett (elektronisk rapportering)](general-electronic-reporting.md)
- Microsoft Dynamics 365 Finance-etikett

#### <a name="usage-notes"></a>Bruksnotater

Dette argumentet kan bare defineres som en konstant, ved hjelp av ett av følgende mønstre som støttes:

- For ER-etiketter:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- For Finance-etiketter:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Ved utformingstidspunktet vises det en feilmelding på siden **[Formeldesigner](er-advanced-formula-editor.md)** hvis ingen etikett blir funnet ved å bruke den oppgitte etikett-ID-en.

### <a name="language"></a>Språk

`language`: *Streng*

En streng som representerer en språkkode.

#### <a name="usage-notes"></a>Bruksnotater

Dette argumentet kan defineres som en tekstkonstant eller som banen til et datakildefelt som returnerer en *Streng*-verdi.

> [!NOTE]
> Samtidig vises det en valideringsfeilmelding hvis ingen språkkoder blir funnet ved hjelp av det angitte `language`-argumentet, når det er definert som en tekstkonstant.
>
> Ved kjøretid returneres oversettelsen for `EN-US`-systemspråket for en angitt etikett hvis ingen språkkoder ble funnet ved hjelp av det angitte `language`-argumentet.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="example-1-system-label"></a><a name=example-1></a>Eksempel 1: Systemetikett

Uttrykkene `GETLABELTEXT (@"SYS70894", "en-us")` og `GETLABELTEXT ("SYS70894", "en-us")` returnerer den engelske oversettelsen "Nothing to print" for `@SYS70894`-appetiketten.

## <a name="example-2-er-label"></a><a name=example-2></a>Eksempel 2: ER-etikett

Du begynner å redigere en [ER-konfigurasjon](general-electronic-reporting.md#Configuration) som har blitt [utledet](er-quick-start2-customize-report.md#DeriveProvidedFormat) fra konfigurasjonen av **ISO20022-kredittoverføring (DE)**. Angi en ny datakilde for typen *[Beregnet felt](er-calculated-field-ds-performance.md)*, og konfigurer uttrykket `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` for denne datakilden. I dette tilfellet, ved kjøretid, returnerer datakilden den tyske oversettelsen "Kreditorenname" for ER-etiketten `@GER_LABEL:VendorName` som ble opprinnelig konfigurert i ER-basiskonfigurasjonen **ISO20022-kredittoverføring (DE)**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)

[Utforme flerspråklige rapporter i elektronisk rapportering](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
