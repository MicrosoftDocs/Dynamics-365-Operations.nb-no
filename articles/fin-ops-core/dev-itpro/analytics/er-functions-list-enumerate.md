---
title: ENUMERATE ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen ENUMERATE.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: adaa2582e6dced428cf1f15a235ecbfd036362e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273256"
---
# <a name="enumerate-er-function"></a>ENUMERATE ER-funksjon

[!include [banner](../includes/banner.md)]

`ENUMERATE`-funksjonen returnerer en ny *Postliste*-verdi som består av opplistede poster i den angitte listen.

## <a name="syntax"></a>Syntaks

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Listen over nummererte poster som returneres, viser følgende tilleggselementer:

- Posten med felt (**Verdi**-komponent)
- Gjeldende postindeks (**Number**-komponent)

## <a name="example"></a>Eksempel

I illustrasjonen nedenfor opprettes **Enumerated**-datakilden som en nummerert liste over leverandørposter fra **Vendors**-datakilden som refererer til VendTable-tabellen.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Illustrasjonen nedenfor viser ER-formatet. I dette formatet opprettes databindinger for å generere utdata i XML-format. Disse utdataene viser enkeltleverandører som opplistede noder.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Følgende illustrasjon viser resultatet når det utformede formatet kjøres.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
