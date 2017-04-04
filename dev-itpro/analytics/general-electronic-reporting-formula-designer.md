---
title: Formeldesigner i elektronisk rapportering
description: "Dette emnet beskriver hvordan du bruker formeldesigneren i elektronisk rapportering (ER). Når du utformer et format for et bestemt elektronisk dokument i ER, kan du bruke Microsoft Excel-lignende formler for datatransformasjon for å oppfylle kravene for fullføringen og formatering for dette dokumentet. Ulike typer funksjoner støttes - tekst, dato og klokkeslett, matematiske logisk, informasjon, datakonvertering og andre (domene-spesifikke bedriftsfunksjoner)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ac8d6c064ca826cc1c2fed07578ca9ce0c66ef66
ms.lasthandoff: 03/31/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Formeldesigner i elektronisk rapportering

Dette emnet beskriver hvordan du bruker formeldesigneren i elektronisk rapportering (ER). Når du utformer et format for et bestemt elektronisk dokument i ER, kan du bruke Microsoft Excel-lignende formler for datatransformasjon for å oppfylle kravene for fullføringen og formatering for dette dokumentet. Ulike typer funksjoner støttes - tekst, dato og klokkeslett, matematiske logisk, informasjon, datakonvertering og andre (domene-spesifikke bedriftsfunksjoner).

<a name="formula-designer-overview"></a>Oversikt over formeldesigner
-------------------------

Elektronisk rapportering (ER) støtter formeldesigneren. Under utformingen kan du derfor konfigurere uttrykk som kan brukes til følgende oppgaver ved kjøretid:

-   transformere data som er mottatt fra en Microsoft Dynamics 365 for Operations-database og som skal fylles ut i en ER-datamodell som er utformet for å være en datakilde for ER-formater (filtrering, gruppering, datatypekonvertering og så videre)
-   formatere data som må sendes til et elektronisk dokument som genereres i henhold til oppsettet og betingelser for et bestemt ER-format (i henhold til forespurt språk eller kultur, koding og så videre).
-   kontroll av prosessen for generering av elektronisk dokument (aktivering/deaktivering av utdataene for bestemte elementer i formatet avhengig av databehandling, avbryte dokumentopprettelse, vise meldinger for sluttbrukere og så videre)

Formeldesignersiden kan åpnes når du gjør noe av følgende:

-   Binder datakileelementer til datamodellkomponenter.
-   Binder datakileelementer til formatkomponenter.
-   Utfører vedlikehold av beregnede felt som en del av datakilder.
-   Definerer synlighetsbetingelsene for inndataparametere for brukere.
-   Utformer et formats transformasjoner.
-   Definerer aktiveringen av betingelser for formatets komponenter.
-   Definerer filnavn for formatets FILE-komponenter.
-   Definerer betingelsene for prosesskontrollvalideringer.
-   Definerer meldingsteksten for prosesskontrollvalideringer.

## <a name="designing-er-formulas"></a>Utforme ER-formler
### <a name="data-binding"></a>Databinding

ER-formeldesigneren kan brukes til å definere et uttrykk som transformerer data som mottas fra datakilder, slik at dataene kan fylles ut i dataforbruker ved kjøretid:

-   Fra Dynamics 365 for Operations-datakilder og kjøretidsparametere til en ER-datamodell.
-   Fra en ER-datamodell til et ER-format.
-   Fra Dynamics 365 for Operations-datakilder og kjøretidsparametere til et ER-format.

Illustrasjonen nedenfor viser utformingen av et uttrykk av denne typen. I dette eksemplet returnerer uttrykket verdien for **Intrastat.AmountMST**-feltet for **Intrastat**-tabellen i Dynamics 365 for Operations, når denne verdien er avrundet til to desimalplasser. [![bilde-uttrykk-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) illustrasjonen nedenfor viser hvordan et uttrykk av denne typen kan brukes. I dette eksemplet er resultatet av uttrykket utformet utfylt i den **Transaction.InvoicedAmount** komponent av den **mva-rapportering modell** datamodellen. [![bilde-uttrykket binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) ved kjøretid, utviklet formelen **ROUND (Intrastat.AmountMST 2)**, runder verdien av den **AmountMST** felt for hver post i den **Intrastat** tabell til to desimalplasser, og fyll ut den avrundede verdien til den **Transaction.InvoicedAmount** komponent av den **mva-rapportering** datamodellen.

### <a name="data-formatting"></a>Dataformatering

ER-formeldesigneren kan brukes til å definere et uttrykk som formaterer data som mottas fra datakilder, slik at dataene kan sendes som en del av det genererende elektroniske dokumentet. Hvis du har formatering som må brukes som en vanlig regel som skal brukes for et format, kan du introdusere formateringen én gang i en formatkonfigurasjonen som en navngitt transformasjon som har et formateringsuttrykk. Denne navngitte transformasjonen kan deretter knyttes til mange formatkomponenter som utdata må formateres etter, i henhold til opprettede uttrykket som ble opprettet. Illustrasjonen nedenfor viser utformingen av en transformasjon av denne typen. I dette eksemplet tar **TrimmedString**-transformasjonen innkommende data for **String**-datatypen, og avrunder innledende og etterfølgende mellomrom når den returnerer strengverdien. [![bilde-transformasjon design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) illustrasjonen nedenfor viser hvordan en Transformasjon av denne typen kan brukes. I dette eksemplet refererer flere formatkomponenter som sender tekst som utdata til det genererende elektroniske dokumentet ved kjøretid, til **TrimmedString**-transformasjonen med navn. [![bilde-transformasjon-Bruk](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) når formater-komponenter refererer til den ** TrimmedString ** transformasjon (for eksempel den **partyName** komponent i den foregående illustrasjonen) dette sender tekst som utdata til generering av dokumentet. Teksten inneholder ikke mellomrom. Hvis du har en formatering som skal brukes individuelt, kan du introdusere denne formateringen som et individuelt uttrykk for binding av en bestemt formatkomponent. Illustrasjonen nedenfor viser et uttrykk av denne typen. I dette eksemplet er **partyType**-formatkomponenten bundet til datakilden via et uttrykk som konverterer innkommende data fra **Model.Company.RegistrationType**-feltet i datakilden til store bokstaver i tekst, og sender teksten som utdata til det elektroniske dokumentet. [![bilde binding med formel](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Prosessflytkontroll

ER-formeldesigneren kan brukes til å definere uttrykk som styrer prosessflyten for generering av dokumenter. Du kan:

-   Definere betingelser som avgjør når en prosess for oppretting av dokument må stoppes.
-   Angi uttrykk som oppretter meldinger for sluttbrukeren om stoppede prosesser eller vise kjøringsloggmeldinger om å fortsette prosessen for rapportgenerering.
-   Angi filnavnene for generering av dokumenter, og kontrollere betingelser de oppretter.

Hver regel av prosessflytkontrollen er utviklet som en enkelt validering. Illustrasjonen nedenfor viser en validering av denne typen. Her er en forklaring på konfigurasjonen i dette eksemplet:

-   Valideringen blir evaluert når **INSTAT**-noden er opprettet i den genererende XML-filen.
-   Hvis listen over transaksjoner er tom, stopper valideringen kjøringsprosessen og returnerer **USANN**.
-   Valideringen returnerer en feilmelding som inneholder teksten for etiketten SYS70894 på brukerens foretrukne språk.

[![bilde-validering](./media/picture-validation.jpg)](./media/picture-validation.jpg) The ER formelen designer kan også brukes til å angi et filnavn for et elektronisk dokument genererer og kontrollere at prosessen med å opprette filen. Illustrasjonen nedenfor viser utformingen av en prosessflytkontroll av denne typen. Her er en forklaring på konfigurasjonen i dette eksemplet:

-   Listen over oppføringer fra **model.Intrastat**-datakilde deles i partier som hver inneholder opptil 1 000 poster.
-   Utdataene oppretter en ZIP-fil som inneholder én fil i XML-format for hvert parti som ble opprettet.
-   Et uttrykk returnerer et filnavn for generering av elektroniske dokumenter ved å kjede sammen filnavnet og filtypen. Filnavnet inneholder parti-ID-en som suffiks for det andre partiet og alle etterfølgende partier.
-   Et uttrykk aktiverer (ved å returnere **SANN**) prosessen for en filopprettelse for partier som inneholder minst én post.

[![filen bildekontroll](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Grunnleggende syntaks

ER-uttrykk kan inneholde én eller flere av følgende elementer:

-   Konstanter
-   Operatører
-   Referanser
-   Baner
-   Funksjoner

#### <a name="constants"></a>Konstanter

Du kan bruke tekst og numeriske konstanter (verdier som ikke er beregnet) når du utformer uttrykk. Hvis du for eksempel uttrykket ** verdi ("100") + 20 ** bruker numerisk konstant 20 og streng konstant "100", og returnerer den numeriske verdien **120**. ER-formeldesigneren støtter avbruddssekvenser, slik at du kan angi uttrykksstrengen som skal håndteres på en annen måte. For eksempel returnerer uttrykket **"Leo Tolstoy ""War and Peace"" Volume 1"** tekststrengen **Leo Tolstoy "War and Peace" Volume 1**.

#### <a name="operators"></a>Operatører

Tabellen nedenfor viser de aritmetiske operatorene som du kan bruke til å utføre grunnleggende matematiske operasjoner, for eksempel addisjon, subtraksjon, multiplikasjon og divisjon.

| Operatør | Betydning              | Eksempel |
|----------|----------------------|---------|
| +        | Tillegg             | 1+2     |
| -        | Subtraksjon Negasjon | 5-2 -1  |
| \*       | Multiplikasjon       | 7\*8    |
| /        | Inndeling             | 9/3     |

Tabellen nedenfor viser sammenligningsoperatorene som støttes, og som du kan bruke til å sammenligne to verdier.

| Operatør | Betydning                  | Eksempel    |
|----------|--------------------------|------------|
| =        | Lik                    | X=Y        |
| &gt;     | Større enn             | X&gt;Y     |
| &lt;     | Mindre enn                | X&lt;Y     |
| &gt;=    | Større enn eller lik | X&gt;=Y    |
| &lt;=    | Mindre eller lik    | X&lt;=Y    |
| &lt;&gt; | Er ikke lik             | X&lt;&gt;Y |

Du kan også bruke et &-tegn (&) som en tekstsammenkoblingsoperator for å koble sammen én eller flere tekststrenger til én enkelt tekststreng.

| Operatør | Betydning     | Eksempel                                        |
|----------|-------------|------------------------------------------------|
| &        | Sammenslåing | "Ingenting å skrive ut" & ": " & "Finner ingen poster" |

#### <a name="operator-precedence"></a>Operatorprioritet

Rekkefølgen som delene av et sammensatt uttrykk evalueres i er viktig. Hvis du for eksempel resultatet av uttrykket ** 1 + 4 / 2 ** varierer, avhengig av om addisjonen eller divisjon-operasjonen utføres først. Du kan bruke parenteser til å definere hvordan uttrykk evalueres. Hvis du for eksempel vil angi at addisjonen skal utføres først, kan du endre det forrige uttrykket til **(1 + 4) / 2**. Hvis operasjonsrekkefølgen som skal utføres i et uttrykk ikke er uttrykkelig definert, er rekkefølgen basert på standardrekkefølgen som er tilordnet til operatorene støttes. Tabellen nedenfor viser operatorene og prioriteten som er tilordnet hver av dem. Operatorer som har høyere prioritet (for eksempel 7) evalueres før operatorer som har lavere prioritet (for eksempel 1).

| Prioritet | Operatører      | Syntaks                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Gruppering       | ( … )                                                    |
| 6          | Medlemstilgang  | … . …                                                    |
| 5          | Funksjonsanrop  | … ( … )                                                  |
| 4          | Multiplikativ | … \* … … / …                                             |
| 3          | Additiv       | … + … … - …                                              |
| 2          | Sammenligning     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Skille     | … , …                                                    |

Operatorer på samme linje har samme prioritet. Hvis et uttrykk inneholder mer enn én av disse operatorene, evalueres uttrykket fra venstre mot høyre. Hvis du for eksempel uttrykket **1 + 6 / 2 \*3 &gt;5** returnerer **sanne**. Vi anbefaler at du bruker parenteser for å eksplisitt angi ønsket evalueringsrekkefølgen for uttrykk, for å gjøre det enklere å lese og vedlikeholde uttrykkene.

#### <a name="references"></a>Referanser

Alle datakilder for gjeldende ER-komponent (en modell eller et format) som er tilgjengelige under utformingen av et uttrykk, kan brukes som navngitte referanser. Gjeldende ER-datamodell inneholder for eksempel datakilden **ReportingDate** som returnerer en verdi for **DATETIME**-datatypen. Hvis du vil formatere denne verdien i generering dokumentet riktig, kan du referere til datakilden i uttrykket som følger: **DATETIMEFORMAT (ReportingDate, "dd-MM-ÅÅÅÅ")** alle tegn som ikke representerer en bokstav i alfabetet, navnet på en flerfeltsbegrensningsdefinisjon datakilde må innledes med et enkelt anførselstegn ('). Hvis navnet på en flerfeltsbegrensningsdefinisjon datakilden inneholder minst ett symbol som representerer en bokstav i alfabetet (for eksempel skilletegn eller andre symboler skriftlig), må navnet være omsluttet av enkle anførselstegn. Her er noen eksempler:

-   Datakilden **Today’s date & time** må refereres i ER-uttrykket slik: **'Today''s date & time’**
-   Metoden **name()** for datakilden **Customers** må refereres i ER-uttrykk slik: **Customers.’name()’**

#### <a name="path"></a>Bane

Når et uttrykk refererer til en strukturert datakilde, kan du bruke banedefinisjonen for å velge et bestemt primitivt element i denne datakilden. Tegnet punktum (.) brukes til å skille enkeltelementene i en strukturert datakilde. Gjeldende ER-datamodell inneholder for eksempel datakilden **InvoiceTransactions** som returnerer listen med poster. Oppføringsstrukturen **InvoiceTransactions** inneholder feltene **AmountDebit** og **AmountCredit** som returnerer numeriske verdier. Du kan derfor utforme følgende uttrykk for å beregne det fakturerte beløpet: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funksjoner

Den neste delen beskrives funksjonene som kan brukes i ER-uttrykk. Alle datakilder i uttrykkskonteksten (gjeldende ER-datamodell eller ER-format), i tillegg til konstanter, kan brukes som parametere for funksjonsanrop i henhold til listen over argumenter for anropsfunksjoner. Gjeldende ER-datamodell inneholder for eksempel datakilden **InvoiceTransactions** som returnerer listen med poster. Oppføringsstrukturen **InvoiceTransactions** inneholder feltene **AmountDebit** og **AmountCredit** som returnerer numeriske verdier. For å beregne det fakturerte beløpet kan du derfor utforme følgende uttrykk som bruker den innebygde ER-avrundingsfunksjonen: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Funksjoner som støttes
Tabellen nedenfor beskriver datamanipuleringsfunksjonene som du kan bruke til å utforme ER-datamodeller og ER-rapporter. Denne listen over funksjoner ikke er fast, og kan utvides av utviklere. Hvis du vil se en oversikt over funksjonene som du kan bruke, kan du gå til funksjonsruten i ER-formeldesigner.

### <a name="date-and-time-functions"></a>Dato- og klokkeslettfunksjoner

| Funksjon                                   | Beskrivelse                                                                                                                                                                                                                                                                                                                                                      | Eksempel                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (dato/klokkeslett, dager)                   | Legg til det angitte antallet dager i den angitte dato-/klokkeslettverdien.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** Returnerer datoen og klokkeslettet sju dager i fremtiden.                                                                                                                                                                                                                            |
| DATETODATETIME (dato)                      | Konverter den angitte datoverdien til en dato-/klokkeslettverdi.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. ' getCurrentDate()')** returnerer den gjeldende Dynamics 365 for operasjoner Øktdato, 12/24/2015, som **12/24/2015 12:00:00 AM**. I dette eksemplet er **CompInfo** en ER-datakilde av typen **Dynamics 365 for Operations/tabell** som refererer til CompanyInfo-tabellen. |
| NOW ()                                     | Returnerer gjeldende dato og klokkeslett for Dynamics 365 for Operations-programserveren som en dato-/klokkeslettverdi.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Returnerer gjeldende dato for Dynamics 365 for Operations-programserveren som en datoverdi.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Returnerer en **nullverdi** for dato.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Returnerer **nullverdi** for dato/klokkeslett.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (dato/klokkeslett, format)          | Konverter den angitte dato-/klokkeslettverdien til en streng i det angitte formatet. (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard og ](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) [egendefinert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-åååå")** returnerer gjeldende dato for Dynamics 365 for Operations-programserveren, 12/24/2015, som **"24-12-2015"**, i henhold til det angitte egendefinerte formatet.                                                                                                          |
| DATETIMEFORMAT (dato/klokkeslett, format, kultur) | Konverter den angitte dato-/klokkeslettverdien til en streng i angitt format og [kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard og ](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) [egendefinert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (NOW(), "d", "de")** returnerer gjeldende dato for Dynamics 365 for Operations-programserveren, 12/24/2015, som **"24.12.2015"**, i henhold til den valgte tyske kulturen.                                                                                                             |
| SESSIONTODAY ()                            | Returnerer gjeldende dato for Dynamics 365 for Operations-økten som en datoverdi.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Returnerer gjeldende dato og klokkeslett for Dynamics 365 for Operations-økten som en verdi for dato og klokkeslett.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (dato, format)                  | Returnerer strengrepresentasjon av dato ved hjelp av angitt format.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-åååå")** returnerer gjeldende dato for Dynamics 365 for Operations-økten 12/24/2015 som “**24-12-2015**” i henhold til det angitte egendefinerte formatet.                                                                                                                      |
| DATEFORMAT (dato, format, kultur)         | Konverter den angitte datoverdien til en streng i angitt format og [kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard og ](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) [egendefinert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)).     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** returnerer gjeldende dato for Dynamics 365 for Operations-økten, 12/24/2015, som **"24.12.2015"**, i henhold til den valgte tyske kulturen.                                                                                                                       |

### <a name="list-functions"></a>Listefunksjoner

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funksjon</th>
<th>beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (inndata, lengde)</td>
<td>Del den angitte inndatastrengen i delstrenger, der har har den angitte lengden. Returner resultatet som en ny liste.</td>
<td><strong>DEL (&quot;abcd&quot;, 3)</strong> returnerer en ny liste som består av to poster som har en <strong>streng</strong> feltet. -Feltet i den første posten inneholder tekst <strong>&quot;abc&quot;</strong>, og -feltet i den andre oppføringen inneholder teksten <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (liste, nummer)</td>
<td>Del den angitte listen i grupper, der hver inneholder det angitte antallet poster. Returnere resultatet som en ny gruppeliste som inneholder følgende elementer:
<ul>
<li>Grupper som vanlige lister (<strong>Value</strong>-komponent)</li>
<li>Gjeldende gruppenummer (<strong>BatchNumber </strong>-komponent)</li>
</ul></td>
<td>I eksemplet nedenfor opprettes <strong>Linjer</strong>-datakilden som en postliste med tre poster, som er delt inn i grupper, som hver inneholder opptil to poster. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>Viser oppsettet utformet format, der bindinger til den <strong>linjer</strong> datakilden er opprettet for å generere output i XML-format, som viser enkelte noder for hver bunke og postene i den. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>Følgende er resultatet av å kjøre utformet format. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (post 1 [, post 2, ...])</td>
<td>Returner en ny liste som opprettes fra de angitte argumentene.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> returnerer en tom post, der listen med felt inneholder alle feltene i postlistene <strong>MainData</strong> og <strong>OtherData</strong>.</td>
</tr>
<tr class="even">
<td>LISTJOIN (liste 1, liste 2, ...)</td>
<td>Returner en sammenkoblet liste som opprettes fra listen av de angitte argumentene.</td>
<td><strong>LISTJOIN (del (&quot;abc&quot;, 1), del (&quot;def&quot;, 1))</strong> returnerer listen over seks poster der én for den <strong>streng</strong> datatype som inneholder bokstaver.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (liste)</td>
<td>Returnerer <strong>SANN</strong> hvis den angitte listen ikke inneholder noen elementer. Hvis ikke, returnes <strong>USANN</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (liste)</td>
<td>Returner en tom liste ved hjelp av den angitte listen som en kilde for listestrukturen.</td>
<td><strong>EMPTYLIST (del (&quot;abc&quot;, 1))</strong> returnerer en ny, tom liste som har samme struktur som i listen som er returnert av <strong>del</strong> funksjon.</td>
</tr>
<tr class="odd">
<td>FIRST (liste)</td>
<td>Returner den første posten i den angitte listen hvis posten ikke er tom. Hvis ikke, iverksette et unntak.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (liste)</td>
<td>Returner den første posten i den angitte listen hvis posten ikke er tom. Hvis ikke, returner en <strong>null</strong>-post.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (liste)</td>
<td>Returner en liste som bare inneholder det første element i den angitte listen.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (bane)</td>
<td>Returnerer en ny liste som er flatet ut og som representerer alle elementer som samsvarer med den angitte banen. Banen må defineres som en gyldig datakildebane til et datakildeelement av datatypen postliste. Dataelementer for banen til streng, dato, osv. skal føre til en feil under utformingen i ER-uttrykksverktøyet.</td>
<td>Hvis du skriver inn <strong>del (&quot;abcdef&quot;, 2)</strong> som en datakilde (DS), <strong>antall (ALLITEMS (DS. Verdi))</strong> returnerer <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (liste [,uttrykk 1, uttrykket 2, ...])</td>
<td>Returner den angitte listen som er sortert i henhold til de angitte argumentene som kan defineres som uttrykk.</td>
<td>Når <strong>Leverandør </strong> er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer <strong> ORDERBY (leverandører, Vendors.'name()')</strong> en oversikt over leverandører sortert etter navn i stigende rekkefølge.</td>
</tr>
<tr class="even">
<td>REVERSE (liste)</td>
<td>Returner den angitte listen i omvendt rekkefølge.</td>
<td>Når <strong>Leverandør </strong> er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer <strong> REVERSE (leverandører, Vendors.'name()')) )</strong> en oversikt over leverandører sortert etter navn i synkende rekkefølge.</td>
</tr>
<tr class="odd">
<td>WHERE (liste, betingelse)</td>
<td>Returner den angitte listen som er filtrert i henhold til den angitte betingelsen. I motsetning til <strong>FILTER</strong>-funksjonen brukes den angitte betingelsen på listen i minnet.</td>
<td>Når <strong>leverandøren</strong> er konfigurert som en datakilde for ER som refererer til tabellen VendTable <strong>der (leverandører, Vendors.VendGroup = &quot;40&quot;)</strong> returnerer en liste over leverandører som tilhører leverandørgruppen 40.</td>
</tr>
<tr class="even">
<td>ENUMERATE (liste)</td>
<td>Returner en ny liste som består av opplistede poster for den angitte listen, og som viser følgende elementer:
<ul>
<li>Angitte listeposter som vanlige lister (<strong>Value</strong>-komponent)</li>
<li>Gjeldende postindeks (<strong>Number</strong>-komponent)</li>
</ul></td>
<td>I eksemplet nedenfor opprettes <strong>Enumerated</strong>-datakilden som en nummerert liste over leverandørposter fra <strong>Vendors</strong>-datakilden som refererer til <strong>VendTable</strong>-tabellen. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Her er et format der databindinger er opprettet for å generere output i XML-format, som viser enkelte leverandører som opplistet noder. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>Dette er resultatet av å kjøre utformet format. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (liste)</td>
<td>Returner antall poster i den angitte listen hvis listen ikke er tom. Hvis ikke, returnes <strong>0</strong> (null).</td>
<td><strong>Antall (del (&quot;abcd&quot;, 3))</strong> returnerer <strong>2</strong>, fordi den <strong>del</strong> funksjonen oppretter en liste som består av to poster.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (bane)</td>
<td>Returnerer en liste for poster opprettet fra et argument av en av følgende typer:
<ul>
<li>Modellopplisting</li>
<li>Formatopplisting</li>
<li>Beholder</li>
</ul>
Listen som opprettes, vil bestå av poster med følgende felt:
<ul>
<li>Navn</li>
<li>Etikett</li>
<li>beskrivelse</li>
</ul>
Etikett og Beskrivelse-feltene returnerer kjøretidsverdier basert på formatet språkinnstillinger.</td>
<td>Følgende eksempel viser opplistingen i en datamodell. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Følgende eksempel viser:
<ul>
<li>Modellopplisting satt inn i en rapport som en datakilde.</li>
<li>ER-uttrykk utformet for å bruke modellopplisting som parameter for denne funksjonen.</li>
<li>Datakilde av postlistetypen settes inn i en rapport ved hjelp av det opprettede ER-uttrykket.</li>
</ul><ph id="t1">
< en href="./media/ger-listoffields-function-in-format-expression.png" ></ph><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> i eksemplet ER formatere elementer som er bundet til datakilden for oppføring liste-typen som ble opprettet ved hjelp av funksjonen LISTOFFIELDS. <a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Dette er et resultat av kjøringen utformet format. <a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Notat:</strong> Translated teksten for etiketter og beskrivelser er fylt ut ER format-utdata i henhold til språkinnstillingene som er konfigurert for overordnede filen og MAPPEN formatere elementer.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (liste, feltnavn, skilletegn)</td>
<td>Returnerer strengen av sammenkoblede verdier for et felt fra en liste som er atskilt med et valgt skilletegn.</td>
<td>Hvis du har angitt SPLIT(“abc” , 1) som en datakilde DS, returnerer uttrykket STRINGJOIN (DS, DS.Value, “:”) “a:b:c”</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (liste, grenseverdi, grensekilde)</td>
<td>Deler den angitte listen inn en ny liste over underordnede lister og returnerer resultatet i oppføringslisteinnhold. Grenseverdiparameteren angir verdien av grensen for deling av opprinnelseslisten. Grensekildeparameteren angir trinnet som totalsummen økes på. Grensen brukes ikke på en enkelt vare i en gitt liste når kildegrensen overskrider den definerte grensen.</td>
<td>Følgende eksempel viser eksempelformatet med bruk av datakilder. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Dette er resultatet format kjøring som viser en liste over vanlige elementer. <a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>Eksemplet nedenfor viser samme format som ble justert for å vise listen over vanlige elementer i grupper når en enkelt satsvis må inneholde varer med total vekt som ikke må overskride grensen på 9. <a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Dette er et resultat av kjøringen justerte format. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Merk:</strong> grensen gjelder ikke for det siste elementet i listen opprinnelse som verdien (11) for sin grense kilde (vekt) overskrider den definerte grensen (9). Bruk enten funksjonen <strong>WHERE</strong> eller <strong>Aktivert</strong>-uttrykket for det tilsvarende elementet i formatet for å ignorere (hoppe over) underordnede lister ved rapportgenerering (om nødvendig).</td>
</tr>
<tr class="odd">
<td>FILTER (liste, betingelse)</td>
<td>Returnerer den angitte listen filtrert etter den angitte betingelsen ved å endre spørringen. I motsetning til <strong>WHERE</strong>-funksjonen, brukes den angitte betingelsen på databasenivået til en ER-datakilde av typen Tabellposter.</td>
<td>FILTER (leverandører, Vendors.VendGroup = &quot;40&quot;) returnerer listen over bare leverandører som hører til gruppen for leverandørenes "40" når <strong>leverandøren</strong> er konfigurert som ER datakilden som refererer til den <strong>VendTable</strong> tabell</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logiske funksjoner

| Funksjon                                                                                | beskrivelse                                                                                                                                                                                                                                                                     | Eksempel                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SAKEN (uttrykk, alternativ 1, føre til 1 \[, alternativ 2, føre til 2\] ... \[, standard resultatet\]) | Evaluer den angitte uttrykksverdien mot de angitte alternative alternativene. Returner resultatet av alternativet som er lik verdien for uttrykket. Hvis ikke, returner det valgfrie angitte standardresultatet (den siste parameteren som ikke innledes av et alternativ). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "VINTER", "11", "VINTER", "12", "VINTER", "")** returnere strengen **"VINTER"** når gjeldende dato for Dynamics 365 for Operations-økten er mellom oktober og desember. Ellers returneres en tom streng. |
| IF (betingelse, verdi 1, verdi 2)                                                        | Returner den angitte verdien 1 når den gitte betingelsen er oppfylt. Hvis ikke, returner verdien 2. Hvis verdien 1 og verdien 2 er poster eller post lister, får resultatet bare feltene som finnes i begge listene.                                                                     | **IF (1=2, "betingelsen er oppfylt", "betingelsen er ikke oppfylt")** returnerer strengen **"betingelse er ikke oppfylt"**.                                                                                                                                                      |
| NOT (betingelse)                                                                         | Returner den omvendte logiske verdien til den angitte betingelsen.                                                                                                                                                                                                                   | **NOT (SANN)** returnerer **USANN**.                                                                                                                                                                                                                            |
| OG (betingelse 1\[, betingelse 2,... \])                                                 | Returnerer **SANN** hvis *alle* angitte betingelser er oppfylt. Hvis ikke, returnes **USANN**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** returnerer **SANN**. **AND (1=2, "a"="a")** returnerer **USANN**.                                                                                                                                                                           |
| ELLER (betingelse 1\[, betingelse 2,... \])                                                  | Returnerer **USANN** hvis *alle* angitte betingelser ikke er oppfylt. Returnerer **SANN** hvis *en* angitt betingelse er oppfylt.                                                                                                                                                                 | **OR (1=2, "a"="a")** returnerer **SANN**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Matematiske funksjoner

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funksjon</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (tall)</td>
<td>Returner den absolutte verdien for det angitte tallet (tallet uten fortegnet).</td>
<td><strong>ABS (-1)</strong> returnerer <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (tall, potens)</td>
<td>Returner resultatet av å sette det angitte positive tallet til angitt potens.</td>
<td><strong>POWER (10, 2)</strong> returnerer <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (streng, desimaltegn, skilletegn for siffergruppering)</td>
<td>Konverter den angitte strengen til et tall. Det angitte symbolet brukes til å skille heltall og deler av et desimaltall, og det angitte tusenskilletegnet brukes også.</td>
<td><strong>NUMBERVALUE (&quot;1 234,56&quot;, &quot;,&quot;, &quot;&quot;)</strong> returnerer verdien <strong>1234,56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (streng)</td>
<td>Konverter den angitte strengen til et tall. Komma og punktum-tegn (.) regnes som desimalskilletegn, og en foranstilt bindestrek (-) brukes som negativt fortegn. Iverksett et unntak hvis det finnes andre ikke-numeriske tegn i den angitte strengen.</td>
<td><strong>VERDI (&quot;1 234,56&quot;)</strong> genererer et unntak.</td>
</tr>
<tr class="odd">
<td>ROUND (tall, desimaler)</td>
<td>Returnerer det angitte tallet som avrundes til angitt antall desimaler:
<ul>
<li>Hvis den angitte desimalverdien er større enn 0 (null), avrundes de angitte tallene til det er angitt antall desimalplasser.</li>
<li>Hvis den angitte desimalverdien er 0 (null), avrundes det angitte tallet til nærmeste heltall.</li>
<li>Hvis den angitte desimalverdien er mindre enn 0 (null), avrundes de angitte tallene til venstre for desimalpunktet.</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> avrunder til to desimalplasser og returnerer <strong>1200.77</strong>. <strong>ROUND (1200.767, -3)</strong> avrunder til nærmeste multiplum av 1 000, og returnerer <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (tall, desimaler)</td>
<td>Returnerer det angitte tallet som avrundes ned (mot null) til angitt antall desimaler. <strong>Obs!</strong>  Denne funksjonen fungerer som <strong>ROUND</strong>, men den avrunder alltid ned det angitte tallet.</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> avrunder ned til to desimalplasser og returnerer <strong>1200.76</strong>. <strong>ROUNDDOWN (1700.767, -3)</strong> avrunder ned til nærmeste multiplum av 1 000, og returnerer <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (tall, desimaler)</td>
<td>Returnerer det angitte tallet som avrundes opp (alltid fra null) til angitt antall desimaler. <strong>Obs!</strong>  Denne funksjonen fungerer som <strong>ROUND</strong>, men den avrunder alltid opp det angitte tallet.</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> avrunder opp til to desimalplasser og returnerer <strong>1200.77</strong>. <strong>ROUNDUP (1200.767, -3)</strong> avrunder opp til nærmeste multiplum av 1 000, og returnerer <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

### <a name="record-functions"></a>Registreringsfunksjoner

| Funksjon             | Beskrivelse                                                                                                                                                                                                                                     | Eksempel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (liste) | Returner en **null**-post som har samme struktur som den angitte postlisten eller posten. **Obs!**  Denne funksjonen er foreldet. Bruk **EMPTYRECORD** i stedet.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** returnerer en ny, tom post som har samme struktur som listen som returneres av **SPLIT**-funksjonen. |
| EMPTYRECORD (post) | Returner en **null**-post som har samme struktur som den angitte postlisten eller posten. **Merk:** A **null** post er en der alle feltene har en tom verdi (**0**\[null\] for tall, en tom streng for strenger, og så videre). | **EMPTYRECORD (SPLIT ("abc", 1))** returnerer en ny, tom post som har samme struktur som listen som returneres av **SPLIT**-funksjonen.   |

### <a name="text-functions"></a>Tekstfunksjoner

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funksjon</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (streng)</td>
<td>Returner den angitte strengen, som konverteres til store bokstaver.</td>
<td><strong>ØVRE (&quot;eksempel&quot;)</strong> returnerer <strong>&quot;eksempel&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (streng)</td>
<td>Returner den angitte strengen, som konverteres til små bokstaver.</td>
<td><strong>LAVERE (&quot;eksempel&quot;)</strong> returnerer <strong>&quot;eksempel&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (streng, antall tegn)</td>
<td>Returner det angitte antallet tegn fra begynnelsen av den angitte strengen.</td>
<td><strong>VENSTRE (&quot;utvalg&quot;, 3)</strong> returnerer <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (streng, antall tegn)</td>
<td>Returner det angitte antallet tegn fra slutten av den angitte strengen.</td>
<td><strong>HØYRE (&quot;utvalg&quot;, 3)</strong> returnerer <strong>&quot;Eksempeletikett&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (streng, startposisjon, antall tegn)</td>
<td>Returner det angitte antallet tegn fra den angitte strengen med start fra angitt posisjon.</td>
<td><strong>MID (&quot;utvalg&quot;, 2, 3)</strong> returnerer <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (streng)</td>
<td>Returner antall tegn i den angitte strengen.</td>
<td><strong>LEN (&quot;eksempel&quot;)</strong> returnerer <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (tall)</td>
<td>Returner strengen av tegn som refereres av det angitte Unicode-tallet.</td>
<td><strong>CHAR (255)</strong> returnerer <strong>&quot;ÿ&quot;</strong>. <strong>Merk:</strong> Den returnerte strengen avhenger av kodingen som er valgt i det overordnede FIL-formatelementet. Listen over støttede kodinger finnes i emnet <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodingsklasse</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (streng 1 [, streng 2, …])</td>
<td>Returner alle angitte tekststrenger, som settes sammen til én streng.</td>
<td><strong>Sette sammen (&quot;abc&quot;, &quot;def&quot;)</strong> returnerer <strong>&quot;abcdef&quot;</strong>. <strong>Merk:</strong> uttrykket <strong>&quot;abc&quot;&amp;&quot;def&quot;</strong> returnerer også <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (streng, mønster, erstatning)</td>
<td>Returner den angitte strengen, der alle forekomster av tegn i den angitte mønsterstrengen erstattes med tegnene i den tilsvarende posisjonen for den angitte erstattingsstrengen.</td>
<td><strong>OVERSETT (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (streng, mønster, erstatning, flagg for vanlig uttrykk)</td>
<td>Når flagget for vanlig uttrykk er <strong>sann</strong>, returneres den angitte strengen, som endres ved å bruke det vanlige uttrykket som er angitt som et mønsterargument for denne funksjonen. Dette uttrykket brukes til å søke etter tegn som skal erstattes. Tegn i det angitte erstatningsargumentet brukes til å erstatte tegnene som blir funnet. Når flagget for vanlig uttrykk er <strong>usann</strong>, fungerer denne funksjonen som <strong>TRANSLATE</strong>.</td>
<td>  <strong>ERSTATTE (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, SANN)</strong> bruker et vanlig uttrykk som fjerner alle ikke-numeriske symboler, og returnerer <strong>&quot;19234564971&quot;</strong>. <strong>ERSTATTE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, USANN)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (inndata)</td>
<td>Returner angitte inndata, som konverteres til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for den gjeldende forekomsten av Dynamics 365 for Operations. For verdier for <strong>real</strong>-typen begrenses strengkonverteringen til to desimalplasser.</td>
<td>Hvis Dynamics-365 for operasjoner forekomst serverens lokale innstilling er definert som <strong>EN-US</strong>, <strong>tekst (nå ())</strong> returnerer den gjeldende Dynamics 365 for Øktdato, 17/12/2015-operasjoner som tekststrengen <strong>&quot;17/12/2015 07:59:23 AM&quot;</strong>. <strong>TEKST (1/3)</strong> returnerer <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (streng 1, streng 2 [, streng, 3, ...])</td>
<td>Returner den angitte strengen, som formateres ved hjelp av forekomster av <strong>%N</strong> med det <em>n</em>. argumentet. Argumentene er strenger. Hvis et argument ikke er angitt for en parameter, returneres parameteren som <strong>&quot;%n&quot;</strong> i strengen. For verdier for <strong>real</strong>-typen begrenses strengkonverteringen til to desimalplasser.</td>
<td>I dette eksemplet returnerer <strong>PaymentModel</strong>-datakilden listen over kundeposter via <strong>Kunder</strong>-komponenten og behandlingsdatodatoverdien via <strong>ProcessingDate</strong>-feltet. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>I ER formatet som er utformet for å generere en elektronisk fil for utvalgte kunder, <strong>PaymentModel</strong> er valgt som en datakilde, og kontroller prosessflyten. Et unntak for sluttbrukere iverksettes når en valgt kunde stoppes for datoen da rapporten behandles. Formelen som er utviklet for denne typen behandlingskontroll kan bruke følgende ressurser:
<ul>
<li>Dynamics 365 for Operations-etiketten SYS70894, som har følgende tekst:
<ul>
<li><strong>For EN-US-språk:</strong>&quot;ingenting å skrive ut&quot;</li>
<li><strong>For DE språk:</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operations-etiketten SYS18389, som har følgende tekst:
<ul>
<li><strong>For EN-US-språk:</strong>&quot;kunde %1 er sperret for %2.&quot;</li>
<li><strong>For DE språk:</strong>&quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Her er formelen som kan utformes: FORMAT (kjede (@&quot;SYS70894&quot;,&quot;. &quot;@&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (modell. ProcessingDate, &quot;d&quot;)) Hvis en rapport er behandlet for den <strong>Litware detaljhandel kunde</strong> på 17 desember 2015 i den <strong>EN-US</strong> kultur og <strong>EN-US</strong> språk, denne formelen returnerer følgende tekst kan presenteres som en Unntaksmelding for sluttbrukeren: &quot;ingenting å skrive ut. Kunden Litware Retail er sperret for 17/12/2015.&quot; Hvis samme rapport behandles den<strong> Litware detaljhandel kunde</strong> på 17 desember 2015 i den <strong>DE</strong> kultur og <strong>DE</strong> språk, denne formelen returnerer følgende tekst, som bruker et annet datoformat: &quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot; <strong>Obs!</strong>  Følgende syntaks brukes i ER-formler for etiketter:
<ul>
<li><strong>For etiketter fra Dynamics 365 for operasjonsressurser:</strong> <strong>@&quot;X&quot;</strong>, der X er etikett-IDen i applikasjonsobjekttreet (AOT)</li>
<li><strong>For etiketter som befinner seg i konfigurasjoner ER:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, der X er etikett-IDen i konfigurasjonen ER</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (tall, format)</td>
<td>Returner strengrepresentasjonen for det angitte tallet i det angitte formatet. (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standard</a> og <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">tilpasset</a>.) Denne funksjonen kjøres i konteksten bestemmer kulturen som brukes til å formatere tall.</td>
<td>For EN-US-kultur <strong>NUMBERFORMAT (0,45, &quot;p&quot;)</strong> returnerer <strong>&quot;45,00%&quot;</strong>. <strong>NUMBERFORMAT (10,45, &quot;#&quot;)</strong> returnerer <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (tall, språk, valuta, flagg for utskrift av valutanavn, desimaler)</td>
<td>Returnerer nummeret stavet (konvertert) til tekststrenger i det definerte språket. Språkkoden er valgfri: Når den er definert som tom streng, brukes språkkoden for kjørekontekst (definert for generering mapper og filer) i stedet. Valutakoden er valgfri. Når den er definert som tom streng, hentes firmavalutaen. Merk at parameteren <strong>Skriv ut valutanavn</strong> og parameteren <strong>Desimaler</strong> bare analyseres for følgende språkkoder: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Merk at parameteren <strong>Skriv ut valutanavn</strong> bare analyseres for Dynamics 365 for Operations-firmaer med landkontekst som støtter valutanedgangen.</td>
<td>NUMERALSTOTEXT (1234,56, &quot;EN&quot;, &quot;&quot;, USANN, 2) returnerer "Ett tusen to hundre og trettifire og 56" NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, USANN, 0) returnerer "Stopp dwadzieścia" NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, SANN, 2) returnerer "евроцент Сто двадцать евро 21"</td>
</tr>
<tr class="odd">
<td>PADLEFT (streng, lengde, utfyllingstegn)</td>
<td>Returnerer en streng med en angitt lengde der begynnelsen av gjeldende streng fylles ut med angitte tegn.</td>
<td>PADLEFT (“1234”, 10, “ “) returnerer tekststrengen “      1234”</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Datainnsamlingsfunksjoner

Funksjon

beskrivelse

Eksempel

FORMATELEMENTNAME ()

Returnerer navnet på elementet til det gjeldende formatet. Returnerer tom streng når flagget **Samle inn utdatadetaljer** for de gjeldende filene er slått av.

Se oppgaveveiledningen **ER Bruke data med formatet utdata for telling og summering** (en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning **) for å lære mer om bruk av disse funksjonene.

SUMMER (nøkkel streng for summering, område1 vilkårstrengen, verdi1 vilkårstrengen \[, område2 vilkårstrengen, verdi2 vilkårstrengen,... \])

Returnerer en sum av nodeverdier (med navnet som er definert som en nøkkel) for XML, som har blitt samlet inn i løpet av denne formatkjøringen, og som oppfyller de angitte betingelsene (en kombinasjon av område og verdi). Returnerer en nullverdi når flagget **Samle inn utdatadetaljer **for de gjeldende filene er deaktivert.

SUMIF (nøkkelstreng for summering, kriterieområdestreng, kriterieverdistreng)

Returnerer en sum av nodeverdier (med navnet som er definert som en nøkkel) for XML, som har blitt samlet inn i løpet av denne formatkjøringen, og som oppfyller de angitte betingelsene (område og verdi). Returnerer en nullverdi når flagget **Samle inn utdatadetaljer **for de gjeldende filene er deaktivert.

COUNTIFS (område1 vilkårstrengen, verdi1 vilkårstrengen \[, område2 vilkårstrengen, verdi2 vilkårstrengen,... \])

Returnerer antallet noder for XML, som har blitt samlet inn i løpet av denne formatkjøringen, og som oppfyller de angitte betingelsene (en kombinasjon av område og verdi). Returnerer en nullverdi når flagget **Samle inn utdatadetaljer **for de gjeldende filene er deaktivert.

COUNTIF (områdekriteriestreng, kriterieverdistreng)

Returnerer antallet noder for XML, som har blitt samlet inn i løpet av denne formatkjøringen, og som oppfyller den angitte betingelsen (område og verdi). Returnerer en nullverdi når flagget **Samle inn utdatadetaljer **for de gjeldende filene er deaktivert.

COLLECTEDLIST (område1 vilkårstrengen, verdi1 vilkårstrengen \[, område2 vilkårstrengen, verdi2 vilkårstrengen,... \])

Returnerer en liste over nodeverdier for XML, som har blitt samlet inn i løpet av denne formatkjøringen, og som oppfyller de angitte betingelsene (område og verdi). Returnerer en tom liste når flagget **Samle inn utdatadetaljer **for de gjeldende filene er slått av.

### <a name="other-business-domainspecific-functions"></a>Andre funksjoner (spesifikke for forretningsområder)

| Funksjon                                                                         | beskrivelse                                                                                                                                                                                                                                                        | Eksempel                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (beløp, kildevaluta, målvaluta, dato, firma)        | Konverter det angitte pengebeløpet fra kildevalutaen til målvalutaen ved å bruke innstillingene for det aktuelle Dynamics 365 for Operations-firmaet på den angitte datoen.                                                                            | **CONVERTCURRENCY (1, "EUR", "NOK", TODAY(), "DEMF")** returnerer tilsvarende én euro i amerikanske dollar på gjeldende øktdato, basert på innstillingene for DEMF-firmaet.                                                                                                                                  |
| ROUNDAMOUNT (tall, desimaler, avrundingsregel)                                       | Avrunder det angitte beløpet i henhold til den angitte avrundingsregelen og det angitte antallet desimalplasser. **Obs!**  Avrundingaregelen må være angitt som en verdi av **RoundOffType**-opplistingen i Dynamics 365 for Operations.                          | Hvis du **modell. RoundOff** parameteren er satt til *** Downward *** **ROUNDAMOUNT (1000.787, 2, modell. RoundOff)** returnerer verdien **1000.78**. Hvis parameteren **model.RoundOff** er satt til **Normal** eller **Avrundes opp**, vil **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** returnere verdien **1000.79**. |
| CURCredRef (sifre)                                                              | Returner en kreditorreferanse basert på sifrene i det angitte fakturanummeret.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** returnerer **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (sifre)                                                                 | Returner en kreditorreferanse som et MOD97-uttrykk basert på sifrene i det angitte fakturanummeret.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** returnerer **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (sifre)                                                              | Returner en ISO-kreditorreferanse basert på sifrene og de alfabetiske symbolene i det angitte fakturanummeret. **Obs!**  Inndataparameteren må oversettes før den sendes til denne funksjonen for å eliminere symboler fra bokstaver som ikke er ISO-kompatible. | **ISOCredRef ("VEND-200002")** returnerer **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (streng, tall)                                  | Hent ekstra finansdimensjons-ID. Dimensjoner er representert i denne strengen som IDer atskilt med komma. Tall definerer seriekoden for den forespurte dimensjonen i denne strengen.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA, BB, kopi, DD, EE, FF, GG, HH", 3) returnerer "Kopi"                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Returnerer koden for det gjeldende firmaet som er loggført.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_BANK\_MOD\_10 (sifre)                                                       | Returnerer en kreditorreferanse som et MOD10-uttrykk basert på sifrene i det angitte fakturanummeret.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") returnerer 3                                                                                                                                                                                                                                                                   |
| Aktiva\_summen (fast aktivum kode, verdikode modell, startdato, sluttdato)               | Returnerer den klargjorte databeholderen for et anleggsmiddelbeløp for en periode.                                                                                                                                                                                         | Aktiva\_summen ("COMP-000001", "Gjeldende", dato1, dato2) returnerer beholderen forberedt data for anleggsmiddelet "COMP 000001" med verdimodellen "Gjeldende" for en periode fra dato1 til dato2.                                                                                                                        |
| Aktiva\_saldo (faste anleggsmidler kode, modell verdikode, Rapporteringsår, rapportering dato) | Returnerer den klargjorte databeholderen for faste anleggsmiddelsaldoer. Rapporteringsår må angis som en verdi for Dynamics-365 for Operations-opplistingen **AssetYear**.                                                                                           | Aktiva\_summen ("COMP-000001", "Gjeldende", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) returnerer forberedt data beholderen av saldoer for aktivaet "COMP-000001" med verdimodellen "Gjeldende" på de gjeldende 365 for operasjoner datoen for klientøkt.                                                                |

### <a name="functions-list-extension"></a>Funksjonslisteutvidelse

ER lar deg utvide listen over funksjoner som brukes i ER-uttrykk. Det er nødvendig med noe utvikling. Hvis du vil ha mer informasjon, kan du se [Utvide listen over elektroniske rapporteringsfunksjoner](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Se også
--------

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Utvide listen over elektroniske rapporteringsfunksjoner (ER)](general-electronic-reporting-formulas-list-extension.md)


