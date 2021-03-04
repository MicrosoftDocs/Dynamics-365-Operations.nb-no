---
title: Liste over ER-funksjoner for tekstkategorien
description: Dette emnet inneholder informasjon om tekstfunksjonene som støttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 228620afc81e154eced572f3b6024d6836d00d66
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686033"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Liste over ER-funksjoner for tekstkategorien

[!include [banner](../includes/banner.md)]

Tekstfunksjoner for elektronisk rapportering (ER) kan brukes til å utføre operasjoner på datakilder av datatypen *Streng*. Dette emnet inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon | Beskrivelse |
|----------|-------------|
| [Char](er-functions-text-char.md) | Denne funksjonen returnerer en *streng*-verdi som viser et enkelt tegn som det angitte Unicode-nummeret refererer til. |
| [Sammenslåing](er-functions-text-concatenate.md) | Denne funksjonen returnerer alle de angitte tekststrengene som en *streng*-verdi etter at de er føyd sammen til én streng. |
| [Format](er-functions-text-format.md) | Denne funksjonen returnerer den angitte strengen som en *streng*-verdi etter at den er formatert ved å erstatte forekomster av **%N** med *N*-te argumentet. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Denne funksjonen søker etter en bestemt *opplistings*-verdi i den angitte opplistingsdatakilden ved hjelp av opplistingsnavnet som er angitt som en *streng*-verdi. Hvis *opplistings*-verdien blir funnet, returnerer funksjonen den. |
| [GuidValue](er-functions-text-guidvalue.md) | Denne funksjonen konverterer de angitte inndataene for *Streng*-datatypen til et dataelement av *GUID*-typen. |
| [JsonValue](er-functions-text-jsonvalue.md) | Denne funksjonen analyserer data i JavaScript Object Notation (JSON)-format som brukes av den angitte banen, og henter en skalarverdi som er basert på den angitte IDen. Den returnerer deretter den utpakkede skalerbare verdien som en *streng*-verdi. |
| [Venstre](er-functions-text-left.md) | Denne funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra starten av den angitte strengen. |
| [Len](er-functions-text-len.md) | Denne funksjonen returnerer en *heltall*-verdi som viser det angitte antallet tegn i den angitte strengen. |
| [Lower](er-functions-text-lower.md) | Denne funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at den er konvertert til små bokstaver. |
| [Mid](er-functions-text-mid.md) | Denne funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra den angitte strengen, og begynner fra den angitte posisjonen. |
| [NumberFormat](er-functions-text-numberformat.md) | Denne funksjonen returnerer en *streng*-verdi som viser det angitte tallet i angitt format og i en valgfri angitt kultur. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Denne funksjonen returnerer det angitte tallet som en *streng*-verdi etter at det er skrevet ut (det vil si konvertert til tekststrenger) på det angitte språket. |
| [PadLeft](er-functions-text-padleft.md) | Denne funksjonen returnerer en *streng*-verdi med den angitte lengden der begynnelsen av den angitte strengen fylles ut med ett eller flere forekomster av de angitte tegnene. |
| [QrCode](er-functions-text-qrcode.md) | Denne funksjonen returnerer en *Container*-verdi som presenterer et QR-kodebilde for den angitte strengen i binært format. |
| [Erstatt](er-functions-text-replace.md) | Denne funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at hele eller deler av den er erstattet med en annen streng. |
| [Høyre](er-functions-text-right.md) | Denne funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra slutten av den angitte strengen. |
| [Tekst](er-functions-text-text.md) | Denne funksjonen returnerer det angitte tallet som en *streng*-verdi etter at de er konvertert til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for gjeldende forekomst av programmet. |
| [Oversett](er-functions-text-translate.md) | Denne funksjonen returnerer en *Streng*-verdi som inneholder resultatet av erstatningen av den angitte teksten i tegn for et annet angitt tegnsett. |
| [Trim](er-functions-text-trim.md) | Denne funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at innledende og etterfølgende mellomrom er avkortet, og når flere mellomrom mellom ord er fjernet. |
| [Upper](er-functions-text-upper.md) | Denne funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at den er konvertert til store bokstaver. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]