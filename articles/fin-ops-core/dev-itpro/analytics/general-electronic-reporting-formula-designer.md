---
title: Formeldesigner i elektronisk rapportering (ER)
description: Dette emnet gir generell informasjon om hvordan du bruker formeldesigneren i elektronisk rapportering.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d96fe041fd0ffb292909c1e724068efebe0184b9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682655"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formeldesigner i elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du bruker formeldesigneren i elektronisk rapportering (ER). Når du utformer et format for et bestemt elektronisk dokument i ER, kan du bruke formler for å transformere data slik at de oppfyller kravene for fullføringen og formatering for dokumentet. Disse formlene ligner på formler i Microsoft Excel. Ulike typer funksjoner støttes i formlene: tekst, dato og klokkeslett, matematisk logiske, informasjon og konverteringsfunksjoner for datatype og andre domenespesifikke forretningsfunksjoner.

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

## <a name="data-binding"></a><a name="Binding"></a>Databinding

ER-formeldesigneren kan brukes til å definere et uttrykk som transformerer data som mottas fra datakilder, slik at dataene kan angis i dataforbruker på følgende måter ved kjøretid:

- Fra programdatakilder og kjøretidsparametere til en ER-datamodellen
- Fra en ER-datamodell til et ER-format
- Fra programdatakilder og kjøretidsparametere til et ER-format

Illustrasjonen nedenfor viser utformingen av et uttrykk av denne typen. I dette eksemplet avrunder uttrykket verdien for **Intrastat.AmountMST**-feltet for Intrastat-tabellen til to desimalplasser og returnerer deretter den avrundede verdien.

[![Databindingsuttrykk](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Illustrasjonen nedenfor viser hvordan et uttrykk av denne typen kan brukes. I dette eksemplet er resultatet av det utformede uttrykket angitt i **Transaction.InvoicedAmount**-komponenten for datamodellen **Avgiftsrapporteringsmodell**.

[![Databindingsuttrykk som brukes](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Under kjøringen avrunder den utformede formelen `ROUND (Intrastat.AmountMST, 2)`, verdien i **AmountMST**-feltet for hver post i Intrastat-tabellen til to desimalplasser. Den angir så den avrundede verdien i **Transaction.InvoicedAmount**-komponenten i **Avgiftsrapportering**-datamodellen.

## <a name="data-formatting"></a><a name="Transformation"></a>Dataformatering

ER-formeldesigneren kan brukes til å definere et uttrykk som formaterer data som mottas fra datakilder, slik at dataene kan sendes som en del av det genererende elektroniske dokumentet. Du kan ha formatering som må brukes som en vanlig regel som skal brukes på nytt for et format. I så fall kan du innføre denne formateringen én gang i formatkonfigurasjonen, som en navngitt transformasjon som har et formateringsuttrykk. Denne navngitte transformasjonen kan deretter knyttes til mange formatkomponenter der utdata må formateres i henhold til formateringsuttrykket som du opprettet.

Illustrasjonen nedenfor viser utformingen av en transformasjon av denne typen. I dette eksemplet forkorter **TrimmedString**-transformasjonen innkommende data for *String*-datatypen ved å fjerne innledende og etterfølgende mellomrom. Det returnerer deretter den avkortede strengverdien.

[![Transformasjon](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Illustrasjonen nedenfor viser hvordan en transformasjon av denne typen kan brukes. I dette eksemplet sender flere formatkomponenter tekst som utdata til det genererende elektroniske dokumentet under kjøring. Alle disse formatkomponentene refererer til **TrimmedString**-transformeringen etter navn.

[![Transformasjon som brukes](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Når formatkomponenter som **partyName**-komponenten i den forrige illustrasjonen refererer til **TrimmedString**-transformasjonen, sender transformasjonen tekst som utdata til det genererende elektroniske dokumentet. Denne teksten inneholder ikke mellomrom.

Hvis du har en formatering som skal brukes individuelt, kan du introdusere denne formateringen som et individuelt uttrykk for binding av en bestemt formatkomponent. Illustrasjonen nedenfor viser et uttrykk av denne typen. I dette eksemplet er **partyType**-formatkomponenten bundet til datakilden via et uttrykk som konverterer innkommende data fra **Model.Company.RegistrationType**-feltet i datakilden til store bokstaver i tekst. Uttrykket sender deretter teksten som utdata til det elektroniske dokumentet.

[![Bruke formatering på en individuell komponent](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Prosessflytkontroll

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

[![Prosessflytkontroll](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Kontroll av dokumentinnhold

ER-formeldesigneren kan brukes til å konfigurere uttrykk som kontrollerer hvilke data som skal plasseres i genererte, elektroniske dokumenter ved kjøring. Uttrykkene kan aktivere eller deaktivere utdataene for bestemte elementer i formatet, avhengig av behandling av data og konfigurert logikk. Disse uttrykkene kan angis for ett enkelt formatelement i **Aktivert**-feltet i **Tilordning**-fanen på **Operasjonsutforming**-siden. Du kan angi uttrykkene som en logisk betingelse som returnerer en *boolsk* verdi:

- Hvis betingelsen returnerer **Sann**, kjøres gjeldende formatelement.
- Hvis betingelsen returnerer **Usann**, hoppes gjeldende formatelement over.

Illustrasjonen nedenfor viser uttrykk av denne typen. (Versjon 11.12.11 av **ISO20022-kredittoverføring (NO)**-formatkonfigurasjon som leveres av Microsoft, brukes som et eksempel.) **XMLHeader**-formatkomponent er konfigurert til å beskrive strukturen i kredittoverføringsmeldingen i henhold til ISO 20022 XML-meldingsstandarder. Formatkomponenten **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** er konfigurert til å legge til **Ustrd** XML-elementet i den genererte meldingen, og plassere remisseinformasjonen i et ustrukturert format som tekst i følgende XML-elementer:

- **PaymentNotes**-komponenten brukes til å produsere teksten i betalingsmerknadene.
- **DelimitedSequence**-komponenten produserer kommadelte fakturanumre som brukes til å utligne gjeldende kredittoverføring.

[![PaymentNotes- og DelimitedSequence-komponenter](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> **PaymentNotes**- og **DelimitedSequence**-komponentene merkes ved hjelp av et spørsmålstegn. Et spørsmålstegn angir at bruken av en komponent er betinget. I dette tilfellet er bruk av komponentene basert på følgende kriterier:
>
> - Uttrykket `@.PaymentsNotes <> ""` som er definert for **PaymentNotes**-komponenten, aktiverer (ved å returnere **SANN**) **Ustrd** XML-elementet til å bli fylt ut med to betalingsmerknader, hvis denne teksten ikke er tom for gjeldende kredittoverføring.
>
>    [![Uttrykk for PaymentNotes-komponenten](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Uttrykket `@.PaymentsNotes = ""` som er definert for **DelimitedSequence**-komponenten, aktiverer (ved å returnere **SANN**) **Ustrd** XML-elementet til å bli fylt ut med en kommadelt liste over fakturanumre som brukes til å utligne gjeldende kredittoverføring, hvis teksten i betalingsmerknader for kredittoverføringen er tom.
>
>    [![Uttrykk for DelimitedSequence-komponenten](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Basert på dette oppsettet vil den genererte meldingen for hver debitorbetaling, **Ustrd** XML-elementet, inneholde enten teksten for betalingsmerknader eller, når denne teksten er tom, en kommadelt liste over fakturanumre som brukes til å utligne betalingen.

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Validering av konfigurerte formler

På **Formeldesigner**-siden velger du **Test** for å validere hvordan den konfigurerte formelen fungerer.

[![Velge test for å validere en formel](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Når verdiene i formelargumenter er obligatoriske, kan du åpne dialogboksen **Testuttrykk** fra siden **Formeldesigner**. I de fleste tilfeller må disse argumentene defineres manuelt fordi de konfigurerte bindingene ikke kjøres under utformingen. Kategorien **Testresultat** på siden **Formel designer** viser resultatet fra utføringen av den konfigurerte formelen.

Følgende eksempel viser hvordan du kan teste formelen som er konfigurert for utenrikshandelsdomenet for å sikre at Intrastat-varekoden bare inneholder sifre.

Når du tester denne formelen, kan du bruke dialogboksen **Testutrykk** til å angi verdien for Intrastat-varekoden for testing.

[![Angi Intrastat-varekoden for testing](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Når du har angitt Intrastat-varekoden og velger **OK**, viser kategorien **Testresultat** på siden **Formeldesigner** resultatet av utførelsen av den konfigurerte formelen. Du kan deretter vurdere om resultatet er akseptabelt. Hvis resultatet ikke er akseptabelt, kan du oppdatere formelen og teste den på nytt.

[![Testresultat](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Noen formler kan ikke testes på utformingstidspunktet. En formel kan for eksempel returnere et resultat av en datatype som ikke kan vises i kategorien **Testresultat.** I dette tilfellet får du en feilmelding som sier at formelen ikke kan testes.

[![Feilmelding](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]