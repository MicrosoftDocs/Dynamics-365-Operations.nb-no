---
title: Formeldesigner i elektronisk rapportering (ER)
description: Dette emnet beskriver hvordan du bruker formeldesigneren i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 07/30/2019
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
ms.openlocfilehash: e55ab83302cc75b1a9d9d3e4f06d2258697b31fc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771220"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formeldesigner i elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du bruker formeldesigneren i elektronisk rapportering (ER). Når du utformer et format for et bestemt elektronisk dokument i ER, kan du bruke formler for å transformere data slik at de oppfyller kravene for fullføringen og formatering for dokumentet. Disse formlene ligner på formler i Microsoft Excel. Ulike typer funksjoner støttes i formlene: tekst, dato og klokkeslett, matematisk logiske, informasjon, konvertering av datatype og andre (domenespesifikke forretningsfunksjoner).

## <a name="formula-designer-overview"></a>Oversikt over formeldesigner

ER støtter formeldesigneren. Under utformingen kan du derfor konfigurere uttrykk som kan brukes til følgende oppgaver ved kjøretid:

- Transformere data som er mottatt fra en programdatabase, og som skal angis i en ER-datamodell som er utformet for å være en datakilde for ER-formater. (Disse transformasjonene kan for eksempel inneholde filtrering, gruppering og datatypekonvertering.)
- Formater data som må sendes til et genererende elektronisk dokumentet i henhold til oppsettet og betingelsene for et bestemt ER-format. (Formatering kan for eksempel gjøres i samsvar med angitt språk eller kultur, eller koding).
- Kontroller opprettingen av elektroniske dokumenter. (For eksempel uttrykkene kan aktivere eller deaktivere utdataene for bestemte elementer i formatet, avhengig av behandling av data. De kan også avbryte opprettingen av dokumentet eller vise meldinger til brukere.)

Du kan åpne **Formeldesigner**-siden når du utfører følgende handlinger:

- Binder datakileelementer til datamodellkomponenter.
- Binder datakileelementer til formatkomponenter.
- Utfører vedlikehold av beregnede felt som er del av datakilder.
- Definerer synlighetsbetingelsene for inndataparametere for brukere.
- Utformer et formats transformasjoner.
- Definerer aktiveringen av betingelser for formatets komponenter.
- Definerer filnavn for formatets FILE-komponenter.
- Definerer betingelsene for prosesskontrollvalideringer.
- Definerer meldingsteksten for prosesskontrollvalideringer.

## <a name="designing-er-formulas"></a>Utforme ER-formler

### <a name="data-binding"></a>Databinding

ER-formeldesigneren kan brukes til å definere et uttrykk som transformerer data som mottas fra datakilder, slik at dataene kan angis i dataforbruker ved kjøretid:

- Fra programdatakilder og kjøretidsparametere til en ER-datamodellen
- Fra en ER-datamodell til et ER-format
- Fra programdatakilder og kjøretidsparametere til et ER-format

Illustrasjonen nedenfor viser utformingen av et uttrykk av denne typen. I dette eksemplet avrunder uttrykket verdien for **Intrastat.AmountMST**-feltet for Intrastat-tabellen til to desimalplasser og returnerer deretter den avrundede verdien.

[![Databinding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Illustrasjonen nedenfor viser hvordan et uttrykk av denne typen kan brukes. I dette eksemplet er resultatet av det utformede uttrykket angitt i **Transaction.InvoicedAmount**-komponenten for datamodellen **Avgiftsrapporteringsmodell**.

[![Databinding som brukes](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Under kjøringen avrunder den utformede formelen **ROUND (Intrastat.AmountMST, 2)** verdien i **AmountMST**-feltet for hver post i Intrastat-tabellen til to desimalplasser. Den angir så den avrundede verdien i **Transaction.InvoicedAmount**-komponenten i **Avgiftsrapportering**-datamodellen.

### <a name="data-formatting"></a>Dataformatering

ER-formeldesigneren kan brukes til å definere et uttrykk som formaterer data som mottas fra datakilder, slik at dataene kan sendes som en del av det genererende elektroniske dokumentet. Du kan ha formatering som må brukes som en vanlig regel som skal brukes på nytt for et format. I så fall kan du innføre denne formateringen én gang i formatkonfigurasjonen, som en navngitt transformasjon som har et formateringsuttrykk. Denne navngitte transformasjonen kan deretter knyttes til mange formatkomponenter der utdata må formateres i henhold til formateringsuttrykket som du opprettet.

Illustrasjonen nedenfor viser utformingen av en transformasjon av denne typen. I dette eksemplet forkorter **TrimmedString**-transformasjonen innkommende data for **String**-datatypen ved å fjerne innledende og etterfølgende mellomrom. Det returnerer deretter den avkortede strengverdien.

[![Transformasjon](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Illustrasjonen nedenfor viser hvordan en transformasjon av denne typen kan brukes. I dette eksemplet sender flere formatkomponenter tekst som utdata til det genererende elektroniske dokumentet under kjøring. Alle disse formatkomponentene refererer til **TrimmedString**-transformeringen etter navn.

[![Transformasjon som brukes](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Når formatkomponenter som **partyName**-komponenten i den forrige illustrasjonen refererer til **TrimmedString**-transformasjonen, sender transformasjonen tekst som utdata til det genererende elektroniske dokumentet. Denne teksten inneholder ikke mellomrom.

Hvis du har en formatering som skal brukes individuelt, kan du introdusere denne formateringen som et individuelt uttrykk for binding av en bestemt formatkomponent. Illustrasjonen nedenfor viser et uttrykk av denne typen. I dette eksemplet er **partyType**-formatkomponenten bundet til datakilden via et uttrykk som konverterer innkommende data fra **Model.Company.RegistrationType**-feltet i datakilden til store bokstaver i tekst. Uttrykket sender deretter teksten som utdata til det elektroniske dokumentet.

[![Bruke formatering på en individuell komponent](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Prosessflytkontroll

ER-formeldesigneren kan brukes til å definere uttrykk som styrer prosessflyten for generering av elektroniske dokumenter. Du kan utføre følgende oppgaver:

- Definere betingelser som avgjør når en prosess for oppretting av dokument må stoppes.
- Angi uttrykk som oppretter meldinger for brukeren om stoppede prosesser eller vise kjøringsloggmeldinger om å fortsette prosessen for rapportgenerering.
- Angi filnavnene for generering av elektroniske dokumenter, og kontroller betingelsene de oppretter.

Hver regel av prosessflytkontrollen er utviklet som en enkelt validering. Illustrasjonen nedenfor viser en validering av denne typen. Her er en forklaring på konfigurasjonen i dette eksemplet:

- Valideringen blir evaluert når **INSTAT**-noden er opprettet under genereringen av XML-filen.
- Hvis listen over transaksjoner er tom, stopper valideringen kjøringsprosessen og returnerer **USANN**.
- Valideringen returnerer en feilmelding som inneholder teksten for etiketten SYS70894 på brukerens foretrukne språk.

[![Validering](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER-formeldesigner kan også brukes til å generere et filnavn for et genererende elektroniske dokument og kontrollere prosessen for oppretting av fil. Illustrasjonen nedenfor viser utformingen av en prosessflytkontroll av denne typen. Her er en forklaring på konfigurasjonen i dette eksemplet:

- Listen med poster fra **modell. Intrastat**-datakilden er delt inn i partier. Hvert parti inneholder opptil 1 000 poster.
- Utdataene oppretter en ZIP-fil som inneholder én fil i XML-format for hvert parti som ble opprettet.
- Et uttrykk returnerer et filnavn for generering av elektroniske dokumenter ved å kjede sammen filnavnet og filnavntypen. Filnavnet inneholder parti-ID-en som suffiks for det andre partiet og alle etterfølgende partier.
- Et uttrykk aktiverer (ved å returnere **SANN**) filopprettingsprosessen for partier som inneholder minst én post.

[![Filkontroll](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="documents-content-control"></a>Kontroll av dokumentinnhold

ER-formeldesigneren kan brukes til å konfigurere uttrykk som kontrollerer hvilke data som skal plasseres i genererte, elektroniske dokumenter ved kjøring. Uttrykkene kan aktivere eller deaktivere utdataene for bestemte elementer i formatet, avhengig av behandling av data og konfigurert logikk. Dette uttrykket kan angis for ett enkelt formatelement i **Aktivert**-feltet i **Tilordning**-fanen på **Operasjonsutforming**-siden som en logisk betingelse som returnerer den **boolske** verdien:

-   Når **True** returneres, kjøres det gjeldende formatelementet.
-   Når **False** returneres, blir det gjeldende formatelementet hoppet over.

Følgende illustrasjon viser uttrykk av denne typen (versjonen **11.12.11** av formatkonfigurasjonen **ISO20022-kredittoverføring (NO)** som angis av Microsoft, er et eksempel). **XMLHeader**-formatkomponenten er konfigurert til å beskrive strukturen til kredittoverføringsmeldingen ved å følge ISO-meldingsstandardene 20022 XML. Formatkomponenten **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** er konfigurert til å legge til i den genererte meldingen, **Ustrd** XML-element, og plassere remisseinformasjonen i et ustrukturert format som tekst i følgende XML-elementer:

-   **PaymentNotes**-komponenten brukes til å produsere teksten i betalingsmerknadene.
-   **DelimitedSequence**-komponenten produserer kommadelte fakturanumre som brukes til å utligne gjeldende kredittoverføring.

[![Operasjonsutforming](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> **PaymentNotes**- og **DelimitedSequence**-komponentene merkes ved hjelp av et spørsmålstegn. Dette betyr at bruk av begge komponentene er betinget, basert på følgende kriterier:

-   Definert for **PaymentNote**-komponenten aktiverer **@.PaymentsNotes<>""**-uttrykket (ved å returnere **TRUE**) utfyllingen til **Ustrd** XML-elementet, teksten for betalingsmerknader når denne teksten for gjeldende kredittoverføring ikke er tom.

[![Operasjonsutforming](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)

-   Definert for **DelimitedSequence**-komponenten aktiverer **@.PaymentsNotes=""**-uttrykket (ved å returnere **TRUE**) utfyllingen til **Ustrd** XML-elementet, atskilt med kommadelte fakturanumre som brukes til å utligne gjeldende kredittoverføring når teksten for betalingsmerknader for denne kredittoverføringen er tom.

[![Operasjonsutforming](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)

Basert på denne innstillingen vil den genererte meldingen for hver debitorbetaling **Ustrd** XML-element, inneholde enten tekst for betalingsmerknader eller, når denne teksten er tom, tekst atskilt med kommadelte tall som brukes til å utligne denne betalingen.

### <a name="basic-syntax"></a>Grunnleggende syntaks

ER-uttrykk kan inneholde én eller flere av følgende elementer:

- Konstanter
- Operatorer
- Referanser
- Baner
- Funksjoner

#### <a name="constants"></a>Konstanter

Når du utformer uttrykk, kan du bruke tekst og numeriske konstanter (dvs. verdier som ikke er beregnet). Uttrykket **VALUE ("100") + 20** bruker for eksempel den numeriske konstanten **20** og strengkonstanten **“100”**, og returnerer den numeriske verdien **120**. ER-formeldesigneren støtter avbruddssekvenser. Derfor kan du angi en uttrykksstreng som skal håndteres på en annen måte. For eksempel returnerer uttrykket **"Leo Tolstoy ""Krig og fred"" Del 1"** tekststrengen **Leo Tolstoy "Krig og fred" Del 1**.

#### <a name="operators"></a>Operatører

Tabellen nedenfor viser de aritmetiske operatorene som du kan bruke til å utføre grunnleggende matematiske operasjoner, for eksempel addisjon, subtraksjon, multiplikasjon og divisjon.

| Operator | Betydning               | Eksempel |
|----------|-----------------------|---------|
| +        | Tillegg              | 1+2     |
| -        | Subtraksjon, negasjon | 5-2, -1 |
| \*       | Multiplikasjon        | 7\*8    |
| /        | Inndeling              | 9/3     |

Tabellen nedenfor viser sammenligningsoperatorene som støttes. Du kan bruke disse operatorene til å sammenligne to verdier.

| Operator | Betydning                  | Eksempel    |
|----------|--------------------------|------------|
| =        | Lik                    | X=Y        |
| &gt;     | Større enn             | X&gt;Y     |
| &lt;     | Mindre enn                | X&lt;Y     |
| &gt;=    | Større enn eller lik | X&gt;=Y    |
| &lt;=    | Mindre eller lik    | X&lt;=Y    |
| &lt;&gt; | Er ikke lik             | X&lt;&gt;Y |

Du kan også bruke et &-tegn (&) som en tekstsammenkoblingsoperator. På denne måten kan du koble sammen én eller flere tekststrenger til én enkelt tekststreng.

| Operatør | Betydning     | Eksempel                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Sammenslåing | "Ingenting å skrive ut" & ":&nbsp;" & "Finner ingen poster" |

##### <a name="operator-precedence"></a>Operatorprioritet

Rekkefølgen som delene av et sammensatt uttrykk evalueres i er viktig. Resultatet av uttrykket **1 + 4 / 2** varierer for eksempel, avhengig av om addisjonen eller divisjonen gjøres først. Du kan bruke parenteser til å definere hvordan uttrykk evalueres. Hvis du for eksempel vil angi at addisjonen skal gjøres først, kan du endre det forrige uttrykket til **(1 + 4) / 2**. Hvis du ikke eksplisitt angir operasjonsrekkefølgen i et uttrykk, er rekkefølgen basert på standardprioriteten som er tilordnet til operatorene som støttes. Tabellen nedenfor viser prioriteten som er tilordnet hver operator. Operatorer som har en høyere prioritet (for eksempel 7) evalueres før operatorer som har en lavere prioritet (for eksempel 1).

| Prioritet | Operatorer      | Syntaks                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Gruppering       | ( … )                                                                   |
| 6          | Medlemstilgang  | … . …                                                                   |
| 5          | Funksjonsanrop  | … ( … )                                                                 |
| 4          | Multiplikativ | … \* …<br>… / …                                                         |
| 3          | Additiv       | … + …<br>… - …                                                          |
| 2          | Sammenligning     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Skille     | … , …                                                                   |

Hvis et uttrykk inneholder flere etterfølgende operatorer med samme prioritet, evalueres disse operasjonene fra venstre mot høyre. Uttrykket **1 + 6 / 2 \* 3 &gt; 5** returnerer for eksempel **sann**. Vi anbefaler at du bruker parenteser for å eksplisitt angi ønsket rekkefølge på operasjoner i uttrykk, slik at uttrykkene er enklere å lese og vedlikeholde.

#### <a name="references"></a>Referanser

Alle datakilder for gjeldende ER-komponent som er tilgjengelige under utformingen av et uttrykk, kan brukes som navngitte referanser. (Den gjeldende ER-komponenten kan være en modell eller et format.) Gjeldende ER-datamodell inneholder for eksempel **ReportingDate**-datakilden, og denne datakilden returnerer en verdi for **DATETIME**-datatypen. Hvis du vil ha verdien riktig formatert i det genererende dokumentet, kan du referere til datakilden i uttrykket som **DATETIMEFORMAT (ReportingDate, "dd-MM-åååå")**.

Alle tegn i navnet på en refererende datakilde som ikke representerer en bokstav i alfabetet, må ha et enkelt anførselstegn (') foran. Hvis navnet på en referansedatakilde inneholder minst ett symbol som ikke representerer en bokstav i alfabetet, må navnet være omsluttet av enkle anførselstegn. (Disse ikke-alfabetiske symbolene kan for eksempel være skilletegn eller andre skriftlige symboler.) Her er noen eksempler:

- Datakilden **Today’s date & time** må refereres i ER-uttrykket som **'Today''s date & time’**.
- Metoden **name()** for datakilden **Customers** må refereres i ER-uttrykk som **Customers.’name()’**.

Hvis metodene for programdatakilder har parametere, brukes følgende syntaks for å kalle disse metodene:

- Hvis **isLanguageRTL**-metoden for **System**-datakilden har en **EN-US**-parameter av **Streng**-datatypen, må denne metoden refereres til i et ER-uttrykk som **System.'isLanguageRTL'("EN-US")**.
- Anførselstegn er ikke obligatorisk når et metodenavn inneholder bare alfanumeriske symboler. De er imidlertid obligatorisk for en metode i en tabell hvis navnet inneholder parentes.

Når du legger til **System**-datakilden i en ER-tilordning som refererer til programklassen **Global**, returnerer uttrykket den boolske verdien **USANN**. Det endrede uttrykket **System.' isLanguageRTL'("AR")** returnerer den boolske verdien **SANN**.

Du kan begrense hvordan verdier blir sendt til parametere av denne metodetypen:

- Bare konstanter kan sendes til metoder av denne typen. Verdiene for konstantene defineres under utformingen.
- Bare primitive (grunnleggende) datatyper støttes for parametere av denne typen. (De primitive datatypene er heltall, reelle tall, boolsk, streng og så videre.)

#### <a name="paths"></a>Baner

Når et uttrykk refererer til en strukturert datakilde, kan du bruke banedefinisjonen for å velge et bestemt primitivt element i denne datakilden. Tegnet punktum (.) brukes til å skille enkeltelementene i en strukturert datakilde. Gjeldende ER-datamodell inneholder for eksempel datakilden **InvoiceTransactions**, og denne datakilden returnerer listen med poster. Oppføringsstrukturen **InvoiceTransactions** inneholder feltene **AmountDebit** og **AmountCredit**, og begge disse feltene returnerer numeriske verdier. Du kan derfor utforme følgende uttrykk for å beregne det fakturerte beløpet: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Funksjoner

Den neste delen beskrives funksjonene som kan brukes i ER-uttrykk. Alle datakilder i uttrykkskonteksten (gjeldende ER-datamodell eller ER-format), kan brukes som parametere for anropsfunksjoner i henhold til listen over argumenter for anropsfunksjoner. Konstanter kan også brukes som parametere for anropsfunksjoner. Gjeldende ER-datamodell inneholder for eksempel datakilden **InvoiceTransactions**, og denne datakilden returnerer listen med poster. Oppføringsstrukturen **InvoiceTransactions** inneholder feltene **AmountDebit** og **AmountCredit**, og begge disse feltene returnerer numeriske verdier. For å beregne det fakturerte beløpet kan du derfor utforme følgende uttrykk som bruker den innebygde ER-avrundingsfunksjonen: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Funksjoner som støttes

Tabellen nedenfor beskriver datamanipuleringsfunksjonene som du kan bruke til å utforme ER-datamodeller og ER-rapporter. Listen over funksjoner er ikke løst. Utviklere kan utvide den. Hvis du vil se en oversikt over funksjonene som du kan bruke, kan du åpne funksjonsruten i ER-formeldesigner.

### <a name="date-and-time-functions"></a>Dato- og klokkeslettfunksjoner

| Funksjon | Beskrivelse | Eksempel |
|----------|-------------|---------|
| ADDDAYS (dato/klokkeslett, dager) | Legg til det angitte antallet dager i den angitte dato-/klokkeslettverdien. | **ADDDAYS (NOW(), 7)** Returnerer datoen og klokkeslettet sju dager i fremtiden. |
| DATETODATETIME (dato) | Konverterer den angitte datoverdien til en dato-/klokkeslettverdi. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** returnerer den gjeldende Finance and Operations-øktens dato, 24. desember 2015, som **12/24/2015 12:00:00 AM**. I dette eksemplet er **CompInfo** en ER-datakilde av typen **Finance and Operations/tabell** og refererer til CompanyInfo-tabellen. |
| NOW () | Returnerer gjeldende dato og klokkeslett for programserveren som en dato-/klokkeslettverdi. | |
| TODAY () | Returnerer gjeldende dato for programserveren som en datoverdi. | |
| NULLDATE () | Returnerer en **nullverdi** for dato. | |
| NULLDATETIME () | Returnerer en **nullverdi** for dato/klokkeslett. | |
| DATETIMEFORMAT (dato/klokkeslett, format) | Konverterer den angitte dato-/klokkeslettverdien til en streng i det angitte formatet. (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard og ](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM-åååå")** returnerer gjeldende dato for programserveren, 24. desember 2015, som **"24-12-2015"**, basert på det angitte egendefinerte formatet. |
| DATETIMEFORMAT (dato/klokkeslett, format, kultur) | Konverter den angitte dato-/klokkeslettverdien til en streng i angitt format og [kultur](https://msdn.microsoft.com/goglobal/bb896001.aspx). (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard og ](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** returnerer gjeldende dato for programserveren, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen. |
| SESSIONTODAY () | Returnerer gjeldende dato for programøkten som en datoverdi. | |
| SESSIONNOW () | Returnerer gjeldende dato og klokkeslett for programøkten som en dato-/klokkeslettverdi. | |
| DATEFORMAT (dato, format) | Returnerer en strengrepresentasjon for den angitte datoen i det angitte formatet. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** returnerer gjeldende dato for programøkten, 24. desember 2015, som **"24-12-2015"**, basert på det angitte egendefinerte formatet. |
| DATEFORMAT (dato, format, kultur) | Konverter den angitte datoverdien til en streng i angitt format og [kultur](https://msdn.microsoft.com/goglobal/bb896001.aspx). (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard og ](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** returnerer gjeldende dato for programøkten, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen. |
| DAYOFYEAR (dato) | Returnerer en heltallsrepresentasjon av antall dager mellom 1. januar og den angitte datoen. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-ÅÅÅÅ"))** returnerer **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-ÅÅÅÅ"))** returnerer **1**. |
| DAYS (dato 1, dato 2) | Returnerer antall dager mellom den første angitte datoen og den andre angitte datoen. Returnerer en positiv verdi når den første datoen er senere enn den andre datoen, returnerer **0** (null) når den første datoen er lik den andre datoen, eller returnerer en negativ verdi når den første datoen er før den andre datoen. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** returnerer **-1**. |

### <a name="data-conversion-functions"></a>Datakonversjonsfunksjoner

| Funksjon | beskrivelse | Eksempel |
|----------|-------------|---------|
| DATETODATETIME (dato) | Konverterer den angitte datoverdien til en dato-/klokkeslettverdi. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** returnerer den gjeldende Finance and Operations-øktens dato, 24. desember 2015, som **12/24/2015 12:00:00 AM**. I dette eksemplet er **CompInfo** en ER-datakilde av typen **Finance and Operations/tabell** og refererer til CompanyInfo-tabellen. |
| DATEVALUE (streng, format) | Returnerer en datorepresentasjon for den angitte strengen i det angitte formatet. | **DATEVALUE ("21-DES-2016", "dd-MMM-åååå")** returnerer datoen 21. desember 2016 basert på angitt egendefinerte format og standardprogrammets **EN-US**-kultur. |
| DATEVALUE (streng, format, kultur) | Returnerer en datorepresentasjon for den angitte strengen i det angitte formatet og kulturen. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** returnerer datoen 21. januar 2016 basert på angitt egendefinert format og kultur. **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** vil imidlertid iverksette et unntak for å informere brukeren om at den angitte strengen ikke gjenkjennes som en gyldig dato. |
| DATETIMEVALUE (streng, format) | Returnerer en dato-/klokkeslettrepresentasjon for den angitte strengen i det angitte formatet. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** returnerer 2:55:00 AM den 21. desember 2016 basert på angitt egendefinert format og standardprogrammets **EN-US**-kultur. |
| DATETIMEVALUE (streng, format, kultur) | Returnerer en dato-/klokkeslettrepresentasjon for den angitte strengen i det angitte formatet og kulturen. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** returnerer 2:55:00 AM den 21. desember 2016 basert på angitt egendefinert format og kultur. **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** vil imidlertid iverksette et unntak for å informere brukeren om at den angitte strengen ikke gjenkjennes som en gyldig dato/klokkeslett. |

### <a name="list-functions"></a>Listefunksjoner

<table>
<thead>
<tr>
<th>Funksjon</th>
<th>beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (inndata, lengde)</td>
<td>Del den angitte inndatastrengen i delstrenger, der har har den angitte lengden. Returner resultatet som en ny liste.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> returnerer en ny liste som består av to poster som har et <strong>STRING</strong>-felt. Feltet i den første posten inneholder teksten <strong>&quot;abc&quot;</strong>, og feltet i den andre posten inneholder teksten <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr>
<td>SPLIT (inndata, skilletegn)</td>
<td>Del den angitte inndatastrengen i delstrenger, basert på det angitte skilletegnet.</td>
<td><strong>SPLIT (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> returnerer en ny liste som består av tre poster som har et <strong>STRING</strong>-felt. Feltet i den første posten inneholder teksten <strong>&quot;X&quot;</strong>, feltet i den andre posten inneholder teksten &quot;&nbsp;&quot;, og feltet i den tredje posten inneholder teksten <strong>&quot;y&quot;</strong>. Hvis skilletegn er tomt, returneres en ny liste som består av én post som har et <strong>STRING</strong>-felt som inneholder inndatateksten. Hvis inndataen er tom, returneres det en ny, tom liste.
Hvis enten inndataen eller skilletegnet ikke er angitt (null), iverksettes et programunntak.</td>
</tr>
<tr>
<td>SPLITLIST (liste, nummer)</td>
<td>Del den angitte listen i grupper, der hver inneholder det angitte antallet poster. Returnere resultatet som en ny gruppeliste som inneholder følgende elementer:
<ul>
<li>Grupper som vanlige lister (<strong>Value</strong>-komponent)</li>
<li>Gjeldende gruppenummer (<strong>Gruppenummer</strong>-komponent)</li>
</ul>
</td>
<td>I følgende illustrasjon opprettes en <strong>Linjer</strong>-datakilde som en postliste med tre poster. Denne listen er delt inn i partier, der hvert inneholder opptil to poster.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Følgende illustrasjon viser det utformede formatoppsettet. I dette formatoppsettet opprettes bindinger til <strong>Linjer</strong>-datakilden for å generere utdata i XML-format. Disse utdataene viser individuelle noder for hvert parti og postene i det.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Følgende illustrasjon viser resultatet når det utformede formatet kjøres.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (post 1 [, post 2, …])</td>
<td>Returner en ny liste som opprettes fra de angitte argumentene.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> returnerer en tom post, der listen med felt inneholder alle feltene i postlistene <strong>MainData</strong> og <strong>OtherData</strong>.</td>
</tr>
<tr>
<td>LISTJOIN (liste 1, liste 2, ...)</td>
<td>Returner en sammenkoblet liste som opprettes fra listen av de angitte argumentene.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> returnerer en liste over seks poster, der ett felt for <strong>STRING</strong>-datatypen inneholder bokstaver.</td>
</tr>
<tr>
<td>ISEMPTY (liste)</td>
<td>Returnerer <strong>SANN</strong> hvis den angitte listen ikke inneholder noen elementer. Hvis ikke, returnes <strong>USANN</strong>.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (liste)</td>
<td>Returner en tom liste ved hjelp av den angitte listen som en kilde for listestrukturen.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> returnerer en ny, tom liste som har samme struktur som listen som returneres av <strong>SPLIT</strong>-funksjonen.</td>
</tr>
<tr>
<td>FIRST (liste)</td>
<td>Returner den første posten i den angitte listen hvis posten ikke er tom. Hvis ikke, iverksette et unntak.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (liste)</td>
<td>Returner den første posten i den angitte listen hvis posten ikke er tom. Hvis ikke, returner en <strong>null</strong>-post.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (liste)</td>
<td>Returner en liste som bare inneholder det første element i den angitte listen.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (bane)</td>
<td>Denne funksjonen kjøres som et minneinternt valg. Den returnerer en ny liste som er flatet ut, og som representerer alle elementer som samsvarer med den angitte banen. Banen må defineres som en gyldig datakildebane til et datakildeelement av datatypen postliste. Dataelementer som banestrengen og datoen skal føre til en feil i ER-uttrykksverktøyet under utformingen.</td>
<td>Hvis du angir <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> som en datakilde (DS), vil <strong>COUNT( ALLITEMS (DS.Value))</strong> returnere <strong>3</strong>.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (bane)</td>
<td>Denne funksjonen kjøres som en koblet SQL-spørring. Den returnerer en ny liste som er flatet ut, og som representerer alle elementer som samsvarer med den angitte banen. Den angitte banen må defineres som en gyldig datakildebane til et datakildeelement til en postlistedatatype, og den må inneholde minst én relasjon. Dataelementer som banestrengen og datoen skal føre til en feil i ER-uttrykksverktøyet under utformingen.</td>
<td>Definer de følgende datakildene i modelltilordningen:
<ul>
<li><strong>CustInv</strong> (<strong>Tabellposter</strong>-type), som refererer til tabellen CustInvoiceTable</li> 
<li><strong>FilteredInv</strong> (<strong>Beregnet-felt</strong>-type), som inneholder uttrykket <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;USA-001&quot;)</strong></li>
<li><strong>JourLines</strong> (<strong>Beregnet-felt</strong>-type), som inneholder uttrykket <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong></li>
</ul>
<p>Når du kjører modelltilordningen for å kalle <strong>JourLines</strong>-datakilden, kjøres følgende SQL-setning:</p>
VELG ... FRA CUSTINVOICETABLE T1 KRYSSKOBLET MED CUSTINVOICEJOUR T2 KRYSSKOBLET MED CUSTINVOICETRANS T3 DER ...
</td>
</tr>
<tr>
<td>ORDERBY (liste [,uttrykk 1, uttrykket 2, ...])</td>
<td>Returnerer den angitte listen når den er sortert i henhold til de angitte argumentene. Disse argumentene kan defineres som uttrykk.</td>
<td>Hvis <strong>Leverandør </strong> er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer <strong> ORDERBY (leverandører, Vendors.'name()')</strong> en oversikt over leverandører sortert etter navn i stigende rekkefølge.</td>
</tr>
<tr>
<td>REVERSE (liste)</td>
<td>Returner den angitte listen i omvendt rekkefølge.</td>
<td>Hvis <strong>Leverandør </strong> er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> en oversikt over leverandører sortert etter navn i synkende rekkefølge.</td>
</tr>
<tr>
<td>WHERE (liste, betingelse)</td>
<td>Returnerer den angitte listen når den er filtrert i henhold til den angitte betingelsen. Den angitte betingelsen brukes på listen i minnet. På denne måten skiller <strong>WHERE</strong>-funksjonen seg fra <strong>FILTER</strong>-funksjonen.</td>
<td>Hvis <strong>Leverandør</strong> er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer <strong>WHERE(leverandører, Vendors.VendGroup = &quot;40&quot;)</strong> en oversikt over bare leverandører som tilhører leverandørgruppe 40.</td>
</tr>
<tr>
<td>ENUMERATE (liste)</td>
<td>Returner en ny liste som består av opplistede poster for den angitte listen, og som viser følgende elementer:
<ul>
<li>Angitte listeposter som vanlige lister (<strong>Value</strong>-komponent)</li>
<li>Gjeldende postindeks (<strong>Number</strong>-komponent)</li>
</ul>
</td>
<td>I illustrasjonen nedenfor opprettes <strong>Enumerated</strong>-datakilden som en nummerert liste over leverandørposter fra <strong>Vendors</strong>-datakilden som refererer til VendTable-tabellen.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Illustrasjonen nedenfor viser formatet. I dette formatet opprettes databindinger for å generere utdata i XML-format. Disse utdataene viser enkeltleverandører som opplistede noder.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Følgende illustrasjon viser resultatet når det utformede formatet kjøres.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (liste)</td>
<td>Returner antall poster i den angitte listen hvis listen ikke er tom. Hvis ikke, returnes <strong>0</strong> (null).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> returnerer <strong>2</strong> fordi <strong>SPLIT</strong>-funksjonen oppretter en liste som består av to poster.</td>
</tr>
<tr>
<td>LISTOFFIELDS (bane)</td>
<td>Returnerer en postliste som er opprettet fra et argument av en av følgende typer:
<ul>
<li>Modellopplisting</li>
<li>Formatopplisting</li>
<li>Beholder</li>
</ul>
<p>Listen som opprettes, består av poster med følgende felt:</p>
<ul>
<li>Navn</li>
<li>Etikett</li>
<li>beskrivelse</li>
</ul>
Under kjøring returnerer <strong>Etikett</strong>- og <strong>Beskrivelse</strong>-feltet verdier som er basert på formatets språkinnstillinger.
</td>
<td>I følgende illustrasjon introduseres en opplisting i en datamodell.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Illustrasjonen nedenfor viser disse detaljene:</p>
<ul>
<li>Modellopplistingen settes inn i en rapport som en datakilde.</li>
<li>Et ER-uttrykk bruker modellopplistingen som en parameter i <strong>LISTOFFIELDS</strong>-funksjonen.</li>
<li>En datakilde av postlistetypen settes inn i en rapport ved hjelp av det opprettede ER-uttrykket.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Eksemplet nedenfor viser elementene i ER-formatet som er bundet til datakilden for postlistetypen som ble opprettet ved hjelp av funksjonen <strong>LISTOFFIELDS</strong>.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Følgende illustrasjon viser resultatet når det utformede formatet kjøres.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Basert på språkinnstillingene for de overordnede FILE- og FOLDER-formatelementene, angis oversatt tekst for etiketter og beskrivelser i utdataene i ER-formatet.</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (bane, språk)</td>
<td>Returnerer en postliste som opprettes fra et argument, for eksempel en modellopplisting, en formatopplisting eller en beholder. Listen som opprettes, består av poster med følgende felt:
<ul>
<li>Navn</li>
<li>Etikett</li>
<li>beskrivelse</li>
<li>Er oversatt</li>
</ul>
Under kjøring returnerer <strong>Etikett</strong>- og <strong>Beskrivelse</strong>-feltet verdier som er basert på formatets språkinnstillinger og det angitte språket. <strong>Er oversatt</strong>-feltet indikerer at <strong>Etikett</strong>-feltet er oversatt til det angitte språket.
</td>
<td>Du bruker for eksempel <strong>Beregnet felt</strong>-datakildetypen til å konfigurere <strong>enumType_de</strong>- og <strong>enumType_deCH</strong>-datakildene for <strong>enumType</strong> datamodellopplistingen.
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>I dette tilfellet kan du bruke følgende uttrykk til å hente etiketten for opplistingsverdien på sveitsisk (tysk) hvis denne oversettelsen er tilgjengelig. Hvis sveitsisk (tysk) oversettelse ikke er tilgjengelig, er etiketten på tysk.</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (liste, feltnavn, skilletegn)</td>
<td>Returnerer en streng som består av sammenkoblede verdier for det angitte feltet fra den angitte listen. Verdiene skilles med det angitte skilletegnet.</td>
<td>Hvis du angir <strong>SPLIT(&quot;abc&quot; , 1)</strong> som datakilde (DS), returnerer <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> <strong>&quot;a-b-c&quot;</strong>.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (liste, grenseverdi, grensekilde)</td>
<td>Deler den angitte listen inn en ny liste over underordnede lister og returnerer resultatet i oppføringslisteinnhold. <strong>Grenseverdi</strong>-parameteren definerer verdien av grensen for deling av originallisten. <strong>Grensekilde</strong>-parameteren definerer trinnet som totalsummen økes på. Grensen brukes ikke på en enkelt vare i originallisten hvis kildegrensen overskrider den definerte grensen.</td>
<td>Illustrasjonen nedenfor viser et format. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>Følgende illustrasjon viser datakildene som brukes for formatet.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Følgende illustrasjon viser resultatet når formatet kjøres. I dette tilfellet er utdataene en flat liste over artikkelvarer.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>I illustrasjonene nedenfor er det samme formatet justert slik at det viser listen over artikkelvarer i partier når et enkelt parti må inneholde artikler, og den totale vekten må ikke overskride grensen på 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Følgende illustrasjon viser resultatet når det justerte formatet kjøres.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] Grensen gjelder ikke for det siste elementet i den originale listen siden verdien (11) av grensekilden (vekt) overskrider den definerte grensen (9). Bruk enten funksjonen <strong>WHERE</strong> eller <strong>Aktivert</strong>-uttrykket for det tilsvarende formatelementet for å ignorere (hoppe over) underordnede lister ved rapportgenerering, om nødvendig.</blockquote>
</td>
</tr>
<tr>
<td>FILTER (liste, betingelse)</td>
<td>Returnerer den angitte listen etter at spørringen er endret for å filtrere den angitte betingelsen. Denne funksjonen er ulik <strong>WHERE</strong>-funksjonen fordi den angitte betingelsen brukes på en ER-datakilde av typen <strong>Tabellposter</strong> på databasenivået. Listen og betingelsen kan defineres ved hjelp av tabeller og relasjoner.</td>
<td>Hvis <strong>Leverandør</strong> er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer <strong>FILTER(leverandører, Vendors.VendGroup = &quot;40&quot;)</strong> en oversikt over bare leverandører som tilhører leverandørgruppe 40. Hvis <strong>Leverandør</strong> er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, og <strong>parmVendorBankGroup</strong> er konfigurert som en ER-datakilde som returnerer en verdi av <strong>String</strong>-datatypen, returnerer <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> en liste over bare leverandørkontoene som tilhører en spesifikk bankgruppe.</td>
</tr>
<tr>
<td>INDEKS (liste, indeks)</td>
<td>Denne funksjonen returnerer en post som er valgt av en bestemt numerisk indeks i listen. Det oppstår et unntak hvis indeksen er utenfor området til postene i listen.</td>
<td>Hvis du angir datakilden <strong>DS</strong> for typen <strong>Beregnet felt</strong>, og den inneholder uttrykket <strong>SPLIT ("A|B|C", “|”), 2</strong>, returnerer <strong>DS.Value</strong>-uttrykket tekstverdien "B". Uttrykket <strong>INDEX (SPLIT ("A|B|C", “|”), 2).Value</strong> returnerer også tekstverdien “B”.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logiske funksjoner

| Funksjon | Beskrivelse | Eksempel |
|----------|-------------|---------|
| CASE (uttrykk, alternativ 1, resultat 1 \[, alternativ 2, resultatet 2\] ... \[, standardresultat\]) | Evaluer den angitte uttrykksverdien mot de angitte alternative alternativene. Returner resultatet av alternativet som er lik verdien for uttrykket. Hvis ikke, returner det valgfrie standardresultatet, hvis et standardresultat er angitt. (Standardresultatet er den siste parameteren som ikke innledes av et alternativ.) | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "VINTER", "11", "VINTER", "12", "VINTER", "")** returnere strengen **"VINTER"** når gjeldende dato for programøkten er mellom oktober og desember. Ellers returneres en tom streng. |
| IF (betingelse, verdi 1, verdi 2) | Returner den første angitte verdien når den angitte betingelsen er oppfylt. Hvis ikke, returner den andre verdien som er angitt. Hvis verdien 1 og verdien 2 er poster eller postlister, har resultatet bare feltene som finnes i begge listene. | **IF (1=2, "betingelsen er oppfylt", "betingelsen er ikke oppfylt")** returnerer strengen **"betingelse er ikke oppfylt"**. |
| NOT (betingelse) | Returner den omvendte logiske verdien til den angitte betingelsen. | **NOT (SANN)** returnerer **USANN**. |
| AND (betingelse 1\[, betingelse 2, ...\]) | Returnerer **SANN** hvis *alle* angitte betingelser er oppfylt. Hvis ikke, returnes **USANN**. | **AND (1=1, "a"="a")** returnerer **SANN**. **AND (1=2, "a"="a")** returnerer **USANN**. |
| OR (betingelse 1\[, betingelse 2, ...\]) | Returnerer **USANN** hvis *alle* angitte betingelser ikke er oppfylt. Returnerer **SANN** hvis *en* angitt betingelse er oppfylt. | **OR (1=2, "a"="a")** returnerer **SANN**. |
| VALUEIN (inndata, liste, uttrykk for listeelement) | Bestem om de angitte inndataene samsvarer med en verdi for et element i den angitte listen. Returnerer **TRUE** hvis de angitte inndataene tilsvarer resultatet av å kjøre det angitte uttrykket for minst én post. Hvis ikke, returnes **USANN**. **Inndata**-parameteren representerer banen til et datakildeelement. Verdien for dette elementet samsvares. **Liste**-parameteren representerer banen til et datakildeelement av postlistetypen som en liste over poster som inneholder et uttrykk. Verdien for dette elementet blir sammenlignet med de angitte inndataene. **Uttrykk for listeelement**-argumentet representerer et uttrykk som enten henviser til eller inneholder ett enkelt felt i den angitte listen som skal brukes for den samsvarende. | For eksempler se delen [Eksempler: VALUEIN (inndata, liste, uttrykk for listeelement)](#examples-valuein-input-list-list-item-expression) nedenfor. |

#### <a name="examples-valuein-input-list-list-item-expression"></a>Eksempler: VALUEIN (inndata, liste, uttrykk for listeelement)
Generelt oversettes **VALUEIN**-funksjonen til et sett med **OR**-betingelser:

(inndata = list.item1.value) OR (inndata = list.item2.value) OR …

##### <a name="example-1"></a>Eksempel 1
Du definerer følgende datakilde i modelltilordningen: **List** (**Beregnet felt**-type). Denne datakilden inneholder uttrykket **SPLIT ("a,b,c", ",")**.

Når en datakilde kalles opp som er konfigurert som uttrykket **VALUEIN ("B", List, List.Value)**, returneres **TRUE**. I dette tilfellet oversettes **VALUEIN**-funksjonen til følgende sett med betingelser:

**(("B" = "a") eller ("B" = "b") eller ("B" = "c"))**, der **("B" = "b")** er lik **TRUE**

Når en datakilde kalles opp som er konfigurert som uttrykket **VALUEIN ("B", List, LEFT(List.Value, 0))**, returneres **FALSE**. I dette tilfellet oversettes **VALUEIN**-funksjonen til følgende betingelse:

**("B" = "")**, som ikke er lik **TRUE**

Legg merke til at den øvre grensen for antall tegn i teksten i en slik betingelse 32 768 tegn. Du bør derfor ikke opprette datakilder som kan overstige denne grensen ved kjøretid. Hvis grensen overskrides, kan programmet slutte å kjøre, og et unntak vil bli registrert. Denne situasjonen kan for eksempel oppstå hvis datakilden er konfigurert som **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)**, og **List1**- og **List2**-listene inneholder et stort antall poster.

I noen tilfeller kan **VALUEIN**-funksjonen oversettes til en databasesetning ved hjelp av **EXISTS JOIN**-operatoren. Denne virkemåter skjer når **FILTER**-funksjonen brukes og følgende betingelser er oppfylt:

- **BE OM SPØRRING**-valget er deaktivert for datakilden for **VALUEIN**-funksjonen som refererer til listen over poster. (Ingen flere betingelser brukes på denne datakilden ved kjøretid.)
- Ingen nestede uttrykk konfigureres for datakilden for **VALUEIN**-funksjonen som refererer til listen over poster.
- Et listeelement for **VALUEIN**-funksjonen refererer til et felt (ikke et uttrykk eller en metode) i den angitte datakilden.

Vurder å bruke dette alternativet i stedet for **WHERE**-funksjonen som er beskrevet tidligere i dette eksemplet.

##### <a name="example-2"></a>Eksempel 2

Du definerer de følgende datakildene i modelltilordningen:

- **In** (**Tabellposter**-type), som refererer til tabellen Intrastat
- **Port** (**Tabellposter**-type), som refererer til tabellen IntrastatPort

Når en datakilde kalles opp som er konfigurert som uttrykket **FILTER (In, VALUEIN(In.Port, Port, Port.PortId)**, genereres følgende SQL-setningen for å returnere filtrerte poster i Intrastat-tabellen:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

For **dataAreaId**-feltene genereres den endelige SQL-setningen ved hjelp av **IN**-operatoren.

##### <a name="example-3"></a>Eksempel 3

Du definerer de følgende datakildene i modelltilordningen:

- **Le** (**Beregnet felt**-type), som inneholder uttrykket **SPLIT ("DEMF,GBSI,USMF", ",")**
- **In** (**Tabellposter**-type), som refererer til Intrastat-tabellen og som alternativet **Kryssfirma** er aktivert for

Når en datakilde kalles opp som er konfigurert som uttrykket **FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)** inneholder den endelige SQL-setningen følgende betingelse:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>Matematiske funksjoner

| Funksjon | beskrivelse | Eksempel |
|----------|-------------|---------|
| ABS (tall) | Returner den absolutte verdien av det angitte tallet. (Altså returner tallet uten fortegn.) | **ABS (-1)** returnerer **1**. |
| POWER (tall, potens) | Returner resultatet av å sette det angitte positive tallet til angitt potens. | **POWER (10, 2)** returnerer **100**. |
| NUMBERVALUE (streng, desimaltegn, skilletegn for siffergruppering) | Konverter den angitte strengen til et tall. Det angitte desimalskilletegnet brukes mellom heltallet og delene av et desimaltall. Den angitte skilletegnet for siffergruppering brukes som tusenskilletegn. | **NUMBERVALUE("1 234,56", ",", " ")** returnerer verdien **1234.56**. |
| VALUE (streng) | Konverter den angitte strengen til et tall. Komma og punktum-tegn (.) regnes som desimalskilletegn, og en foranstilt bindestrek (-) brukes som negativt fortegn. Iverksett et unntak hvis den angitte strengen inneholder andre ikke-numeriske tegn. | **VALUE ("1 234,56")** genererer et unntak. |
| ROUND (tall, desimaler) | Returnerer det angitte tallet etter det er avrundet til angitt antall desimaler:<ul><li>Hvis verdien for **desimal**-parameteren er større enn 0 (null), avrundes det angitte tallet til så mange desimalplasser.</li><li>Hvis verdien for **desimal**-parameteren er **0** (null), avrundes det angitte tallet til nærmeste heltall.</li><li>Hvis verdien for **desimal**-parameteren er mindre enn 0 (null), avrundes det angitte tallet til venstre for desimalpunktet.</li></ul> | **ROUND (1200.767, 2)** avrunder til to desimalplasser og returnerer **1200.77**. **ROUND (1200.767, -3)** avrunder til nærmeste multiplum av 1 000, og returnerer **1000**. |
| ROUNDDOWN (tall, desimaler) | Returnerer det angitte tallet etter det er avrundet ned til angitt antall desimaler.<blockquote>[!NOTE] Denne funksjonen fungerer som **ROUND**, men den avrunder alltid ned det angitte tallet (mot null).</blockquote> | **ROUNDDOWN (1200.767, 2)** avrunder ned til to desimalplasser og returnerer **1200.76**. **ROUNDDOWN (1700.767, -3)** avrunder ned til nærmeste multiplum av 1 000, og returnerer **1000**. |
| ROUNDUP (tall, desimaler) | Returnerer det angitte tallet etter det er avrundet opp til angitt antall desimaler.<blockquote>[!NOTE] Denne funksjonen fungerer som **ROUND**, men den avrunder alltid opp det angitte tallet (bort fra null).</blockquote> | **ROUNDUP (1200.763, 2)** avrunder opp til to desimalplasser og returnerer **1200.77**. **ROUNDUP (1200.767, -3)** avrunder opp til nærmeste multiplum av 1 000, og returnerer **2000**. |

### <a name="data-conversion-functions"></a>Datakonversjonsfunksjoner

| Funksjon | beskrivelse | Eksempel |
|----------|-------------|---------|
| VALUE (streng) | Konverter den angitte strengen til et tall. Komma og punktum-tegn (.) regnes som desimalskilletegn, og en foranstilt bindestrek (-) brukes som negativt fortegn. Iverksett et unntak hvis den angitte strengen inneholder andre ikke-numeriske tegn. | **VALUE ("1 234,56")** genererer et unntak. |
| NUMBERVALUE (streng, desimaltegn, skilletegn for siffergruppering) | Konverter den angitte strengen til et tall. Det angitte desimalskilletegnet brukes mellom heltallet og delene av et desimaltall. Den angitte skilletegnet for siffergruppering brukes som tusenskilletegn. | **NUMBERVALUE("1 234,56", ",", " ")** returnerer **1234.56**. |
| INTVALUE (streng) | Returnerer en heltallsrepresentasjon av den angitte strengen. Desimaler avrundes. | **INTVALUE ("100.77")** returnerer **100**. |
| INTVALUE (tall) | Returnerer en heltallsrepresentasjon av det angitte tallet. Desimaler avrundes. | **INTVALUE ("-100,77")** returnerer **-100**. |
| INT64VALUE (streng) | Returnerer en int64-representasjon av den angitte strengen. Desimaler avrundes. | **INT64VALUE ("22565422744")** returnerer **22565422744**. |
| INT64VALUE (tall) | Returnerer en int64-representasjon av det angitte tallet. Desimaler avrundes. | **INT64VALUE (“22565422744,00”)** returnerer **22565422744**. |

### <a name="record-functions"></a>Registreringsfunksjoner

| Funksjon | beskrivelse | Eksempel |
|----------|-------------|---------|
| NULLCONTAINER (liste) | Returner en **null**-post som har samme struktur som den angitte postlisten eller posten.<blockquote>[!NOTE] Denne funksjonen er foreldet. Bruk **EMPTYRECORD** i stedet.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** returnerer en ny, tom post som har samme struktur som listen som returneres av **SPLIT**-funksjonen. |
| EMPTYRECORD (post) | Returner en **null**-post som har samme struktur som den angitte postlisten eller posten.<blockquote>[!NOTE] En **null**-post er en post der alle felt har en tom verdi. En tom verdi er **0** (null) for tall, en tom streng for strenger og så videre.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** returnerer en ny, tom post som har samme struktur som listen som returneres av **SPLIT**-funksjonen. |

### <a name="text-functions"></a>Tekstfunksjoner

<table>
<thead>
<tr>
<th>Funksjon</th>
<th>beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (streng)</td>
<td>Returner den angitte strengen etter den er konvertert til store bokstaver.</td>
<td><strong>UPPER(&quot;Eksempel&quot;)</strong> returnerer <strong>&quot;EKSEMPEL&quot;</strong>.</td>
</tr>
<tr>
<td>LOWER (streng)</td>
<td>Returner den angitte strengen etter den er konvertert til små bokstaver.</td>
<td><strong>LOWER (&quot;Eksempel&quot;)</strong> returnerer <strong>&quot;eksempel&quot;</strong>.</td>
</tr>
<tr>
<td>LEFT (streng, antall tegn)</td>
<td>Returner det angitte antallet tegn fra begynnelsen av den angitte strengen.</td>
<td><strong>LEFT (&quot;Eksempel&quot;, 3)</strong> returnerer <strong>&quot;Eks&quot;</strong>.</td>
</tr>
<tr>
<td>RIGHT (streng, antall tegn)</td>
<td>Returner det angitte antallet tegn fra slutten av den angitte strengen.</td>
<td><strong>RIGHT (&quot;Eksempel&quot;, 3)</strong> returnerer <strong>&quot;pel&quot;</strong>.</td>
</tr>
<tr>
<td>MID (streng, startposisjon, antall tegn)</td>
<td>Returner det angitte antallet tegn fra den angitte strengen med start fra angitt posisjon.</td>
<td><strong>MID (&quot;Eksempel&quot;, 2, 3)</strong> returnerer <strong>&quot;kse&quot;</strong>.</td>
</tr>
<tr>
<td>LEN (streng)</td>
<td>Returner antall tegn i den angitte strengen.</td>
<td><strong>LEN (&quot;Eksempel&quot;)</strong> returnerer <strong>6</strong>.</td>
</tr>
<tr>
<td>CHAR (tall)</td>
<td>Returner strengen av tegn som refereres av det angitte Unicode-tallet.</td>
<td><strong>CHAR (255)</strong> returnerer <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE] Strengen som denne funksjonen returnerer, avhenger av kodingen som er valgt i det overordnede FIL-formatelementet. Listen over kodinger finner du her <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodingsklasse</a>.</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (streng 1 [, streng 2, …])</td>
<td>Returner alle angitte tekststrenger etter de er satt sammen til én streng.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> returnerer <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE] Uttrykket <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> returnerer også <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (streng, mønster, erstatning)</td>
<td>Returner den angitte strengen etter at alle forekomster av tegn i den angitte mønsterstrengen er erstattet med tegnene i den tilsvarende posisjonen i den angitte erstattingsstrengen.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>REPLACE (streng, mønster, erstatning, flagg for vanlig uttrykk)</td>
<td>Når den angitte parameteren <strong>flagg for vanlig uttrykk</strong> er <strong>sann</strong>, returneres den angitte strengen etter at den er endret, ved å bruke det vanlige uttrykket som er angitt som <strong>mønster</strong>-argument for denne funksjonen. Dette uttrykket brukes til å søke etter tegn som skal erstattes. Tegn i det angitte <strong>erstatning</strong>-argumentet brukes til å erstatte tegnene som blir funnet. Når den angitte parameteren <strong>flagg for vanlig uttrykk</strong> er <strong>usann</strong>, fungerer denne funksjonen som <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> bruker et vanlig uttrykk som fjerner alle ikke-numeriske symboler, og returnerer <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, usann)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>TEXT (inndata)</td>
<td>Returner angitte inndata etter at de er konvertert til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for gjeldende forekomst av programmet. For verdier for <strong>real</strong>-typen begrenses strengkonverteringen til to desimalplasser.</td>
<td>Hvis de nasjonale innstillingene for Finance and Operations-forekomstens server er definert som <strong>EN-US</strong>, returnerer <strong>TEXT (NOW ())</strong> gjeldende dato for programøkten, 17. desember 2015, som tekststrengen <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> returnerer <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr>
<td>FORMAT (streng 1, streng 2 [, streng, 3, ...])</td>
<td>Returner den angitte strengen etter at den er formatert ved hjelp av forekomster av <strong>%N</strong> med argumentet <em>n</em>th. Argumentene er strenger. Hvis et argument ikke er angitt for en parameter, returneres parameteren som <strong>&quot;%N&quot;</strong> i strengen. For verdier for <strong>real</strong>-typen begrenses strengkonverteringen til to desimalplasser.</td>
<td>I følgende illustrasjon returnerer <strong>PaymentModel</strong>-datakilden listen over kundeposter via <strong>Kunder</strong>-komponenten og behandlingsdatodatoverdien via <strong>ProcessingDate</strong>-feltet.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>I ER-formatet som er utformet for å generere en elektronisk fil for utvalgte kunder, velges <strong>PaymentModel</strong> som en datakilde og styrer prosessflyten. Et unntak for å informere brukeren iverksettes når en valgt kunde stoppes for datoen da rapporten behandles. Formelen som er utviklet for denne typen behandlingskontroll kan bruke følgende ressurser:</p>
<ul>
<li>Etiketten SYS70894, som har følgende tekst:
<ul>
<li><strong>For EN-US-språk:</strong> &quot;Nothing to print&quot;</li>
<li><strong>For DE-språk:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Etiketten SYS18389, som har følgende tekst:
<ul>
<li><strong>For EN-US-språk</strong>: &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>For DE-språk</strong>: &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Her er formelen som kan utformes:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Hvis en rapport behandles for <strong>Litware Retail</strong>-kunden 17. desember 2015 i <strong>EN-US</strong>-kulturen og <strong>EN-US</strong>-språket, returnerer denne formelen teksten nedenfor, som kan vises for brukeren som en unntaksmelding:</p>
<p>&quot;Ingenting å skrive ut. Litware Retail-kunden stoppes for 12/17/2015.&quot;</p>
<p>Hvis den samme rapporten behandles for <strong>Litware Retail</strong>-kunden 17. desember 2015, i <strong>DE</strong>-kulturen og <strong>DE</strong>-språket, returnerer formelen følgende tekst som bruker et annet datoformat:</p>
<p>&quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE] Følgende syntaks brukes i ER-formler for etiketter:
<ul>
<li><strong>For etiketter fra Finance and Operations-appressurser:</strong> <strong>@&quot;X&quot;</strong>, der <strong>X</strong> er etikett-ID-en i applikasjonsobjekttreet (AOT)</li>
<li><strong>For etiketter som ligger i ER-konfigurasjoner:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, der <strong>X</strong> er etikett-ID-en i ER-konfigurasjonen</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (tall, format)</td>
<td>Returner en strengrepresentasjon for det angitte tallet i det angitte formatet. (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se <a href="https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx">standard</a> og <a href="https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx">egendefinert</a>.) Konteksten denne funksjonen kan kjøres i, bestemmer kulturen som brukes til å formatere tall.</td>
<td>For EN-US-kulturen returnerer <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> returnerer <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr>
<td>NUMBERFORMAT (tall, format, kultur)</td>
<td>Returner en strengrepresentasjon for det angitte tallet i angitt format og kultur. (Hvis du vil ha informasjon om hvilke formater som støttes, kan du se <a href="https://docs.microsoft.com/dotnet/standard/base-types/standard-numeric-format-strings">standard</a> og <a href="https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings">egendefinert</a>.)</td>
<td><strong>NUMBERFORMAT (10/3, “F2”, "de")</strong> returnerer <strong>3,33</strong>, mens <strong>NUMBERFORMAT (10/3, “F2”, "en-us")</strong> returnerer <strong>3.33</strong>.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (tall, språk, valuta, flagg for utskrift av valutanavn, desimaler)</td>
<td>Returner det angitte tallet når det har blitt stavet (konvertert til tekststrenger) på det angitte språket. Språkkoden er valgfri. Når den er definert som en tom streng, brukes språkkoden for kjørekontekst. (Språkkoden for kjørekonteksten defineres for en genererende mappe eller fil.) Valutakoden er også valgfri. Når den er definert som en tom streng, brukes firmavalutaen.
<blockquote>[!NOTE] Parameteren <strong>Skriv ut valutanavn</strong> og parameteren <strong>Desimaler</strong> analyseres bare for følgende språkkoder: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> og <strong>RU</strong>. I tillegg analyseres parameteren <strong>Skriv ut valutanavn</strong> bare for firmaer der land- eller områdekonteksten støtter navn for valutanedgang.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> returnerer <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> returnerer <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> returnerer <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr>
<td>PADLEFT (streng, lengde, utfyllingstegn)</td>
<td>Returner en streng med den angitte lengden der begynnelsen av den angitte strengen fylles ut med de angitte tegnene.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> returnerer tekststrengen <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr>
<td>TRIM (streng)</td>
<td>Returner den angitte tekststrengen etter at innledende og etterfølgende mellomrom er avkortet, og når flere mellomrom mellom ord er fjernet.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Eksempel&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;tekst&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> returnerer <strong>&quot;Eksempeltekst&quot;</strong>.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (bane til kilde for opplistingsdata, tekst i etikett for opplistingsverdi)</td>
<td>Returner en verdi for den bestemte kilden for opplistingsdata basert på den angitte teksten for etiketten for opplisting.</td>
<td>I følgende illustrasjon introduseres opplistingen <strong>ReportDirection</strong> i en datamodell. Legg merke til at etiketter er definert for opplistingsverdier.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Illustrasjonen nedenfor viser disse detaljene:</p>
<ul>
<li>Modellopplistingen <strong>ReportDirection</strong> er satt inn i en rapport som en datakilde, <strong>$Direction</strong>.</li>
<li>ER-uttrykket <strong>$IsArrivals</strong> er utformet for å bruke modellopplistingen som en parameter for denne funksjonen. Verdien av uttrykket er <strong>SANN</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (inndata)</td>
<td>Konverter den angitte inndataen for <strong>Streng</strong>-datatypen til et dataelement i <strong>GUID</strong>-datatype.<blockquote>[!NOTE] For å konvertere i motsatt retning (det vil si å konvertere angitt inndata av datatypen <strong>GUID</strong> til et dataelement av datatypen <strong>String</strong>), kan du bruke funksjonen <strong>TEXT()</strong>.</blockquote></td>
<td>Du definerer de følgende datakildene i modelltilordningen:
<ul>
<li><strong>myID</strong> (<strong>Beregnet-felt</strong>-type), som inneholder uttrykket <strong>GUIDVALUE (&quot;AF5CCDAC-F728-4609-8C8B-A4B30B0C0AA0&quot;)</strong></li>
<li><strong>Brukere</strong> (<strong>Tabellposter</strong>-type), som refererer til tabellen UserInfo</li>
</ul>
Når disse datakildene er definert, kan du bruke et uttrykk som <strong>FILTER (Users, Users.objectId = myID)</strong> til å filtrere UserInfo-tabellen ved <strong>objectId</strong>-feltet for <strong>GUID</strong>-datatypen.
</td>
</tr>
<tr>
<td>JSONVALUE (id, bane)</td>
<td>Analyser data i JavaScript Object Notation (JSON)-format som brukes av den angitte banen til å hente en skalarverdi som er basert på den angitte IDen.</td>
<td>Datakilden <strong>$JsonField</strong> inneholder følgende data i JSON-format: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. For denne datakilden returnerer </strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong> verdien <strong>7.3.1234.1</strong> av <strong>Streng</strong>-datatypen.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Datakonversjonsfunksjoner

| Funksjon | beskrivelse | Eksempel |
|----------|-------------|---------|
| TEXT (inndata) | Returner angitte inndata etter at de er konvertert til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for gjeldende forekomst av programmet. For verdier for **real**-typen begrenses strengkonverteringen til to desimalplasser. | Hvis de nasjonale innstillingene for Finance and Operations-forekomstens server er definert som **EN-US**, returnerer **TEXT (NOW ())** gjeldende dato for Finance and Operations-økten, 17. desember 2015, som tekststrengen **12/17/2015 07:59:23 AM**. **TEXT (1/3)** returnerer **"0.33"**. |
| QRCODE (streng) | Returner et Quick Response Code-bilde (QR-kode) i base64-binærformat for den angitte strengen. | **QRCODE ("eksempeltekst")** returnerer **U2FtcGxlIHRleHQ =**. |

### <a name="data-collection-functions"></a>Datainnsamlingsfunksjoner

| Funksjon | beskrivelse | Eksempel |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Returner navnet på elementet til det gjeldende formatet. Returner en tom streng når flagget **Samle inn utdatadetaljer** for de gjeldende filene er slått av. | For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen **ER Bruke data med formatet utdata for telling og summering**, som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**. |
| SUMIFS (nøkkelstreng for summering, kriterieområde1 streng, kriterieverdi1 streng \[, kriterieområde2 streng, kriterieverdi2 streng, …\]) | Returner summen av verdiene som ble samlet inn for XML-noder (der navnet er definert som en nøkkel) da formatet ble kjørt, og som oppfyller de angitte betingelsene (kombinasjon av områder og verdier). Returner en **0** (null)-verdi når flagget **Samle inn utdatadetaljer** for de gjeldende filene er deaktivert. | |
| SUMIF (nøkkelstreng for summering, kriterieområdestreng, kriterieverdistreng) | Returner summen av verdiene som ble samlet inn for XML-noder (der navnet er definert som en nøkkel) da formatet ble kjørt, og som oppfyller den angitte betingelsen (område og verdi). Returner en **0** (null)-verdi når flagget **Samle inn utdatadetaljer** for de gjeldende filene er deaktivert. | |
| COUNTIFS (kriterieområde1 streng, kriterieverdi1 streng \[, kriterieområde2 streng, kriterieverdi2 streng, …\]) | Returner antallet XML-noder som ble samlet inn da formatet ble kjørt, og som oppfyller de angitte betingelsene (en kombinasjon av områder og verdier). Returner en **0** (null)-verdi når flagget **Samle inn utdatadetaljer** for de gjeldende filene er deaktivert. | |
| COUNTIF (områdekriteriestreng, kriterieverdistreng) | Returner antallet XML-noder som ble samlet inn da formatet ble kjørt, og som oppfyller den angitte betingelsen (område og verdi). Returner en **0** (null)-verdi når flagget **Samle inn utdatadetaljer** for de gjeldende filene er deaktivert. | |
| COLLECTEDLIST (kriterieområde1 streng, kriterieverdi1 streng \[, kriterieområde2 streng, kriterieverdi2 streng, …\]) | Returner listen av verdier som ble samlet inn for XML-noder da formatet ble kjørt, og som oppfyller de angitte betingelsene (område og verdi). Returner en tom liste når flagget **Samle inn utdatadetaljer** for de gjeldende filene er slått av. | |

### <a name="other-business-domainspecific-functions"></a>Andre funksjoner (spesifikke for forretningsområder)

| Funksjon | beskrivelse | Eksempel |
|----------|-------------|---------|
| CONVERTCURRENCY (beløp, kildevaluta, målvaluta, dato, firma) | Konverter det angitte pengebeløpet fra angitt kildevaluta til angitt målvaluta ved å bruke innstillingene for det aktuelle firmaet på den angitte datoen. | **CONVERTCURRENCY (1, "EUR", "NOK", TODAY(), "DEMF")** returnerer tilsvarende én euro i amerikanske dollar på gjeldende øktdato, basert på innstillingene for DEMF-firmaet. |
| ROUNDAMOUNT (tall, desimaler, avrundingsregel) | Avrunder det angitte beløpet til det angitte antallet desimalplasser i henhold til den angitte avrundingsregelen.<blockquote>[!NOTE] Avrundingsregelen må være angitt som en verdi av **RoundOffType**-opplistingen.</blockquote> | Hvis parameteren **model.RoundOff** er satt til **Downward**, vil **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** returnere verdien **1000.78**. Hvis parameteren **model.RoundOff** er satt til **Normal** eller **Avrundes opp**, vil **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** returnere verdien **1000.79**. |
| CURCredRef (sifre) | Returner en kreditorreferanse basert på sifrene i det angitte fakturanummeret. | **CURCredRef ("VEND-200002")** returnerer **"2200002"**. |
| MOD\_97 (sifre) | Returner en kreditorreferanse som et MOD97-uttrykk basert på sifrene i det angitte fakturanummeret. | **MOD\_97 ("VEND-200002")** returnerer **"20000285"**. |
| ISOCredRef (sifre) | Returner en ISO-kreditorreferanse (International Organization for Standardization) basert på sifrene og de alfabetiske symbolene i det angitte fakturanummeret.<blockquote>[!NOTE] Inndataparameteren må oversettes før den sendes til denne funksjonen for å eliminere symboler fra bokstaver som ikke er ISO-kompatible.</blockquote> | **ISOCredRef ("VEND-200002")** returnerer **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (streng, tall) | Hent den spesifiserte ekstra finansdimensjons-ID-en. I **streng**-parameteren er dimensjoner representert som IDer atskilt med komma. **Tall**-parameteren definerer seriekoden for den forespurte dimensjonen i strengen. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** returnerer **"CC"**. |
| GetCurrentCompany () | Returner en tekstrepresentasjon av koden for den juridiske enheten (firma) som en bruker er logget på nå. | **GETCURRENTCOMPANY ()** returnerer **USMF** for en bruker som er logget på firmaet **Contoso Entertainment System USA**. |
| CH\_BANK\_MOD\_10 (sifre) | Returner en kreditorreferanse som et MOD10-uttrykk basert på sifrene i det angitte fakturanummeret. | **CH\_BANK\_MOD\_10 ("VEND-200002")** returnerer **3**. |
| FA\_SUM (anleggsmiddelkode, verdimodellkode, startdato, sluttdato) | Returner den klargjorte databeholderen for det faste anleggsmiddelbeløpet for den angitte perioden. | **FA\_SUM ("COMP-000001", "Current", Date1, Date2)** returnerer den klargjorte databeholderen for anleggsmidlet **"COMP-000001"** som har verdimodellen **"Gjeldende"** for en periode fra **Date1** til **Date2**. |
| FA\_BALANCE (anleggsmiddelkode, verdimodellkode, rapporteringsår, rapporteringsdato) | Returner den klargjorte databeholderen for den faste anleggsmiddelsaldoen. Rapporteringsåret må angis som en verdi for **AssetYear**-opplistingen. | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** returnerer den klargjorte databeholderen for saldoer for anleggsmidlet **"COMP-000001"** som har verdimodellen **"Gjeldende"** på den gjeldende datoen for programøkten. |
| TABLENAME2ID (streng) | Returner en heltallsrepresentasjon for en tabell-ID for det angitte tabellnavnet. | **TABLENAME2ID ("Intrastat")** returnerer **1510**. |
| ISVALIDCHARACTERISO7064 (streng) | Returner den boolske verdien **SANN** når den angitte strengen representerer et gyldig internasjonalt bankkontonummer (IBAN). Hvis ikke, returner den boolske verdien **USANN**. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** returnerer **SANN**. **ISVALIDCHARACTERISO7064 ("AT61")** returnerer **USANN**. |
| NUMSEQVALUE (nummerseriekode, område, område-id) | Returner den nye genererte verdien for en nummerserie, basert på den angitte nummerseriekoden, område og område-ID. Området må være angitt som en verdi av **ERExpressionNumberSequenceScopeType**-nummereringen (**Delt**, **Juridisk enhet** eller **Firma**). For **Delt**-området angi en tom streng som område-ID. For områdene **Firma** og **Juridisk enhet** angi firmakoden som område-ID. For områdene **Firma** og **Juridisk enhet**, hvis du angir en tom streng som område-ID, brukes den gjeldende firmakoden. | Du definerer de følgende datakildene i modelltilordningen:<ul><li>**enumScope** (typen **Dynamics 365 for Operations**-opplisting), som refererer til opplistingen **ERExpressionNumberSequenceScopeType**</li><li>**NumSeq** (**Beregnet felt**-type), som inneholder uttrykket **NUMSEQVALUE ("Gene\_1", enumScope.Company, "")**</li></ul>Når **NumSeq**-datatypen kalles opp, returneres den nye genererte verdien for **Gene\_1**-nummerserien som er konfigurert for firmaet som levererte konteksten som ER-formatet kjøres under. |
| NUMSEQVALUE (nummerseriekode) | Returner den nye genererte verdien for en nummerserie, basert på den angitte nummerserien, omfanget **Firma** og (som område-ID) koden for firmaet som leverer konteksten som ER-formatet kjører under. | Du definerer følgende datakilde i modelltilordningen: **NumSeq** (**Beregnet felt**-type). Denne datakilden inneholder uttrykket **NUMSEQVALUE ("Gene\_1")**. Når **NumSeq**-datatypen kalles opp, returneres den nye genererte verdien for **Gene\_1**-nummerserien som er konfigurert for firmaet som levererte konteksten som ER-formatet kjøres under. |
| NUMSEQVALUE (post-ID for nummerserie) | Returner den nye genererte verdien for en nummerserie, basert på den angitte post-ID-en for nummerserie. | Du definerer de følgende datakildene i modelltilordningen:<ul><li>**LedgerParms** (**Tabell**-type), som refererer til tabellen LedgerParameters</li><li>**NumSeq** (**Beregnet felt**-type), som inneholder uttrykket **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)**</li></ul>Når **NumSeq**-datatypen kalles opp, returneres den nye genererte verdien for nummerserien som er konfigurert i økonomimodul-parameterne for firmaet som leverer konteksten som ER-formatet kjøres under. Denne nummerserien identifiserer journaler unikt og fungerer som et partinummer som kobler sammen transaksjonene. |

### <a name="functions-list-extension"></a>Funksjonslisteutvidelse

ER lar deg utvide listen over funksjoner som brukes i ER-uttrykk. Det er nødvendig med noe utvikling. Hvis du vil ha mer informasjon, kan du se [Utvide listen over elektroniske rapporteringsfunksjoner (ER)](general-electronic-reporting-formulas-list-extension.md).

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Utvide listen over elektroniske rapporteringsfunksjoner (ER)](general-electronic-reporting-formulas-list-extension.md)
