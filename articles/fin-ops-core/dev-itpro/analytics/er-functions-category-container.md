---
title: Liste over ER-funksjoner i beholderkategorien
description: Dette emnet inneholder informasjon om beholderfunksjonene som støttes i Elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 46d1af85773f6c3d07865658c554dee74fae625f
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739100"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Liste over ER-funksjoner i beholderkategorien

[!include [banner](../includes/banner.md)]

Beholder [funksjoner](er-formula-language.md#functions) for [Elektronisk rapportering (ER)](general-electronic-reporting.md) kan brukes til å utføre operasjoner som omfatter datakilder av datatypen *Beholder*. Disse operasjonene skjer når behandlingsdataene representerer en samling binære data i format for stort binærobjekt (BLOB-format). Dette emnet inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon | beskrivelse |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Denne funksjonen returnerer en *Beholder*-verdi som består av binært innhold som dekodes fra den angitte ASCII-strengen som representerer en Base64-gruppe med binær-til-tekst-kodingsoppsett. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)
