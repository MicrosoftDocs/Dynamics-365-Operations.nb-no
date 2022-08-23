---
title: ORDERBY ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen ORDERBY.
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
ms.openlocfilehash: 23ace859bf75b2adb6ef8604475519a015486948
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282569"
---
# <a name="orderby-er-function"></a>ORDERBY ER-funksjonen

[!include [banner](../includes/banner.md)]

`ORDERBY`-funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er sortert i henhold til de angitte argumentene. Disse argumentene kan defineres som uttrykk.

## <a name="syntax-1"></a><a name="syntax-1"></a>Syntaks 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Syntaks 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Denne syntaksen støttes for Microsoft Dynamics 365 Finance versjon 10.0.25 og senere.

## <a name="arguments"></a>Argumenter

`location`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Plasseringen der sorteringen skal kjøres. Følgende alternativer er gyldige:

- "Query"
- "InMemory"

`list`: *[Postliste](er-formula-supported-data-types-composite.md#record-list)*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`expression 1`: *Felt*

Den gyldige banen til et felt i datakilden som `list`-argumentet for den kalte funksjonen refererer til. Det refererte feltet må være et felt av den primitive datatypen. Dette argumentet er obligatorisk.

`expression N`: *Felt*

Den gyldige banen til et felt i datakilden som `list`-argumentet for den kalte funksjonen refererer til. Det refererte feltet må være et felt av den primitive datatypen. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

### <a name="syntax-1"></a>Syntaks 1

Datasortering utføres alltid i minnet til appserveren. Hvis du vil ha mer informasjon, kan du se [eksempel 1](#example-1).

### <a name="syntax-2"></a>Syntaks 2

### <a name="sorting-in-memory"></a>Sortere i minne

Når `location`-argumentet er angitt som **InMemory**, utføres datasortering i minnet til en appserver. Hvis du vil ha mer informasjon, kan du se [eksempel 2](#example-2).

### <a name="sorting-in-database"></a>Sortere i database

Når `location`-argumentetet angitt som **Query**, utføres datasortering på databasenivå. I dette tilfellet må `list`-argumentet peke til en av følgende [ER-datakilder (Electronic Reporting)](general-electronic-reporting.md) som angir appkilden som det kan opprettes en direkte databasespørring for:

- En datakilde av *Tabellposter*-typen
- Relasjon av en datakilde av *Tabellposter*-typen
- En datakilde av typen *Beregnet felt*

Argumentene `expression 1` og `expression N` må peke til felter for en ER-datakilde som angir de relevante feltene for appkilden som en direkte databasespøring også kan etableres for.

Hvis en direkte databasespørring ikke kan opprettes, oppstår det en [valideringsfeil](er-components-inspections.md#i18) i ER-modelltilordningsutformingen. Meldingen du mottar, sier at ER-uttrykket som inneholder funksjonen `ORDERBY`, ikke kan kjøres under kjøring.

For bedre ytelse anbefaler vi at du bruker **Query**-alternativet når sorteringen er konfigurert for appdatakilder som kan inneholde et stort antall poster (for eksempel apptabeller for transaksjoner).

> [!NOTE]
> Selve `ORDEBY`-funksjonen kan ikke oversettes til en direkte databasespørring. Derfor er det ikke mulig å kjøre spørringer mot en ER-datakilde som inneholder denne funksjonen. Den kan heller ikke brukes når det gjelder ER-funksjoner , for eksempel [FILTER](er-functions-list-filter.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md), der bare datakilder som kan spørres, kan brukes.

Hvis du vil ha mer informasjon , kan du se [eksempel 3](#example-3) og [eksempel 4](#example-4).

### <a name="comparability"></a>Sammenlignbarhet

Siden SQL Database-motoren og Finance-appserveren kan bruke en annen rangeringsverdi for ett enkelt tegn, kan sorteringsresultatet for den samme listen over poster være forskjellig når et [Streng](er-formula-supported-data-types-primitive.md#string)-felt brukes til sortering. Hvis du vil ha mer informasjon, kan du se [eksempel 5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>Eksempel 1: Standardkjøring i minnet

Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("C|B|A", "|")`, genererer uttrykket `FIRST( ORDERBY( DS, DS. Value)).Value` tekstverdien **"A"**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>Eksempel 2: Eksplisitt kjøring i minnet

Hvis **Leverandør** er konfigurert som en ER-datakilde av *Tabellposter*-typen som refererer til **VendTable**-tabellen, returnerer både uttrykket `ORDERBY (Vendor, Vendor.'name()')` og uttrykket `ORDERBY ("InMemory", Vendor, Vendor.'name()')` en liste over leverandører sortert etter navn i stigende rekkefølge.

Når du konfigurerer uttrykket `ORDERBY ("Query", Vendor, Vendor.'name()')` i ER-utformingen av modelltilordningen, oppstår det en [valideringsfeil](er-components-inspections.md#i8) ved utformingstidspunktet fordi `Vendor.'name()'`-banen refererer til en appmetode som har logikk som ikke kan oversettes til en direkte databasespørring.

## <a name="example-3-database-query"></a><a name="example-3"></a>Eksempel 3: Databasespørring

Hvis **TaxTransaction** er konfigurert som en ER-datakilde av *Tabellpost*-typen som refererer til **TaxTrans**-tabellen, sorterer uttrykket `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` poster på appdatabasenivået og returnerer en liste over avgiftstransaksjoner som er sortert etter avgiftskode i stigende rekkefølge.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>Eksempel 4: Datakilder som kan spørres

Hvis **TaxTransaction** er konfigurert som en ER-datakilde for *Tabellposter*-typen som refererer til **TaxTrans**-tabellen, kan ER-datakilden **TaxTransactionFiltered** konfigureres slik at den inneholder uttrykket `FILTER(TaxTransaction, TaxCode="VAT19")`, som vil hente transaksjoner for en angitt avgiftskode. Fordi den konfigurerte ER-datakilden **TaxTransactionFiltered** kan spørres, kan uttrykket `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` konfigureres til å returnere listen over filtrerte avgiftstransaksjoner som er sortert etter transaksjonsdato i stigende rekkefølge.

Hvis du konfigurerer **TaxTransactionOrdered** som en ER-datakilde av typen *Beregnet felt* som inneholder uttrykket `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)`, og en ER-datakilde av typen *Beregnet felt* som inneholder uttrykket `FILTER(TaxTransactionOrdered, TaxCode="VAT19")`, oppstår det en [valideringsfeil](er-components-inspections.md#i18) ved utformingstidspunktet i ER-utformingen av modelltilordningen. Denne feilen oppstår fordi det første argumentet til [FILTER](er-functions-list-filter.md#usage-notes)-funksjonen må refererer til en ER-datakilde som kan spørres, men **TaxTransactionOrdered**-datakilden som inneholder `ORDERBY`-funksjonen, kan ikke spørres.

## <a name="example-5-comparability"></a><a name="example-5"></a>Eksempel 5: Sammenlignbarhet

### <a name="prerequisites"></a>Forutsetninger

1. Angi **DS1**-datakilden av *Beregnet felt*-typen som inneholder uttrykket `SPLIT ("D1|_D2|D3", "|")`
2. Åpne siden **[Finansdimensjonsverdier](../../../finance/general-ledger/financial-dimensions.md)**, og velg **CostCenter**-dimensjonen.
3. Angi følgende dimensjonsverdier: **D1**, **\_D2** og **D3**.

### <a name="sorting-in-memory"></a>Sortere i minne

1. Konfigurer **DS2**-datakilden av *Beregnet felt*-typen som inneholder uttrykket `ORDERBY("InMemory", DS1, DS1.Value)`
2. Legg merke til at uttrykket `FIRST(DS2).Value` returnerer tekstverdien **"D1"**, uttrykket `INDEX(DS2, COUNT(DS2)).Value` returnerer tekstverdien **"\_D2"**, og uttrykket `STRINGJOIN(DS2, DS2.Value, "|")` returnerer tekstverdien **"D1\|D3\|\_D2"**.

### <a name="sorting-in-database"></a>Sortere i database

1. Angi **DS3**-datakilden av *Tabellposter*-typen som refererer til **FinancialDimensionValueEntity**-enheten.
2. Konfigurer **DS4**-datakilden av *Beregnet felt*-typen som inneholder uttrykket `FILTER(DS3, DS3.FinancialDimension="CostCenter")`
3. Konfigurer **DS5**-datakilden av *Beregnet felt*-typen som inneholder uttrykket `ORDERBY(DS4, DS4.DimensionValue)`
4. Legg merke til at uttrykket `FIRST(DS5).Value` returnerer tekstverdien **"\_D2"**, uttrykket `INDEX(DS5, COUNT(DS5)).Value` returnerer tekstverdien **"D3"**, og uttrykket `STRINGJOIN(DS5, DS5.Value, "|")` returnerer tekstverdien **"\_D2\|D1\|D3"**.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
