---
title: SPLITLIST ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLITLIST.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: ef0b548173a01cc5a15fcfb743dfb29397c1349b3c2926fa6401399459d07026
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776128"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER-funksjonen

[!include [banner](../includes/banner.md)]

`SPLITLIST`-funksjonen deler den angitte listen i underlister (eller grupper), der hver inneholder det angitte antallet poster. Deretter returneres resultatet som en ny *postliste*-verdi som består av partiene.

## <a name="syntax-1"></a>Syntaks 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`number`: *Heltall*

Maksimalt antall poster per parti.

`on-demand reading flag`: *Boolsk*

En *boolsk* verdi som angir om elementer i underlister skal genereres ved behov.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Listen over partier som returneres, inneholder følgende elementer:

 - **Verdi:** *Liste*

    Listen over oppføringer som tilhører gjeldende parti.

- **BatchNumber:** *Heltall*

    Nummeret for gjeldende parti i den returnerte listen.

Når flagget for lesing ved behov er satt til **Sann**, genereres underlister etter forespørsel som tillater reduksjon i minneforbruk, men som kan føre til ytelsesreduksjon hvis elementer ikke brukes sekvensielt.

## <a name="example"></a>Eksempel

I følgende illustrasjon opprettes en **Linjer**-datakilde som en postliste med tre poster. Denne listen er delt inn i partier, der hvert inneholder opptil to poster.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Følgende illustrasjon viser det utformede formatoppsettet. I dette formatoppsettet opprettes bindinger til **Linjer**-datakilden for å generere utdata i XML-format. Disse utdataene viser individuelle noder for hvert parti og postene i det.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Følgende illustrasjon viser resultatet når det utformede formatet kjøres.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
