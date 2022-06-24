---
title: Liste over ER-funksjoner i datainnsamlingskategorien
description: Denne artikkelen inneholder informasjon om datainnsamlingsfunksjonene som støttes i elektronisk rapportering (ER).
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
ms.openlocfilehash: a8d4f5068bedcf1f15ae5257e29004a4773ef84c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908568"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Liste over ER-funksjoner i datainnsamlingskategorien

[!include [banner](../includes/banner.md)]

Datainnsamlingsfunksjoner for elektronisk rapportering (ER) brukes til å telle og summere i et ER-format som kjøres, basert på data fra utdataene som allerede er generert i **Tekst**- eller **Xml**-format. Denne fremgangsmåten brukes til å forbedre ytelsen til et ER-format som kjøres, til å angi verdier for løpende totaler i genererte dokumenter og til andre formål. Denne artikkelen inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon | Beskrivelse |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Denne funksjonen returnerer en *Postliste*-verdi som inneholder listen over verdier som ble returnert av egenskapen **Verdi for innsamlet datanøkkel** for formatelementer og samlet inn når formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene. Hver betingelse består av et nøkkelområde og en nøkkelverdi. |
| [CountIF](er-functions-datacollection-countif.md) | Denne funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen. Betingelsen består av et nøkkelområde og en nøkkelverdi. |
| [CountIFs](er-functions-datacollection-countifs.md) | Denne funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene. Hver betingelse består av et nøkkelområde og en nøkkelverdi. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Denne funksjonen returnerer en *streng*-verdi som representerer navnet på det gjeldende ER-formatets element. |
| [SumIF](er-functions-datacollection-sumif.md) | Denne funksjonen returnerer en *Reell*-verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen. Betingelsen består av et nøkkelområde og en nøkkelverdi. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Denne funksjonen returnerer en *Reell*-verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene. Hver betingelse består av et nøkkelområde og en nøkkelverdi. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]