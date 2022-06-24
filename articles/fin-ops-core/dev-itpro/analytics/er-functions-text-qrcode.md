---
title: QRCODE ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen QRCODE.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: e1bcb053297b05f38a1185b54bde25c09411dd9e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905148"
---
# <a name="qrcode-er-function"></a>QRCODE ER-funksjonen

[!include [banner](../includes/banner.md)]

`QRCODE`-funksjonen returnerer en *Container*-verdi som presenterer et QR-kodebilde for den angitte strengen i binært format.

## <a name="syntax"></a>Syntaks

```vb
QRCODE (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *streng*-verdi som representerer den opprinnelige teksten.

## <a name="return-values"></a>Returverdier

*Container*

Den resulterende binære strømmen.

## <a name="example"></a>Eksempel

Du kan konfigurere et elektronisk rapportering (ER)-format til å generere et utgående Microsoft Office-dokument i format (Excel-arbeidsbøker eller Word-dokumenter) ved hjelp av en forhåndsdefinert mal. Denne malen kan inneholde et **Bilde**-objekt (Excel-arbeidsbok) eller en **Bildeinnholdskontroll** (Word-dokument) som en plassholder for et bilde av en QR-kode. Du må legge til det konfigurerte ER-formatet et **celle**-element som vil bli brukt til å fylle inn denne plassholderen. Hvis du vil angi hvilken informasjon som skal lagres i en QR-kode, må du definere en binding for dette **celle**-elementet. Du kan for eksempel konfigurere en slik binding som inneholder følgende uttrykk:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Når du kjører det konfigurerte ER-formatet, blir tekstverdien for **LabelText**-feltet i **model.ListOfShelfLabels**-datakilden brukt til å generere et QR-kodebilde. Dette bildet vil erstatte en plassholder for et QR-kodebilde i dokumentmalen ved hjelp av å generere et utgående dokument. Når dette bildet av det genererte dokumentet skannes, returnerer det teksten som ble hentet fra **LabelText**-feltet i **model.ListOfShelfLabels**-datakilden. Hvis du vil ha mer informasjon, se [Bygge inn bilder og figurer i dokumenter d.u genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]