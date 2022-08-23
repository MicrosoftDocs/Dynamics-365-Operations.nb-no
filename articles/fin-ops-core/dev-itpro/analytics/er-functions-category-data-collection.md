---
title: Liste over ER-funksjoner i datainnsamlingskategorien
description: Denne artikkelen inneholder informasjon om datainnsamlingsfunksjonene som støttes i elektronisk rapportering (ER).
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: e01bed49646ffe344004f9eb51e9013e1b4c5430
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286157"
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
