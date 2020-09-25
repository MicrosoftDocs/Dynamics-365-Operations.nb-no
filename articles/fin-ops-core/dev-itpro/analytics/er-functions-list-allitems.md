---
title: ALLITEMS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ALLITEMS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47113d52e15d3d61f00b3c54229e286eb0f1a8d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745399"
---
# <a name="allitems-er-function"></a>ALLITEMS ER-funksjon

[!include [banner](../includes/banner.md)]

`ALLITEMS`-funksjonen kjøres som et minneinternt valg og returnerer en ny utflatet *Postliste*-verdi som en liste over poster som representerer alle elementer som samsvarer med den angitte banen.

## <a name="syntax"></a>Syntaks

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumenter

`path`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Banen må defineres som en gyldig datakildebane til et datakildeelement av datatypen *Postliste*. Dataelementer som banestrengen og datoen skal føre til en feil i ER-uttrykksverktøyet under utformingen.

Vi anbefaler ikke at du bruker denne funksjonen for transaksjonsdatakilder som kan inneholde store mengder data. I stedet bør du vurdere å bruke [ALLTEMSQUERY](er-functions-list-allitemsquery.md)-funksjonen.

## <a name="example-1"></a>Eksempel 1

Hvis du angir `SPLIT("abcdef" , 2)` som datakilde **DS**, returnerer uttrykket `COUNT( ALLITEMS (DS))` **3**.

## <a name="example-2"></a>Eksempel 2

Hvis du angir **Vend** som datakilde for datatypen *postliste* som refererer til VendTable-programtabellen, returnerer uttrykket `ALLITEMS (Vend.'<Relations'.ContactPerson)` en sammenslått liste over poster som har tabellstrukturen **ContactPerson**, og inneholder alle kontaktpersoner som kan åpnes ved hjelp av **ContactPerson.ContactForParty == VendTable.Party**-relasjonen, og som er tilgjengelig for alle leverandører fra den refererte leverandørtabellen.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)
