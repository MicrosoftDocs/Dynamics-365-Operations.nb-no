---
title: FILTER ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FILTER.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: e857306574dda7bad5dd25fc7708514997d8e86f
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922429"
---
# <a name="filter-er-function"></a>FILTER ER-funksjon

[!include [banner](../includes/banner.md)]

`FILTER`-funksjonen returnerer den angitte listen som en *Postliste*-verdi etter at spørringen er endret, slik at den filtrerer etter den angitte betingelsen.

## <a name="syntax"></a>Syntaks

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`condition`: *Boolsk*

Et gyldig betingelsesuttrykk som brukes til å filtrere poster i den angitte listen.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a><a name="usage-notes"></a>Bruksnotater

Denne funksjonen er ulik [WHERE](er-functions-list-where.md)-funksjonen fordi den angitte betingelsen brukes på en ER-datakilde av typen *Tabellposter* på databasenivået. Listen og betingelsen kan defineres ved hjelp av tabeller og relasjoner.

Hvis ett av eller begge argumentene som er konfigurert for denne funksjonen (`list` og `condition`), ikke tillater at denne forespørselen skal oversettes til det direkte SQL-kallet, utløses et unntak ved utformingstid. Dette unntaket informerer brukeren om at enten `list` eller `condition` ikke kan brukes til å spørre databasen.

> [!NOTE]
> `FILTER`-funksjonen har en annen funksjon enn `WHERE`-funksjonen når [`VALUEIN`](er-functions-logical-valuein.md)-funksjonen brukes til å angi utvalgskriteriene.
> 
> - Hvis `VALUEIN`-funksjonen brukes i området for `WHERE`-funksjonen, og det andre argumentet for å henvise til en datakilde som ikke returnerer noen poster, vurderes den boolske *[usann](er-formula-supported-data-types-primitive.md#boolean)*-verdien som `VALUEIN``VALUEIN` returnerer. Uttrykket `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` returnerer derfor ingen leverandørposter hvis **VendGroups**-datakilden ikke returnerer noen leverandørgruppeposter.
> - Hvis `VALUEIN`-funksjonen brukes i området for `FILTER`-funksjonen, og det andre argumentet for å henvise til en datakilde som ikke returnerer noen poster, ignoreres den boolske *[usann](er-formula-supported-data-types-primitive.md#boolean)*-verdien som `VALUEIN``VALUEIN` returnerer. Uttrykket `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` returnerer derfor alle leverandørposter hvis **Leverandører**-datakilden, selv om **VendGroups**-datakilden ikke returnerer noen leverandørgruppeposter.

## <a name="example-1"></a>Eksempel 1

Hvis **Vendor** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `FILTER (Vendors, Vendors.VendGroup = "40")` en liste over bare leverandører som tilhører leverandørgruppe 40.

## <a name="example-2"></a>Eksempel 2

Hvis **Vendor** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, og **parmVendorBankGroup** er konfigurert som en ER-datakilde som returnerer en verdi av *Streng*-datatypen, returnerer uttrykket `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` en liste over bare leverandørkontoene som tilhører en spesifikk bankgruppe.

## <a name="example-3"></a>Eksempel 3

Du angir datakilde **DS** av *Beregnet felt*-typen som inneholder uttrykket `SPLIT ("A,B,C", ",")`. Deretter skriver du inn et annet uttrykk, `FILTER( DS, DS.Value = "B")`. Når du prøver å lagre dette uttrykket i ER-formeldesigneren, utløses følgende unntak: "Valideringsfeil: Listeuttrykket for FILTER-funksjonen er ikke søkbart."

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
