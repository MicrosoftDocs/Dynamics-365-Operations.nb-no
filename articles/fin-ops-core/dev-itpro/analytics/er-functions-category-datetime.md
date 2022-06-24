---
title: Liste over ER-funksjoner i kategorien Dato og klokkeslett
description: Denne artikkelen inneholder informasjon om dato- og klokkeslettfunksjoner som støttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 09/09/2021
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
ms.openlocfilehash: e6e15d143bad016883f03ecf0125ce9429215a71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880257"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Liste over ER-funksjoner i kategorien Dato og klokkeslett

[!include [banner](../includes/banner.md)]

Dato- og klokkeslettfunksjoner for elektronisk rapportering (ER) kan brukes til å trekke ut informasjon fra dato- og klokkeslettverdier, og til å utføre operasjoner på dem. Denne artikkelen inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon | Beskrivelse |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Denne funksjonen returnerer en *[Datetime](er-formula-supported-data-types-primitive.md#datetime)*-verdi som er det angitte antallet dager før eller etter en angitt startdato. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | Denne funksjonen returnerer en *Datetime*-verdi som konverteres fra en gitt dato/tid-verdi i én tidssone til en dato/klokkeslett-verdi i en annen tidssone. |
| [DateFormat](er-functions-datetime-dateformat.md) | Denne funksjonen returnerer en *[streng](er-formula-supported-data-types-primitive.md#string)*-verdi som viser en gitt datoverdi som tekst i angitt format og i en valgfri angitt kultur. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Denne funksjonen returnerer en *streng*-verdi som viser en gitt dato/klokkeslett-verdi som tekst i angitt format og i en valgfri angitt kultur. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Denne funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt kultur til en dato/klokkeslett-verdi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Denne funksjonen returnerer en *Datetime*-verdi som konverteres fra en gitt datoverdi til en dato/klokkeslett-verdi i Coordinated Universal Time (Greenwich middeltid \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | Denne funksjonen returnerer en *[Date](er-formula-supported-data-types-primitive.md#date)*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt kultur til en dato/klokkeslett-verdi. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Denne funksjonen returnerer en *[Heltall](er-formula-supported-data-types-primitive.md#integer)*-verdi som representerer antall dager mellom 1. januar og den angitte datoen. |
| [Dager](er-functions-datetime-days.md) | Denne funksjonen returnerer en *Heltall*-verdi som representerer antall dager mellom en angitt dato og en annen angitt dato. |
| [Now](er-functions-datetime-now.md) | Denne funksjonen returnerer en *Datetime*-verdi som representerer gjeldende dato og klokkeslett for programserveren. |
| [NullDate](er-functions-datetime-nulldate.md) | Denne funksjonen returnerer en *dato*-verdi som representerer **null**-datoen (1. januar 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Denne funksjonen returnerer en *DateTime*-verdi som representerer **null** dato/klokkeslett-verdien (1. januar 1900) i Coordinated Universal Time. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Denne funksjonen returnerer en *Datetime*-verdi som representerer gjeldende dato og klokkeslett for programøkt. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Denne funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programøkt. |
| [I dag](er-functions-datetime-today.md) | Denne funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programserveren. |
| [WeekNum](er-functions-datetime-weeknum.md) | Denne funksjonen returnerer en *Heltall*-verdi som representerer uken i året. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
