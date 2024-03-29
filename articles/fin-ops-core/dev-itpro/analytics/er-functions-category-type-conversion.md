---
title: Liste over ER-funksjoner i typekonverteringskategorien
description: Denne artikkelen inneholder informasjon om konverteringsfunksjonene som støttes i elektronisk rapportering (ER).
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
ms.openlocfilehash: 00fe8c5bce40a59580509a719212f163238815be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292624"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Liste over ER-funksjoner i typekonverteringskategorien

[!include [banner](../includes/banner.md)]

Konverteringsfunksjoner for elektronisk rapportering (ER)-type kan brukes til å konvertere verdier mellom typer. Denne artikkelen inneholder et sammendrag av disse funksjonene.

## <a name="type-conversion-functions"></a>Typekonverteringsfunksjoner

| Funksjon | Beskrivelse |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Denne funksjonen returnerer en *Int64*-verdi som representerer den angitte strengen. |
| [IntValue](er-functions-conversion-intvalue.md)       | Denne funksjonen returnerer en *Int*-verdi som representerer den angitte strengen. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Denne funksjonen returnerer en *reell* verdi som er konvertert fra den angitte *streng*-verdien. Under konverteringen vurderes de angitte skilletegnene for desimal- og siffergruppering. |
| [Verdi](er-functions-conversion-value.md)             | Denne funksjonen returnerer en *reell* verdi som er konvertert fra den angitte *streng*-verdien. |

## <a name="type-conversion-functions-in-the-container-category"></a>Typekonverteringsfunksjoner i beholderkategorien

Tabellen nedenfor beskriver funksjonene for typekonvertering i [beholder](er-functions-category-container.md)kategorien.

| Funksjon | beskrivelse |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Denne funksjonen konverterer de angitte inndataene for *Streng*-typen til et dataelement av typen *Beholder*. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Typekonverteringsfunksjoner i kategorien Dato og klokkeslett

Tabellen nedenfor beskriver funksjonene for typekonvertering i kategorien [dato og klokkeslett](er-functions-category-datetime.md).

| Funksjon | Beskrivelse |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Denne funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt *streng*-verdi i angitt format og i en valgfri angitt kultur til en dato/klokkeslett-verdi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Denne funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt *dato*-verdi til en dato/klokkeslett-verdi i Coordinated Universal Time (Greenwich middeltid \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | Denne funksjonen returnerer en *dato*-verdi som konverteres fra en gitt *streng*-verdi i angitt format og i en valgfri angitt kultur til en datoverdi. |

## <a name="type-conversion-functions-in-the-list-category"></a>Typekonverteringsfunksjoner i listekategorien

Tabellen nedenfor beskriver funksjonene for typekonvertering i [listekategorien](er-functions-category-list.md).

| Funksjon | Beskrivelse |
|----------|-------------|
| [Liste](er-functions-list-list.md)                 | Denne funksjonen returnerer en *Postliste*-verdi som en ny liste som er opprettet fra de angitte argumentene for typen *Container (post)*. |
| [ListOfFields](er-functions-list-listoffields.md) | Denne funksjonen returnerer en *postliste*-verdi som opprettes basert på strukturen til et gitt argument for typen *Opplisting* eller *Container (post)*. |
| [Del](er-functions-list-split.md)               | Denne funksjonen deler den angitte *Streng*-verdien inn i delstrenger og returnerer resultatet som en ny *Postliste*-verdi. |
| [StringJoin](er-functions-list-stringjoin.md)     | Denne funksjonen returnerer en *Streng*-verdi som består av sammenkoblede verdier for det angitte feltet fra den angitte *Postliste*-verdien. Verdiene kan skilles med det angitte skilletegnet. |

## <a name="type-conversion-functions-in-the-text-category"></a>Typekonverteringsfunksjoner i tekstkategorien

Tabellen nedenfor beskriver funksjonene for typekonvertering i [tekstkategorien](er-functions-category-text.md).

| Funksjon | Beskrivelse |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Denne funksjonen returnerer en *streng*-verdi som representerer et enkelt tegn som det angitte Unicode-nummeret refererer til. |
| [GuidValue](er-functions-text-guidvalue.md)       | Denne funksjonen konverterer de angitte inndataene for *Streng*-datatypen til et dataelement av *GUID*-typen. |
| [NumberFormat](er-functions-text-numberformat.md) | Denne funksjonen returnerer en *streng*-verdi som representerer det angitte tallet i angitt format og i en valgfri angitt kultur. |
| [QrCode](er-functions-text-qrcode.md)             | Denne funksjonen returnerer en *Container*-verdi som presenterer et QR-kodebilde for den angitte strengen i binært format. |
| [Tekst](er-functions-text-text.md)                 | Denne funksjonen returnerer en *Streng*-verdi som representerer det angitte tallet etter at det er konvertert til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for gjeldende forekomst av programmet. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
