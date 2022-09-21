---
title: Kontrollere den konfigurerte ER-komponenten for å forhindre kjøretidsproblemer
description: Denne artikkelen forklarer hvordan du undersøker de konfigurerte komponentene for elektronisk rapportering (ER) for å forhindre kjøretidsproblemer som kan oppstå.
author: kfend
ms.date: 09/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 1ca59d6c26dbcf065adb952409da30002d951f62
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476861"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Kontrollere den konfigurerte ER-komponenten for å forhindre kjøretidsproblemer

[!include[banner](../includes/banner.md)]

Alle konfigurerte komponenter i [ER-](general-electronic-reporting.md)[format](er-overview-components.md#format-components-for-outgoing-electronic-documents) og [modelltilordning](er-overview-components.md#model-mapping-component) kan [valideres](er-fillable-excel.md#validate-an-er-format) på utformingstidspunktet. Under denne valideringen kjører en konsekvenskontroll for å forhindre kjøretidsproblemer som kan oppstå, for eksempel kjøringsfeil og ytelsesreduksjon. For hvert problem som blir funnet, vises banen til et problemelement. For enkelte problemer er en automatisk reparasjon tilgjengelig.

Som standard brukes valideringen automatisk i følgende tilfeller for en ER-konfigurasjon som inneholder de tidligere nevnte ER-komponentene:

- Du [importerer](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) en ny versjon av en ER-konfigurasjon i din forekomst av Microsoft Dynamics 365 Finance.
- Du endrer statusen til den redigerbare ER-konfigurasjonen fra **Utkast** til **Fullført**.
- Du [rebaserer](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) en redigerbar ER-konfigurasjon ved å bruke en ny baseversjon.

Du kan eksplisitt kjøre denne valideringen. Velg ett av følgende tre alternativer, og følg fremgangsmåten som er angitt:

- Alternativ 1:

    1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
    2. I konfigurasjonstreet i venstre rute velger du den ønskede ER-konfigurasjonen som inneholder ER-format- eller ER-modelltilordningskomponenten.
    3. I **Versjoner**-hurtigfanen velger du den ønskede versjonen av den valgte ER-konfigurasjonen.
    4. Velg **Valider** i handlingsruten.

- Alternativ 2, for et ER-format:

    1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
    2. I konfigurasjonstreet i venstre rute velger du den ønskede ER-konfigurasjonen som inneholder ER-formatkomponenten.
    3. I **Versjoner**-hurtigfanen velger du den ønskede versjonen av den valgte ER-konfigurasjonen.
    4. Velg **Utforming** i handlingsruten.
    5. På siden **Formatutforming**, i handlingsruten, velger du **Valider**.

- Alternativ 3, for en ER-modelltilordning:

    1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
    2. I konfigurasjonstreet i venstre rute velger du den ønskede ER-konfigurasjonen som inneholder ER-modelltilordningskomponenten.
    3. I **Versjoner**-hurtigfanen velger du den ønskede versjonen av den valgte ER-konfigurasjonen.
    4. Velg **Utforming** i handlingsruten.
    5. På siden **Tilordning av modell til datakilde** velger du **Utforming** i handlingsruten.
    6. På siden **Modelltilordningsutforming** i handlingsruten velger du **Valider**.

Hvis du vil hoppe over valideringen når konfigurasjonen importeres, følger du disse trinnene.

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. Sett alternativet **Valider konfigurasjonen etter import** til **Nei**.

Hvis du vil hoppe over valideringen når du endrer eller rebaserer versjonsstatusen, følger du disse trinnene.

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. Sett **Hopp over validering ved konfigurasjonens statusendring og rebasering** til **Ja**.

ER bruker følgende kategorier til å gruppere kontrollinspeksjoner for konsekvens:

- **Kjøring** – Inspeksjoner som oppdager kritiske problemer som kan forekomme under kjøring. Disse problemene er for det meste på **feil**-nivå. 
- **Ytelse** – Inspeksjoner som oppdager problemer som kan føre til ineffektiv kjøring av konfigurerte ER-komponenter. Disse problemene er for det meste på **Advarsel**-nivå.
- **Dataintegritet** – Inspeksjoner som oppdager problemer som kan føre til datatap eller kjøretidsproblemer. Disse problemene er for det meste på **Advarsel**-nivå.

## <a name="list-of-inspections"></a>Liste over inspeksjoner

Tabellen nedenfor gir en oversikt over inspeksjonene som ER gir. Hvis du vil ha mer informasjon om disse inspeksjonene, bruker du koblingene i den første kolonnen for å gå til de relevante delene i denne artikkelen. Disse delene forklarer typene av komponenter som ER gir inspeksjoner for, og hvordan du kan konfigurere ER-komponenter på nytt for å forhindre problemer.

<table>
<thead>
<tr>
<th>Navn</th>
<th>Kategori</th>
<th>Nivå</th>
<th>Melding</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Typekonvertering</a></td>
<td>Kjøring</td>
<td>Feil</td>
<td>
<p>Kan ikke konvertere uttrykk av typen &lt;type&gt; til felt av typen typen &lt;type&gt;.</p>
<p><b>Kjøretidsfeil:</b> Unntak for type</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Type kompatibilitet</a></td>
<td>Kjøring</td>
<td>Feil</td>
<td>
<p>Det konfigurerte uttrykket kan ikke brukes som binding for gjeldende formatelement til en datakilde, fordi dette uttrykket returnerer verdien av datatypen &lt;type&gt;, som er utenfor området for datatyper som støttes av det gjeldende formatelementet av typen &lt;type&gt;.</p>
<p><b>Kjøretidsfeil:</b> Unntak av typen</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Mangler konfigurasjonselement</a></td>
<td>Kjøring</td>
<td>Feil</td>
<td>
<p>Finner ikke banen &lt;bane&gt;.</p>
<p><b>Kjøretidsfeil:</b> Element av konfigurasjons&lt;banen&gt; finnes ikke</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Utføring av et uttrykk med FILTER-funksjon</a></td>
<td>Kjøring</td>
<td>Feil</td>
<td>
<p>Listeuttrykket for FILTER-funksjonen er ikke queryable.</p>
<p><b>Kjøretidsfeil:</b> Filtrering støttes ikke. Valider konfigurasjonen for å få flere detaljer om dette.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>Kjøring av en GROUPBY-datakilde</a></td>
<td>Kjøring</td>
<td>Feil</td>
<td>Banen &lt;bane&gt; støtter ikke spørring.</td>
</tr>
<tr>
<td>Kjøring</td>
<td>Feil</td>
<td>
<p>Group by-funksjonen kan ikke utføres med spørring.</p>
<p><b>Kjøretidsfeil:</b> Group by-funksjonen kan ikke utføres med spørring.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>Kjøring av en JOIN-datakilde</a></td>
<td>Kjøring</td>
<td>Feil</td>
<td>
<p>Kan ikke bli med i en liste&lt;bane&gt; som ikke er et filter i spørring.</p>
<p><b>Kjøretidsfeil:</b> Den Joined-forbundne funksjonen må være et filteruttrykk. Det beregnede feltet er kalt opp felt.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Funksjonen FILTER foretrekkes foran WHERE</a></td>
<td>Ytelse</td>
<td>Advarsel</td>
<td>Bruk av FILTER-funksjonen for uttrykket er foretrukket foran WHERE fra et ytelsesperspektiv. Velg Løs for å erstatte automatisk.</td>
</tr>
<tr>
<td><a href='#i8'>Funksjonen ALLITEMSQUERY foretrekkes foran ALLITEMS</a></td>
<td>Ytelse</td>
<td>Advarsel</td>
<td>Bruk av ALLITEMSQUERY-funksjonen for uttrykket er foretrukket foran ALLITEMS fra et ytelsesperspektiv. Velg Løs for å erstatte automatisk.</td>
</tr>
<tr>
<td><a href='#i9'>Vurdering ved saker med tomme lister</a></td>
<td>Kjøring</td>
<td>Advarsel</td>
<td>
<p>Liste&lt;banen&gt; har ingen kontroll for tom liste, og dette kan føre til en feil ved kjøretid. Legg til en kontroll for sak med tom liste.</p>
<p><b>Kjøretidsfeil:</b> Listen er tom ved &lt;bane&gt;</p>
<p><b><a href='#i9a'>Potensielt problem</a>:</b> Linjen blir fylt opp én gang, mens en datakilde som den er utfylt fra, inneholder flere poster</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Utføring av et uttrykk med FILTER-funksjon (bufring)</a></td>
<td>Kjøring</td>
<td>Feil</td>
<td>
<p>FILTER-funksjonen kan ikke brukes på den valgte typen datakilde. En datakilde for tabellposteringstypen er bare tilgjengelig når den ikke er bufret og ikke har lagt til nestede datakilder manuelt.</p>
<p><b>Kjøretidsfeil:</b> Filtrering støttes ikke. Valider konfigurasjonen for å få flere detaljer om dette.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Manglende binding</a></td>
<td>Kjøring</td>
<td>Advarsel</td>
<td>
<p>Banen &lt;bane&gt; har ingen binding til noen datakilder når den bruker modellens tilordning.</p>
<p><b>Kjøretidsfeil:</b> Banen &lt;bane&gt; er ikke bundet</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Ikke koblet mal</a></td>
<td>Dataintegritet</td>
<td>Advarsel</td>
<td>Filen &lt;navn&gt; er ikke koblet til noen filkomponenter og vil bli fjernet etter endring av status for konfigurasjonsversjon.</td>
</tr>
<tr>
<td><a href='#i13'>Ikke synkronisert format</a></td>
<td>Dataintegritet</td>
<td>Advarsel</td>
<td>Definert navn &lt;komponentnavn&gt; finnes ikke i Excel-regnearket &lt;regnearknavn&gt;</td>
</tr>
<tr>
<td><a href='#i14'>Ikke synkronisert format</a></td>
<td>Dataintegritet</td>
<td>Advarsel</td>
<td>
<p>Koden &lt;Kodet Word-innholdskontroll&gt; finnes ikke i Word-malfil</p>
<p><b>Kjøretidsfeil:</b> Koden &lt;Kodet Word-innholdskontroll&gt; finnes ikke i Word-malfil.</p>
</td>
</tr>
<tr>
<td><a href='#i15'>Ingen standardtilordning</a></td>
<td>Dataintegritet</td>
<td>Feil</td>
<td>
<p>Det finnes mer enn én modelltilordning for datamodellen &lt;modellnavn (rotbeskrivelse)&gt; i konfigurasjonene &lt;konfigurasjonsnavn atskilt med komma&gt;. Angi én av konfigurasjonene som standard</p>
<p><b>Kjøretidsfeil:</b> Det finnes mer enn én modelltilordning for datamodellen &lt;modellnavn (rotbeskrivelse)&gt; i konfigurasjonene &lt;konfigurasjonsnavn atskilt med komma&gt;. Angi én av konfigurasjonene som standard.</p>
</td>
</tr>
<tr>
<td><a href='#i16'>Inkonsekvent innstilling for topptekst- eller bunntekstkomponenter</a></td>
<td>Dataintegritet</td>
<td>Feil</td>
<td>
<p>Topptekst/bunntekst (&lt;komponenttype: Topptekst eller Bunntekst&gt;) er inkonsekvent</p>
<p><b>Kjøretid:</b> Den sist konfigurerte komponenten brukes i kjøretid hvis utkastversjonen av det konfigurerte ER-formatet utføres.</p>
</td>
</tr>
<tr>
<td><a href='#i17'>Inkonsekvent innstilling av sidekomponent</a></td>
<td>Dataintegritet</td>
<td>Feil</td>
<td>Det er mer enn to områdekomponenter uten replikering. Fjern unødvendige komponenter.</td>
</tr>
<tr>
<td><a href='#i18'>Utføring av et uttrykk med ORDERBY-funksjon</a></td>
<td>Kjøring</td>
<td>Feil</td>
<td>
<p>Listeuttrykket for ORDERBY-funksjonen kan ikke spørres.</p>
<p><b>Kjøretidsfeil:</b> Sortering støttes ikke. Valider konfigurasjonen for å få flere detaljer om dette.</p>
</td>
</tr>
<tr>
<td><a href='#i19'>Foreldet appartefakt</a></td>
<td>Dataintegritet</td>
<td>Advarsel</td>
<td>
<p>Elementet &lt;bane&gt; er merket som foreldet.<br>eller<br>Elementet &lt;bane&gt; er merket som foreldet med meldingen &lt;meldingstekst&gt;.</p>
<p><b>Eksempel på kjøretidsfeil:</b> Finner ikke klassen '&lt;bane&gt;'.</p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Typekonvertering

ER kontrollerer om datatypen for et datamodellfelt er kompatibel med datatypen for et uttrykk som er konfigurert som binding for feltet. Hvis datatypene ikke er kompatible, oppstår det en valideringsfeil i ER-modelltilordningsutforming. Meldingen du mottar, sier at ER ikke kan konvertere et uttrykk av typen A til et felt av typen B.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start å konfigurere ER-datamodellen og ER-modelltilordningskomponentene samtidig.
2. Legg til et felt med navnet **X** i datamodelltreet, og velg **Heltall** som datatype.

    ![X-feltet og heltallsdatatype er lagt til i datamodustreet på datamodellsiden.](./media/er-components-inspections-01.png)

3. I uformingen av modelltilordning legger du til en datakilde av typen **Beregnet felt** i ruten **Datakilder**.
4. Gi den nye datakilden navnet **Y**, og konfigurer den slik at den inneholder uttrykket `INTVALUE(100)`.
5. Bind **X** til **Y**.
6. I datamodeldesigner endrer du datatypen for **X**-feltet fra **Heltall** til **Int64**.
7. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**.

    ![Validere den redigerbare modelltilordningskomponenten på siden Modelltilordningsutforming.](./media/er-components-inspections-01.gif)

8. Velg **Valider** for å kontrollere modelltilordningskomponenten for valgt ER-konfigurasjon på siden **Konfigurasjoner**.

    ![Inspisering av modelltilordningskomponenten på siden Konfigurasjoner.](./media/er-components-inspections-01a.png)

9. Legg merke til at det oppstår en valideringsfeil. Meldingen angir at verdien for typen **Heltall** som uttrykket `INTVALUE(100)` i datakilden **Y** returnerer, ikke kan lagres i datamodellfeltet **X** av typen **Int64**.

Følgende illustrasjon viser kjøretidsfeilen som oppstår hvis du ignorerer advarselen og velger **Kjør** for å kjøre et format som er konfigurert til å bruke modelltilordningen.

![Kjøretidsfeil på siden Formatutforming.](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Oppdater datamodellstrukturen ved å endre datatypen for datamodellfeltet, slik at det samsvarer med datatypen for uttrykket som er konfigurert for bindingen for dette feltet. I eksemplet ovenfor må datatypen for **X**-feltet endres tilbake til **Heltall**.

#### <a name="option-2"></a>Alternativ 2

Oppdater modelltilordningen ved å endre uttrykket for datakilden som er bundet til datamodellfeltet. I det forrige eksemplet må uttrykket for **Y**-datakilden endres til `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Type kompatibilitet

ER kontrollerer om datatypen for et formatelement er kompatibel med datatypen for et uttrykk som er konfigurert som binding for formatelementet. Hvis datatypene ikke er kompatible, oppstår det en valideringsfeil i ER-operasjonsutforming. Meldingen du motttar, sider at det konfigurerte uttrykket ikke kan brukes som binding for det gjeldende formatelementet til en datakilde, fordi dette uttrykket returnerer en verdi av datatypen A, som er utenfor området for datatypene som støttes av det gjeldende formatelementet av typen B.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start å konfigurere ER-datamodellen og ER-formatkomponentene samtidig.
2. Legg til et felt med navnet **X** i datamodelltreet, og velg **Heltall** som datatype.
3. Legg til et formatelement av den typen **Numerisk** i formatstrukturtreet.
4. Navnet på det nye formatelementet **Y**. I feltet **Numerisk type** velger du **Heltall** som datatype.
5. Bind **X** til **Y**.
6. I formatstrukturtreet endrer du datatypen til **Y**-formatelementet fra **Heltall** til **Int64**.
7. Velg **Valider** for å kontrollere den redigerbare formatkomponenten på siden **Formatutforming**.

    ![Validerer type kompatibilitet på Formatutforming-siden.](./media/er-components-inspections-02.gif)

8. Legg merke til at det oppstår en valideringsfeil. Meldingen angir at det konfigurerte uttrykket bare kan godta **Int64**-verdier. Derfor kan verdien i datamodellfeltet **X** av typen **Heltall** ikke angis i formatelementet **Y**.

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Oppdater formatstrukturen ved å endre datatypen for formatelementet **Numerisk**, slik at det samsvarer med datatypen for uttrykket du har konfigurert for bindingen for dette elementet. I det foregående eksemplet må verdien for **Numerisk type** for **X**-formatelementet endres tilbake til **Heltall**.

#### <a name="option-2"></a>Alternativ 2

Oppdater formattilordningen for **X**-formatelementet ved å endre uttrykket fra `model.X` til `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Mangler konfigurasjonselement

ER kontrollerer om bindingsuttrykkene bare inneholder datakilder som er konfigurert i den redigerbare ER-komponenten. For hver binding som inneholder en datakilde som mangler i den redigerbare ER-komponenten, oppstår det en valideringsfeil i ER-operasjonsutforming eller i ER-modelltilordningsutformingen.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start å konfigurere ER-datamodellen og ER-modelltilordningskomponentene samtidig.
2. Legg til et felt med navnet **X** i datamodelltreet, og velg **Heltall** som datatype.

    ![Datamodelltre med X-felt og heltallsdatatype på datamodellsiden.](./media/er-components-inspections-01.png)

3. I uformingen av modelltilordning legger du til en datakilde av typen **Beregnet felt** i ruten **Datakilder**.
4. Gi den nye datakilden navnet **Y**, og konfigurer den slik at den inneholder uttrykket `INTVALUE(100)`.
5. Bind **X** til **Y**.
6. Slett datakilden **Y** i ruten **Datakilder** i modelltilordningsutformingen.
7. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**.

    ![Inspeksjon av den redigerbare ER-modelltilordningskomponenten på siden Modelltilordningsutforming.](./media/er-components-inspections-03.gif)

8. Legg merke til at det oppstår en valideringsfeil. Meldingen angir at bindingen for **X**-datamodellfeltet inneholder banen som refererer til **Y**-datakilden, men denne datakilden finnes ikke.

### <a name="automatic-resolution"></a>Automatisk løsning

Velg **Opphev binding** for å reparere dette problemet automatisk ved å fjerne den manglende datakildebindingen.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Opphev **X**-datamodellfeltet for å slutte å referere til den ikke-eksisterende **Y**-datakilden.

#### <a name="option-2"></a>Alternativ 2

I modelltilordningsutformingen legger du til datakilden **Y** på nytt i ruten **Datakilder**.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Utføring av et uttrykk med FILTER-funksjon

Den innebygde ER-funksjonen [FILTER](er-functions-list-filter.md) brukes til å få tilgang til programtabeller, visninger eller dataenheter ved å plassere ett enkelt SQL-kall for å hente de nødvendige dataene som en liste med poster. En datakilde for **Postliste**-typen brukes som et argument av denne funksjonen, og angir programkilden for kallet. ER kontrollerer om en direkte SQL-spørring kan opprettes til en datakilde som det refereres til i `FILTER`-funksjonen. Hvis en direktespørring ikke kan opprettes, oppstår det en valideringsfeil i ER-modelltilordningsutforming. Meldingen du mottar, sier at ER-uttrykket som inneholder funksjonen `FILTER`, ikke kan kjøres under kjøring.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-modelltilordningskomponenten.
2. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
3. Gi den nye datakilden navnet **Leverandør**. I **Tabell**-feltet velger **VendTable** for å angi at denne datakilden skal be om tabellen VendTable.
4. Legg til en datakilde av typen **Beregnet felt**.
5. Gi den nye datakilden navnet **FilteredVendor**, og konfigurer den slik at den inneholder uttrykket `FILTER(Vendor, Vendor.AccountNum="US-101")`.
6. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**, og kontroller at `FILTER(Vendor, Vendor.AccountNum="US-101")`-uttrykket i **Leverandør**-datakilden kan spørres.
7. Endre **Leverandør**-datakilden ved å legge til et nestet felt av typen **Beregnet felt** for å hente det relevante leverandørkontonummeret.
8. Gi det nye nestede feltet navnet **$AccNumber**, og konfigurer det, slik at det inneholder uttrykket `TRIM(Vendor.AccountNum)`.
9. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**, og kontroller at `FILTER(Vendor, Vendor.AccountNum="US-101")`-uttrykket i **Leverandør**-datakilden kan spørres.

    ![Verifisering av uttrykket som har FILTER-funksjonen, kan spørres på siden Modelltilordningsutforming.](./media/er-components-inspections-04.gif)

10. Legg merke til at det oppstår en valideringsfeil, fordi **Leverandør**-datakilden inneholder et nestet felt av typen **Beregnet felt** som ikke tillater at uttrykket for datakilden **FilteredVendor** oversettes til den direkte SQL-setningen.

Følgende illustrasjon viser kjøretidsfeilen som oppstår hvis du ignorerer advarselen og velger **Kjør** for å kjøre et format som er konfigurert til å bruke modelltilordningen.

![Kjøretidsfeil som oppstår når du kjører det redigerbare formatet på formatutformingssiden.](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

I stedet for å legge til et nestet felt av typen **Beregnet felt** i datakilden **Leverandør** legger du til det nestede feltet **$AccNumber** i datakilden **FilteredVendor** og konfigurerer det, slik at det inneholder uttrykket `TRIM(FilteredVendor.AccountNum)`. På denne måten kan uttrykket `FILTER(Vendor, Vendor.AccountNum="US-101")` kjøres på SQL-nivå og beregne det nestede feltet **$AccNumber** etterpå.

#### <a name="option-2"></a>Alternativ 2

Endre uttrykket for **FilteredVendor**-datakilden fra `FILTER(Vendor, Vendor.AccountNum="US-101")` til `WHERE(Vendor, Vendor.AccountNum="US-101")`. Vi ikke anbefaler at du endrer uttrykket for en tabell som har et stort datavolum (transaksjonstabell), fordi alle postene vil bli hentet, og valget av nødvendige poster vil bli utført i minnet. Derfor kan denne fremgangsmåten føre til dårlig ytelse. Hvis du vil ha mer informasjon, kan du se [funksjonen WHERE ER f](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>Kjøring av en GROUPBY-datakilde

Datakilden **GROUPBY** deler spørringsresultatet inn i grupper med poster, vanligvis for å gjøre én eller flere aggregasjoner på hver gruppe. Hver **GROUPBY**-datakilde kan konfigureres slik at den kjøres enten på databasenivå eller i minnet. Når en **GROUPBY**-datakilde er konfigurert slik at den kjøres på databasenivå, kontrollerer ER for eksempel om en direkte SQL-spørring kan opprettes til en datakilde som det refereres til i datakilden. Hvis en direktespørring ikke kan opprettes, oppstår det en valideringsfeil i ER-modelltilordningsutforming. Meldingen du mottar, sier at den konfigurerte **GROUPBY**-datakilden ikke kan kjøres under kjøring.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-modelltilordningskomponenten.
2. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
3. Gi den nye datakilden navnet **Trans**. I **Tabell**-feltet velger du **VendTrans** for å angi at denne datakilden skal be om en VendTrans-tabell.
4. Legg til en datakilde av typen **Grupper etter**.
5. Gi den nye datakilden navnet **GroupedTrans**, og konfigurer den på følgende måte:

    - Velg **Trans**-datakilden som kilde for poster som skal grupperes.
    - I feltet **Utførelseslokasjon** velger du **Spørring** for å angi at du vil kjøre datakilden på databasenivå.

    ![Konfigurere datakilden på siden Rediger GroupBy-parametere.](./media/er-components-inspections-05a.gif)

6. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**, og kontroller at den konfigurerte **GroupedTrans**-datakilden kan spørres.
7. Endre **Trans**-datakilden ved å legge til et nestet felt av typen **Beregnet felt** for å hente det relevante leverandørkontonummeret.
8. Gi den nye datakilden navnet **$AccNumber**, og konfigurer den slik at den inneholder uttrykket `TRIM(Trans.AccountNum)`.

    ![Konfigurere datakilden på siden Modelltilordningsutforming.](./media/er-components-inspections-05a.png)

9. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**, og kontroller at den konfigurerte **GroupedTrans**-datakilden kan spørres.

    ![Validering av ER-modelltilordningskomponenten og kontroll av at datakilden GroupedTrans kan spørres på siden Modelltilordningsutforming.](./media/er-components-inspections-05b.png)

10. Legg merke til at det oppstår en valideringsfeil, fordi **Trans**-datakilden inneholder et nestet felt av typen **Beregnet felt** som ikke tillater at kallet etter datakilden **GroupedTrans** oversettes til den direkte SQL-setningen.

Følgende illustrasjon viser kjøretidsfeilen som oppstår hvis du ignorerer advarselen og velger **Kjør** for å kjøre et format som er konfigurert til å bruke modelltilordningen.

![Kjøretidsfeil som oppstår når advarselen ignoreres på siden Formatutforming.](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

I stedet for å legge til et nestet felt av typen **Beregnet felt** i datakilden **Trans** legger du til det nestede feltet **$AccNumber** for elementet **GroupedTrans.lines** i datakilden **GroupedTrans** og konfigurerer det, slik at det inneholder uttrykket `TRIM(GroupedTrans.lines.AccountNum)`. På denne måten kan datakilden **GroupedTrans** kjøres på SQL-nivå og beregne det nestede feltet **$AccNumber** etterpå.

#### <a name="option-2"></a>Alternativ 2

Endre verdien for feltet **Utførelseslokasjon** for datakilden **GroupedTrans** fra **Spørring** til **I minnet**. Vi anbefaler ikke at du endrer verdien for en tabell som har et stort datavolum (transaksjonstabell), fordi alle postene vil bli hentet, og gruppering og aggregering vil bli utført i minnet. Derfor kan denne fremgangsmåten føre til dårlig ytelse.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>Kjøring av en JOIN-datakilde

[JOIN](er-join-data-sources.md)-datakilden kombinerer poster fra to eller flere databasetabeller basert på relaterte felt. Hver **JOIN**-datakilde kan konfigureres slik at den kjøres enten på databasenivå eller i minnet. Når en **JOIN**-datakilde er konfigurert slik at den kjøres på databasenivå, kontrollerer ER for eksempel om en direkte SQL-spørring kan opprettes til datakilder som det refereres til i datakilden. Hvis en SQL-spørring ikke kan opprettes med minst én referert datakilde, oppstår det en valideringsfeil i ER-modelltilordningsutforming. Meldingen du mottar, sier at den konfigurerte **JOIN**-datakilden ikke kan kjøres under kjøring.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-modelltilordningskomponenten.
2. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
3. Gi den nye datakilden navnet **Leverandør**. I **Tabell**-feltet velger **VendTable** for å angi at denne datakilden skal be om tabellen VendTable.
4. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
5. Gi den nye datakilden navnet **Trans**. I **Tabell**-feltet velger du **VendTrans** for å angi at denne datakilden skal be om en VendTrans-tabell.
6. Legg til en datakilde av typen **Beregnet felt** som det nestede feltet i **Leverandør**-datakilden.
7. Gi den nye datakilden navnet **FilteredTrans**, og konfigurer den slik at den inneholder uttrykket `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.
8. Legg til en datakilde av typen **Join**.
9. Gi den nye datakilden navnet **JoinedList**, og konfigurer den på følgende måte:

    1. Legg til **Leverandør**-datakilden som det første postsettet som skal slås sammen.
    2. Legg til **Vendor.FilteredTrans**-datakilden som det andre postsettet som skal slås sammen. Velg **INNER** som type.
    3. I feltet for **Kjøring** velger du **Spørring** for å angi at du vil kjøre datakilden på databasenivå.

    ![Konfigurere datakilden på Join-utformingssiden.](./media/er-components-inspections-06a.gif)

10. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**, og kontroller at den konfigurerte **JoinedList**-datakilden kan spørres.
11. Endre uttrykket for **Vendor.FilteredTrans**-datakilden fra `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` til `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**, og kontroller at den konfigurerte **JoinedList**-datakilden kan spørres.

    ![Validering av den redigerbare modelltilordningskomponenten og kontroll av at JoinedList-datakilden kan spørres på siden Modelltilordningsutforming.](./media/er-components-inspections-06b.png)

13. Legg merke til at det oppstår en valideringsfeil fordi uttrykket for **Vendor.FilteredTrans**-datakilden ikke kan oversettes til det direkte SQL-kallet. I tillegg tillater ikke det direkte SQL-kallet at kallet for **JoinedList**-datakilden oversettes til den direkte SQL-setningen.

    ![Kjøretidsfeil fra den mislykkede valideringen av JoinedList-datakilden på siden Modelltilordningsutforming.](./media/er-components-inspections-06c.png)

Følgende illustrasjon viser kjøretidsfeilen som oppstår hvis du ignorerer advarselen og velger **Kjør** for å kjøre et format som er konfigurert til å bruke modelltilordningen.

![Kjøre det redigerbare formatet på formatutformingssiden.](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Endre uttrykket for **Vendor.FilteredTrans**-datakilde fra `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` tilbake til `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, som advarselen anbefaler.

![Oppdatert uttrykk for datakilde på siden Modelltilordningsutforming.](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Alternativ 2

Endre verdien for feltet **Utførelse**-feltet for datakilden **JoinedList** fra **Spørring** til **I minnet**. Vi anbefaler ikke at du endrer verdien for en tabell som har et stort datavolum (transaksjonstabell), fordi alle postene vil bli hentet, og sammenkoblingen skjer i minnet. Derfor kan denne fremgangsmåten føre til dårlig ytelse. Det vises en valideringsadvarsel som informerer deg om denne risikoen.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Funksjonen FILTER foretrekkes foran WHERE

Den innebygde ER-funksjonen [FILTER](er-functions-list-filter.md) brukes til å få tilgang til programtabeller, visninger eller dataenheter ved å plassere ett enkelt SQL-kall for å hente de nødvendige dataene som en liste med poster. [WHERE](er-functions-list-where.md)-funksjonen henter alle poster fra den angitte kilden og registrerer valget i minnet. En datakilde for **Postliste**-typen brukes som et argument for begge funksjoner og angir en kilde for hentinga av postene. ER kontrollerer om et direkte SQL-anrop kan opprettes til en datakilde som det refereres til i **WHERE**-funksjonen. Hvis et direkteanrop kan opprettes, oppstår det en valideringsadvarsel i ER-modelltilordningsutforming. Meldingen du mottar, anbefaler at du bruker **FILTER**-funksjonen i stedet for **WHERE**-funksjonen for å forbedre effektiviteten.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-modelltilordningskomponenten.
2. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
3. Gi den nye datakilden navnet **Trans**. I **Tabell**-feltet velger du **VendTrans** for å angi at denne datakilden skal be om en VendTrans-tabell.
4. Legg til en datakilde av typen **Beregnet felt** som det nestede feltet i **Leverandør**-datakilden.
5. Gi den nye datakilden navnet **FilteredTrans**, og konfigurer den slik at den inneholder uttrykket `WHERE(Trans, Trans.AccountNum="US-101")`.
6. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
7. Gi den nye datakilden navnet **Leverandør**. I **Tabell**-feltet velger **VendTable** for å angi at denne datakilden skal be om tabellen VendTable.
8. Legg til en datakilde av typen **Beregnet felt**.
9. Gi den nye datakilden navnet **FilteredVendor**, og konfigurer den slik at den inneholder uttrykket `WHERE(Vendor, Vendor.AccountNum="US-101")`.
10. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**.

    ![Kontrollere den redigerbare modelltilordningskomponenten på siden Modelltilordningsutforming.](./media/er-components-inspections-07a.png)

11. Legg merke til at valideringsadvarsler anbefaler at du bruker **FILTER**-funksjonen i stedet for **WHERE** -funksjonen for datakildene **FilteredVendor** og **FilteredTrans**.

    ![Anbefaling om å bruke FILTER-funksjonen i stedet for WHERE-funksjonen på siden Modelltilordningsutforming.](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Velg **Løs** for å erstatte **WHERE**-funksjonen med **FILTER**-funksjonen i uttrykket for alle datakilder som vises i rutenettet i **Advarsler**-fanen for denne typen inspeksjon.

Du kan også velge raden for en enkelt advarsel i rutenettet og deretter velge **Rett opp valgte**. I dette tilfellet endres uttrykket automatisk bare i datakilden som er nevnt i den valgte advarselen.

![Hvis du velger Løs, erstattes WHERE-funksjonen med FILTER-funksjonen automatisk på siden Modelltilordningsutforming.](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Manuell løsing

Du kan justere uttrykkene for alle datakildene i valideringsrutenettet, manuelt ved å erstatte **WHERE**-funksjonen med **FILTER**-funksjonen.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Funksjonen ALLITEMSQUERY foretrekkes foran ALLITEMS

De innebygde ER-funksjonene [ALLITEMS](er-functions-list-allitems.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md) returnerer utflatet **Postliste**-verdi som består av en liste over poster som representerer alle elementer som samsvarer med den angitte banen. ER kontrollerer om et direkte SQL-anrop kan opprettes til en datakilde som det refereres til i **ALLITEMS**-funksjonen. Hvis et direkteanrop kan opprettes, oppstår det en valideringsadvarsel i ER-modelltilordningsutforming. Meldingen du mottar, anbefaler at du bruker **ALLITEMSQUERY**-funksjonen i stedet for **ALLITEMS**-funksjonen for å forbedre effektiviteten.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-modelltilordningskomponenten.
2. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
3. Gi den nye datakilden navnet **Leverandør**. I **Tabell**-feltet velger **VendTable** for å angi at denne datakilden skal be om tabellen VendTable.
4. Legg til en datakilde av typen **Beregnet felt** for å hente postene for flere leverandører.
5. Gi den nye datakilden navnet **FilteredVendor**, og konfigurer den slik at den inneholder uttrykket `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.
6. Legg til en datakilde av typen **Beregnet felt** for å hente transaksjonene for alle filtrerte leverandører.
7. Gi den nye datakilden navnet **FilteredVendorTrans**, og konfigurer den slik at den inneholder uttrykket `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.
8. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**.

    ![Inspeksjon av den redigerbare modelltilordningskomponenten på siden Modelltilordningsutforming.](./media/er-components-inspections-08a.png)

9. Legg merke til at det oppstår en valideringsadversel. Meldingen anbefaler at du bruker **ALLITEMSQUERY**-funksjonen i stedet for **ALLITEMS**-funksjonen for **FilteredVendorTrans**-datakilden.

    ![Anbefaling om å bruke ALLITEMSQUERY-funksjonen i stedet for ALLITEMS-funksjonen på siden Modelltilordningsutforming.](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Velg **Løs** for å erstatte **ALLITEMS**-funksjonen med **ALLITEMSQUERY**-funksjonen i uttrykket for alle datakilder som vises i rutenettet i **Advarsler**-fanen for denne typen inspeksjon.

Du kan også velge raden for en enkelt advarsel i rutenettet og deretter velge **Rett opp valgte**. I dette tilfellet endres uttrykket automatisk bare i datakilden som er nevnt i den valgte advarselen.

![Valg av Løs på siden Modelltilordningsutforming.](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Manuell løsing

Du kan justere uttrykkene for alle datakildene som er nevnt i valideringsrutenettet, manuelt ved å erstatte **ALLITEMS**-funksjonen med **ALLITEMSQUERY**-funksjonen.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Vurdering ved saker med tomme lister

Du kan konfigurere ER-format- eller modelltilordningskomponenten til å hente feltverdien for en datakilde av typen **Postliste**. ER kontrollerer om utformingen vurderer saken der en datakilde som kalles, ikke inneholder noen poster (det vil si at den er tom), for å forhindre kjøretidsfeil når en verdi hentes fra et felt for en ikke-eksisterende post.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start å konfigurere ER-datamodellen, ER-modelltilordningen og ER-formatkomponentene samtidig.
2. Legg til et rotelement som heter **Root3**, i datamodelltreet.
3. Endre **Root3**-elementet ved å legge til et nestet element av typen **Postliste**.
4. Gi den nye nestede elementet navnet **Leverandør**.
5. Endre **Leverandør**-elementet på følgende måte:

    - Legg til et nestet felt av typen **Streng**, og gi det navnet **Navn**.
    - Legg til et nestet felt av typen **Streng**, og gi det navnet **AccountNumber**.

    ![Legge til nestede felt på datamodellsiden.](./media/er-components-inspections-09a.png)

6. I uformingen av modelltilordning legger du til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter** i ruten **Datakilder**.
7. Gi den nye datakilden navnet **Leverandør**. I **Tabell**-feltet velger **VendTable** for å angi at denne datakilden skal be om tabellen VendTable.
8. Legg til en datakilde av typen **Generell \\ Inndataparameter** for å søke etter en leverandørkonto i dialogboksen for kjøretid.
9. Gi den nye datakilden navnet **RequestedAccountNum**. I feltet **Etikett** angir du **Leverandørens kontonummer**. I feltet for **navn på Operations-datatype** beholder du standardverdien være, **Beskrivelse**.
10. Legg til en datakilde av typen **Beregnet felt** for å filtrere en leverandør som det spørres om.
11. Gi den nye datakilden navnet **FilteredVendor**, og konfigurer den slik at den inneholder uttrykket `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Bind datamodellelementene til konfigurerte datakilder på følgende måte:

    - Bind **FilteredVendor** til **Leverandør**.
    - Bind **FilteredVendor.AccountNum** til **Vendor.AccountNumber**.
    - Bind **FilteredVendor.'name()'** til **Vendor.Name**.

    ![Binde datamodellelementer på siden Modelltilordningsutforming.](./media/er-components-inspections-09b.png)

13. I formatstrukturtreet legger du til følgende elementer for å generere et utgående dokument i XML-format som inneholder leverandørdetaljene:

    1. Legg til rot-XML-elementet **Setning**.
    2. For XML-elementet **Setning** legger du til det nestede XML-elementet **Part**.
    3. For XML-elementet **Part** legger du til følgende nestede XML-attributter:

        - Navn
        - AccountNum

14. Bind formatelementer til angitte datakilder på følgende måte:

    - Bind formatelementet **Setning\\Part\\Navn** til datakildefeltet **model.Vendor.Name**.
    - Bind formatelementet **Setning\\Part\\AccountNum** til datakildefeltet **model.Vendor.AccountNumber**.

15. Velg **Valider** for å kontrollere den redigerbare formatkomponenten på siden **Formatutforming**.

    ![Validering av formatelementene du har bundet til datakilder på siden Formatutforming.](./media/er-components-inspections-09c.png)

16. Legg merke til at det oppstår en valideringsfeil. Meldingen angir at det kan oppstå en feil for de konfigurerte formatkomponentene **Setning\\Part\\Navn** og **Setning\\Part\\AccountNum** under kjøring hvis listen `model.Vendor` er tom.

    ![Valideringsfeil om en mulig feil for de konfigurerte formatkomponentene.](./media/er-components-inspections-09d.png)

Følgende illustrasjon viser kjøretidsfeilen som oppstår hvis du ignorerer advarselen og velger **Kjør** for å kjøre formatet og velger kontonummeret for en ikke-eksisterende leverandør. Fordi den forespurte leverandøren ikke finnes, vil `model.Vendor` være tom (det vil si at den ikke inneholder noen poster).

![Kjøretidsfeil som oppstår under formattilordningskjøringen.](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Du kan velge **Fjern binding** for den valgte raden i rutenettet i fanen **Advarsler**. Bindingen som det pekes til i **Bane**-kolonnen, fjernes automatisk fra formatelementene.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Du kan binde formatelementet **Setning\\Part\\Navn** til datakildeelementet `model.Vendor`. Under kjøringen kaller denne bindingen datakilden `model.Vendor` først. Når `model.Vendor` returnerer en tom postliste, kjøres ikke de nestede formatelementene. Det skjer derfor ingen valideringsadvarsler for denne formatkonfigurasjonen.

![Binding av formatelementet til datakildeelementet på formatutformingssiden.](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Alternativ 2

Endre bindingen for formatelementet **Setning\\Part\\Navn** fra `model.Vendor.Name` til `FIRSTORNULL(model.Vendor).Name`. Den oppdaterte bindingen utfører en betinget konvertering av den første posten av datakilden `model.Vendor` av typen **Postliste** til en ny datakilde av typen **Post**. Den nye datakilden inneholder samme sett med felt.

- Hvis minst én post er tilgjengelig i datakilden `model.Vendor`, fylles feltene i denne oppføringen ut med verdiene i feltene for den første posten i datakilden `model.Vendor`. I dette tilfellet vil den oppdaterte bindingen returnere leverandørnavnet.
- Ellers blir hvert felt i posten som opprettes, fylt med standardverdien for datatypen til det feltet. I dette tilfellet returneres den tomme strengen som standardverdi for **Streng**-datatypen.

Det oppstår derfor ingen valideringsadvarsler for området for **Setning\\Part\\Navn**-formatelementet når det er bundet til uttrykket `FIRSTORNULL(model.Vendor).Name`.

![Endret binding løser valideringsadvarsler på formateringssiden for utforming.](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Alternativ 3

Hvis du eksplisitt vil angi dataene som legges inn i et generert dokument når datakilden `model.Vendor` for typen **Postliste** returnerer ingen poster (teksten **Ikke tilgjengelig** i dette eksemplet), endrer du bindingen for **Setning\\Part\\Navn** fra `model.Vendor.Name` til `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Du kan også bruke uttrykket `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Tilleggsvurdering

Inspeksjon advarer også om et annet mulig problem. Når du binder **Setning\\Part\\Navn** og **Setning\\Part\\AccountNum** til de riktige feltene i datakilden `model.Vendor` av typen **Postliste**, blir disse bindingene som standard kjørt og tar verdiene i de aktuelle feltene for den første posten i datakilden `model.Vendor`, hvis listen ikke er tom.

Fordi du ikke har bundet **Setning\\Part** til datakilden `model.Vendor`, vil ikke **Setning\\Part**-elementet gjentas for hver post i datakilden `model.Vendor` under formateringskjøring. I stedet blir et generert dokument fylt ut med informasjon fra bare den første posten i postlisten, hvis listen inneholder flere poster. Derfor kan det være et problem hvis formatet skal fylle et generert dokument med informasjon om alle leverandørene fra datakilden `model.Vendor`. Du kan løse dette problemet ved å binde **Setning\\Part**-elementet til datakilden `model.Vendor`.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Utføring av et uttrykk med FILTER-funksjon (bufring)

Flere innebygde ER-funksjoner, inkludert [FILTER](er-functions-list-filter.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md), brukes til å få tilgang til programtabeller, visninger eller dataenheter ved å plassere ett enkelt SQL-kall for å hente de nødvendige dataene som en liste med poster. En datakilde av **Postliste**-typen brukes som et argument for hver av disse funksjonene og angir en programkilde for kallet. ER kontrollerer om et direkte SQL-anrop kan opprettes til en datakilde som det refereres til i én av disse funksjonene. Hvis et direkteanrop ikke kan opprettes fordi datakilden ble merket som [bufret](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), oppstår det en valideringsfeil i ER-modelltilordningsutforming. Meldingen du mottar, sier at ER-uttrykket som inneholder én av disse funksjonene, ikke kan kjøres under kjøring.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-modelltilordningskomponenten.
2. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
3. Gi den nye datakilden navnet **Leverandør**. I **Tabell**-feltet velger **VendTable** for å angi at denne datakilden skal be om tabellen VendTable.
4. Legg til en datakilde av typen **Generell \\ Inndataparameter** for å søke etter en leverandørkonto i dialogboksen for kjøretid.
5. Gi den nye datakilden navnet **RequestedAccountNum**. I feltet **Etikett** angir du **Leverandørens kontonummer**. I feltet for **navn på Operations-datatype** beholder du standardverdien være, **Beskrivelse**.
6. Legg til en datakilde av typen **Beregnet felt** for å filtrere en leverandør som det spørres om.
7. Gi den nye datakilden navnet **FilteredVendor**, og konfigurer den slik at den inneholder uttrykket `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
8. Merk den konfigurerte **Leverandør**-datakilden som hurtigbufret.

    ![Konfigurasjon av modelltilordningskomponenten på siden Modelltilordningsutforming.](./media/er-components-inspections-10a.gif)

9. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**.

    ![Validering av FILTER-funksjonen som også brukes av datakilden for bufret leverandør på siden Modelltilordningsutforming.](./media/er-components-inspections-10a.png)

10. Legg merke til at det oppstår en valideringsfeil. Meldingen angir at **FILTER**-funksjonen ikke kan brukes på den bufrede **Leverandør**-datakilden.

Følgende illustrasjon viser kjøretidsfeilen som oppstår hvis du ignorerer advarselen og velger **Kjør** for å kjøre formatet.

![Kjøretidsfeil som oppstår under formattilordningskjøring på siden Formatutforming.](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Fjern **Buffer**-flagget fra **Leverandør**-datakilden. Datakilden **FilteredVendor** vil deretter bli kjørbar, men **Leverandør**-datakilden som det refereres til i tabellen VendTable, vil bli brukt hver gang **FilteredVendor**-dsatakilden kalles.

#### <a name="option-2"></a>Alternativ 2

Endre uttrykket for **FilteredVendor**-datakilden fra `FILTER(Vendor, Vendor.AccountNum="US-101")` til `WHERE(Vendor, Vendor.AccountNum="US-101")`. I dette tilfellet vil datakilden **Leverandør** som det henvises til i tabellen VendTable, bare brukes i det første kallet til **Leverandør**-datakilden. Valget av poster vil imidlertid bli utført i minnet. Derfor kan denne fremgangsmåten føre til dårlig ytelse.

## <a name="missing-binding"></a><a id="i11"></a>Manglende binding

Når du konfigurerer en ER-formatkomponent, tilbys den grunnleggende ER-datamodellen som en standard datakilde for ER-formatet. Når det konfigurerte ER-formatet kjøres, brukes [standard modelltilordning](er-country-dependent-model-mapping.md) for den grunnleggende modellen til å fylle datamodellen med programdata. ER-formatutformingen viser en advarsel hvis du binder et formatelement til et datamodellelement som ikke er bundet til en datakilde i modelltilordningen som for øyeblikket er valgt som standardmodelltilordning for det redigerbare formatet. Denne typen bindinger kan ikke kjøres under kjøring, fordi formatet som kjøres, ikke kan fylle et bundet element med programdata. Derfor oppstår det en feil under kjøring.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start å konfigurere ER-datamodellen, ER-modelltilordningen og ER-formatkomponentene samtidig.
2. Legg til et rotelement som heter **Root3**, i datamodelltreet.
3. Endre **Root3**-elementet ved å legge til et nytt nestet element av typen **Postliste**.
4. Gi den nye nestede elementet navnet **Leverandør**.
5. Endre **Leverandør**-elementet på følgende måte:

    - Legg til et nestet felt av typen **Streng**, og gi det navnet **Navn**.
    - Legg til et nestet felt av typen **Streng**, og gi det navnet **AccountNumber**.

    ![Tillegg av nestede felt i elementet Leverandør på siden Datamodell.](./media/er-components-inspections-11a.png)

6. I uformingen av modelltilordning legger du til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter** i ruten **Datakilder**.
7. Gi den nye datakilden navnet **Leverandør**. I **Tabell**-feltet velger **VendTable** for å angi at denne datakilden skal be om tabellen VendTable.
8. Legg til en datakilde av typen **Generell \\ Inndataparameter** for å spørre om en leverandørkonto i dialogboksen for kjøretid.
9. Gi den nye datakilden navnet **RequestedAccountNum**. I feltet **Etikett** angir du **Leverandørens kontonummer**. I feltet for **navn på Operations-datatype** beholder du standardverdien være, **Beskrivelse**.
10. Legg til en datakilde av typen **Beregnet felt** for å filtrere en leverandør som det spørres om.
11. Gi den nye datakilden navnet **FilteredVendor**, og konfigurer den slik at den inneholder uttrykket `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Bind datamodellelementene til konfigurerte datakilder på følgende måte:

    - Bind **FilteredVendor** til **Leverandør**.
    - Bind **FilteredVendor.AccountNum** til **Vendor.AccountNumber**.

    > [!NOTE]
    > Datamodellfeltet **Vendor.Name** forblir ubundet.

    ![Datamodellelementer som er bundet til konfigurerte datakilder og et datamoduselement som forblir ubundet på siden for modelltilordningsutforming.](./media/er-components-inspections-11b.png)

13. I formatstrukturtreet legger du til følgende elementer for å generere et utgående dokument i XML-format som inneholder detaljene for leverandører som det spørres om:

    1. Legg til rot-XML-elementet **Setning**.
    2. For XML-elementet **Setning** legger du til det nestede XML-elementet **Part**.
    3. For XML-elementet **Part** legger du til følgende nestede XML-attributter:

        - Navn
        - AccountNum

14. Bind formatelementene til angitte datakilder på følgende måte:

    - Bind formatelementet **Setning\\Part** til datakildeelementet `model.Vendor`.
    - Bind formatelementet **Setning\\Part\\Navn** til datakildefeltet **model.Vendor.Name**.
    - Bind formatelementet **Setning\\Part\\AccountNum** til datakildefeltet **model.Vendor.AccountNumber**.

15. Velg **Valider** for å kontrollere den redigerbare formatkomponenten på siden **Formatutforming**.

    ![Validering av ER-formatkomponenten på siden for formatutforming.](./media/er-components-inspections-11c.png)

16. Legg merke til at det oppstår en valideringsadversel. Meldingen angir at **model.Vendor.Name**-datakildefeltet ikke er bundet til en datakilde i modelltilordningen som er konfigurert til å brukes av formatet. Derfor kan det hende at **Setning\\Part\\Navn** ikke fylles under kjøring, og det kan oppstå et kjøretidsunntak.

    ![Validerer ER-formatkomponenten på siden for formatutforming.](./media/er-components-inspections-11d.png)

Følgende illustrasjon viser kjøretidsfeilen som oppstår hvis du ignorerer advarselen og velger **Kjør** for å kjøre formatet.

![Kjøre det redigerbare formatet på formatutformingssiden.](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Endre den konfigurerte modelltilordningen ved å legge til en binding for **model.Vendor.Name**-datakildefeltet.

#### <a name="option-2"></a>Alternativ 2

Endre det konfigurerte formatet ved å fjerne bindingen for formatelementet **Setning\\Part\\Navn**.

## <a name="not-linked-template"></a><a id="i12"></a>Ikke koblet mal

Når du [manuelt](er-fillable-excel.md#manual-entry) konfigurerer en ER-formatkomponent til å bruke en mal til å generere et utgående dokument, må du legge til **Excel\\Fil**-elementet manuelt, legge til den nødvendige malen som et vedlegg til den redigerbare komponenten og velge dette vedlegget i det nye **Excel\\Fil**-elementet. På denne måten angir du at elementet som er lagt til, vil fylle den valgte malen under kjøring. Når du konfigurerer en formatkomponentversjon i **Utkast**-status, kan du legge til flere maler i den redigerbare komponenten, og deretter velge hver mal i elementet **Excel\\Fil** for å kjøre ER-formatet. På denne måten kan du se hvordan forskjellige maler fylles under kjøring. Hvis du har maler som ikke er valgt i noen **Excel\\Fil**-elementer, varsler ER-formatutformingen om at disse malene vil bli slettet fra den redigerbare ER-formatkomponentversjonen når statusen endres fra **Utkast** til **Fullført**.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-formatkomponenten.
2. I formatstrukturtreet legger du til **Excel\\Fil**-elementet.
3. For **Excel\\Fil**-elementet du nettopp la til, legger du til en Excel-arbeidsbokfil, **A.xlsx**, som et vedlegg. Bruk dokumenttypen som er konfigurert i [ER-parameterne](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) for å angi lagring for ER-formatmalene.
4. For **Excel\\Fil**-elementet legger du til en ny Excel-arbeidsbokfil, **B.xlsx**, som et vedlegg. Bruk samme dokumenttype som brukes for arbeidsbokfil A.
5. I **Excel\\Fil**-elementet velger du arbeidsbokfil A.
6. Velg **Valider** for å kontrollere den redigerbare formatkomponenten på siden **Formatutforming**.

    ![Validere den redigerbare formatkomponenten i arbeidsbokfilen på siden for formatutforming.](./media/er-components-inspections-12a.gif)

7. Legg merke til at det oppstår en valideringsadversel. Meldingen angir at arbeidsbokfilen B. xlsx ikke er koblet til noen komponenter, og at den vil bli fjernet etter at statusen for konfigurasjonsversjonen er endret.

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

Endre det konfigurerte formatet ved å fjerne alle maler som ikke er koblet til et **Excel\\Fil**-element.

## <a name="not-synced-format"></a><a id="i13"></a>Ikke synkronisert format

Når du [konfigurerer](er-fillable-excel.md) en ER-formatkomponent til å bruke en Excel-mal for å generere et utgående dokument, kan du legge til **Excel\\Fil**-elementet manuelt, legge til den nødvendige malen som et vedlegg til den redigerbare komponenten og velge dette vedlegget i det nye **Excel\\Fil**-elementet. På denne måten angir du at elementet som er lagt til, vil fylle den valgte malen under kjøring. Fordi den tillagte Excel-malen er utformet eksternt, kan det hende at det redigerbare ER-formatet inneholder Excel-navn som mangler i malen som er lagt til. ER-formatutformingen advarer deg om eventuelle inkonsekvenser mellom egenskapene til ER-formatelementer som refererer til navn som ikke er inkludert i Excel-malen som er lagt til.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-formatkomponenten.
2. I formatstrukturtreet legger du til **Excel\\Fil**-elementet **Rapport**.
3. For **Excel\\Fil**-elementet du nettopp la til, legger du til en Excel-arbeidsbokfil, **A.xlsx**, som et vedlegg. Bruk dokumenttypen som er konfigurert i [ER-parameterne](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) for å angi lagring for ER-formatmalene.

    > [!IMPORTANT]
    > Kontroller at Excel-arbeidsboken som er lagt til, ikke inneholder navnet **ReportTitle**.

4. Legg til **Excel\\Celle**-elementet **Tittel** som et nestet element i elementet **Rapport**. I feltet **Excel-område** angir du **ReportTitle**.
5. Velg **Valider** for å kontrollere den redigerbare formatkomponenten på siden **Formatutforming**.

    ![Validering av de nestede elementene og feltene på siden Formatutforming.](./media/er-components-inspections-13a.png)

6. Legg merke til at det oppstår en valideringsadversel. Meldingen angir at navnet **ReportTitle** ikke finnes på arket **Ark1** i Excel-malen du bruker.

    ![Valideringsadvarsel om at navnet ReportTitle ikke finnes på Ark1 av Excel-malen.](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Endre det konfigurerte formatet ved å fjerne alle elementer som refererer til Excel-navn som mangler i malen.

#### <a name="option-2"></a>Alternativ 2

[Oppdater](er-fillable-excel.md#template-import) det redigerbare ER-formatet ved å importere en Excel-mal. Strukturen til det redigerbare ER-formatet [synkroniseres](modify-electronic-reporting-format-reapply-excel-template.md) med strukturen til den importerte Excel-malen.

### <a name="additional-consideration"></a>Tilleggsvurdering

Hvis du vil lære hvordan formateringsstrukturen kan synkroniseres med en ER-mal i malredigeringsprogrammet for [Behandling av forretningsdokument](er-business-document-management.md), kan du se [Oppdatere strukturen for en forretningsdokumentmal](er-bdm-update-structure.md).

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>Ikke synkronisert med et Word-malformat

Når du [konfigurerer](er-fillable-excel.md) en ER-formatkomponent til å bruke en Word-mal til å generere et utgående dokument, kan du legge til **Excel\\Fil**-elementet manuelt, legge til den nødvendige Word-malen som et vedlegg til den redigerbare komponenten og velge dette vedlegget i det nye **Excel\\Fil**-elementet.

> [!NOTE]
> Når Word-dokumentet er vedlagt, presenterer ER-formatutformingen det redigerbare elementet som **Word\\Fil**.

På denne måten angir du at elementet som er lagt til, vil fylle den valgte malen under kjøring. Fordi den tillagte Word-malen er utformet eksternt, kan det hende at det redigerbare ER-formatet inneholder referanser til Word-innholdskontroller som mangler i malen som er lagt til. ER-formatutformingen advarer deg om eventuelle inkonsekvenser mellom egenskapene til ER-formatelementer som refererer til innholdskontroller som ikke er inkludert i Word-malen som er lagt til.

Hvis du vil ha et eksempel som viser hvordan dette problemet kan forekomme, kan du se [Konfigurere det redigerbare formatet for å skjule sammendragsdelen](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Endre det konfigurerte formatet ved å slette formelen **Fjernet** fra formatelementet som er nevnt i valideringsvarselet.

#### <a name="option-2"></a>Alternativ 2

Endre Word-malen som brukes, ved å [legge til](er-design-configuration-word-suppress-controls.md#tag-control) den obligatoriske koden i den relevante Word-innholdskontrollen.

## <a name="no-default-mapping"></a><a id="i15"></a>Ingen standardtilordning

Når inspeksjonen [Manglende binding](#i11) utføres, evalueres de kontrollerte formatbindingene mot bindingene til den relevante modelltilordningskomponenten. Ettersom du kan importere [flere](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER-modelltilordningskonfigurasjoner til Finance-forekomsten, og hver konfigurasjon kan inneholde den aktuelle modelltilordningskomponenten, må du velge én konfigurasjon som standardkonfigurasjon. Hvis du prøver å kjøre, redigere eller validere det kontrollerte ER-formatet, skjer det et unntak, og du får følgende melding: "Det finnes flere modeller for tilordning av datamodellen i \<model name (root descriptor)\> i konfigurasjonene \<configuration names separated by comma\>. Angi én av konfigurasjonene som standard.

Hvis du vil ha et eksempel som viser hvordan dette problemet kan oppstå og hvordan det kan ordnes, kan du se [Behandle flere avledede tilordninger for én modellrot](er-multiple-model-mappings.md).

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>Inkonsekvent innstilling for komponentene Topptekst eller Bbunntekst

Når du [konfigurerer](er-fillable-excel.md) en ER-formatkomponent til å bruke en Excel-mal til å generere et utgående dokument, kan du legge til komponenten **Excel\\Topptekst** for å fylle ut topptekster øverst i et regneark i en Excel-arbeidsbok. Du kan også legge til komponenten **Excel\\Bunntekst** for å fylle ut bunntekster nederst i et regneark. For hver komponent av typen **Excel\\Topptekst** eller **Excel\\Bunntekst** du legger til, må du gi egenskapen **Utseende for topptekst/bunntekst** en verdi for å angi sidene som komponenten skal kjøres for. Ettersom du kan konfigurere flere komponenter av typen **Excel\\Topptekst** eller **Excel\\Bunntekst** for én komponent av typen **Ark**, og du kan generere ulike topptekster eller bunntekster for forskjellige typer sider i et Excel-regneark, må du konfigurere én komponent av typen **Excel\\Topptekst** eller **Excel\\Bunntekst** for en bestemt verdi for egenskapen **Utseende for topptekst/bunntekst**. Hvis mer enn én komponent av typen **Excel\\Topptekst** eller **Excel\\Bunntekst** blir konfigurert for en bestemt verdi for egenskapen **Utseende for topptekst/bunntekst**, det oppstår en valideringsfeil og du får følgende feilmelding: "Topptekster/bunntekster (&lt;komponenttype: Topptekst eller Bunntekst&gt;) samsvarer ikke."

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Endre det konfigurerte formatet ved å slette en av de inkonsekvente komponentene av typen **Excel\\Topptekst** eller **Excel\\Bunntekst**.

#### <a name="option-2"></a>Alternativ 2

Endre verdien for egenskapen **Utseende for topptekst/bunntekst** for en av de inkonsekvente komponentene av typen **Excel\\Topptekst** eller **Excel\\Bunntekst**.

## <a name="inconsistent-setting-of-page-component"></a><a id="i17"></a>Inkonsekvent innstilling av sidekomponent

Når du [konfigurerer](er-fillable-excel.md) en ER-formatkomponent til å bruke en Excel-mal til å generere et utgående dokument, kan du legge til **Excel\\-side**-komponenten for å paginere et generert dokument ved å bruke ER-formler. For hver **Excel\\-side**-komponent du legger til, kan du legge til mange nestede [Område](er-fillable-excel.md#range-component)-komponenter og likevel være kompatibel med følgende [struktur](er-fillable-excel.md#page-component-structure):

- Den første nestede **Område**-komponenten kan konfigureres slik at egenskapen **Replikeringsretning** settes til **Ingen replikasjon**. Dette området brukes til å lage sidehoder i genererte dokumenter.
- Du kan legge til mange andre nestede **Område**-komponenter der egenskapen **Replikeringsretning** er satt til **Loddrett**. Disse områdene brukes til å fylle ut genererte dokumenter.
- Den siste nestede **Område**-komponenten kan konfigureres slik at egenskapen **Replikeringsretning** settes til **Ingen replikasjon**. Dette området brukes til å lage bunntekster på sider i genererte dokumenter og til å legge til de nødvendige sideskiftene.

Hvis du ikke følger denne strukturen for et ER-format i ER-formatdesigneren ved utforming, oppstår det en valideringsfeil, og du får følgende feilmelding: "Det er mer enn to områdekomponenter uten replikering. Fjern unødvendige komponenter".

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

Endre det konfigurerte formatet ved å endre egenskapen **Replikeringsretning** for alle inkonsekvente **Excel\\-område**-komponenter.

## <a name="executability-of-an-expression-with-orderby-function"></a><a id="i18"></a>Utføring av et uttrykk med ORDERBY-funksjon

Den innebygde [ORDERBY](er-functions-list-orderby.md) ER-funksjonen brukes til å sortere postene for en ER-datakilde for typen **[Postliste](er-formula-supported-data-types-composite.md#record-list)** som er angitt som et argument for funksjonen.

Argumenter for `ORDERBY`-funksjonen kan [angis](er-functions-list-orderby.md#syntax-2) til å sortere poster for apptabeller, visninger eller dataenheter ved å plassere ett enkelt databasekall for å hente de sorterte dataene som en liste over poster. En datakilde for **Postliste**-typen brukes som et argument av funksjonen, og angir appkilden for kallet.

ER kontrollerer om en direkte databasespørring kan opprettes til en datakilde som det refereres til i `ORDERBY`-funksjonen. Hvis en direktespørring ikke kan opprettes, oppstår det en valideringsfeil i ER-modelltilordningsutforming. Meldingen du mottar, sier at ER-uttrykket som inneholder funksjonen `ORDERBY`, ikke kan kjøres under kjøring.

Fremgangsmåten nedenfor viser hvordan dette problemet kan oppstå.

1. Start med å konfigurere ER-modelltilordningskomponenten.
2. Legg til en datakilde av typen **Dynamics 365 for Operations \\ Tabellposter**.
3. Gi den nye datakilden navnet **Leverandør**. I **Table**-feltet velger du **VendTable** for å angi at denne datakilden skal be om tabellen **VendTable**.
4. Legg til en datakilde av typen **Beregnet felt**.
5. Gi den nye datakilden navnet **OrderedVendors**, og konfigurer den slik at den inneholder uttrykket `ORDERBY("Query", Vendor, Vendor.AccountNum)`.
 
    ![Konfigurer datakildene på siden Modelltilordningsutforming.](./media/er-components-inspections-18-1.png)

6. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**, og kontroller at uttrykket i **OrderedVendors**-datakilden kan spørres.
7. Endre **Leverandør**-datakilden ved å legge til et nestet felt av typen **Beregnet felt** for å hente det relevante leverandørkontonummeret.
8. Gi det nye nestede feltet navnet **$AccNumber**, og konfigurer det, slik at det inneholder uttrykket `TRIM(Vendor.AccountNum)`.
9. Velg **Valider** for å kontrollere den redigerbare modelltilordningskomponenten på siden **Modelltilordningsutforming**, og kontroller at uttrykket i **Leverandør**-datakilden kan spørres.

    ![Verifisering av at uttrykket i leverandørdatakilden kan spørres på siden Modelltilordningsutforming.](./media/er-components-inspections-18-2.png)

10. Legg merke til at det oppstår en valideringsfeil, fordi **Leverandør**-datakilden inneholder et nestet felt av typen **Beregnet felt** som ikke tillater at uttrykket for datakilden **OrderedVendors** oversettes til den direkte databasesetningen. Den samme feilen skjer ved kjøretid hvis du ignorerer valideringsfeilen og velger **Kjør** for å kjøre denne modelltilordningen.

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

#### <a name="option-1"></a>Alternativ 1

I stedet for å legge til et nestet felt av typen **Beregnet felt** i datakilden **Leverandør** legger du til det nestede feltet **$AccNumber** i datakilden **FilteredVendors** og konfigurerer feltet, slik at det inneholder uttrykket `TRIM(FilteredVendor.AccountNum)`. På denne måten kan uttrykket `ORDERBY("Query", Vendor, Vendor.AccountNum)` kjøres på databasenivå, og beregnningen av det nestede feltet **$AccNumber** kan utføres etterpå.

#### <a name="option-2"></a>Alternativ 2

Endre uttrykket for **FilteredVendors**-datakilden fra `ORDERBY("Query", Vendor, Vendor.AccountNum)` til `ORDERBY("InMemory", Vendor, Vendor.AccountNum)`. Vi ikke anbefaler at du endrer uttrykket for en tabell som har et stort datavolum (transaksjonstabell), fordi alle postene vil bli hentet, og sorteringen av nødvendige poster vil bli utført i minnet. Derfor kan denne fremgangsmåten føre til dårlig ytelse.

## <a name="obsolete-application-artifact"></a><a id="i19"></a>Foreldet appartefakt

Når du utformer en ER-modelltilordningskomponent eller en ER-formatkomponent, kan du konfigurere et ER-uttrykk til å kalle en appartefakt i ER, for eksempel en databasetabell, en metode for en klasse osv. I Finance versjon 10.0.30 og senere kan du tvinge ER til å advare deg om at den artefakten som det refereres til, er merket i kildekoden som foreldet. Denne advarselen kan være nyttig, fordi foreldede artefakter til slutt vanligvis fjernes fra kildekoden. Hvis du blir informert om statusen til en artefakt, kan du slutte å bruke den foreldede artefakten i den redigerbare ER-komponenten før den fjernes fra kildekoden, noe som forhindrer at du kaller ikke-eksisterende programartefakter fra en ER-komponent ved kjøretid.

Aktiver funksjonen **Valider foreldede elementer for datakilder for elektronisk rapportering** i **Funksjonsbehandling** for å begynne å evaluere det foreldede attributtet til appartefakter under inspeksjonen av en redigerbar ER-komponent. Det foreldede attributtet evalueres for følgende typer appartefakter:

- Databasetabell
    - Felt i en tabell
    - Metode i en tabell
- Appklasse
    - Metode i en klasse

> [!NOTE]
> Det vises en advarsel under inspeksjonen av den redigerbare ER-komponenten for en datakilde som refererer til en foreldet artefakt bare når denne datakilden brukes i minst én bindende verdi av denne ER-komponenten.

> [!TIP]
> Når [SysObsoleteAttribute](../dev-ref/xpp-attribute-classes.md#sysobsoleteattribute)-klassen brukes til å varsle kompilatoren om å utstede advarselsmeldinger i stedet for feil, viser inspeksjonsvarslingen den angitte advarselen i kildekoden ved utformingstidspunktet på hurtigfanen **Detaljer** på siden **Modelltilordningsutforming** eller **Formatutforming**.

Illustrasjonen nedenfor viser valideringsvarselingen som skjer når det foreldede `DEL_Email`-feltet i `CompanyInfo`-apptabellen er bundet til et datamodellfelt ved å bruke den konfigurerte `company`-datakilden.

![Se gjennom valideringsadvarselene på hurtigfanen Detaljer på siden Modelltilordningsutforming.](./media/er-components-inspections-19a.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Ingen alternativer for automatisk korrigering av dette problemet er tilgjengelig.

### <a name="manual-resolution"></a>Manuell løsing

Endre den konfigurerte modelltilordningen eller formatet ved å fjerne alle bindinger til en datakilde som refererer til en foreldet appartefakt.

## <a name="additional-resources"></a>Tilleggsressurser

[ALLITEMS ER-funksjon](er-functions-list-allitems.md)

[ALLITEMSQUERY ER-funksjon](er-functions-list-allitemsquery.md)

[INT64VALUE ER-funksjon](er-functions-conversion-int64value.md)

[INTVALUE ER-funksjonen](er-functions-conversion-intvalue.md)

[FILTER ER-funksjon](er-functions-list-filter.md)

[WHERE ER-funksjonen](er-functions-list-where.md)

[Bruke JOIN-datakilder til å hente data fra flere programtabeller i ER-modelltilordninger](er-join-data-sources.md)

[Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md)

[Oversikt over administrasjon av forretningsdokument](er-business-document-management.md)

[Skjule Word-innholdskontroller i genererte rapporter](er-design-configuration-word-suppress-controls.md)

[Behandle flere avledede tilordninger for én modellrot](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
