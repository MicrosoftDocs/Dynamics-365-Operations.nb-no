---
title: Formelspråk i elektronisk rapportering
description: Denne artikkelen gir generell informasjon om hvordan du bruker formelspråket i elektronisk rapportering.
author: kfend
ms.date: 05/04/2020
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7df29c74b2a430ed9d974cad709b975e4fd9cd35
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283291"
---
# <a name="electronic-reporting-formula-language"></a>Formelspråk i elektronisk rapportering

[!include [banner](../includes/banner.md)]

Elektronisk rapportering (ER) gir en kraftig datatransformasjonsopplevelse. Språket som brukes til å uttrykke de nødvendige datamanipulasjonene i [ER-formeldesigneren](general-electronic-reporting-formula-designer.md), ligner på formelspråket i Microsoft Excel.

## <a name="basic-syntax"></a>Grunnleggende syntaks

ER-uttrykk kan inneholde én eller flere av følgende elementer:

- [Konstanter](#Constants)
- [Operatorer](#Operators)
- [Referanser](#References)
- [Baner](#Paths)
- [Funksjoner](#Functions)

## <a name="constants"></a><a name="Constants"></a>Konstanter

Når du utformer uttrykk, kan du bruke tekst og numeriske konstanter (dvs. verdier som ikke er beregnet). Uttrykket `VALUE ("100") + 20` bruker for eksempel den numeriske konstanten **20** og strengkonstanten **"100"**, og returnerer den numeriske verdien **120**.

ER-formeldesigneren støtter avbruddssekvenser. Derfor kan du angi en uttrykksstreng som skal håndteres på en annen måte. Uttrykket `"Leo Tolstoy ""War and Peace"" Volume 1"` returnerer for eksempel tekststrengen **Leo Tolstoy "Krig og fred" Del 1.**

## <a name="operators"></a><a name="Operators"></a>Operatører

Tabellen nedenfor viser de aritmetiske operatorene som du kan bruke til å utføre grunnleggende matematiske operasjoner, for eksempel addisjon, subtraksjon, multiplikasjon og divisjon.

| Operator | Betydning               | Eksempel     |
|----------|-----------------------|-------------|
| +        | Tillegg              | `1+2`       |
| -        | Subtraksjon, negasjon | `5-2`, `-1` |
| \*       | Multiplikasjon        | `7\*8`      |
| /        | Inndeling              | `9/3`       |

Tabellen nedenfor viser sammenligningsoperatorene som støttes. Du kan bruke disse operatorene til å sammenligne to verdier.

| Operator | Betydning                  | Eksempel      |
|----------|--------------------------|--------------|
| =        | Lik                    | `X=Y`        |
| &gt;     | Større enn             | `X>Y`        |
| &lt;     | Mindre enn                | `X<Y`        |
| &gt;=    | Større enn eller lik | `X>=Y`       |
| &lt;=    | Mindre enn eller lik    | `X<=Y`       |
| &lt;&gt; | Er ikke lik             | `X<>Y`       |

Du kan også bruke et &-tegn (&) som en tekstsammenkoblingsoperator. På denne måten kan du koble sammen én eller flere tekststrenger til én enkelt tekststreng.

| Operator | Betydning     | Eksempel                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Sammenslåing | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Operatorprioritet

Rekkefølgen som delene av et sammensatt uttrykk evalueres i er viktig. Resultatet av uttrykket `1 + 4 / 2` varierer for eksempel, avhengig av om addisjonen eller divisjonen gjøres først. Du kan bruke parenteser til å definere hvordan uttrykk evalueres. Hvis du for eksempel vil angi at addisjonen skal gjøres først, kan du endre det forrige uttrykket til `(1 + 4) / 2`. Hvis du ikke eksplisitt angir operasjonsrekkefølgen i et uttrykk, er rekkefølgen basert på standardprioriteten som er tilordnet til operatorene som støttes. Tabellen nedenfor viser prioriteten som er tilordnet hver operator. Operatorer som har en høyere prioritet (for eksempel 7) evalueres før operatorer som har en lavere prioritet (for eksempel 1).

| Prioritet | Operatorer      | Syntaks                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Gruppering       | ( … )                                                                   |
| 6          | Medlemstilgang  | … . …                                                                   |
| 5          | Funksjonsanrop  | … ( … )                                                                 |
| 4          | Multiplikativ | … \* …<br>… / …                                                         |
| 3          | Additiv       | … + …<br>… - …                                                          |
| 2          | Sammenligning     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Skille     | … , …                                                                   |

Hvis et uttrykk inneholder flere etterfølgende operatorer med samme prioritet, evalueres disse operasjonene fra venstre mot høyre. Uttrykket `1 + 6 / 2 \* 3 > 5` returnerer for eksempel **sann**. Vi anbefaler at du bruker parenteser for å eksplisitt angi ønsket rekkefølge på operasjoner i uttrykk, slik at uttrykkene er enklere å lese og vedlikeholde.

## <a name="references"></a><a name="References"></a>Referanser

Alle datakilder for gjeldende ER-komponent som er tilgjengelige under utformingen av et uttrykk, kan brukes som navngitte referanser. Gjeldende ER-komponent kan enten være en modelltilordning eller et format. Gjeldende ER-modelltilordning inneholder for eksempel datakilden **ReportingDate**, som returnerer en verdi for [*DateTime*](er-formula-supported-data-types-primitive.md#datetime)-datatypen. Hvis du vil ha verdien riktig formatert i det genererende dokumentet, kan du referere til datakilden i uttrykket som `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Alle tegn i navnet på en refererende datakilde som ikke representerer en bokstav i alfabetet, må ha et enkelt anførselstegn (') foran. Hvis navnet på en referansedatakilde inneholder minst ett symbol som ikke representerer en bokstav i alfabetet, må navnet være omsluttet av enkle anførselstegn. Disse ikke-alfabetiske symbolene kan for eksempel være skilletegn eller andre skriftlige symboler. Her er noen eksempler:

- Datakilden **Today's date & time** må refereres til i ER-uttrykket som `'Today''s date & time'`.
- Metoden **name()** for datakilden **Customers** må refereres i ER-uttrykk som `Customers.'name()'`.

Hvis metodene for programdatakilder har parametere, brukes følgende syntaks for å kalle disse metodene:

- Hvis **isLanguageRTL**-metoden for **System**-datakilden har en **EN-US**-parameter av [*Streng*](er-formula-supported-data-types-primitive.md#string)-datatypen, må denne metoden refereres til i et ER-uttrykk som `System.isLanguageRTL("EN-US")`.
- Anførselstegn er ikke obligatorisk når et metodenavn inneholder bare alfanumeriske symboler. De er imidlertid obligatorisk for en metode i en tabell hvis navnet inneholder parentes.

Når du legger til **System**-datakilden i en ER-tilordning som refererer til programklassen **Global**, returnerer uttrykket `System.isLanguageRTL("EN-US ")` den *boolske* verdien **USANN**. Det endrede uttrykket `System.isLanguageRTL("AR")` returnerer den *boolske* verdien **SANN**.

Du kan begrense hvordan verdier blir sendt til parametere av denne metodetypen:

- Bare konstanter kan sendes til metoder av denne typen. Verdiene for konstantene defineres under utformingen.
- Bare [primitive](er-formula-supported-data-types-primitive.md) (grunnleggende) datatyper støttes for parametere av denne typen. De primitive datatypene inkluderer *heltall*, *reelle tall*, *boolsk* og *streng*.

## <a name="paths"></a><a name="Paths"></a>Baner

Når et uttrykk refererer til en strukturert datakilde, kan du bruke banedefinisjonen for å velge et bestemt primitivt element i denne datakilden. Tegnet punktum (.) brukes til å skille enkeltelementene i en strukturert datakilde. Gjeldende ER-modelltilordning inneholder for eksempel datakilden **InvoiceTransactions**, og denne datakilden returnerer listen med poster. Oppføringsstrukturen **InvoiceTransactions** inneholder feltene **AmountDebit** og **AmountCredit**, og begge disse feltene returnerer numeriske verdier. Derfor kan du utforme følgende uttrykk for å beregne det fakturerte beløpet: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Konstruksjonen `InvoiceTransactions.AmountDebit` i dette uttrykket er banen som brukes til å få tilgang til **AmountDebit**-feltet i **InvoiceTransactions**-datakilden i *Postliste*-typen.

### <a name="relative-path"></a>Relativ bane

Hvis banen til en strukturert datakilde starter med et krøllalfategn (@), er det en relativ bane. Krøllalfategnet vises i stedet for den gjenstående delen av den absolutte banen til den hierarkiske trestrukturen som brukes. Illustrasjonen nedenfor viser et eksempel. Her angir den absolutte banen `Ledger.'accountingCurrency()'` at regnskapsvalutaverdien fra **Finans**-datakilden angis i **AccountingCurrency**-feltet i datamodellen.

![Eksempel på en absolutt bane på siden for ER-modelltilordningsutforming.](./media/ER-FormulaLanguage-AbsolutePath.png)

Eksemplet i illustrasjonen nedenfor viser hvordan en relativ bane brukes. Den relative banen `@.AccountNum` angir at **AccountNum**-feltet for **Intrastat**-datakilden (som vises ett nivå over **AccountNum**-feltet i datamodellens hierarkiske tre) brukes til å angi kontonummeret for kunden eller leverandøren i datamodellens **AccountNum**-felt.

![Eksempel på en relativ bane på siden for ER-modelltilordningsutforming.](./media/ER-FormulaLanguage-RelativePath1.png)

Den gjenstående delen av den absolutte banen vises også i [ER-formelredigeringen](general-electronic-reporting-formula-designer.md).

![Gjenstående del av den absolutte banen på siden ER-formeldesigner.](./media/ER-FormulaLanguage-RelativePath2.png)

Hvis du vil ha mer informasjon, kan du se [Bruke en relativ bane i databindinger for ER-modeller og -formater](relative-path-data-bindings-er-models-format.md).

## <a name="functions"></a><a name="Functions"></a>Funksjoner

Innebygde ER-funksjoner kan brukes i ER-uttrykk. Alle datakilder i uttrykkskonteksten (dvs. gjeldende ER-modelltilordning eller ER-format), kan brukes som parametere for anropsfunksjoner i henhold til listen over argumenter for anropsfunksjoner. Konstanter kan også brukes som parametere for anropsfunksjoner. Gjeldende ER-modelltilordning inneholder for eksempel datakilden **InvoiceTransactions**, og denne datakilden returnerer listen med poster. Oppføringsstrukturen **InvoiceTransactions** inneholder feltene **AmountDebit** og **AmountCredit**, og begge disse feltene returnerer numeriske verdier. For å beregne det fakturerte beløpet kan du derfor utforme følgende uttrykk som bruker den innebygde ER-avrundingsfunksjonen: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Når du utformer ER-modelltilordninger og ER-rapporter, kan du bruke ER-funksjoner fra følgende kategorier:

- [Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)
- [Listefunksjoner](er-functions-category-list.md)
- [Logiske funksjoner](er-functions-category-logical.md)
- [Matematiske funksjoner](er-functions-category-mathematical.md)
- [Registreringsfunksjoner](er-functions-category-record.md)
- [Tekstfunksjoner](er-functions-category-text.md)
- [Datainnsamlingsfunksjoner](er-functions-category-data-collection.md)
- [Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)
- [Typekonverteringsfunksjoner](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Funksjonslisteutvidelse

ER lar deg utvide listen over funksjoner som brukes i ER-uttrykk. Det er nødvendig med noe utvikling. Hvis du vil ha mer informasjon, kan du se [Utvide listen over elektroniske rapporteringsfunksjoner (ER)](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Sammensatte uttrykk

Du kan opprette sammensatte uttrykk som bruker funksjoner fra forskjellige kategorier, forutsatt at datatypene samsvarer. Når du bruker funksjoner sammen, må du samsvare datatypen for utdataene fra én funksjon med datatypen inndata som kreves av en annen funksjon. Hvis du for eksempel vil unngå en mulig "listen-er-tom"-feil i en binding av et felt til et ER-formatelement, kan du kombinere funksjoner fra [Liste](er-functions-category-list.md)-kategorien med en funksjon fra [Logisk](er-functions-category-logical.md)-kategorien, som følgende eksempel viser. Her bruker formelen [IF](er-functions-logical-if.md)-funksjonen til å teste om **IntrastatTotals**-listen er tom før den returnerer verdien for den nødvendige samlingen fra denne listen. Hvis **IntrastatTotals**-listen er tom, returnerer formelen **0** (null).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Flere løsninger

Du kan ofte få samme datatransformasjonsresultat på flere måter ved å bruke funksjoner fra ulike kategorier eller ulike funksjoner fra samme kategori. Det forrige uttrykket kan for eksempel også konfigureres ved hjelp av [COUNT](er-functions-list-count.md)-funksjonen fra [Liste](er-functions-category-list.md)-kategorien.

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Utvide listen over funksjoner for elektronisk rapportering](general-electronic-reporting-formulas-list-extension.md)

[Støttede primitive datatyper](er-formula-supported-data-types-primitive.md)

[Sammensatte datatyper som støttes](er-formula-supported-data-types-composite.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
