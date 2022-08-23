---
title: REPEAT ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen REPEAT.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220695"
---
# <a name="repeat-er-function"></a>REPEAT ER-funksjonen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`REPEAT`-funksjonen bygger en post som inneholder feltet som har en verdi som samsvarer med de angitte inndataene. Deretter returneres en ny *postliste* med en post som gjentas et bestemt antall ganger.

## <a name="syntax"></a>Syntaks

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumenter

`item`: Alle støttede [primitive](er-formula-supported-data-types-primitive.md) datatyper eller [komposittdatatype](er-formula-supported-data-types-composite.md)

Verdien som skal gjentas.

`number`: *Heltall*

Antall repetisjoner.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Listen over gjentatte poster som returneres, viser følgende felter:

- Den angitte verdien (`Item`-felt)
- Nåværende postindeks (`Number`-felt)

> [!NOTE]
> Fordi enbasert nummerering brukes for denne funksjonen, har `Number`-feltet verdien **1** for å returnere den første posten i den resulterende listen.

Du kan bruke denne funksjonen til å multiplisere eksisterende data slik at du kan gjøre ytelse og volumtesting av løsninger for [elektronisk rapportering (ER)](general-electronic-reporting.md) ved hjelp av [RSAT (Regression suite automation tool)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Eksempel

Du vil generere et dokument i XML-format som må inneholde så mange `Party` XML-elementer som du angir i et dataoppføringsfelt i dialogboksen ved kjøretid, før utføringen av et ER-format starter.

Illustrasjonen nedenfor viser ER-[formatet](er-overview-components.md#format-component). I dette formatet legges det enkle `Party` XML-elementet til for å vise egenskapene til én enkelt part.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Illustrasjonen nedenfor viser følgende konfigurerte datakilder:

- `Party`-datakilden som representerer en enkelt part. `Party.Value`-feltet brukes til å vise en enkelt tekstverdi.
- `NumberOfRepeats`-[datakilden](er-user-input-parameter-data-sources.md) som brukes til å tilby et dataregistreringsfelt i dialogboksen ved kjøretid, slik at du kan angi antall parter som skal angis i det genererte dokumentet.
- `Party2`-datakilden som gjentar `Party`-posten antall ganger du har angitt i `NumberOfRepeats`-datakilden.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Den neste illustrasjonen viser databindinger av det redigerbare ER-formatet som er opprettet for å generere utdata i XML-format. Disse utdataene viser enkeltpartene som opplistede noder.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Illustrasjonen nedenfor viser resultatet når det designede formatet kjøres, og verdien for `NumberOfRepeats`-datakilden er angitt som **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
