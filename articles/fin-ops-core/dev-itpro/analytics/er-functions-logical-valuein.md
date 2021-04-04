---
title: VALUEIN ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen VALUEIN.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
ms.topic: article
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
ms.openlocfilehash: e5a0ac314a61abce610407550e65479cbf5a6b5b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565838"
---
# <a name="valuein-er-function"></a>VALUEIN ER-funksjonen

[!include [banner](../includes/banner.md)]

`VALUEIN`-funksjonen bestemmer om de angitte inndataene samsvarer med en verdi for et angitt element i den angitte listen. Den returnerer en *boolsk* verdi av **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen. Hvis ikke returneres den *boolske* verdien **USANN**.

## <a name="syntax"></a>Syntaks

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumenter

`input`: *Felt*

Den gyldige banen til et element i en datakilde i *Postliste*-typen. Verdien for dette elementet samsvares.

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`list item expression`: *Boolsk*

Et gyldig betingelsesuttrykk som enten henviser til eller inneholder ett enkelt felt i den angitte listen som skal brukes for den samsvarende.

## <a name="return-values"></a>Returverdier

*Boolsk*

Den resulterende *boolske* verdien.

## <a name="usage-notes"></a>Bruksnotater

Generelt oversettes `VALUEIN`-funksjonen til et sett med **OR**-betingelser. Hvis listen over **OR**-betingelser er stor, og den maksimal totale lengde på en SQL-setning kan overstiges, bør du vurdere å bruke [`VALUEINLARGE`](er-functions-logical-valueinlarge.md)-funksjonen.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

I noen tilfeller kan den oversettes til en database SQL-setning ved hjelp av `EXISTS JOIN`-operatoren.

## <a name="example-1"></a>Eksempel 1

Du definerer **Liste**-datakilden for *Beregnet felt*-typen i modelltilordningen. Denne datakilden inneholder uttrykket `SPLIT ("a,b,c", ",")`.

Når en datakilde kalles og den er konfigurert som `VALUEIN ("B", List, List.Value)`-uttrykket, returneres **SANN**. I dette tilfellet oversettes `VALUEIN` -funksjonen til følgende sett med betingelser: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, der `("B" = "b")` er lik **SANN**.

Når en datakilde kalles og den er konfigurert som `VALUEIN ("B", List, LEFT(List.Value, 0))`-uttrykket, returneres **USANN**. I dette tilfellet oversettes `VALUEIN`-funksjonen til følgende betingelse: `("B" = "")`, som ikke er lik **SANN**.

Den øvre grensen for antall tegn i teksten i en slik betingelse er 32 768 tegn. Du bør derfor ikke opprette datakilder som kan overstige denne grensen ved kjøretid. Hvis grensen overskrides, slutter programmet å kjøre, og et unntak blir registrert. Denne situasjonen kan for eksempel oppstå hvis datakilden er konfigurert som `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, og **List1** og **List2**-listene inneholder et stort antall poster.

I noen tilfeller kan `VALUEIN`-funksjonen oversettes til en databasesetning ved hjelp av `EXISTS JOIN`-operatoren. Denne virkemåter skjer når [`FILTER`](er-functions-list-filter.md)-funksjonen brukes og følgende betingelser er oppfylt:

- **BE OM SPØRRING**-valget er deaktivert for datakilden for `VALUEIN`-funksjonen som refererer til listen over poster. Ingen flere betingelser brukes på denne datakilden ved kjøretid.
- Ingen nestede uttrykk konfigureres for datakilden for `VALUEIN`-funksjonen som refererer til listen over poster.
- Et listeelement for `VALUEIN`-funksjonen refererer til et felt for den angitte datatypen, ikke til et uttrykk eller en metode for datakilden.

Vurder å bruke dette alternativet i stedet for [`WHERE`](er-functions-list-where.md)-funksjonen som er beskrevet tidligere i dette eksemplet.

## <a name="example-2"></a>Eksempel 2

Du definerer de følgende datakildene i modelltilordningen:

- **I**-datakilden for *Tabellposter*-typen. Denne datakilden refererer til Intrastat-tabellen.
- **Port**-datakilden for *Tabellposter*-typen. Denne datakilden refererer til IntrastatPort-tabellen.

Når en datakilde kalles opp som er konfigurert som uttrykket `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, genereres følgende SQL-setning for å returnere filtrerte poster i Intrastat-tabellen.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

For **dataAreaId**-feltene genereres den endelige SQL-setningen ved hjelp av `IN`-operatoren.

## <a name="example-3"></a>Eksempel 3

Du definerer de følgende datakildene i modelltilordningen:

- **Le**-datakilden for *Beregnet felt*-typen. Denne datakilden inneholder uttrykket `SPLIT ("DEMF,GBSI,USMF", ",")`.
- **I**-datakilden for *Tabellposter*-typen. Denne datakilden refererer til Intrastat-tabellen, og alternativet **Kryssfirma** er aktivert for den.

Når en datakilde kalles opp som er konfigurert som uttrykket `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, inneholder den endelige SQL-setningen følgende betingelse.

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Tilleggsressurser

[Logiske funksjoner](er-functions-category-logical.md)

[VALUEINLARGE-funksjoner](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]