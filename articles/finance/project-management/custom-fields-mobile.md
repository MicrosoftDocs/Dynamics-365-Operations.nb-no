---
title: Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på IOS og Android
description: Dette emnet inneholder vanlige mønstre for bruk av utvidelser for implementering av egendefinerte felt.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080778"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på IOS og Android

[!include [banner](../includes/banner.md)]

Dette emnet inneholder vanlige mønstre for bruk av utvidelser for implementering av egendefinerte felt. Følgende emner dekkes:

- De forskjellige datatypene som det egendefinerte feltrammeverket støtter
- Vise skrivebeskyttede eller redigerbare felt i timeregistreringsoppføringer og lagre brukerleverte verdier tilbake til databasen
- Vise skrivebeskyttede felt i timeregistreringshodet
- Integrere annen egendefinert forretningslogikk for å angi standardverdier i felt og utføre tilleggsvalidering

## <a name="audience"></a>Målgruppe

Dette emnet er ment for utviklere som integrerer sine egendefinerte felt i Microsoft Dynamics 365 Project Timesheet-mobilapplikasjonen som er tilgjengelig for Apple iOS og Google Android. Det antas at leserne er kjent med funksjonene for utvikling og prosjekttimeregistrering i X++.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datakontrakt – TSTimesheetCustomField X++-klasse

Klassen **TSTimesheetCustomField** er X++-datakontraktklassen som representerer informasjon om et egendefinert felt for timeregistreringsfunksjonalitet. Det blir sendt lister over de egendefinerte feltobjektene både på TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten for å vise egendefinerte felt i mobilappen.

- **TSTimesheetDetails** – timeregistreringshodekontrakten.
- **TSTimesheetEntry** – kontrakten for timeregistreringstransaksjonen. Grupper av disse objektene som har samme prosjektinformasjon og **timesheetLineRecId**-verdi, utgjør en linje.

### <a name="fieldbasetype-types"></a>fieldBaseType (typer)

Egenskapen **FieldBaseType** i **TsTimesheetCustom**-objektet bestemmer typen av feltet som vises i appen. Følgende **Typer**-verdier som støttes.

| Typer-verdi | Type              | Notater |
|-------------|-------------------|-------|
| 0           | Streng (og Opplisting) | Feltet vises som et tekstfelt. |
| 1           | Heltall           | Verdien vises som et tall uten desimaler. |
| 2           | Kommatall              | Verdien vises som et tall med desimaler.<p>Hvis du vil vise den reelle verdien som en valuta i appen, bruker du **fieldExtenededType**-egenskapen. Du kan bruke egenskapen **numberOfDecimals** til å angi antall desimaler som vises.</p> |
| 3           | Dato              | Datoformater bestemmes av brukerens innstilling for **Dato, klokkeslett og nummerformat**, som er angitt under **Innstillinger for språk og land/område** i **Brukeralternativer**. |
| 4           | Boolsk           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Hvis egenskapen **stringOptions** ikke er angitt på **TSTimesheetCustomField**-objektet, gis det et fritekstfelt til brukeren.

    Egenskapen **stringLength** kan brukes til å angi den maksimale strenglengden som brukere kan angi.

- Hvis egenskapen **stringOptions** er angitt på **TSTimesheetCustomField**-objektet, er disse listeelementene de eneste verdiene brukerne kan velge ved å bruke alternativknappene (valgknapper).

    I dette tilfellet kan strengfeltet fungere som en opplistingsverdi for brukeroppføring. Hvis du vil lagre verdien i databasen som en opplisting, kan du manuelt tilordne strengverdien tilbake til opplistingsverdien før du lagrer databasen ved hjelp av kommandokjeden (se delen "Bruke kommandokjede på klassen TSTimesheetEntryService for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for å se et eksempel).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Du kan bruke denne egenskapen til å formatere reelle verdier som valuta. Denne fremgangsmåten gjelder bare når **fieldBaseType**-verdien er **Kommatall**.

- **TSCustomFieldExtendedType:None** – Ingen formatering brukes.
- **TSCustomFieldExtendedType::Currency** – Formaterer verdien som valuta.

    Når valutaformatering er aktiv, kan **stringValue**-feltet brukes til å sende valutakoden som skal vises i appen. Verdien er en skrivebeskyttet verdi.

    Feltet **realValue** inneholder pengebeløpet som skal lagres i databasen.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Du kan bruke denne egenskapen til å angi hvor det egendefinerte feltet skal vises i appen.

- **TSCustomFieldSection::Header** – Feltet vises i **Vis flere detaljer**-delen i appen. Begge feltene er alltid skrivebeskyttet.
- **TSCustomFieldSection::Line** – Feltet vil vises etter alle medfølgende linjefelt på timeregistreringsoppføringer. Disse feltene kan enten være redigerbare eller skrivebeskyttet.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Denne egenskapen identifiserer feltet når verdiene som appen gir, lagres tilbake til databasen.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Denne egenskapen identifiserer feltet når verdiene som appen gir, lagres tilbake til databasen.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Sett denne egenskapen til **Ja** for å angi at feltet i timeregistreringsdelen skal være redigerbar av brukere. Sett egenskapen til **Nei** for å skrivebeskytte feltet.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Sett denne egenskapen til **Ja** for å angi at feltet i timeregistreringsdelen skal være obligatorisk.

### <a name="label-str"></a>label (str)

Denne egenskapen angir etiketten som vises ved siden av feltet i appen.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Denne egenskapen gjelder bare når **fieldBaseType** er satt til **Streng**. Hvis **stringOptions** er angitt, angis strengverdiene som er tilgjengelige for valg via alternativknapper (valgknapper), av strengene i listen. Hvis ingen strenger angis, tillates fritekstregistrering i strengfeltet (se delen "Bruke kommandokjede på klassen TSTimesheetEntryService for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for et eksempel).

### <a name="stringlength-int"></a>stringLength (int)

Denne egenskapen angir den maksimale lengden for et strengfelt. Den gjelder bare når **fieldBaseType** er satt til **Streng**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Denne egenskapen angir antall desimaler som vises for et reelt felt. Den gjelder bare når **fieldBaseType** er satt til **Kommatall**.

### <a name="ordersequence-int"></a>orderSequence (int)

Denne egenskapen kontrollerer i hvilken rekkefølge de egendefinerte feltene vises i appen når mer enn ett egendefinert felt er angitt. Felt som har lavere tall, vises først.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

For felt av typen **Boolsk** sender denne egenskapen den boolske verdien for feltet mellom serveren og appen.

### <a name="guidvalue-guid"></a>guidValue (guid)

For felt av typen **GUID** sender denne egenskapen den globalt unike identifikatoren (GUID) for feltet mellom serveren og appen.

### <a name="int64value-int64"></a>int64Value (int64)

For felt av typen **Int64** sender denne egenskapen int64-verdien for feltet mellom serveren og appen.

### <a name="intvalue-int"></a>intValue (int)

For felt av typen **Int** sender denne egenskapen int-verdien for feltet mellom serveren og appen.

### <a name="realvalue-real"></a>realValue (real)

For felt av typen **Kommatall** sender denne egenskapen kommatallverdien for feltet mellom serveren og appen.

### <a name="stringvalue-str"></a>stringValue (str)

For felt av typen **Streng** sender denne egenskapen strengverdien for feltet mellom serveren og appen. Det brukes også for felt av typen **Kommatall** som formateres som valuta. For disse feltene brukes egenskapen til å sende valutakoden til appen.

### <a name="datevalue-date"></a>dateValue (date)

For felt av typen **Dato** sender denne egenskapen datoverdien for feltet mellom serveren og appen.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Vise og lagre et egendefinert felt i timeregistreringsdelen

Nedenfor vises et skjermbilde fra mobilappen for en timeregistreringsoppretting. Den viser medfølgende felt og et egendefinert felt i delen "Tidsoppføring" som kalles "Teststreng" med opplistingsverdien "andre alternativ" som allerede er angitt.

![Egendefinert felt for teststreng i appen](media/timesheet-entry.jpg)



Nedenfor vises et skjermbilde fra mobilappen til brukeren som velger et av opplistingsalternativene som er tilgjengelig for det egendefinerte feltet "Teststreng".  De to alternativene er "Første alternativ" og "Andre alternativ", som vises som alternativknapper. Det andre alternativet er allerede valgt.

![Alternativknapper (valgknapper) for det egendefinerte feltet Teststreng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Utvid TSTimesheetLine-tabellen, slik at den har et egendefinert felt

I vanlige scenarioer er det sannsynlig at dataene for et egendefinert felt i delen timeregistreringsoppføring blir lagret i TSTimesheetLine-tabellen. Det kan imidlertid brukes andre tabeller hvis dataene kan hentes basert på en TSTimesheetTrans-post som oppgis, eller hvis det ikke finnes en bestemt postkontekst (hvis for eksempel feltet er angitt som skrivebeskyttet i prosjektparameterne).

Legg merke til at egendefinerte felt ikke trenger å ha noen reservedatabaseposter. De kan genereres dynamisk basert på X++-logikk. Denne fremgangsmåten kan være nyttig i skrivebeskyttede scenarioer (se delen "Bruke kommandokjede på klassen TSTimesheetDetails, metoden buildCustomFieldListForHeader for å fylle ut timeregistreringsdetaljer" for et eksempel på dynamisk genererte egendefinerte feltverdier.)

Nedenfor vises et skjermbilde fra Visual Studio i applikasjonsobjekttreet. Det viser en utvidelse av TSTimesheetLine-tabellen med TestLineString-feltet lagt til som et egendefinert felt.

![Linjestreng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Bruk kommandokjede på buildCustomFieldList-metoden til TSTimesheetSettings-klassen for å vise et felt i delen timeregistreringsoppføring

Denne koden kontrollerer visningsinnstillingene for feltet i appen. Det kontrollerer for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken inndeling feltet vises i.

Følgende eksempel viser et strengfelt på tidsoppføringer. Dette feltet har to alternativer, **Første alternativ** og **Andre alternativ**, som er tilgjengelige via alternativknapper (valgknapper). Feltet i appen er knyttet til **TestLineString**-feltet som legges til i TSTimesheetLine-tabellen.

Legg merke til bruken av **TSTimesheetCustomField::newFromMetatdata()**-metoden for å forenkle initialiseringen av de egendefinerte feltegenskapene: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** og **numberOfDecimals**. Du kan også angi disse parameterne manuelt slik du vil.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Bruke kommandokjede på buildCustomFieldListForEntry-metoden til TSTimesheetEntry-klassen for å angi verdier i en timeregistreringsoppføring

Metoden **buildCustomFieldListForEntry** brukes til å angi verdier på de lagrede timeregistreringslinjene i mobilappen. Den bruker en TSTimesheetTrans-post som en parameter. Felt fra denne posten kan brukes til å fylle ut den egendefinerte feltverdien i appen.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Bruk kommandokjeden på TSTimesheetEntryService-klassen til å lagre en timeregistreringsoppføring fra appen tilbake til databasen

Hvis du vil lagre et egendefinert felt tilbake til databasen i vanlig bruk, må du utvide flere metoder:

- Metoden **timesheetLineNeedsUpdating** brukes til å fastsette om linjeposten er endret av brukeren i appen og må lagres til databasen. Hvis ytelse ikke er av betydning, kan denne metoden forenkles, slik at den alltid returnerer **sann**.
- Metodene **populateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** kan utvides, slik at de angir verdier i TSTimesheetLine-databaseposten fra TSTimesheetEntry-datakontraktposten som er angitt. I eksemplet nedenfor ser du hvordan tilordningen mellom databasefeltet og oppføringsfeltet utføres manuelt via via X++-kode.
- Metoden **populateTimesheetWeekFromEntry** kan også utvides hvis det egendefinerte feltet som er tilordnet **TSTimesheetEntry**-objektet, må skrive tilbake til TSTimesheetLineweek-databasetabellen.

> [!NOTE]
> Det følgende eksemplet lagrer verdien **firstOption** eller **secondOption** som brukeren velger, i databasen som en rå-strengverdi. Hvis databasefeltet er et felt av typen **Opplisting**, kan disse verdiene tilordnes til en opplistingsverdi manuelt og deretter lagres til et opplistingsfelt i databasetabellen.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Vise et egendefinert felt i topptekstdelen for timeregistrering

Nedenfor vises et skjermbilde fra mobilappen til en bruker som viser en timeregistrering. Knappen "Mer informasjon" er valgt i øvre høyre hjørne for å vise alternativet "Vis flere detaljer".  

![Vis flere detaljer-kommando](media/show-more.png)

Nedenfor vises et skjermbilde fra mobilappen som viser "Mer"-delen av en timeregistrering. Et egendefinert felt kalt "Utnyttelsesrate for denne timeregistreringen (beregnet egendefinert felt)" er lagt til i topptekstdelen for timeregistrering. En skrivebeskyttet verdi på "0,667" angis for det egendefinerte feltet.

![Mer-del](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Utvid TSTimesheetTable-tabellen, slik at den har et egendefinert felt

I vanlige scenarioer er det sannsynlig at dataene for et egendefinert felt i topptekstdelen hentes fra TSTimesheetHeader-tabellen. Det kan imidlertid brukes andre tabeller hvis dataene kan hentes basert på en TSTimesheetTable-post som oppgis, eller hvis det ikke finnes en bestemt postkontekst (hvis for eksempel feltet er angitt som skrivebeskyttet i prosjektparameterne).

Legg merke til at egendefinerte felt ikke trenger å ha noen reservedatabaseposter. De kan genereres dynamisk basert på X++-logikk. Eksemplet nedenfor viser denne fremgangsmåten.

Felt i topptekstinndelingen er alltid skrivebeskyttet i appen.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Bruke kommandokjede på buildCustomFieldList-metoden til TSTimesheetSettings-klassen for å vise et felt i topptekstdelen

Denne koden kontrollerer visningsinnstillingene for feltet i appen. Det kontrollerer for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken inndeling feltet vises i.

Følgende eksempel viser en beregnet verdi i hodedelen i appen.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Bruke kommandokjede på buildCustomFieldListForHeader-metoden til TSTimesheetDetails-klassen for å fylle ut timeregistreringsdetaljer

Metoden **buildCustomFieldListForHeader** brukes til å fylle ut timeregistreringshodedetaljene i mobilappen. Den bruker en TSTimesheetTable-post som en parameter. Felt fra denne posten kan brukes til å fylle ut den egendefinerte feltverdien i appen. Følgende eksempel leser ikke verdier fra databasen. I stedet brukes X++-logikk til å generere en beregnet verdi som deretter vises i appen.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Andre muligheter for konfigurerbarhet/utvidelse

### <a name="adding-additional-validation-for-the-app"></a>Legge til ekstra validering for appen

Eksisterende logikk for timeregistreringsfunksjonalitet på databasenivå vil fremdeles fungere som forventet. Hvis du vil avbryte fullføringen av lagre- eller send-operasjoner og vise en bestemt feilmelding, kan du legge til **iverksett feil("melding til bruker")** i koden via en kommandokjedeutvidelse. Her er tre eksempler på nyttige utvidelsesmetoder:

- Hvis **validateWrite** i TSTimesheetLine-tabellen returnerer **usann** under en lagringsoperasjon for en timeregistreringslinje, vises en feilmelding i mobilappen.
- Hvis **validateSubmit** i TSTimesheetTable-tabellen returnerer **usann** under innsending av timeregistrering i appen, vises en feilmelding for brukeren.
- Logikk som fyller ut felt (for eksempel **Linjeegenskap**) under **sett inn**-metoden i TSTimesheetLine-tabellen, vil fortsatt kjøre.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Skjule og merke medfølgende felt som skrivebeskyttet via konfigurasjon

Fra prosjektparameterne kan du gjøre medfølgende felt skrivebeskyttet eller skjult i mobilappen. Angi alternativene i delen **Mobile timeregistreringer** i kategorien **Timeregistrering** på siden **Parametere for prosjektstyring og regnskap**.

![Prosjektparametere](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Endre aktivitetene som er tilgjengelige for valg via utvidelser

Aktivitetene som er tilgjengelige for valg for et prosjekt, fylles ut via metodene **getActivitiesForProject()** og **getActivityQuery()** i **TsTimesheetProjectService**-klassen. Du kan bruke kommandokjeden til å endre denne virkemåten, slik at den samsvarer med forretningsscenarioet for aktivitetene som er tilgjengelige for valg for et bestemt prosjekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Angi en standard prosjektkategori for timeregistreringsoppføringer

Registrering av en standard prosjektkategori i timeregistreringsoppføringer forekommer på tre nivåer. Du kan bruke kommandokjeden til å utvide virkemåten på hvilke som helst eller alle disse nivåene for å oppnå den ønskede atferden. Følgende hierarki brukes:

1. Appen prøver å plassere standardkategori fra prosjektressursen. Denne standardkategorien er angitt i metodene **getCurrentUserResource** og **getDelegatedResourcesForCurrentUser** i **TSTimesheetSettingsService**-klassen.
2. Hvis standardkategorien ikke er angitt på prosjektressursnivå, prøver appen å hente den fra prosjektaktiviteten. Denne standardkategorien angis i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.
3. Hvis standardkategorien ikke er angitt på prosjektaktivitetsnivå, hentes standardkategorien fra prosjektparametrene. Denne standardkategorien angis i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.
