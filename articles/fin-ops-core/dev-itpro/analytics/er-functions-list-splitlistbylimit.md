---
title: SPLITLISTBYLIMIT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLITLISTBYLIMIT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5bf13b7c1e7cab7c803b352370084421a8180dee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743445"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER-funksjonen

[!include [banner](../includes/banner.md)]

`SPLITLISTBYLIMIT`-funksjonen deler den angitte listen inn i en ny liste over underlister (grupper). Antall poster i hvert parti beregnes dynamisk. Denne funksjonen returneres resultatet som en ny *postliste*-verdi som består av partiene.

## <a name="syntax"></a>Syntaks

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`limit value`: *Heltall* eller *Reell*

Maksimumsverdien for grensen som brukes til å dele den opprinnelige listen i partier.

`limit source`: *Felt*

Den gyldige banen til et felt av *Heltall* eller *Reell*-typen i den angitte listen. Verdien i dette feltet definerer trinnet som den totale summen økes på.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Listen over partier som returneres, inneholder følgende elementer:

- **Verdi**: *Liste*

    Listen over oppføringer som tilhører gjeldende parti.

- **BatchNumber**: *Heltall*

    Nummeret for gjeldende parti i den returnerte listen.

Grensen brukes ikke på en enkelt vare i originallisten hvis kildegrensen overskrider den definerte grensen.

## <a name="example"></a>Eksempel

Illustrasjonen nedenfor viser et ER-format.

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Følgende illustrasjon viser datakildene som brukes for formatet.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Følgende illustrasjon viser resultatet når formatet kjøres. I dette tilfellet er utdataene en flat liste over artikkelvarer.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

I illustrasjonene nedenfor er det samme formatet justert slik at det viser listen over artikkelvarer i partier hvis et enkelt parti må inneholde artikler, og den totale vekten må ikke overskride grensen på 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Følgende illustrasjon viser resultatet når det justerte formatet kjøres.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Grensen gjelder ikke for det siste elementet i den originale listen siden verdien (**11**) av grensekilden (**vekt**) overskrider den definerte grensen (**9**). For å ignorere underlister under rapportgenerering bruker du enten funksjonen `WHERE`- eller **Aktivert**-uttrykket for det tilsvarende formatelementet, etter behov.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
