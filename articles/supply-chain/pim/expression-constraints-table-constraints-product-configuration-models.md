---
title: Uttrykksbegrensninger og tabellbegrensninger i produktkonfigurasjonsmodeller
description: Dette emnet beskriver bruken av uttrykks- og tabellbegrensninger. Begrensninger kontrollerer attributtverdiene du kan velge når du konfigurerer produkter for en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre. Du kan bruke uttrykksbegrensninger eller tabellbegrensninger, avhengig av hvordan du foretrekker å bygge begrensningene.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be9d9ae48d21db077928ba7bd5615fea47ea5181
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434606"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Uttrykksbegrensninger og tabellbegrensninger i produktkonfigurasjonsmodeller

[!include [banner](../includes/banner.md)]

Dette emnet beskriver bruken av uttrykks- og tabellbegrensninger. Begrensninger kontrollerer attributtverdiene du kan velge når du konfigurerer produkter for en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre. Du kan bruke uttrykksbegrensninger eller tabellbegrensninger, avhengig av hvordan du foretrekker å bygge begrensningene. 

Begrensninger brukes til å kontrollere attributtverdiene du kan velge når du konfigurerer produkter for en salgsordre, et salgstilbud, en bestilling eller en produksjonsordre. Du kan bruke uttrykksbegrensninger eller tabellbegrensninger, avhengig av hvordan du foretrekker å bygge begrensningene.

## <a name="what-are-expression-constraints"></a>Hva er uttrykksbegrensninger?
Uttrykksbegrensninger kjennetegnes ved et uttrykk som bruker aritmetiske og boolske operatorer og funksjoner. En uttrykksrestriksjon skrives for en bestemt komponent i en produktkonfigurasjonsmodell. Det kan ikke brukes på nytt eller deles med en annen komponent. Uttrykksbegrensningene for en komponent kan imidlertid referere til attributter for delkomponenter for komponenten.

## <a name="what-are-table-constraints"></a>Hva er tabellbegrensninger?
Tabellbegrensninger viser kombinasjonene av verdier som er tillatt for attributter når du konfigurerer et produkt. Definisjoner av tabellbegrensninger kan brukes generelt. Når du oppretter en tabellbegrensning for en komponent i en produktkonfigurasjonsmodell, velger du en tabellbegrensningsdefinisjon. Hvis du vil opprette kombinasjonene som er tillatt, legger du til attributter for bestemte typer i komponentene. Hver attributt har en bestemt verdi.

### <a name="example-of-a-table-constraint"></a>Eksempel på tabellbegrensning

Dette eksemplet viser hvordan du kan begrense konfigurasjonen av en høyttaler til bestemte kabinettyper og fronter. Den første tabellen viser kabinettyper og fronter som vanligvis er tilgjengelige for konfigurasjon. Verdiene er definert for attribyttypene **Kabinettyper** og **Frontgrill**.

| Attributtype | Verdier                      |
|----------------|-----------------------------|
| Kabinettyper | Svart, eik, Rosewood, hvit |
| Frontgrill    | Svart, metall, hvit         |

Den neste tabellen viser kombinasjonene som er definert av tabellbegrensningen **Farge og finish**. Ved å bruke denne tabellbegrensningen, kan du konfigurere en høyttaler som har eik-finish og en svart grill, en Rosewood-finish og en hvit grill og så videre.

| Ferdig         | Grill                       |
|----------------|-----------------------------|
| Eik            | Svart                       |
| Rosewood       | Hvit                       |
| Hvit          | Svart                       |
| Hvit          | Hvit                       |
| Svart          | Svart                       |
| Svart          | Metall                       | 

Du kan opprette systemdefinerte og brukerdefinerte tabellbegrensninger. Hvis du vil ha mer informasjon, se [Systemdefinerte og brukerdefinerte tabellbegrensninger](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Hvilken syntaks skal brukes for å skrive begrensninger?
Du må bruke OML-syntaks (Optimization Modeling Language) når skriver begrensningene. Systemet bruker Microsoft Solver Foundation-begrensningsløseren til å løse begrensningene.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Bør jeg bruke tabellbegrensninger eller uttrykksbegrensninger?
Du kan enten bruke uttrykksbegrensninger eller tabellbegrensninger, avhengig av hvordan du foretrekker å bygge begrensningene. Du bygger opp en tabellbegrensning som en matrise, mens en uttrykksrestriksjon er et enkeltuttrykk. Når du konfigurerer et produkt, spiller det ingen rolle hvilken type betingelse som brukes. Følgende eksempel viser forskjellen mellom de to metodene.  

Når du konfigurerer et produkt ved hjelp av følgende begrensningsoppsett, er disse kombinasjonene tillatt:

-   Et produkt i fargen svart og størrelse 30 eller 50
-   Et produkt i fargen rødt og størrelse 20

### <a name="table-constraint-setup"></a>Tabellbegrensningsoppsett

| Farge | Størrelse |
|-------|------|
| Svart | 30   |
| Svart | 50   |
| Rød   | 20   |

### <a name="expression-constraint-setup"></a>Uttrykksrestriksjonsoppsett

(Farge == "Svart" & (størrelse == "30" | størrelse == "50")) | (farge == "Rød" & størrelse = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Bør jeg bruke operatorer eller infiksnotasjoner når jeg skriver uttrykksbegrensninger?
Du kan skrive en uttrykksbegrensning ved å bruke de tilgjengelige prefiksoperatorene eller ved hjelp av en infix-notasjon. For operatorene **Min**, **Maks** og **Abs** kan du ikke bruke en infix-notasjon. Disse operatorene er inkludert som standard i de fleste programmeringsspråk.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Hvilke operatorer og infiksnotasjoner kan jeg bruke når jeg skriver uttrykksbegrensninger?
Tabellen nedenfor viser operatorene og infix-notasjonene som du kan bruke når du skriver en uttrykksrestriksjon for en komponent i en produktkonfigurasjonsmodell. I eksemplene i den første tabellen kan du se hvordan du skriver inn et uttrykk med infiksnotasjon eller operatorer.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operatør</th>
<th>Beskrivelse</th>
<th>Syntaks</th>
<th>Eksempler</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implies</td>
<td>Dette er tilfelle hvis den første betingelsen er Usann, den andre betingelsen er Sann, eller begge deler.</td>
<td>Implies[a, b], infix: a -: b</td>
<td><ul>
<li><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</li>
<li><strong>Infiksnotasjon:</strong> x != 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Og</td>
<td>Dette gjelder bare hvis alle betingelsene er oppfylt. Hvis antallet betingelser er 0 (null), gir den <strong>True</strong>.</td>
<td>And[argumenter], infix: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>Operator:</strong> And[x == 2, y &lt;= 2]</li>
<li><strong>Infiksnotasjon:</strong> x == 2 &amp; y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eller</td>
<td>Dette er tilfelle hvis en betingelse er Sann. Hvis antallet betingelser er 0 (null), gir den <strong>False</strong>.</td>
<td>Or[argumenter], infix: a | b | ... | z</td>
<td><ul>
<li><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</li>
<li><strong>Infiksnotasjon:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Pluss</td>
<td>Det summerer betingelsene. Hvis antallet betingelser er 0 (null), gir den <strong>0</strong>.</td>
<td>Plus[argumenter], infix: a + b + ... + z</td>
<td><ul>
<li><strong>Operator:</strong> Plus[x, y, 2] == z</li>
<li><strong>Infiksnotasjon:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Minus</td>
<td>Dette opphever argumentet. Dette må ha nøyaktig én betingelse.</td>
<td>Minus[uttrykk], infiks: -uttrykk</td>
<td><ul>
<li><strong>Operator:</strong> Minus[x] == y</li>
<li><strong>Infiksnotasjon:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Dette krever absoluttverdien til betingelsen. Dette må ha nøyaktig én betingelse.</td>
<td>Abs[uttrykk]</td>
<td><strong>Operator:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Tider</td>
<td>Dette tar produktet for betingelsene. Hvis antallet betingelser er 0 (null), gir den <strong>1</strong>.</td>
<td>Times[argumenter], infix: a * b * ... * z</td>
<td><ul>
<li><strong>Operator:</strong> Times[x, y, 2] == z</li>
<li><strong>Infiksnotasjon:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Styrke</td>
<td>Dette krever en eksponentiell verdi. Dette gjelder eksponentiering fra høyre mot venstre. Det vil si den er høyre-assosiativ, og derfor tilsvarer <strong>Kraft[a, b, c]</strong> <strong>Kraft[a, Kraft[b, c]]</strong>. <strong>Styrke</strong> kan bare brukes med en positiv konstant som eksponent.</td>
<td>Styrke[argumenter], infix: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>Operator:</strong> Power[x, 2] == y</li>
<li><strong>Infiksnotasjon:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maks.</td>
<td>Dette gir den største betingelsen. Hvis antallet betingelser er 0 (null), gir den <strong>Infinity</strong>.</td>
<td>Max[argumenter]</td>
<td><strong>Operator:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Min</td>
<td>Dette gir den minste betingelsen. Hvis antallet betingelser er 0 (null), gir den <strong>Infinity</strong>.</td>
<td>Min[argumenter]</td>
<td><strong>Operator:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Ikke</td>
<td>Dette gir det logisk motsatte av betingelsen. Dette må ha nøyaktig én betingelse.</td>
<td>Not[uttrykk], infiks: !uttrykk</td>
<td><ul>
<li><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</li>
<li><strong>Infiksnotasjon:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Eksemplene i den neste tabellen viser hvordan du skriver en infix-notasjon.


|  Infiksnotasjon   |                                          beskrivelse                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     x + y + z     |                                           Tillegg                                            |
|    x \* y \* z    |                                        Multiplikasjon                                         |
|       x - y       | Binær subtraksjon oversettes på samme måte som binær addisjon med en negert andreverdi. |
|     x ^ y ^ z     |                          Eksponentiering med høyre-assosiativitet                          |
|        !x         |                                          Boolsk ikke                                          |
|      x -: y       |                                      Boolsk implikasjon                                      |
|         x         |                                               y                                               |
|     x & y & z     |                                          Boolsk og                                          |
|    x == y == z    |                                           Likhet                                            |
|    x != y != z    |                                           Spesifikk                                            |
|  x &lt; y &lt; z  |                                           Mindre enn                                           |
|  x &gt; y &gt; z  |                                         Større enn                                          |
| x &lt;= y &lt;= z |                                     Mindre eller lik                                     |
| x &gt;= y &gt;= z |                                   Større enn eller lik                                    |
|        (x)        |                           Parenteser overstyrer standardprioritet.                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Hvorfor valideres ikke uttrykksbegrensningene mine riktig?
Du kan ikke bruke reserverte nøkkelord som problemløsernavn for attributter, komponenter eller delkomponenter i en produktkonfigurasjonsmodell. Her er en liste over reserverte nøkkelord som du ikke kan bruke:

-   Tak
-   Element
-   Lik
-   Gulv
-   Hvis
-   Mindre
-   Større
-   Implies
-   Logg
-   Maks.
-   Min.
-   Minus
-   Pluss
-   Styrke
-   Tider
-   Spor
-   Modell
-   Beslutningsprofil
-   Mål


<a name="additional-resources"></a>Tilleggsressurser
--------

[Opprette en uttrykksbegrensning](tasks/add-expression-constraint-product-configuration-model.md)

[Legge til beregning i en produktkonfigurasjonsmodell](tasks/add-calculation-product-configuration-model.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]