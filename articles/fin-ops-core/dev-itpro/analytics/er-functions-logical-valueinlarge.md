---
title: VALUEINLARGE ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen VALUEINLARGE.
author: kfend
ms.date: 08/17/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 425dbce8f229acbb9c8d721c8f1a554989e0533c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288093"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER-funksjonen

[!include [banner](../includes/banner.md)]

`VALUEINLARGE`-funksjonen bestemmer om de angitte inndataene av typen *Int64* eller *Heltall* samsvarer med en verdi for et angitt element i den angitte listen. Funksjonen returnerer verdien *boolsk* som **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen. Hvis ikke returneres den *boolske* verdien **USANN**. For å forstå forskjellen fra `VALUEIN`-funksjonen kan du se i delen [Bruksmerknad](#usage_note) senere i denne artikkelen.

## <a name="syntax"></a>Syntaks

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumenter

`input`: *Felt*

Den gyldige banen til et datakildeelement av *Postliste*-typen. Verdien for dette elementet samsvares.

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`list item expression`: *Uttrykk*

Et gyldig betingelsesuttrykk som enten henviser til eller inneholder ett enkelt felt i den angitte listen som skal brukes for den samsvarende.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name=""></a><a name="usage_note">Bruksnotater</a>

Når de angitte inndataene representerer en *Int64*- eller *Heltall*-type for et datakildeelement, et kall som kan oversettes til en direkte SQL-setning, konverteres den angitte listen til en midlertidig SQL-tabell, og samsvaret utføres i databasen ved å utføre én enkelt `EXISTS JOIN`-spørring. Hvis ikke fungerer denne funksjonen som [`VALUEIN`](er-functions-logical-valuein.md)-funksjonen.

Når de angitte inndataene representerer et datakildeelement som er utformet som et annet element enn typen *Int64* og *Heltall*, oppstår det en feil under utformingen der du blir informert om at `VALUEINLARGE`-funksjonen ikke kan brukes for det konfigurerte ER-uttrykket.

Når `VALUEINLARGE`-funksjonsuttrykket kjøres og mer enn én midlertidig tabell brukes i omfanget av denne utførelsen, oppstår det en kjøretidsfeil.

## <a name="example"></a>Eksempel

Du definerer de følgende datakildene i modelltilordningen:

- **I**-datakilden for *Tabellposter*-typen.
    - Denne datakilden refererer til **Intrastat**-tabellen.
    - Alternativet **Kryssfirma** er satt til **Nei**.
- **InMemory**-datakilden for *Beregnet felt*-typen.
    - Denne datakilden inneholder uttrykket `WHERE (In, In.Port <> "")`.
- **InFiltered**-datakilden for *Beregnet felt*-typen.
    - Denne datakilden inneholder uttrykket `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Når datakilden **InFiltered** kalles i konteksten for firmaet **DEMF**, opprettes det en ny midlertidig tabell i programdatabasen, den innsamlede minnelisten for post-ID-koder settes inn i denne tabellen, og følgende SQL-setning genereres for å returnere filtrerte poster for **Intrastat**-tabellen.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)

[VALUEIN-funksjonen](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
