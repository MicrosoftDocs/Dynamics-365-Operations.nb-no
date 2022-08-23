---
title: Liste over ER-funksjoner i beholderkategorien
description: Denne artikkelen inneholder informasjon om beholderfunksjonene som støttes i Elektronisk rapportering (ER).
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: f07c3645f824fc2fe8ca156c8cf06840e993a9a5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282659"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Liste over ER-funksjoner i beholderkategorien

[!include [banner](../includes/banner.md)]

Beholder [funksjoner](er-formula-language.md#Functions) for [Elektronisk rapportering (ER)](general-electronic-reporting.md) kan brukes til å utføre operasjoner som omfatter datakilder av datatypen *Beholder*. Disse operasjonene skjer når behandlingsdataene representerer en samling binære data i format for stort binærobjekt (BLOB-format). Denne artikkelen inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon | beskrivelse |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Denne funksjonen returnerer en *Beholder*-verdi som består av binært innhold som dekodes fra den angitte ASCII-strengen som representerer en Base64-gruppe med binær-til-tekst-kodingsoppsett. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
