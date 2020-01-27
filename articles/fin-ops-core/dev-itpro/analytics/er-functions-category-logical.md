---
title: Liste over ER-funksjoner i den logiske kategorien
description: Dette emnet inneholder informasjon om de logiske funksjonene som støttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916643"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Liste over ER-funksjoner i den logiske kategorien

[!include [banner](../includes/banner.md)]

Logiske funksjoner for elektronisk rapportering (ER) kan brukes til å arbeide med logiske verdier for å utføre mer enn én sammenligning i ett enkelt uttrykk eller teste flere betingelser. Dette emnet inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon | Beskrivelse |
|----------|-------------|
| [Og](er-functions-logical-and.md)                       | Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis alle de angitte betingelsene er sanne. Hvis ikke returneres den *boolske* verdien **USANN**. |
| [Sak](er-functions-logical-case.md)                     | Denne funksjonen evaluerer verdien til det angitte uttrykket mot de angitte alternative valgene, og returnerer resultatet av det første alternativet som tilsvarer verdien til det angitte uttrykket. Hvis ikke returnerer den et valgfritt standard resultat hvis et standard resultat er angitt som det siste argumentet i den kalte funksjonen som ikke innledes av et alternativ. Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene. |
| [Hvis](er-functions-logical-if.md)                         | Denne funksjonen returnerer den første verdien hvis den angitte betingelsen er oppfylt. Hvis ikke returneres den andre verdien som er angitt. Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene. |
| [Ikke](er-functions-logical-not.md)                       | Denne funksjonen returnerer den omvendte logiske verdien til den angitte betingelsen som en *boolsk* verdi. |
| [Or](er-functions-logical-or.md)                         | Denne funksjonen returnerer en *boolsk* verdi av **USANN** hvis alle de angitte betingelsene er usanne. Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis en angitt betingelse er sann. |
| [ValueIn](er-functions-logical-valuein.md)               | Denne funksjonen bestemmer om de angitte inndataene samsvarer med en verdi for et angitt element i den angitte listen. Den returnerer en *boolsk* verdi av **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen. Hvis ikke returneres den *boolske* verdien **USANN**. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)
